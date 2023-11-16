 VacationWeather360

Project Overview:

VacationWeather360 is a project focused on providing insightful climate data analysis for holiday planning in Honolulu, Hawaii. The analysis involves leveraging Python, SQLAlchemy ORM queries, Pandas, and Matplotlib to explore climate data stored in an SQLite database.

Part 1: Climate Data Exploration

Steps:

Database Connection:

Connect to the climate database using SQLAlchemy's create_engine() function.
Utilize automap_base() to reflect database tables into classes, creating references to the station and measurement classes.
Establish a SQLAlchemy session to link Python to the database.
Ensure proper closure of the session.
Precipitation Analysis:

Find the most recent date in the dataset.
Retrieve the preceding 12 months of precipitation data.
Load the results into a Pandas DataFrame, sort by date, and visualize the data with a plot.
Print summary statistics for the precipitation data.
Station Analysis:

Calculate the total number of weather stations in the dataset.
Identify the most active station with the highest observation count.
Determine the lowest, highest, and average temperatures for the most active station.
Query the previous 12 months of temperature observations (TOBS) data for the most active station and create a histogram.
Part 2: Climate App Design

Flask API Routes:

/ (Homepage):

Lists all available routes.
/api/v1.0/precipitation:

Returns the last 12 months of precipitation data in JSON format.
/api/v1.0/stations:

Provides a JSON list of weather stations.
/api/v1.0/tobs:

Queries the previous year's temperature observations for the most active station and returns them in JSON format.
/api/v1.0/<start> and /api/v1.0/<start>/<end>:

Returns JSON lists of minimum, average, and maximum temperatures for specified date ranges.
Usage:

Run the Flask app using the command python app.py.
