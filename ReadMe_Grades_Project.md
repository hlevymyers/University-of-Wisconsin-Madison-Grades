
# ReadMe

## University of Wisconsin at Madison Examination of Grade Distributions 

## Abstract:

Grades at the university level are a reflection of student learning, professor teaching and engagement with the subject. Using a publicly available dataset from the University of Wisconsin, Madison, student grades from 2006 to 2017 were examined to see if there is a difference in grades in STEM or traditional liberal arts classes, large or small classes, morning or afternoon classes and if there was grade inflation over the decade. No significant difference was detected in grade distributions in STEM when compared with traditional liberal arts classes or in morning and afternoon classes. Grade inflation was just barely significant; more study on the topic would be advised in order to reach robust conclusions. However, there is a very real difference in grade distributions in large classes when compared with small ones with small classes having significantly higher grades and more "A"s overall given. 

## The Data Set

The University of Wisconsin at Madison (UW-M) administration is concerned about enrollment, retention and graduation rates. As part of addressing this concern, an examination of grades across all subjects covering the years 2006 - 2017. The goal was to understand four issues: 1. if STEM fields had different grade distributions than traditional liberal arts subjects, 2. Did large classes (more than 35 students, which is the 75th percentile of enrollment) had a different grade distribution than smaller classes, 3. Does the time of day (before or after noon) make a difference in grades, and 4. Has there been a change in grade distributions over the 10 years of the dataset. The assumption is that grades are a proxy for student success and knowledge gained. They also acted as a proxy for enrollment, one grade per student. UW-M publishes reports for all courses (and sections of these courses), instructors, subjects, and grade reports for each section for every Fall and Spring semester since 2006.

There are more than 9,000 courses in this dataset. There are nearly 200,000 course sections with grades, with 3 million grades reported in total. 18,000 instructors are included in the dataset, all of whom are associated with various sections that may or may not have grades reported for them.

The data was retrieved from the UW Madison registrar office, and extracted from PDF files using the open source tool, madgrades-extractor. This information was publicaly available on kaggle at (https://www.kaggle.com/Madgrades/uw-madison-courses). This is the work of Helen Levy-Myers and Llewellyn Hickes Jones.

The tables included: 'instructors', 'grade_dist', 'courses', 'course_offerings', 'subjects', 'subject_memberships', 'sections', 'schedules', 'rooms', 'focus', 'teachings', 'Term' .

This schema was also provided.

![image.png](attachment:image.png)

One of the first steps was calculating a grade point average (GPA) for each class. Grade values are assigned by the university registrar. Class enrollment assumed that each student received only one grade and each grade represented a single student. "No Work" was assumed to be a "F" score as the registrar noted that this grade should often be recored as a "F." All other non-credit grades, such as satisfactory, progress, etc. were not included. A weighted GPA was also calculated and used in some analysis.

More than 100,000 or 52% of the classes offered do not have any grades. Grades are the metric this analysis is based on for enrollment and student engagement. Without grades, these classes are not useful to the analysis. The class with the most zero-grades is Research (13,074), and other research/thesis classes are at the top. The bottom lists more unique classes like Thai Poetry that appeal to only a few students. These classes were eliminated from the dataset.

## Do STEM Majors have a Different Grade Distribution than Liberal Arts Majors?

There are 200 majors that are not arranged in any order and often have similar names which most likely reflects that majors name changes over the decade. "English" is both upper case and title case. A new variable was added and added to the table assigning each major a STEM or Liberal Arts (LIB_ARTS) label. The assignment was based on the list of STEM majors that the National Science Foundation uses and the Department of Homeland Security uses for H-1B visas that STEM-eligible degrees. Majors that appeared on either list were given the STEM label. Medical related majors, such as nursing, are not included in STEM designations. (https://en.wikipedia.org/wiki/Science,_technology,_engineering,_and_mathematics)


## Do Large Classes have a Different Grade Distribution than Small Classes?

The 75th distribution level for class size is 35 students and was determined to be the cutoff for large and small classes. Large and small classes do have signficantly different grade distributions. This was confirmed using the Central Limit Theorem. The reason may possibly related to large classes have a required bell curve. Small classes, especially those six and smaller, distribute more "A"s.


## Do Morning Classes have a Different Grade Distribution than Afternoon Classes?

There is some research and many stories about the best time for a class, student learning, attendance and enrollment. The day was divided at noon for morning and evening classes. There was no difference found between morning and afternoon classes with a single cutoff. It is possible that with more time frames more differences would be found.


## Has There Been Grade Distribution During the Past Decade?

The p-value for this is exactly at 5%, indicating there is grade inflation, but as it just on the line of significant, more research should be done to provide an solid answer on this topic.