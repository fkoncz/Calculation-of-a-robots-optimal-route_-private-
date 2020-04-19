# PLEASE CONTACT ME FOR MY PRIVATE REPO FOR THE SOLUTION IN PYTHON!


# Calculation-of-a-robots-optimal-route_-private-
Calculating a robots optimal route

# Robots optimal route calculator
This acts the solution for calculating the optimal path of a robot with given coordinates in a square format (100m by 100m) factory described below.


# The challenge:
A course is set up in a 100m by 100m factory. Certain points are identified within the space as waypoints to visit to receive goods. They are ordered -- there is a waypoint 1, a waypoint 2, etc. Your robot must start at (0,0). From there, it should go to waypoint 1, stop for 10 second, go to waypoint 2, stop for 10 second, and so on. It must finally end up at, and stop for 10 second on (100,100).

Each waypoint except (0,0) and (100,100) has a time penalty for missing the load to reflect the time needed for a human to handle the work later. So, if your robot went straight from waypoint 1 to waypoint 3, skipping waypoint 2, it would incur waypoint 2's penalty. Note that once it hits waypoint 3, it cannot go back to waypoint 2. It must hit the waypoint in order. Since your robot must stop for 10 seconds on each waypoint to be loaded, it is not in danger of hitting a waypoint accidentally too soon. For example, if waypoint 3 lies directly between waypoints 1 and 2, your robot can go straight from 1 to 2, right over 3, without stopping. Since it didn't stop to be loaded, waypoint 3's penalty will not be incurred. Your final score is the amount of time (in seconds) your robot takes to reach (100,100), completing the course, plus all penalties. Smaller scores are better.

The robot is very manoeuvrable, but a bit slow. It moves at 2 m/s, but can turn very quickly. During the 10 seconds it stops on a waypoint point, it can easily turn to face the next waypoint. Thus, it can always move in a straight line between target points.
Because your robot is a bit slow, it might be advantageous to skip some waypoints and incur their penalty, rather than actually manoeuvring to them. Given a description of a course, determine your robot's best (lowest) possible time.
You may use any language you choose, as long as your submission is straightforward to run.


# Input
There will be several test cases. Each test case will begin with a line with one integer, N (1 <= N <= 1000) which is the number of waypoints on the course. Each of the next N lines will describe a waypoint with three integers, X, Y and P, where (X, Y) is a location on the course ( 1 <= X, Y <= 99, X and Y in meters) and P is the penalty incurred if your robot misses that waypoint (1 <= P <= 100). The waypoints will be given in order -- the first line after N is target 1, the next is waypoint 2, and so on. All the waypoints on a given course will be unique -- there will be at most one waypoint point at any location on the course. End of input will be marked by a line with a single '0'.


# Output
For each test case, output a single decimal number, indicating the smallest possible time for that factory. Output this number rounded (NOT truncated) to three decimal places. Print each answer on its own line, and do not print any blank lines between answers.

# See "sample_input_*.txt" and "sample_output_*.txt", where:
cat sample_input_small.txt | ./solution_executable | tee sample_output_small.txt

#Input examples:
10
60 65 20
40 80 90
15 80 55
60 50 70
35 25 15
85 30 20
75 25 10
80 30 90
60 70 10
65 35 55
30
40 30 80
25 60 45
5 70 30
45 20 40
70 70 35
75 75 50
50 10 10
50 25 35
65 25 55
90 65 70
90 50 15
85 10 15
10 95 95
25 30 90
25 65 5
85 90 90
90 75 15
35 20 85
55 40 45
25 10 60
10 55 60
30 10 25
90 55 35
35 10 90
75 80 20
20 45 60
25 70 35
80 95 20
35 60 25
90 65 40
50
15 30 30
40 30 95
65 35 10
95 75 70
40 25 50
30 65 55
60 65 60
35 95 30
5 25 75
55 35 65
70 75 90
25 55 80
15 50 65
15 55 95
55 55 50
20 20 30
65 40 25
15 35 65
70 60 35
25 30 80
65 15 15
55 35 5
55 95 20
30 30 70
65 15 60
35 55 15
50 75 20
20 30 80
95 35 70
15 50 20
35 5 100
45 25 20
85 35 85
25 95 75
90 20 70
70 90 85
15 25 95
75 90 40
85 25 90
85 35 100
30 80 80
30 90 75
50 50 95
95 95 85
5 90 30
40 15 65
30 45 25
5 15 65
15 25 60
80 60 55
0

#Output example:
272.589
870.817
1536.355
