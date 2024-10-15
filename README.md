!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Book Appointment</title>
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css">
    <style>
        .book_section { padding: 60px 0; }
        .book_section h4 { position: relative; padding-bottom: 5px; margin-bottom: 35px; }
        .book_section h4 span { color: #00c6a9; }
        .book_section form { padding: 35px 45px; box-shadow: 0 0 15px 10px rgba(0, 0, 0, 0.07); background-color: #fff; }
        .book_section form label { color: #000; }
        .book_section form .form-control { border: 1px solid #00c6a9; }
        .book_section form button.btn { background-color: #252525; color: #fff; }
    </style>
</head>
<body>

<section class="book_section layout_padding">
    <div class="container">
        <div class="row">
            <div class="col">
                <form method="POST" action="confirmation.php">
                    <h4>BOOK <span>APPOINTMENT</span></h4>
                    <div class="form-row">
                        <div class="form-group col-lg-4">
                            <label for="inputPatientName">Patient Name</label>
                            <input type="text" class="form-control" id="inputPatientName" name="patientName" required>
                        </div>
                        <div class="form-group col-lg-4">
                            <label for="inputDoctorName">Doctor's Name</label>
                            <select class="form-control" id="inputDoctorName" name="doctorName" required>
                                <option value="Dr.Henry">Dr.Henry</option>
                                <option value="Dr.Jennie">Dr.Jennie</option>
                                <option value="Dr.Marco">Dr.Marco</option>
                            </select>
                        </div>
                        <div class="form-group col-lg-4">
                            <label for="inputDepartmentName">Department's Name</label>
                            <select class="form-control" id="inputDepartmentName" name="departmentName" required>
                                <option value="Psychology">Psychology</option>
                                <option value="Cardiology">Cardiology</option>
                                <option value="Dermatologist">Dermatologist</option>
                            </select>
                        </div>
                    </div>
                    <div class="form-row">
                        <div class="form-group col-lg-4">
                            <label for="inputPhone">Phone Number</label>
                            <input type="tel" class="form-control" id="inputPhone" name="phone" required>
                        </div>
                        <div class="form-group col-lg-4">
                            <label for="inputSymptoms">Symptoms</label>
                            <input type="text" class="form-control" id="inputSymptoms" name="symptoms" required>
                        </div>
                        <div class="form-group col-lg-4">
                            <label for="inputDate">Choose Date</label>
                            <input type="text" class="form-control" id="inputDate" name="date" placeholder="MM-DD-YYYY" required readonly>
                        </div>
                    </div>
                    <div class="btn-box">
                        <button type="submit" class="btn">Submit Now</button>
                    </div>
                </form>
            </div>
        </div>
    </div>
</section>

</body>
</html>
