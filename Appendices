## APPENDICES


# APPENDIX A

/*   import - begin   */
libname PERM '/folders/myfolders/'; 

proc import 
	datafile='/folders/myfolders/sasuser.v94/clothing_store_pp_opt1.csv' 
	dbms=csv out=WORK.MIS543_M8_PP_OPT1 replace;
	GETNAMES=YES;
run;

/*   data - begin   */
data sales;
	infile '/folders/myfolders/sasuser.v94/clothing_store_pp_opt1.csv' DLM=',';
	input customer_id zip_code num_purch_visits total_net_sales cc_card avg_spent_visit p_sweaters p_knit_tops p_knit_dres p_blouses p_jackets p_car_pnts p_cas_pnts p_shirts p_dresses p_suits p_outerwear p_jewelry p_fashion p_legwear p_collectibles gmp numb_mkt_promos num_days_cust_file mrkdn_pntg lifestyle_clustype pcnt_rtns days_btwn_purch lifetime_avg_btwn_visits;
run;

proc datasets lib=WORK nolist;
	modify MIS543_M8_PP_OPT1;
	label customer_id='Customer ID';
	label zip_code='Zip Code';
	label num_purch_visits='Number of Purchases in Visit' ;
	label total_net_sales='Total Net Sales';
	label cc_card='Credit Card';
	label avg_spent_visit='Average Amount Spent per Visit';
	label p_sweaters='Sweaters (Total Sales %)';
	label p_knit_tops='Tops (Total Sales %)';
	label p_knit_dres='Knit Dresses (Total Sales %)';
	label p_blouses='Blouses (Total Sales %)';
	label p_jackets='Jackets (Total Sales %)';
	label p_car_pnts='Career Pants (Total Sales %)';
	label p_cas_pnts='Casual Pants (Total Sales %)';
	label p_shirts='Shirts (Total Sales %)';
	label p_dresses='Dresses (Total Sales %)';
	label p_suits='Suits (Total Sales %)';
	label p_outerwear='Outerwear (Total Sales %)';
	label p_jewelry='Jewelry (Total Sales %)';
	label p_fashion='Fashionable Wear (Total Sales %)';
	label p_legwear='Leg Wear (Total Sales %)';
	label p_collectibles='Collectibles (Total Sales %)';
	label gmp='Gross Margin Percentage';
	label num_mkt_promos='Number of Marketing Promotions on File';
	label num_days_cust_file='Number of Days the Customer has been on File';
	label mrkdn_pntg='Markdown Percentage on Customer Purchases';
	label lifestyle_clustype='Lifestyle Cluster Type';
	label pcnt_rtns='Percent of Returns';
	label days_btwn_purch='Number of Days Between Purchases';
	label lifetime_avg_btwn_visits='Lifetime Average Days between Visits';
run;
/*   data - end   */


/*   SUMMARY STATISTICS   */  
/*   preliminiary summary statistics - begin   */
ods noproctitle;
ods graphics / imagemap=on;

proc means data=WORK.MIS543_M8_PP_OPT1 chartype mean median mode std min max range n vardef=df;
	title 'Summary Statistics';
	var num_purch_visits;
	var total_net_sales;
	var avg_spent_visit;
	var p_sweaters;
	var p_knit_tops;
	var p_knit_dres;
	var p_blouses;
	var p_jackets;
	var p_car_pnts;
	var p_cas_pnts;
	var p_shirts;
	var p_dresses;
	var p_suits;
	var p_outerwear;
	var p_jewelry;
	var p_fashion;
	var p_legwear;
	var p_collectibles;
	var gmp;
	var num_mkt_promos;
	var num_days_cust_file;
	var mrkdn_pntg;
	var lifestyle_clustype;
	var pcnt_rtns;
	var days_btwn_purch;
	var lifetime_avg_btwn_visits;
run;
/*   preliminiary summary statistics - end   */



# APPENDIX B

/*  One-Way Anova on lifestyle_clustype and p_jackets - begin  */
Title;
ods noproctitle;
ods graphics / reset width=15.0in height=6.0in imagemap;

proc glm data=WORK.MIS543_M8_PP_OPT1_LC plots(only);
	class lifestyle_clustype;
	model p_jackets=lifestyle_clustype;
	means lifestyle_clustype / welch plots=none;
	lsmeans lifestyle_clustype / plots=(meanplot);
	run;
quit;
/*  One-Way Anova on lifestyle_clustype and p_jackets - end  */



# APPENDIX C

/*   import - begin   */
libname PERM '/folders/myfolders/'; 

proc import 
	datafile='/folders/myfolders/sasuser.v94/clothing_store_pp_opt1.csv' 
	dbms=csv out=WORK.MIS581_M8_PP_OPT1 replace;
	GETNAMES=YES;
run;

/*   data - begin   */
data sales;
	infile '/folders/myfolders/sasuser.v94/clothing_store_pp_opt1.csv' DLM=',';
	input customer_id zip_code num_purch_visits total_net_sales cc_card avg_spent_visit p_sweaters p_knit_tops p_knit_dres p_blouses p_jackets p_car_pnts p_cas_pnts p_shirts p_dresses p_suits p_outerwear p_jewelry p_fashion p_legwear p_collectibles gmp numb_mkt_promos num_days_cust_file mrkdn_pntg lifestyle_clustype pcnt_rtns days_btwn_purch lifetime_avg_btwn_visits;
run;

proc datasets lib=WORK nolist;
	modify MIS581_M8_PP_OPT1;
	label customer_id='Customer ID';
	label zip_code='Zip Code';
	label num_purch_visits='Number of Purchases in Visit' ;
	label total_net_sales='Total Net Sales';
	label cc_card='Credit Card';
	label avg_spent_visit='Average Amount Spent per Visit';
	label p_sweaters='Sweaters (Total Sales %)';
	label p_knit_tops='Tops (Total Sales %)';
	label p_knit_dres='Knit Dresses (Total Sales %)';
	label p_blouses='Blouses (Total Sales %)';
	label p_jackets='Jackets (Total Sales %)';
	label p_car_pnts='Career Pants (Total Sales %)';
	label p_cas_pnts='Casual Pants (Total Sales %)';
	label p_shirts='Shirts (Total Sales %)';
	label p_dresses='Dresses (Total Sales %)';
	label p_suits='Suits (Total Sales %)';
	label p_outerwear='Outerwear (Total Sales %)';
	label p_jewelry='Jewelry (Total Sales %)';
	label p_fashion='Fashionable Wear (Total Sales %)';
	label p_legwear='Leg Wear (Total Sales %)';
	label p_collectibles='Collectibles (Total Sales %)';
	label gmp='Gross Margin Percentage';
	label num_mkt_promos='Number of Marketing Promotions on File';
	label num_days_cust_file='Number of Days the Customer has been on File';
	label mrkdn_pntg='Markdown Percentage on Customer Purchases';
	label lifestyle_clustype='Lifestyle Cluster Type';
	label pcnt_rtns='Percent of Returns';
	label days_btwn_purch='Number of Days Between Purchases';
	label lifetime_avg_btwn_visits='Lifetime Average Days between Visits';
run;
/*   data - end   */


/*   SUMMARY STATISTICS   */  
/*   preliminiary summary statistics - begin   */
ods noproctitle;
ods graphics / imagemap=on;

proc means data=WORK.MIS581_M8_PP_OPT1 chartype mean median mode std min max range n vardef=df;
	title 'Summary Statistics';
	var num_purch_visits;
	var total_net_sales;
	var avg_spent_visit;
	var p_sweaters;
	var p_knit_tops;
	var p_knit_dres;
	var p_blouses;
	var p_jackets;
	var p_car_pnts;
	var p_cas_pnts;
	var p_shirts;
	var p_dresses;
	var p_suits;
	var p_outerwear;
	var p_jewelry;
	var p_fashion;
	var p_legwear;
	var p_collectibles;
	var gmp;
	var num_mkt_promos;
	var num_days_cust_file;
	var mrkdn_pntg;
	var lifestyle_clustype;
	var pcnt_rtns;
	var days_btwn_purch;
	var lifetime_avg_btwn_visits;
run;
/*   preliminiary summary statistics - end   */



# APPENDIX D

/*   secondary summary statistics - begin   */
ods noproctitle;
ods graphics / imagemap=on;

proc means data=WORK.MIS581_M8_PP_OPT1 chartype mode min max range vardef=df;
	title 'Summary Statistics';
	var zip_code;
	var num_purch_visits;
	var cc_card;
	var num_mkt_promos;
	var num_days_cust_file;
	var lifestyle_clustype;
	var days_btwn_purch;
	var lifetime_avg_btwn_visits;
run;
/*   secondary summary statistics - end   */



# APPENDIX E

/*  ONE-WAY ANOVA  */
/*  One-Way Anova on lifestyle_clustype and p_jackets - begin  */
Title;
ods noproctitle;
ods graphics / reset width=5.5in height=2.5in imagemap;

proc glm data=WORK.MIS581_M8_PP_OPT1_LC plots(only);
	class lifestyle_clustype;
	model p_jackets=lifestyle_clustype;
	means lifestyle_clustype / welch plots=none;
	lsmeans lifestyle_clustype / plots=(meanplot);
	run;
quit;
/*  One-Way Anova on lifestyle_clustype and p_jackets - end  */



# APPENDIX F

/*  One-Way Anova on lifestyle_clustype and total_net_sales - begin  */
Title;
ods noproctitle;
ods graphics / reset width=5.5in height=2.5in imagemap;

proc glm data=WORK.MIS581_M8_PP_OPT1_LC plots(only);
	class lifestyle_clustype;
	model total_net_sales=lifestyle_clustype;
	means lifestyle_clustype / welch plots=none;
	lsmeans lifestyle_clustype / plots=(meanplot);
	run;
quit;
/*  One-Way Anova on lifestyle_clustype and total_net_sales - end  */



# APPENDIX G

/*  One-Way Anova on cc_card and total_net_sales - begin  */
Title;
ods noproctitle;
ods graphics / reset width=5.5in height=2.0in imagemap;

proc glm data=WORK.MIS581_M8_PP_OPT1_LC plots(only);
	class total_net_sales;
	model cc_card=total_net_sales;
	means total_net_sales / welch plots=none;
	lsmeans total_net_sales / plots=(meanplot);
	run;
quit;
/*  One-Way Anova on cc_card and total_net_sales - end  */



# APPENDIX H

/*  One-Way Anova on lifestyle_clustype and avg_spent_visit - begin  */
Title;
ods noproctitle;
ods graphics / reset width=5.5in height=2.0in imagemap;

proc glm data=WORK.MIS581_M8_PP_OPT1_LC plots(only);
	class lifestyle_clustype;
	model avg_spent_visit=lifestyle_clustype;
	means lifestyle_clustype / welch plots=none;
	lsmeans lifestyle_clustype / plots=(meanplot);
	run;
quit;
/*  One-Way Anova on lifestyle_clustype and avg_spent_visit - end  */



# APPENDIX I

/*  One-Way Anova on cc_card and pcnt_rtns - begin  */
Title;
ods noproctitle;
ods graphics / reset width=5.5in height=2.0in imagemap;

proc glm data=WORK.MIS581_M8_PP_OPT1_LC plots(only);
	class cc_card;
	model pcnt_rtns=cc_card;
	means cc_card / welch plots=none;
	lsmeans cc_card / plots=(meanplot);
	run;
quit;
/*  One-Way Anova on cc_card and pcnt_rtns - end  */




# APPENDIX J

/*  One-Way Anova on lifestyle_clustype and pcnt_rtns - begin  */
Title;
ods noproctitle;
ods graphics / reset width=5.5in height=2.0in imagemap;

proc glm data=WORK.MIS581_M8_PP_OPT1_LC plots(only);
	class lifestyle_clustype;
	model pcnt_rtns=lifestyle_clustype;
	means lifestyle_clustype / welch plots=none;
	lsmeans lifestyle_clustype / plots=(meanplot);
	run;
quit;
/*  One-Way Anova on lifestyle_clustype and pcnt_rtns - end  */



# APPENDIX K

/*  One-Way Anova on lifestyle_clustype and num_mkt_promos - begin  */
Title;
ods noproctitle;
ods graphics / reset width=5.5in height=2.0in imagemap;

proc glm data=WORK.MIS581_M8_PP_OPT1_LC plots(only);
	class lifestyle_clustype;
	model num_mkt_promos=lifestyle_clustype;
	means lifestyle_clustype / welch plots=none;
	lsmeans lifestyle_clustype / plots=(meanplot);
	run;
quit;
/*  One-Way Anova on lifestyle_clustype and num_mkt_promos - end  */



# APPENDIX L

/*  PREDICTIVE   */
/*   import - begin   */
libname PERM '/folders/myfolders/'; 

proc import 
	datafile='/folders/myfolders/sasuser.v94/clothing_store_pp_opt1_lc.csv' 
	dbms=csv out=WORK.MIS581_M8_PP_OPT1_LC replace;
	GETNAMES=YES;
run;

