 ♪ Bass music playing ♪  ♪ Preston Lewis: Hi, my name is Preston, and today I'm going to be talking about how to bring accessibility to charts in your apps.

Let's go over what we're going to cover today.

First, we'll talk about some of the benefits of making your charts accessible.

Then, we'll go over some principles for making inclusive decisions for the visual aspects of your chart.

Next, we'll discuss how to make your charts perceivable and navigable with VoiceOver.

And lastly, we'll talk about an exciting new feature called "audio graphs" and how to support them in your app.

So, let's get started.

Data is so important in our modern world.

We use data every day to make decisions about our finances, our health, our goals, and so many other things.

But in order to make any use of data, we have to be able to understand it.

Charts are useful because they allow us to quickly understand what our data is telling us without having to get too deep into the details.

But charts are not inherently accessible for blind or low-vision people.

There's no value in a visual chart if you can't see it.

The accessibility team has been working hard for years to make data more accessible to blind and low-vision people.

This year, you can bring the full power of your charts to people with blindness or low vision by supporting audio graphs in your apps.

Let's look at an example.

Here is an example app showing historical birth rates from the year 1917 to 1975.

When you look at this chart, you can immediately see some interesting features.

You can see that the birth rate decreased to a minimum around the year 1935, and then quickly increased to about the year 1960 and then decreased again.

We can give blind and low-vision people the same ability to quickly get a sense of the data using the new audio graph VoiceOver feature.

Let me show you how it works.

First, I'm going to find the Audio Graph menu in the VoiceOver rotor.

VoiceOver: Audio graph.

Preston: Then I'll swipe down until I hear "Chart Details".

VoiceOver: Play audio graph. Chart details.

Preston: Then I'll double-tap to open the audio graph Explorer view.

VoiceOver: Audio graph. Heading.

Preston: Then I'll navigate to the Play button to play the audio graph, which will play the data series as a continuous tone.

VoiceOver: Twentieth-century birth rates.

Play audio graph. Button.

Preston: Let's listen to it now.

 VoiceOver: Complete.

Preston: Wasn't that exciting? What you just heard was the same chart as the one you see, represented auditorily instead of visually.

The pitches you heard correspond to birth rates over time with lower pitches meaning lower values and higher pitches meaning higher values.

These pitches exactly mirror the line in the visual chart.

So even without seeing the chart, the audio graph allows you to perceive its important features in just a few seconds.

Now that we have a general sense of the data, let's get more precise information about the features we're interested in.

The next thing we might want to know is approximately what the maximum birth rate was and what year it occurred.

To do this, audio graphs provide an interactive mode where VoiceOver users can double-tap and hold and then drag to listen to the data at their own pace.

If they pause, VoiceOver will read the data value corresponding to the user's current position in the audio graph.

Let's use this interactive mode to try to find the maximum birth rate and what year it occurred.

VoiceOver: Twentieth-century birth rates.

  Data point. 1960. 268 births per 10,000 people.

Preston: By scrubbing through the audio graph until we heard the highest pitch, then pausing to hear the data value, we can tell that the maximum birth rate was 268 per 10,000 people around the year 1960.

Because we know the maximum occurred around 1960, we might even be able to infer that this peak corresponds to the baby boom era.

We can figure all of this out just from the sonified representation of the chart.

OK, now let's look at an example of a different kind of chart.

This chart is a scatter plot showing the relationship between vehicle weight on the X axis and fuel efficiency on the Y axis for several different types of automobiles.

In the audio graph for this chart, each tone you hear will represent a data point for one automobile, just like each visual data point on the visual chart.

The pitch of each tone will represent the automobile's fuel efficiency in miles per gallon, so higher pitches signify more fuel-efficient vehicles.

Take a second to think about what you expect to hear when I play this audio graph.

Let's hear what it sounds like.

Try to listen to hear whether the data is trending upwards or downwards.

 VoiceOver: Complete.

Preston: Hopefully you heard the downward trend.

This trend means that bigger automobiles tend to be less fuel-efficient in this data set.

Imagine how much longer it would have taken to understand this relationship if we only had the raw data points available to us and we had to look at each data point individually.

Also, if you were listening closely, you might have heard the very high-pitched outlier in this data set.

It sticks out in the audio graph just like it sticks out in the visual chart and happens to be the only hybrid vehicle in this data set.

If you wanted to get more information about the outlier, you could use the interactive mode to navigate through the data until you hear the highest pitch, then pause to hear the data value, just like we did with the birth rate chart.

In addition to the audio graph, this explorer view provides summary information about important features of the data like shape, trend, and outliers, which are inferred from an automatic statistical analysis of this chart's data.

Along with the audio graph, VoiceOver can read this summary information to complete our understanding of the data.

OK, let's quickly recap the benefits of accessible charts.

Making your charts accessible allows your data-rich applications to reach wider audiences, including blind and low-vision people.

It will empower your users by giving them helpful tools for understanding the data in your charts, which will help them leverage the incredible power of data in their personal and professional lives.

And lastly, with new API coming this year, making your charts is easier than ever before.

I'm really excited to show you how to support audio graphs in your apps, but we need to cover some general chart accessibility topics first, starting with how you can make your charts more visually accessible.

There are a few simple things you can do to make your visual charts more understandable for everybody.

Take this chart as an example.

This is simple line chart that shows average monthly rainfall for tropical and arid regions.

Let's apply some accessibility principles to improve the visual accessibility of this chart.

First, it's important to use high-contrast colors whenever possible.

High contrast between foreground and background colors makes your chart easier to look at and understand, especially for people with low vision.

As you can see, the lines' contrast against their background is pretty low.

The title and label text also seem a bit dim.

Let's update these colors to have higher contrast against the background.

That's much better.

You can check contrast ratios between colors to determine whether or not the contrast is sufficient.

The Accessibility Inspector that comes bundled with Xcode has a Color Contrast Calculator that you can use.

It's good to aim for contrast ratios of at least 4.5:1.

The next thing you can do to improve your chart's visual accessibility is to avoid problematic color pairings.

It's generally good practice to avoid using red and green together if possible.

Red and green color blindness is the most common type and using these colors together can make your chart difficult to understand for some people.

So here's the line chart again, with a green line representing rainfall in tropical regions and a red line representing rainfall in arid regions.

You can probably tell which data series is which using the color encoding in the legend.

But if you have deuteranopia, a form of red-green color blindness, the chart might look something more like this to you.

It would be hard for you to tell which line represents tropical rainfall and which line represents arid rainfall with these colors.

Let's improve this by replacing the red color with blue.

This might not seem like a huge change, but to someone with red-green color blindness, this chart might now look like this.

With this small adjustment, it becomes easy for someone with red-green colorblindness to spot the difference between the series.

It's also good to avoid using blue and yellow together because this family of color blindness is the second most common.

These are some good improvements, but let's take this one step further by using symbols in addition to color for distinguishing your data series.

Using data symbols makes it so that people can understand your chart without having to rely on color at all.

So here's our chart again.

And now let's add some symbols for each data series.

Notice the tropical data series has circles now, and the arid data series has squares.

You can tell which series is which now just by looking at the associated symbols.

This means that even a person who can't perceive color at all can now understand your chart.

It's good to do all of these things by default, but again, sometimes design or product constraints might limit your choice of colors or decision to include symbols.

In these cases, you can still provide an accessible experience by supporting a few simple accessibility settings.

If you can't have symbols in your chart for the default case, you can still provide an accessible experience by adding symbols when the Differentiate Without Color system accessibility setting is enabled.

If you can't easily change your color set for product reasons, consider adopting higher-contrast colors when the Increase Contrast accessibility setting is set.

Reducing the use of transparency can also make your chart more visually accessible.

If your chart uses transparency effects, consider disabling them when the Reduce Transparency accessibility setting is on.

If you're building a macOS rather than an iOS app, each of these settings has a counterpart on macOS that you can support.

You'll find links to developer documentation for these APIs in the materials for this session.

Now let's look at how we can make your data navigable for VoiceOver.

Now, I love coffee, and I love programming.

Let's pretend for a minute there's a relationship between the amount of coffee consumed and amount of code an engineer produces as shown in this chart.

Just pretend.

Also, the data goes up to 12 cups of coffee, But don't worry, no engineers were harmed in the making of this data; it's all made up.

All right, let's see how we can make this data navigable for VoiceOver users.

Here's an example snippet of code from a chart view class and its corresponding model object.

The chart view might have a reference to its model, and a function for drawing itself.

And the model might have the chart's title and data points contained in a simple struct.

The first thing you'll want to do is make the chart a container.

This will help VoiceOver group your chart elements correctly and aid in navigation.

To make your chart a container, simply override accessibilityContainerType on your ChartView and return the semanticGroup container type.

Again, this is important for VoiceOver navigation and communicating which elements belong to the chart.

Next, we need to give our chart an accessibilityLabel.

This tells VoiceOver what to speak when it encounters your chart.

Typically, this should just be your chart's title or something similar that VoiceOver can speak to uniquely identify your chart in your UI.

Last but not least, you'll want to provide an accessibility element for each data point.

You can provide these elements by overriding your chart view's accessibilityElements property.

This will create elements inside your chart that VoiceOver can navigate, so that people can get information about individual data points.

To implement this, you can simply use "map" to build an array of accessibility elements from your list of data points.

For each data point, we'll create a new UIAccessibilityElement object, specifying the ChartView as its accessibilityContainer.

Then, we'll provide a string representation of the data point for the element's accessibilityValue property.

This string is what VoiceOver will speak when it navigates to these data point elements.

In your code, you'll probably want this string to be localized, and you may want to use a strings dictionary to define proper pluralization rules.

For this example, though, let's just keep it simple.

Lastly, we need to provide an accessibility frame for our element so that VoiceOver knows where it lives on the screen.

You'll probably already have logic for computing the frame for each data point elsewhere, since you needed this to draw the visual chart.

If you have it available, you can reuse that logic here.

You can now return your finished accessibility element for this data point.

All right! Let's see what we've accomplished so far.

VoiceOver: Cups of coffee versus lines of code.

Zero cups. Twenty lines of code.

One cup. Thirty lines of code.

Two cups. Thirty-five lines of code.

Three cups. Thirty-two lines of code.

Preston: Great! As you heard, VoiceOver now speaks the title when it focuses an element inside the chart because we made the chart a semantic group and gave it an accessibility label.

We also made it possible to navigate through each data point by creating a UIAccessibilityElement to represent each one.

There's one more thing I want to mention before we move on.

Sometimes you might have hundreds or even thousands of data points.

In these cases, you definitely don't want to make an accessibility element for each data point because there will just be way too many to navigate.

Instead, we suggest breaking up your chart into reasonable intervals and making an accessibility element for each interval rather than each data point.

This will provide a better navigation experience as well as improve performance while still being understandable.

We're not done yet; we can do even more.

Making data navigable is important, but we're still only presenting raw data to VoiceOver users one point at a time.

The value of charts is their ability to show us what the data is really telling us, and to help us look beyond individual data points.

This is where audio graphs come in.

So now -- finally -- let's talk about how to implement audio graph support for your chart.

Imagine we have a ChartModel struct that contains all the information we need to define a particular chart.

In your code, you probably have a model object that looks something like this already.

If you don't, don't worry.

These concepts will still apply to your code however it's organized.

For our example, let's say a chart has a title and a summary, it has an X and a Y axis, and each axis has a title as well as a numeric range representing the minimum and maximum displayable values for the axis.

And lastly, it has an array of data points containing our chart's actual data.

We'll use the information in this example model object to enable the audio graph feature for our chart.

First, import the Accessibility framework, then extend your ChartView class to conform to the AXChart protocol.

Conforming to the AXChart protocol is easy because there's only one property to support.

You just need to implement accessibilityChartDescriptor.

The chart descriptor object you construct will contain all of the information VoiceOver needs to provide the audio graph experience.

Let's walk through how to build one of these chart descriptors step by step.

First, we need to create an axis descriptor object for each axis.

Each axis descriptor provides information to VoiceOver about whether it represents categorical or numerical data, the range of displayable values for the axis, the positions of grid lines, and how to format speakable data values.

Since the X axis is numeric for our coffee chart, we'll create a numeric axis descriptor.

If we had categorical data on our X axis, we'd use a categorical axis descriptor instead.

We'll provide the title and range for this axis using our model object.

We can also optionally provide the positions of grid lines on this axis if we have them.

When you provide grid lines, they're represented in the audio graph as haptic feedback during playback and interaction.

We'll leave this empty for now since we don't have any X-axis grid lines in this chart.

For numeric axes, we also need to create a valueDescriptionProvider closure.

This closure is very important because it tells VoiceOver how to speak the values on this axis, so it can say "5 cups" instead of just saying "5".

For this axis, we'll format the description to speak "cups" after the value.

Again, in your code, you would probably want to localize this string with proper pluralization rules, but let's keep this example simple.

We'll do the same thing to create an axis descriptor for our Y axis, except we'll format our value description to say "lines of code" rather than "cups." Now that we have the basic structure of our chart defined, let's add the data.

To do this, you add a data series descriptor for each data series.

We only have one data series in this chart, so we'll just create one data series descriptor, passing in the name of the series, whether or not it is continuous, and the actual data points for this series.

You should pass "false" for "isContinuous" when the series is visually represented using discrete marks, like points or bars, and you should pass "true" when the series is visually represented as a line.

For the series' data, we need to provide an array of AXDataPoint objects.

The easiest way to do this is to just map them from the data in the chart model.

We're almost there! We just have one last thing to do.

And that's to put all the pieces together to build our AXChartDescriptor object.

We'll give it a title, which should, again, be the title of our chart.

Then, if we have one, we can provide a summary of our chart.

This is kind of like providing alt text for your chart.

You should use this property to communicate the most important insights from your data in a sentence or two.

This summary text will be presented to users in the audio graph explorer view.

This can be incredibly helpful to VoiceOver users trying to understand your chart.

Lastly, we'll provide the axis and data series descriptors we created earlier to complete our chart descriptor and then we'll return it.

That's it! Let's see the final result.

VoiceOver: Audio graph. Play audio graph.

Chart details. Audio graph. Heading: Cups of coffee versus lines of code.

Play audio graph. Button.

 Complete.

Preston: Let's recap.

Be sure to make accessible choices for the visual design of your chart.

This includes using good contrast ratios, using symbols in addition to color to differentiate categories of data, and avoiding color schemes that might be problematic for colorblind users.

Be sure to expose your data elements in the accessibility tree to make them perceivable and navigable to VoiceOver users.

And last but not least, implement the AXChart protocol and accessibilityChartDescriptor on your chart view to allow VoiceOver users to get the same value out of your chart as sighted users.

Now you have everything you need to create rich, accessible charts for everyone.

We hope you'll use these tools to empower your users since data is so incredibly important in our lives.

Charts are one of our very best tools for understanding data in a data-rich world, and now you can bring this benefit to everyone! ♪
