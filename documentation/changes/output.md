---
layout: default
title: Change output | Liquibase Docs
---

<!-- ====================================================== -->
<!-- GENERATED BY ChangeDocGenerator DO NOT MODIFY MANUALLY -->
<!-- ====================================================== -->

  <script>
  $(function() {
    $( "#changelog-tabs" ).tabs();
  });
</script>

# Change: 'output'

Logs a message and continues execution.

## Available Attributes ##

<table>
<tr><th>Name</th><th>Description</th><th>Required&nbsp;For</th><th>Supports</th><th>Since</th></tr>
<tr><td style='vertical-align: top'>message</td><td style='vertical-align: top'>Message to output</td><td style='vertical-align: top'></td><td style='vertical-align:top'>all</td><td style='vertical-align: top'></td></tr>
<tr><td style='vertical-align: top'>target</td><td style='vertical-align: top'>Target for message. Possible values: STDOUT, STDERR, FATAL, WARN, INFO, DEBUG. Default value: STDERR</td><td style='vertical-align: top'></td><td style='vertical-align:top'>all</td><td style='vertical-align: top'></td></tr>
</table>

<div id='changelog-tabs'>
<ul>
    <li><a href="#tab-xml">XML Sample</a></li>
    <li><a href="#tab-yaml">YAML Sample</a></li>
    <li><a href="#tab-json">JSON Sample</a></li>
  </ul>
<div id='tab-xml'>
{% highlight xml %}
<changeSet author="liquibase-docs"
        id="output-example"
        objectQuotingStrategy="LEGACY">
    <output target="STDERR">Make sure you feed the cat</output>
</changeSet>
{% endhighlight %}
</div>
<div id='tab-yaml'>
{% highlight yaml %}
changeSet:
  id: output-example
  author: liquibase-docs
  objectQuotingStrategy: LEGACY
  changes:
  - output:
      message: Make sure you feed the cat
      target: STDERR

{% endhighlight %}
</div>
<div id='tab-json'>
{% highlight json %}
{
  "changeSet": {
    "id": "output-example",
    "author": "liquibase-docs",
    "objectQuotingStrategy": "LEGACY",
    "changes": [
      {
        "output": {
          "message": "Make sure you feed the cat",
          "target": "STDERR"
        }
      }]
    
  }
}

{% endhighlight %}
</div>
</div>


## SQL Generated From Above Sample (MySQL)

{% highlight sql %}

{% endhighlight %}

## Database Support

<table style='border:1;'>
<tr><th>Database</th><th>Notes</th><th>Auto Rollback</th></tr>
<tr><td>DB2</td><td><b>Supported</b></td><td>No</td></tr>
<tr><td>DB2</td><td><b>Supported</b></td><td>No</td></tr>
<tr><td>Derby</td><td><b>Supported</b></td><td>No</td></tr>
<tr><td>Firebird</td><td><b>Supported</b></td><td>No</td></tr>
<tr><td>H2</td><td><b>Supported</b></td><td>No</td></tr>
<tr><td>HyperSQL</td><td><b>Supported</b></td><td>No</td></tr>
<tr><td>INGRES</td><td><b>Supported</b></td><td>No</td></tr>
<tr><td>Informix</td><td><b>Supported</b></td><td>No</td></tr>
<tr><td>MariaDB</td><td><b>Supported</b></td><td>No</td></tr>
<tr><td>MySQL</td><td><b>Supported</b></td><td>No</td></tr>
<tr><td>Oracle</td><td><b>Supported</b></td><td>No</td></tr>
<tr><td>PostgreSQL</td><td><b>Supported</b></td><td>No</td></tr>
<tr><td>SQL Server</td><td><b>Supported</b></td><td>No</td></tr>
<tr><td>SQLite</td><td><b>Supported</b></td><td>No</td></tr>
<tr><td>Sybase</td><td><b>Supported</b></td><td>No</td></tr>
<tr><td>Sybase Anywhere</td><td><b>Supported</b></td><td>No</td></tr>
</table>