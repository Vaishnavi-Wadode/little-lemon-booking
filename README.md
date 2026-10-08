# little-lemon-booking

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Little Lemon - Book a Table</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <img src="logo.png" alt="Little Lemon Logo" width="300">
        <nav>
            <!-- Add your navigation links here if needed -->
        </nav>
    </header>

    <main>
        <section class="booking-form">
            <h1>Book Your Table</h1>
            <p>Reserve a spot at Little Lemon for an unforgettable dining experience.</p>

            <form id="bookingForm" action="https://httpbin.org/post" method="POST">
                <fieldset>
                    <legend>Personal Details</legend>

                    <label for="fname">First Name *</label>
                    <input type="text" id="fname" name="fname" required>

                    <label for="lname">Last Name *</label>
                    <input type="text" id="lname" name="lname" required>

                    <label for="email">Email Address *</label>
                    <input type="email" id="email" name="email" required>

                    <label for="phone">Phone Number</label>
                    <input type="tel" id="phone" name="phone">
                </fieldset>

                <fieldset>
                    <legend>Reservation Details</legend>

                    <label for="guests">Number of Guests *</label>
                    <select id="guests" name="guests" required>
                        <option value="1">1 Person</option>
                        <option value="2" selected>2 People</option>
                        <option value="3">3 People</option>
                        <option value="4">4 People</option>
                        <option value="5">5 People</option>
                        <option value="6">6 People</option>
                        <option value="7">7 People</option>
                        <option value="8">8+ People (Please specify in comments)</option>
                    </select>

                    <label for="date">Reservation Date *</label>
                    <input type="date" id="date" name="date" required>

                    <label for="time">Reservation Time *</label>
                    <input type="time" id="time" name="time" min="11:00" max="22:00" required>

                    <label for="occasion">Occasion (Optional)</label>
                    <select id="occasion" name="occasion">
                        <option value="">None</option>
                        <option value="birthday">Birthday</option>
                        <option value="anniversary">Anniversary</option>
                        <option value="business">Business Dinner</option>
                        <option value="other">Other</option>
                    </select>

                    <label for="seating">Seating Preference</label>
                    <div>
                        <input type="radio" id="indoor" name="seating" value="indoor" checked>
                        <label for="indoor">Indoor</label>

                        <input type="radio" id="outdoor" name="seating" value="outdoor">
                        <label for="outdoor">Outdoor</label>

                        <input type="radio" id="no-preference" name="seating" value="no preference">
                        <label for="no-preference">No Preference</label>
                    </div>

                    <label for="comments">Special Requests / Comments</label>
                    <textarea id="comments" name="comments" rows="4"></textarea>
                </fieldset>

                <button type="submit">Confirm Reservation</button>
            </form>
        </section>
    </main>

    <footer>
        <p>&copy; 2023 Little Lemon. All rights reserved.</p>
    </footer>

    <!-- Link to JavaScript file -->
    <script src="script.js"></script>
</body>
</html>
