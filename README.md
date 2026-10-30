
<p align=center> <img src="images/wave-logo-transparent.png"></p>

<h1 align=middle> WAVE Telecom-Portfolio </h1>

<p align=center>Subscription &amp; Churn Dashboard &mdash; Junior-Level Business Analysis<br>&nbsp;Power BI | Simulated Saudi telecom data | January 2022&ndash;December 2024</p>

<h2>Introduction </h2>
WAVE Telecom is a fictional Saudi telecommunications operator used in this project to explore subscription performance, customer retention, and regional business trends through data analysis. Using simulated data from January 2022 to December 2024, this Power BI dashboard examines how subscription plans and customer segments contribute to monthly-fee value, where subscription churn is most prominent, and how performance varies across cities.
The dashboard brings these perspectives together to help identify performance patterns, highlight potential retention priorities, and support more informed business decisions. Its findings provide a starting point for investigating subscription growth and retention opportunities across WAVE Telecom.




<h2>Report objectives</h2>

The analysis focuses on four key business questions:
-	Plan Performance: Which subscription categories and plans contribute the most monthly-fee value, and which experience the highest subscription churn?
-	Customer Retention: Which customer segments show the greatest retention challenges, and where could targeted retention efforts be most useful?
-	Time Trends: How has the monthly-fee value associated with new subscriptions changed over the three-year period?
-	Regional Performance: Which cities have the strongest subscription performance, and where do differences in churn and support activity warrant further investigation?

  
<table align="center">
	<tbody>
		<tr>
			<td><p style="text-align: center;"><strong> Metric </strong></p></td>
			<td><p style="text-align: center;"><strong> Result </strong></p></td>
			<td><p style="text-align: center;"><strong> Interpretation </strong></p></td>
		</tr>
		<tr>
			<td><p><strong> Subscription records </strong></p></td>
			<td><p>6,248</p></td>
			<td><p>Unique subscription records in the fact table.</p></td>
		</tr>
		<tr>
			<td><p><strong> Customers represented </strong></p></td>
			<td><p>2,617</p></td>
			<td><p>Distinct customers appearing in the fact table; customers may have multiple subscriptions.</p></td>
		</tr>
		<tr>
			<td><p><strong> Sum of net monthly fee values </strong></p></td>
			<td><p>SAR 1,007,656.45</p></td>
			<td><p>Sum of subscription-level net monthly fees across records, not recognized accounting revenue.</p></td>
		</tr>
		<tr>
			<td><p><strong> Subscription-level churn rate </strong></p></td>
			<td><p>10.3%</p></td>
			<td><p>643 churned subscription records / 6,248 subscription records.</p></td>
		</tr>
		<tr>
			<td><p><strong> Support tickets </strong></p></td>
			<td><p>3,787</p></td>
			<td><p>Total support-ticket counts recorded across subscription rows.</p></td>
		</tr>
		<tr>
			<td><p><strong> Upgrade records </strong></p></td>
			<td><p>684</p></td>
			<td><p>Subscription records flagged as upgrades.</p></td>
		</tr>
	</tbody>
</table>

---
<h2>1. Executive summary</h2>

The dataset contains 6,248 subscription records, 3,000 customer records, 8 plans and 8 regional records. 
The sum of net monthly fees associated with the subscription records is SAR 1,007,656.45.<br /><br />
Postpaid has the largest total monthly-fee value in the category.
while the strongest subscription-level retention concern is concentrated in Prepaid plans and Student/Individual customer segments. 
City results are relatively close in revenue, but Madinah has the highest observed city subscription-level churn rate.


---
<h2>2. Subscription cohort fee-value trend</h2>


<table>
	<tbody>
		<tr>
			<td>  <p><strong> Subscription start year </strong></p> </td>
			<td>  <p><strong> Records </strong></p>	</td>
			<td>	<p><strong> Net monthly-fee value (SAR) </strong></p>	</td>
			<td>	<p><strong> Change vs prior year </strong></p> </td>
			<td>	<p><strong> Record-count change </strong></p>	</td>
		</tr>
		<tr>
			<td>	<p><strong> 2022 </strong></p>	</td>
			<td>	<p> 1,631 </p>  </td>
			<td>	<p> 264,467.95 </p>	</td>
			<td>	<p>  </p> </td>
			<td>	<p>  </p>	</td>
		</tr>
		<tr>
			<td>	<p><strong> 2023 </strong></p></td>
			<td>	<p> 2,178 </p>	</td>
			<td>	<p> 346,943.95 </p>	</td>
			<td>	<p> +31.2% </p>	</td>
			<td>	<p> +33.5% </p> </td>
		</tr>
		<tr>
			<td>	<p><strong> 2024 </strong></p>	</td>
			<td>	<p> 2,439 </p>	</td>
			<td>	<p> 396,244.55 </p>	</td>
			<td>	<p> +14.2% </p>	</td>
			<td>	<p> +12.0% </p>	</td>
		</tr>
	</tbody>
</table>

   
> The total net monthly-fee value associated with subscriptions created in 2023 and 2024 is higher than in 2022, The highest year-quarter cohort fee-value total is 2024 Q4 (SAR 113,144), followed by 2024 Q3 (SAR 111,550), but the year-over-year growth rate slowed in 2024.

![waterfall](images/wave-waterfall-churn-rate.png)


---
<h2>3. Plan category performance [plan + segments image]</h2>

<table>
	<tbody>
		<tr>
			<td><p><strong> Category </strong></p></td>
			<td><p><strong> Records </strong></p></td>
			<td><p><strong> Net monthly-fee value (SAR) </strong></p></td>
			<td><p><strong> Net monthly-fee value % </strong></p></td>
			<td><p><strong> Churned subscriptions </strong></p></td>
			<td><p><strong> Subscription churn rate </strong></p></td>
		</tr>
		<tr>
			<td><p><strong> Postpaid </strong></p></td>
			<td><p>3,086</p></td>
			<td><p>617,890.10</p></td>
			<td><p>61%</p></td>
			<td><p>217</p></td>
			<td><p>7.0%</p></td>
		</tr>
		<tr>
			<td><p><strong> Prepaid </strong></p></td>
			<td><p>2,671</p></td>
			<td><p>176,790.30</p></td>
			<td><p>18%</p></td>
			<td><p>397</p></td>
			<td><p>14.9%</p></td>
		</tr>
		<tr>
			<td><p><strong> Business </strong></p></td>
			<td><p>491</p></td>
			<td><p>212,976.05</p></td>
			<td><p>21%</p></td>
			<td><p>29</p></td>
			<td><p>5.9%</p></td>
		</tr>
	</tbody>
</table>

> Postpaid contributes the largest fee value across the subscriptions in the dataset (about 61%). Prepaid has the highest subscription churn rate (14.9%) and the largest number of churned subscription records (397). This makes Prepaid a sensible retention-investigation priority. 






<table>
	<tbody>
		<tr>
			<td>
				<p><strong> Plan </strong></p>
			</td>
			<td>
				<p><strong> Net monthly-fee value (SAR) </strong></p>
			</td>
			<td>
				<p><strong> Subscription churn rate </strong></p>
			</td>
			<td>
				<p><strong> Practical read </strong></p>
			</td>
		</tr>
		<tr>
			<td>
				<p><strong> Pro Unlimited </strong></p>
			</td>
			<td>
				<p>322,088.50</p>
			</td>
			<td>
				<p>6.3%</p>
			</td>
			<td>
				<p>Largest plan fee-value contribution.</p>
			</td>
		</tr>
		<tr>
			<td>
				<p><strong> Plus 50GB </strong></p>
			</td>
			<td>
				<p>169,025.60</p>
			</td>
			<td>
				<p>8.4%</p>
			</td>
			<td>
				<p>High fee-value contribution; 
          <br>monitor retention.</p>
			</td>
		</tr>
		<tr>
			<td>
				<p><strong> Basic 5GB </strong></p>
			</td>
			<td>
				<p>54,397.35</p>
			</td>
			<td>
				<p>15.7%</p>
			</td>
			<td>
				<p>Higher churn; 
          <br>investigate plan fit and perceived value.</p>
			</td>
		</tr>
		<tr>
			<td>
				<p><strong> Student 15GB </strong></p>
			</td>
			<td>
				<p>24,363.90</p>
			</td>
			<td>
				<p>17.1%</p>
			</td>
			<td>
				<p>Highest observed plan churn rate; 
          <br>investigate student needs and affordability.</p>
			</td>
		</tr>
	</tbody>
</table>

<p align=center><img src="images/wave-cluster-plan.png"></p>


---
<h2>4. Customer segments</h2>
Segment	Records	Net monthly-fee value (SAR)	Subscription churn rate

<table>
	<tbody>
		<tr>
			<td>			<p><strong>Segment</strong></p>			</td>
			<td>				<p><strong>Records</strong></p>			</td>
			<td>				<p><strong>Net monthly-fee value (SAR)</strong></p>			</td>
			<td>				<p><strong>Subscription churn rate</strong></p></td>
		</tr>
		<tr>
			<td>				<p><strong>Individual</strong></p>			</td>
			<td>				<p>3,074</p>			</td>
			<td>				<p>381,384.50</p>			</td>
			<td>				<p>10.8%</p>			</td>
		</tr>
		<tr>
			<td>				<p><strong>Family</strong></p>			</td>
			<td>				<p>1,278</p>			</td>
			<td>				<p>277,452.90</p>			</td>
			<td>				<p>6.3%</p>			</td>
		</tr>
		<tr>
			<td>				<p><strong>Business</strong></p>			</td>
			<td>				<p>770</p>			</td>
			<td>				<p>274,645.75</p>			</td>
			<td>				<p>5.3%</p>			</td>
		</tr>
		<tr>
			<td>				<p><strong>Student</strong></p>			</td>
			<td>				<p>1,126</p>			</td>
			<td>				<p>74,173.30</p>			</td>
			<td>				<p>16.8%</p>			</td>
		</tr>
	</tbody>
</table>

> Student subscriptions have the highest observed churn rate (16.8%), followed by Individual subscriptions (10.8%). Family and Business subscriptions have lower rates.



---
<h2>5. Regional performance[cluster]</h2>

<table>
    <tbody>
        <tr>
            <td><p><strong> City </strong></p> </td>
            <td><p><strong> Records </strong></p> </td>
            <td><p><strong> Net monthly-fee value (SAR) </strong></p>   
            <td><p><strong> Subscription churn rate </strong></p> </td>
            <td><p><strong> Avg. tickets per record </strong></p> </td>
        </tr>
        <tr>
            <td><p><strong> Riyadh </strong></p></td>
            <td><p>843</p></td>
            <td><p>136,451.40</p></td>
            <td><p>10.3%</p></td>
            <td><p>58%</p></td>
        </tr>
        <tr>
            <td><p><strong> Madinah </strong></p></td>
            <td><p>830</p></td>
            <td><p>134,593.15</p></td>
            <td><p>11.8%</p></td>
            <td><p>62%</p></td>
        </tr>
        <tr>
            <td><p><strong> Abha </strong></p></td>
            <td><p>812</p></td>
            <td><p>134,586.15</p></td>
            <td><p>11.1%</p></td>
            <td><p>58%</p></td>
        </tr>
        <tr>
            <td><p><strong> Makkah </strong></p> </td>
            <td><p>838</p></td>
            <td><p>131,709.50</p></td>
            <td><p>9.4%</p></td>
            <td><p>64%</p></td>
        </tr>
        <tr>
            <td><p><strong> Jeddah </strong></p></td>
            <td><p>747</p></td>
            <td><p>122,380.90</p></td>
            <td><p>8.3%</p></td>
            <td><p>64%</p></td>
        </tr>
        <tr>
            <td><p><strong> Tabuk </strong></p></td>
            <td><p>729</p></td>
            <td><p>119,418.65</p></td>
            <td><p>10.7%</p></td>
            <td><p>59%</p></td>
        </tr>
        <tr>
            <td><p><strong> Dammam </strong></p></td>
            <td><p>730</p></td>
            <td><p>116,951.50</p></td>
            <td><p>10.1%</p></td>
            <td><p>63%</p></td>
        </tr>
        <tr>
            <td><p><strong> Khobar </strong></p></td>
            <td><p>719</p></td>
            <td><p>111,565.20</p></td>
            <td><p>10.4%</p></td>
            <td><p>56%</p></td>
        </tr>
    </tbody>
</table>




> Riyadh has the highest fee value associated with its subscriptions; Khobar has the lowest. Madinah has the highest subscription churn rate (11.8%), while Jeddah has the lowest (8.3%). 

<p align=center> <img src="images/wave-cluster-city.png"> </p>

---
<h2>6. Actionable recommendations</h2>

-	Prioritize a Prepaid retention diagnostic. Break subscription churn down by plan, segment, acquisition channel, discount and subscription age. Test a targeted intervention with a comparison group before scaling it.
-	Investigate Student 15GB and Basic 5GB. Check plan fit, affordability and usage needs. Test renewal reminders or a better-fitting plan before applying broad discounts.<br>
-	Protect high-value Postpaid plans. Monitor subscription churn and downgrade signals for Pro Unlimited and Plus 50GB; assess retention alongside monthly-fee value.<br>
-	Run a focused Madinah review. Compare its plan/segment mix and service measures with lower-churn cities before attributing the difference to network or support quality.<br>
-	Label the current time trend as subscription cohort fee value. To analyze recognized revenue by month, add billing-history data with billed/recognized amounts and billing dates.<br>
-	Agree KPI definitions before publishing. Keep subscription-level churn separate from customer active status, and document the denominator for each KPI.


---
<h2>7. Caveat</h2>

- No churn reason, ticket category, ticket resolution time, network quality, or customer lifetime value fields are present in the fact-table
> which limits causal explanations.

-	The dataset does not show revenue earned during each calendar period.
> So billing-history table would be needed to analyze recognized revenue over time.


---
<h2>8. Dataset and quality review [ERD]</h2>

Technical details: 

- dim_customers (3,000 rows)
- dim_plans (8)
- dim_regions (8)
- fact_subscriptions (6,248)
- No blank cells or exact duplicate rows were found in the supplied sheets. 
- The subscription_id key in fact-table is unique, while customer_id is repeated which is normal for a transaction/event-style fact.
- All customer_id, plan_id and region_id values in the fact table match a record in their respective dimensions. 
- The date-derived year and month columns match subscription_date.


![ERD](images/wave-erd.png)

--- 

<p align="center">
<strong>
		 Disclaimer:
		<br />
		 These are descriptive findings from simulated data for demonstration purposes,
		<br />
		 not actual Saudi telecom market performance.
	</strong>
</p>

