
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Appointment Confirmation</title>
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css">
    <style>
        .confirmation_section {
            padding: 60px 0;
        }
        .confirmation {
            padding: 35px 45px;
            box-shadow: 0 0 15px 10px rgba(0, 0, 0, 0.07);
            background-color: #fff;
            border-radius: 5px;
        }
        .confirmation h1 {
            margin-bottom: 20px;
            color: #00c6a9;
        }
        .confirmation ul {
            list-style-type: none;
            padding: 0;
        }
        .confirmation ul li {
            margin: 10px 0;
        }
    </style>
</head>
<body>

<section class="confirmation_section">
    <div class="container">
        <div class="row">
            <div class="col">
                <div class="confirmation">
                    <?php
                    if ($_SERVER["REQUEST_METHOD"] == "POST") {
                        $patientName = htmlspecialchars($_POST['patientName']);
                        $doctorName = htmlspecialchars($_POST['doctorName']);
                        $departmentName = htmlspecialchars($_POST['departmentName']);
                        $phone = htmlspecialchars($_POST['phone']);
                        $symptoms = htmlspecialchars($_POST['symptoms']);
                        $date = htmlspecialchars($_POST['date']);

                        echo "<h1>Appointment Confirmation</h1>";
                        echo "<p>Thank you, <strong>$patientName</strong>!</p>";
                        echo "<p>Your appointment has been confirmed.</p>";
                        echo "<ul>
                                <li><strong>Doctor's Name:</strong> $doctorName</li>
                                <li><strong>Department:</strong> $departmentName</li>
                                <li><strong>Phone Number:</strong> $phone</li>
                                <li><strong>Symptoms:</strong> $symptoms</li>
                                <li><strong>Date:</strong> $date</li>
                              </ul>";
                    } else {
                        echo "<p>No appointment data submitted.</p>";
                    }
                    ?>
                </div>
            </div>
        </div>
    </div>
</section>

</body>
</html>
