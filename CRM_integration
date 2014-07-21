//Javascript to pull Google Analytics cookies for form submission
//Taken from Justin Cutroni: http://cutroni.com/blog/2007/10/29/integrating-google-analytics-with-a-crm/

var z = _uGC(document.cookie, '__utmz=', ';');
var source = _uGC(z, 'utmcsr=', '|');
var medium = _uGC(z, 'utmcmd=', '|');
var term = _uGC(z, 'utmctr=', '|');
var content = _uGC(z, 'utmcct=', '|');
var campaign = _uGC(z, 'utmccn=', '|');
var gclid = _uGC(z, 'utmgclid=', '|');
if (gclid !="-") {
 source = 'google';
 medium = 'cpc';
}

var csegment = _uGC(document.cookie, '__utmv=', ';');
if (csegment != '-') {
 var csegmentex = /[1-9]*?\.(.*)/;
 csegment = csegment.match(csegmentex);
 csegment = csegment[1];

} else {
 csegment = '';
}


var a = _uGC(document.cookie, '__utma=', ';');
var aParts = a.split(".");
var nVisits = aParts[5];



function _uGC(l,n,s)
{
if (!l || l=="" || !n || n=="" || !s || s=="") return "-";
var i,i2,i3,c="-";
i=l.indexOf(n);
i3=n.indexOf("=")+1;
if (i > -1) {
i2=l.indexOf(s,i); if (i2 < 0){ i2=l.length; }
c=l.substring((i+i3),i2);
}
return c;
}

document.getElementById("utm_medium").value =medium; /* Campaign_Medium */
document.getElementById("utm_source").value =source; /* Campaign_Source */
document.getElementById("utm_campaign").value =campaign; /* Campaign_CampaignName */
document.getElementById("utm_term").value =term; /* Campaign_Term */
document.getElementById("utm_content").value =content; /* Campaign_Content */
document.getElementById("total_visits").value =nVisits; /* Total Visits */
