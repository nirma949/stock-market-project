# stock-market-project
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Business Dashboard</title>

<style>

*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:Segoe UI, sans-serif;
}

body{
    background:#f4f4f4;
}

/* NAVBAR */

.navbar{
    height:70px;
    background:#fff;
    display:flex;
    justify-content:space-between;
    align-items:center;
    padding:0 30px;
    border-bottom:1px solid #ddd;
}

.logo{
    font-size:22px;
    font-weight:bold;
    color:#3498db;
}

.nav-links{
    display:flex;
    gap:30px;
}

.nav-links a{
    text-decoration:none;
    color:#555;
    font-size:13px;
    text-transform:uppercase;
    font-weight:600;
}

.nav-links a.active{
    color:#000;
    border-bottom:3px solid #4db8ff;
    padding-bottom:22px;
}

.profile{
    display:flex;
    gap:15px;
    align-items:center;
}

/* DASHBOARD TITLE */

.header{
    background:#fff;
    padding:15px 30px;
    color:#555;
    border-bottom:1px solid #ddd;
}

/* TOP ANALYTICS */

.analytics{
    background:linear-gradient(90deg,#3c87d8,#1d197f);
    color:white;
    padding:40px;
    display:grid;
    grid-template-columns:1fr 1.5fr 1fr;
    gap:40px;
}

/* LEFT STATS */

.stats{
    display:grid;
    grid-template-columns:1fr 1fr;
    gap:30px;
}

.stat h4{
    font-size:13px;
    color:#cfe8ff;
    margin-bottom:10px;
}

.stat h2{
    font-size:46px;
    font-weight:300;
}

/* BAR CHART */

.chart-area{
    text-align:center;
}

.chart-title{
    margin-bottom:20px;
}

.bar-chart{
    height:220px;
    display:flex;
    justify-content:center;
    align-items:flex-end;
    gap:18px;
}

.bar{
    width:35px;
    background:#6fd2ff;
}

.bar:nth-child(1){height:160px;}
.bar:nth-child(2){height:90px;}
.bar:nth-child(3){height:70px;}
.bar:nth-child(4){height:170px;}
.bar:nth-child(5){height:100px;}
.bar:nth-child(6){height:130px;}

/* DONUT */

.donut-box{
    text-align:center;
}

.donut{
    width:180px;
    height:180px;
    border-radius:50%;
    margin:auto;
    background:
    conic-gradient(
        #55d7a7 0 60%,
        #ff5c87 60% 100%
    );
    position:relative;
}

.donut::after{
    content:"60%";
    position:absolute;
    width:120px;
    height:120px;
    background:#28217f;
    border-radius:50%;
    top:30px;
    left:30px;
    display:flex;
    align-items:center;
    justify-content:center;
    color:white;
    font-size:36px;
}

.legend{
    margin-top:20px;
    display:flex;
    justify-content:center;
    gap:25px;
}

/* TABLE SECTION */

.tables{
    padding:25px;
    display:grid;
    grid-template-columns:1fr 2fr;
    gap:20px;
}

.card{
    background:white;
    padding:15px;
    border:1px solid #e2e2e2;
}

.card h3{
    margin-bottom:15px;
    color:#444;
}

/* TABLE */

table{
    width:100%;
    border-collapse:collapse;
}

th{
    background:#f5f5f5;
    text-align:left;
    padding:12px;
    font-size:13px;
}

td{
    padding:12px;
    border-bottom:1px solid #eee;
    font-size:13px;
}

tfoot td{
    font-weight:bold;
    text-align:right;
    padding-top:15px;
}

/* RESPONSIVE */

@media(max-width:1000px){

.analytics{
    grid-template-columns:1fr;
}

.tables{
    grid-template-columns:1fr;
}

.stats{
    grid-template-columns:1fr 1fr;
}

}

</style>
</head>
<body>

<nav class="navbar">

    <div class="logo">Company</div>

    <div class="nav-links">
        <a href="#" class="active">Dashboard</a>
        <a href="#">Bid Board</a>
        <a href="#">Quotes</a>
        <a href="#">Jobs</a>
        <a href="#">Products</a>
        <a href="#">Customers</a>
        <a href="#">Accounting</a>
        <a href="#">Settings</a>
    </div>

    <div class="profile">
        👤 ⚡
    </div>

</nav>

<div class="header">
    John Smith's Dashboard
</div>

<section class="analytics">

    <div class="stats">

        <div class="stat">
            <h4>Work To Bid</h4>
            <h2>$500K</h2>
        </div>

        <div class="stat">
            <h4>Quoted Work</h4>
            <h2>$120K</h2>
        </div>

        <div class="stat">
            <h4>Contracted</h4>
            <h2>$350K</h2>
        </div>

        <div class="stat">
            <h4>Job Margin</h4>
            <h2>$90K</h2>
        </div>

    </div>

    <div class="chart-area">

        <div class="chart-title">
            <h3>Jobs Won by Month</h3>
        </div>

        <div class="bar-chart">
            <div class="bar"></div>
            <div class="bar"></div>
            <div class="bar"></div>
            <div class="bar"></div>
            <div class="bar"></div>
            <div class="bar"></div>
        </div>

    </div>

    <div class="donut-box">

        <h3>Win/Loss Percent by Value</h3>

        <div class="donut"></div>

        <div class="legend">
            <span>🔴 40% Loss</span>
            <span>🟢 60% Win</span>
        </div>

    </div>

</section>

<section class="tables">

    <div class="card">

        <h3>Outstanding Receivables</h3>

        <table>

            <thead>
                <tr>
                    <th>Invoice</th>
                    <th>Amount</th>
                </tr>
            </thead>

            <tbody>

                <tr>
                    <td>Invoice #0561.05</td>
                    <td>$30,000</td>
                </tr>

                <tr>
                    <td>Invoice #1054.02</td>
                    <td>$22,000</td>
                </tr>

                <tr>
                    <td>Invoice #0611.01</td>
                    <td>$34,000</td>
                </tr>

                <tr>
                    <td>Invoice #0061.00</td>
                    <td>$12,000</td>
                </tr>

            </tbody>

            <tfoot>
                <tr>
                    <td colspan="2">Total $98,000</td>
                </tr>
            </tfoot>

        </table>

    </div>

    <div class="card">

        <h3>Active Jobs</h3>

        <table>

            <thead>
                <tr>
                    <th>Customer</th>
                    <th>Job #</th>
                    <th>Quote #</th>
                    <th>Status</th>
                    <th>Amount</th>
                </tr>
            </thead>

            <tbody>

                <tr>
                    <td>ABC Company</td>
                    <td>15601</td>
                    <td>P-K-0059</td>
                    <td>Partially Ordered</td>
                    <td>$34,000</td>
                </tr>

                <tr>
                    <td>123LCC</td>
                    <td>17001</td>
                    <td>P-C561</td>
                    <td>Fully Received</td>
                    <td>$22,000</td>
                </tr>

                <tr>
                    <td>Westgate School</td>
                    <td>68110</td>
                    <td>K-K-555</td>
                    <td>Fully Ordered</td>
                    <td>$44,000</td>
                </tr>

                <tr>
                    <td>ABC Company</td>
                    <td>15601</td>
                    <td>P-K-0059</td>
                    <td>Partially Ordered</td>
                    <td>$34,000</td>
                </tr>

            </tbody>

            <tfoot>
                <tr>
                    <td colspan="5">Total $168,000</td>
                </tr>
            </tfoot>

        </table>

    </div>

</section>

</body>
</html>
