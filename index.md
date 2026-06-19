---
layout: home
title: "Barcoded Ticketing for Public Transport - an EU Project"
---

# What is BT4PT?

Seamless multimodal and multi-operator travel across Europe is a major goal of EU transport policy.
This goal is based on environmental arguments (less pollution, more sustainability, and climate targets), 
economic arguments (less energy consumption, less congestion), and social arguments (making it easier for citizens to 
work, study, and do business across borders).

A prerequisite for this revolution in European transport is the development of a standard to integrate electronic 
ticketing for all public transport modes in all countries of Europe, and beyond.

The goal of this project is to develop and implement a harmonised standard for the format of ticketing across Europe,
in line with the objectives of current and upcoming EU legislation.
The project will deliver:
- A **CEN Technical Specification (CEN/TS)** for the ticket format.
- A **CEN Technical Report (CEN/TR)** outlining governance and long-term maintenance.

After this project has concluded, these standards will be reviewed and later upgraded to full, mandatory, European
standards; setting the mandate for how ticketing works across Europe.

# How can I get involved?

Currently, we are soliciting input from public transport operators globally about how their ticketing currently works.
The goal of this research is to obtain a complete picture of the current landscape of public transport and how it is
ticketed, such that we can create a unifying standard covering all possible use-cases.

We have prepared a questionaire covering the information we need to perfect our work. If you work for a public transport
operator, or any other company involved in transport ticketing, we'd love to hear from you by filling out our questionaire.

[QUESTIONNAIRE TO BE COMPLETED]

Please send the completed document to [questionnaire@bt4pt.eu](mailto:questionnaire@bt4pt.eu).

# The work so far

We have so far completed a first draft of the data layout of the ticket format, specified in ASN.1.
If you are technically inclined, you can browse our ASN.1 specifications and comment on them [on GitHub](https://github.com/BT4PT/ASN1).

An interactive render is also available:

- [MultiModalTicketData](https://asn1.bt4pt.eu/oid/iso/identified-organization/dod/internet/private/enterprise/uic/fcb/modules/mmtd/v1/0/) defining the encoding of a transport product.
- [BarcodeHeader](https://asn1.bt4pt.eu/oid/iso/identified-organization/dod/internet/private/enterprise/uic/fcb/modules/header/v3/0/) defining the security envelope used to protect ticket contents.
- [DynamicContentData](https://asn1.bt4pt.eu/oid/iso/identified-organization/dod/internet/private/enterprise/uic/fcb/modules/dcd/v2/0/) defining elements for a rotating (dynamic) ticket.
- [FixedPointData](https://asn1.bt4pt.eu/oid/iso/identified-organization/dod/internet/private/enterprise/uic/fcb/modules/fpd/v1/0/) defining elements for identifying locations in a transport context, such as stations, vehicles, or seats.

# Who's involved?

Hover over the below map to discover the countries represented on the BT4PT project.
Is your country not represented? If you work for a public transport company there, get in touch; we'd love to hear what you have to add!

<div class="d-grid justify-content-center">
<div id="regions_div" style="width: 900px; height: 500px;"></div>
</div>
<script type="text/javascript" src="https://www.gstatic.com/charts/loader.js"></script>
<script type="text/javascript">
  google.charts.load('current', {
    'packages':['geochart'],
  });
  google.charts.setOnLoadCallback(drawRegionsMap);

  function drawRegionsMap() {
    var data = google.visualization.arrayToDataTable([
      ['Country'],
      ['Germany'],
      ['Netherlands'],
      ['Switzerland'],
      ['Norway'],
      ['United Kingdom'],
      ['Austria'],
      ['France'],
      ['Slovenia'],
      ['Belgium'],
    ]);

    var options = {
        defaultColor: "004494",
        datalessRegionColor: "E3E3E3",
        region: "150"
    };

    var chart = new google.visualization.GeoChart(document.getElementById('regions_div'));

    chart.draw(data, options);
  }
</script>
