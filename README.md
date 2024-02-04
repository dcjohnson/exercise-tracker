# exercise-tracker

## V1 Features

Track exercises within a mesocycle by laying out the plan for a week then auto-populating exercises for a new week; they should just be copied from the correct day in the previous week. 

Then we will add the ability to plan several weeks ahead within a mesocycle. 

We need the ability to list multiple mesocycles and group them into a program. 

## Implementation details

A rust server serving up a Bootstrap JS website; we will use some simple database for storing database. Would a document store be best for storing the data?

This would be for a particular day within the program. This would be a specific document within the doc store.
Probably just use files for now.
```
{
  "exercises": [
	  {
		  "name": "Romanian Deadlift",
			"setsAndReps": "4x8",
			"weight": "85 Kilos",
			"additionalNotes", "blah blah blah"
	]
}
```

```
program name | description | start week | end week
```

```
program name | date | exercise document ID
```

As you specify each week within your program, it pulls the previous week and allows you to make modifications