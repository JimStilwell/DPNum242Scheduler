# DPNum242Scheduler
Optimized scheduler with options.

	Author: Jim Stilwell
	
	Date: 01/06/2016
	
	IDE: Eclipse Kepler SR2
	
	Language: C++ (MinGW / http://mingw.org/)
	

	Note* These programs are designed to show case my programming style and capabilities so I may occasionally
	perform operations that wouldn't make sense in the real world (like jumbling a sorted list just so I can sort it again right afterward).

	Problem Description
	-------------------
	Given a list of event start times and end times how many events can you attend if overlap is not allowed.
	Bonus 1: make up names associated with each event and provide them in the output
	Bonus 2: the first line is a must attend event. Optimize the remaining events while insuring attendance of the first event.
	My challenge 1: Any single event can be tagged as a must attend event, the rest of the events must be optimized around it.
	My challenge 2: Place events in a 2D space and calculate travel times between events where 1 unit apart = 1 minute travel time
	My challenge 3: Example Inputs are all pre-sorted by Start Time I will randomize them and resort them in the app

	Input
	1530 1600
	1555 1645
	1600 1630
	1635 1715
	Expected Output
	3
	Actual Output (with details)


	Assumptions:
	Inputs are not pre-sorted based on start times
	The initial number is not known at run time
	There is no transit time between events.
	If your first event has an end time of 1400 and the next event has the same start time, they are a valid combination

	My Solution:
	Store Multiple Events in an XML doc
	Create a class to hold all inputs
	Iterate through every possible combination of events checking for overlap at each step
	If the maximum number of events = the number of inputs, quit.
	Hold each combination in memory and select the combination with the maximum value
	If multiple combinations tie for maximum number of events, report back each option

	Tags:
	Multidimensional Arrays
	XML Created with XML Copy Editor (http://sourceforge.net/projects/xml-copy-editor/)
	Xerces-C++ XML parser from apache.org
	Quick Sorting
	Randomization
	OO
	URL: https://www.reddit.com/r/dailyprogrammer/comments/3u6o56/20151118_challenge_242_intermediate_vhs_recording/


