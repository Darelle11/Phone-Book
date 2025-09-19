# Phone-Book
DARELLE

<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Corporate Job Aid - Phone Book</title>
    <style>
        body { font-family: Arial, sans-serif; margin: 20px; background-color: #f9f9f9; }
        h1 { color: #333; }
        input[type="text"] {
            width: 100%;
            padding: 10px;
            margin-bottom: 20px;
            font-size: 16px;
            border: 1px solid #ccc;
        }
        table {
            width: 100%;
            border-collapse: collapse;
            background-color: #fff;
        }
        th, td {
            padding: 12px;
            border: 1px solid #ddd;
            text-align: left;
        }
        th {
            background-color: #004080;
            color: white;
        }
        tr:hover {
            background-color: #f1f1f1;
        }
    </style>
</head>
<body>
    <h1>Phone Book Directory</h1>
    <input type="text" id="searchInput" onkeyup="filterTable()" placeholder="Search for department, phone number, or notes...">

    <table id="phoneBookTable">
        <thead>
            <tr>
                <th>Department</th>
                <th>Phone Number</th>
                <th>Notes</th>
            </tr>
        </thead>
        <tbody>
            <tr><td>PCS</td><td>800-215-0575</td><td>Collections agency, provide to caller</td></tr>
            <tr><td>Language Line</td><td>877-906-6955</td><td>Region 3, Group patient, Business Office</td></tr>
            <tr><td>Site Support</td><td>424-653-3007</td><td>Insurance calls, department of health, wellfare check, cold transfer, not for patients</td></tr>
            <tr><td>Mailing Address</td><td>PO BOX 744860</td><td>Los Angeles, CA 90074-4880</td></tr>
            <tr><td>Online Payment</td><td>Pay.optum.com</td><td>Patient online payment portal</td></tr>
            <tr><td>OCMG Email</td><td>oga_ocmg_smg@optum.com</td><td>Centralized email</td></tr>
            <tr><td>PRD Vendor</td><td>PRD-VendorSupport@optum.optumcare.com</td><td>Business Office contact</td></tr>
            <tr><td>Financial Assistance</td><td>19191 S Vermont Ave</td><td>7th Floor, Torrance CA, 90502</td></tr>
            <tr><td>Claims Recovery</td><td>818-774-9721</td><td>Third Party Liability, Subpoena requests, law firm, auto insurance</td></tr>
            <tr><td>Patient Support</td><td>800-403-4160</td><td>HMO patient billing inquiries</td></tr>
            <tr><td>Claims Dept</td><td>310-965-1100</td><td>Provider's office claim status</td></tr>
            <tr><td>Medical Records</td><td>310-212-0030</td><td>Request for medical records</td></tr>
            <tr><td>LHCP</td><td>855-922-0781</td><td>Calls prior to Sept 15, 2025</td></tr>
            <tr><td>Online Portal Issue</td><td>866-262-4586</td><td>Technical support</td></tr>
            <tr><td>OptumRX</td><td>800-356-3477</td><td>Pharmacy support</td></tr>
            <tr><td>OCMG / NEXTGEN</td><td>833-505-3287</td><td>Calls prior to July 15, 2025</td></tr>
            <tr><td>EPIC</td><td>844-672-0036</td><td>Statement date after July 15, 2025</td></tr>
            <tr><td>CA IT Helpdesk</td><td>310-630-2300</td><td>Agents only</td></tr>
            <tr><td>CA HD</td><td>888-848-3375</td><td>IT Helpdesk</td></tr>
            <tr><td>Lab Corp</td><td>800-845-6167</td><td>Lab support</td></tr>
            <tr><td>Quest Diagnostics</td><td>800-758-6647</td><td>Lab support</td></tr>
            <tr><td>Scheduled Service</td><td>877-267-8861</td><td>Service inquiries</td></tr>
            <tr><td>SMG / Saddleback</td><td>949-465-8155</td><td>Calls for DOS prior to July 15, 2025</td></tr>
            <tr><td>MyChart Support</td><td>855-873-2376</td><td>Website or mobile app support</td></tr>
            <tr><td>Optum Main Office</td><td>310-354-4200</td><td>Accounts payable department</td></tr>
            <tr><td>Radnet/Beverly Radiology</td><td>800-272-3638</td><td>Radiology support</td></tr>
        </tbody>
    </table>

    <script>
        function filterTable() {
            var input = document.getElementById("searchInput");
            var filter = input.value.toLowerCase();
            var table = document.getElementById("phoneBookTable");
            var tr = table.getElementsByTagName("tr");

            for (var i = 1; i < tr.length; i++) {
                var tdList = tr[i].getElementsByTagName("td");
                var rowText = "";
                for (var j = 0; j < tdList.length; j++) {
                    rowText += tdList[j].textContent.toLowerCase();
                }
                tr[i].style.display = rowText.includes(filter) ? "" : "none";
            }
        }
    </script>
</body>
</html>
