# Grafana-Docs
Documentation for grafana &amp; prometheus

Grafana supports querying Prometheus. The Grafana data source for Prometheus is included since Grafana 2.5.0 (2015-10-28).
The following shows an example Grafana dashboard which queries Prometheus for data:

Grafana screenshot

# Using

By default, Grafana will be listening on http://localhost:3000. The default login is "admin" / "admin".

# Creating a Prometheus data source

To create a Prometheus data source:

   1. Click on the Grafana logo to open the sidebar menu.
   2. Click on "Data Sources" in the sidebar.
   3.  Click on "Add New".
   4. Select "Prometheus" as the type.
   5. Set the appropriate Prometheus server URL (for example, http://your_server_ip:9090/)
   6. Adjust other data source settings as desired (for example, turning the proxy access off).
   7. Click "Add" to save the new data source.
   
The following shows an example data source configuration:

Data source configuration

# Creating a Prometheus graph

Follow the standard way of adding a new Grafana graph. Then:

   1. Click the graph title, then click "Edit".
   2.  Under the "Metrics" tab, select your Prometheus data source (bottom right).
   3.  Enter any Prometheus expression into the "Query" field, while using the "Metric" field to lookup metrics via       autocompletion.
   4. To format the legend names of time series, use the "Legend format" input. For example, to show only the method and status labels of a returned query result, separated by a dash, you could use the legend format string {{method}} - {{status}}.
   5. Tune other graph settings until you have a working graph.

The following shows an example Prometheus graph configuration: Prometheus graph creation

# Importing pre-built dashboards from Grafana.com

Grafana.com maintains a collection of shared dashboards which can be downloaded and used with standalone instances of Grafana. Use the Grafana.com "Filter" option to browse dashboards for the "Prometheus" data source only.

You must currently manually edit the downloaded JSON files and correct the datasource: entries to reflect the Grafana data source name which you chose for your Prometheus server. Use the "Dashboards" → "Home" → "Import" option to import the edited dashboard file into your Grafana install.
