# Ticket-Issuers-Scheduling
## **Optimized Ticket Worker Scheduling at Kandy Railway Station**
This project addresses the challenges of inefficient ticket worker scheduling at the Kandy Railway Station, which has resulted in overstaffing during off-peak hours and understaffing during peak hours. The primary goal was to develop an optimized scheduling model to ensure the right number of workers are available at all times, thereby improving both operational efficiency and customer service.


## **Problem Overview**
The Kandy Railway Station faces staffing and scheduling challenges, particularly after merging two shifts into one extended shift due to labor regulations. The two new shifts are:




-  Shift 1: 8:00 AM to 4:00 PM 


-  Shift 2: 4:00 PM to 8:00 AM 

Currently, the station has 12 ticket issuers, but management believed this was insufficient and proposed hiring 5 additional workers. A mathematical analysis revealed that the 12 existing workers could theoretically suffice by using the maximum allowable overtime of 11-12 hours per week. However, this was deemed a poor solution from the workers' perspective, as it could lead to burnout and dissatisfaction. The project, therefore, aimed to find the optimal number of new hires to balance operational needs with worker satisfaction.





## **Methodology**
A mixed-integer linear programming (MILP) model was developed to solve the scheduling problem. The model's objective was to minimize the total number of workers recruited while ensuring a fair workload distribution and compliance with various constraints.

**Key Constraints:**

-  Each shift must have at least 4 workers.

-  Workers cannot be scheduled for two consecutive shifts.

-  Each worker must be assigned at least one day and one night shift per week.

-  Workers must work a minimum of 48 hours per week, with a maximum of 12 permissible overtime hours.

**Software and Tools:**


-  PuLP: Used to formulate and solve the optimization problem.


-  Pandas: Used for data handling and analysis.


-  Matplotlib: Used for data visualization.

## **Results and Discussion**
The analysis evaluated four scenarios with varying numbers of additional workers:



-  Instance 1 (13 workers): Overtime hours remained high, at 11-12 hours per worker per week, which did not improve worker satisfaction.



-  Instance 2 (14 workers): This proved to be the optimal solution. It reduced overtime hours to 3 per worker per week, provided flexibility, and met the minimum shift coverage of 4 workers per shift.






-  Instance 3 (15 workers): This scenario led to overstaffing, which was unnecessary and inefficient, although overtime was minimal.




-  Instance 4 (16 workers): This resulted in significant overstaffing, making the system inflexible and overly costly.

The project concluded that recruiting 2 additional workers (for a total of 14) is the most practical and cost-effective solution, balancing operational efficiency, cost, and worker satisfaction. This optimized staffing level reduces the reliance on overtime, thereby lowering stress and fatigue among employees while maintaining compliance with labor regulations.





## **Conclusion**##
The successful application of mathematical optimization using the PuLP library provided a data-driven solution to the scheduling problem at the Kandy Railway Station. The model provides a sustainable workforce management plan that addresses current operational challenges and enhances the station's reputation for reliable and passenger-friendly service.
