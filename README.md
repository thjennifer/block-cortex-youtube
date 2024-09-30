# YouTube

<h2><span style="color:#2d7eea">What does this Looker Block do for me?</span></h2>

Get a comprehensive overview of your campaign spend, performance and audience targeting with actionable insights for paid media campaigns on YouTube purchased with DV360 platform.

Jumpstart your paid media marketing analytics for YouTube by ingesting your campaign data into Google BigQuery with pre-packaged ingestion pipelines and reporting views provided by Google Cloud Cortex Framework for Marketing.

Install this Looker Model for YouTube to gain insights on cost, impressions, click & view rates, key audience targeting and engagement metrics. Enhance visualizations with more granular metrics like creative (ad level), demographics and YouTube placement.

You can also extend to insights beyond Marketing with other datasets in the Google Cloud Cortex Framework that provide reporting views for enterprise data sources like your enterprise CRM or ERP systems.

<h2>What insights are possible?</h2>

Following insights are provided out-of-the-box:

<h3> Overall Campaign Performance </h3>

Overview of high-level campaign performance and engagement metrics including:

- Total Impressions, Total Clicks, CTR (Click Through Rate)
- Total TrueView Views, TrueView VR (TrueView View Rate)
- Total Spend, CPM (Cost per Mille), CPC (Cost per Click), CPV (Cost per TrueView)

<h3> What was the performance and spend by month? </h3>

- Impressions by Month
- Cumulative Monthly Spend

<h3> What campaigns have run and how did they perform? </h3>

- YouTube Line Items in chronological view
- Impressions, TrueView views and Clicks by YouTube Line Item
- Impressions by Device Type and YouTube Line Item
- Detailed Performance by YouTube Line Item

<h3> What was the performance by audience and ad format? </h3>

- Impressions and TrueView views by
  - Age Group and Gender
  - Audience Segment Type
  - YouTube Ad Format

<h2>Required Data</h2>

Get the required BigQuery datasets for this block by following the installation instructions for [Google Cloud Cortex Framework](https://github.com/GoogleCloudPlatform/cortex-data-foundation).

<h2>Installation Instructions</h2>

Manually install this LookML Model following one of the options below.

<h4> Option A: Marketplace Install via Git </h4>

Refer to the Looker documentation for [Installing a Tool from Marketplace.](https://cloud.google.com/looker/docs/marketplace#installing_a_tool_from_a_git_url) Provide values for the required prompts as outlined in next section Required Parameters.

<h4> Option B: Manual Install via Fork of this Repository </h4>

- [Fork this GitHub repository](https://docs.github.com/en/get-started/quickstart/fork-a-repo#forking-a-repository)
- [Create a blank LookML project](https://cloud.google.com/looker/docs/create-projects#creating_a_blank_project) with any name (e.g., cortex_marketing_youtube)
- [Connect the new LookML project to the forked repository](https://cloud.google.com/looker/docs/setting-up-git-connection)
- Update the values of constants in the manifest.lkml file as described in the next section Required Parameters
- [Commit and deploy changes to production](https://cloud.google.com/looker/docs/version-control-and-deploying-changes#getting_your_changes_to_production)
With the Looker project based on your forked repository, you can customize the LookML to fit your unique business needs.

<h2><span style="color:#2d7eea">Required Parameters</span></h2>

> ⚠️ These required values are configured during the Marketplace Installation process, or if this model was installed from a forked Git repository, you will update the values for these constants in the `manifest.lkml` file for the project.

- **Connection Name**: Name of the BigQuery Connection allowing Looker to query the Cortex Framework REPORTING dataset.

- **Google Cloud Project ID**: The Google Cloud project ID where the YouTube reporting dataset resides in BigQuery. [Identifying Project ID](https://cloud.google.com/resource-manager/docs/creating-managing-projects#identifying_projects)

- **Reporting Dataset**: The deployed Cortex REPORTING dataset where the YouTube reporting views reside within the Google Cloud BigQuery project. Depending on the deployment settings for the [Google Cloud Cortex Framework](https://github.com/GoogleCloudPlatform/cortex-data-foundation) (see section Required Data), this dataset name would typically end with  _REPORTING.

<h2><span style="color:#2d7eea">Other Considerations</span></h2>

- **Persistent Derived Tables**: If using this block with production data, you may want to convert some derived tables to [Persistent Derived Tables (PDTs)](https://cloud.google.com/looker/docs/derived-tables#persistent_derived_tables) to improve query performance. Ensure your BigQuery Connection has enabled PDTs, then update any derived table syntax with the desired [persistence strategy](https://cloud.google.com/looker/docs/derived-tables#persistence_strategies).

- **Liquid Templating Language**: Some constants, views, Explores and dashboards use liquid templating language. For more information, see Looker's [Liquid Variable Reference](https://cloud.google.com/looker/docs/liquid-variable-reference) documentation.

- (Optional) **Unhide additional dimensions and measures**: Some dimensions and measures have been hidden to simplify reporting and data understanding. However should you find anything valuable missing, simply update a field's hidden property to No in the relevant views.

<h2><span style="color:#2d7eea">Additional Resources</span></h2>

To learn more about LookML and how to develop visit:
- [Looker Best Practices](https://cloud.google.com/looker/docs/best-practices/home)
- [Looker/Google Cloud Training](https://www.cloudskillsboost.google/catalog)
