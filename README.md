<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Travel Itinerary Planning Questionnaire</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
        }
        h1 {
            text-align: center;
        }
        .section {
            margin-bottom: 15px;
        }
        .collapsible {
            background-color: #f9f9f9;
            color: #333;
            cursor: pointer;
            padding: 10px;
            width: 100%;
            border: none;
            text-align: left;
            outline: none;
            font-size: 16px;
        }
        .content {
            padding: 0 18px;
            max-height: 0;
            overflow: hidden;
            transition: max-height 0.2s ease-out;
            background-color: white;
            border: 1px solid #ddd;
            border-top: none;
        }
    </style>
    <script>
        document.addEventListener('DOMContentLoaded', function() {
            var collapsibles = document.querySelectorAll('.collapsible');
            collapsibles.forEach(function(collapsible) {
                collapsible.addEventListener('click', function() {
                    this.classList.toggle('active');
                    var content = this.nextElementSibling;
                    if (content.style.maxHeight) {
                        content.style.maxHeight = null;
                    } else {
                        content.style.maxHeight = content.scrollHeight + 'px';
                    }
                });
            });
        });
    </script>
</head>
<body>
    <h1>Travel Itinerary Planning Questionnaire</h1>
    <form>

        <!-- Section 1: Personal and Travel Details -->
        <div class="section">
            <button type="button" class="collapsible">1. Personal & Travel Details</button>
            <div class="content">
                <label for="name">Full Name:</label>
                <input type="text" id="name" name="name" required><br><br>

                <label for="contact">Contact Number:</label>
                <input type="text" id="contact" name="contact" required><br><br>

                <label for="email">Email Address:</label>
                <input type="email" id="email" name="email" required><br><br>

                <label for="additional-travelers">Number of Travelers (including yourself):</label>
                <input type="number" id="additional-travelers" name="additional-travelers" min="1" value="1" required><br><br>

                <label for="purpose">Purpose of Travel:</label>
                <input type="text" id="purpose" name="purpose" required><br><br>

                <label for="destination">Destination(s):</label>
                <input type="text" id="destination" name="destination" required><br><br>

                <label for="travel-dates">Travel Dates:</label>
                <input type="text" id="travel-dates" name="travel-dates" required><br><br>

                <label for="departure-city">Departure City:</label>
                <input type="text" id="departure-city" name="departure-city" required><br><br>
            </div>
        </div>

        <!-- Section 2: Flight Preferences -->
        <div class="section">
            <button type="button" class="collapsible">2. Flight Preferences</button>
            <div class="content">
                <label for="airline">Preferred Airline(s):</label>
                <input type="text" id="airline" name="airline"><br><br>

                <label>Class:</label>
                <select name="class" id="class">
                    <option value="economy">Economy</option>
                    <option value="business">Business</option>
                    <option value="first">First</option>
                </select><br><br>

                <label for="departure-time">Preferred Departure Time:</label>
                <input type="text" id="departure-time" name="departure-time"><br><br>

                <label>Layovers Acceptable?</label>
                <select name="layover" id="layover">
                    <option value="yes">Yes</option>
                    <option value="no">No</option>
                </select><br><br>

                <label for="frequent-flyer">Frequent Flyer Number(s):</label>
                <input type="text" id="frequent-flyer" name="frequent-flyer"><br><br>

                <label for="special-requests">Special Requests:</label>
                <textarea id="special-requests" name="special-requests" rows="2"></textarea><br><br>
            </div>
        </div>

        <!-- Section 3: Accommodation Preferences -->
        <div class="section">
            <button type="button" class="collapsible">3. Accommodation Preferences</button>
            <div class="content">
                <label>Hotel Star Rating:</label>
                <select name="hotel-rating" id="hotel-rating">
                    <option value="3-star">3-Star</option>
                    <option value="4-star">4-Star</option>
                    <option value="5-star">5-Star</option>
                </select><br><br>

                <label for="location">Location Preference:</label>
                <input type="text" id="location" name="location" required><br><br>

                <label for="room-type">Room Type:</label>
                <input type="text" id="room-type" name="room-type" required><br><br>

                <label for="special-requirements">Special Requirements:</label>
                <textarea id="special-requirements" name="special-requirements" rows="2"></textarea><br><br>

                <label for="budget">Budget per Night:</label>
                <input type="text" id="budget" name="budget" required><br><br>
            </div>
        </div>

        <!-- Section 4: Transportation -->
        <div class="section">
            <button type="button" class="collapsible">4. Transportation</button>
            <div class="content">
                <label>Airport Transfers Needed?</label>
                <select name="transfers" id="transfers">
                    <option value="yes">Yes</option>
                    <option value="no">No</option>
                </select><br><br>

                <label for="transportation">Preferred Mode of Transportation:</label>
                <input type="text" id="transportation" name="transportation"><br><br>

                <label for="car-preferences">Specific Car Service/Rental Preferences:</label>
                <input type="text" id="car-preferences" name="car-preferences"><br><br>

                <label for="additional-transport">Additional Transportation Needs:</label>
                <textarea id="additional-transport" name="additional-transport" rows="2"></textarea><br><br>
            </div>
        </div>

        <!-- Section 5: Schedule & Itinerary -->
        <div class="section">
            <button type="button" class="collapsible">5. Schedule & Itinerary</button>
            <div class="content">
                <label for="schedule">Set Schedule?</label>
                
