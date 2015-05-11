+++

date = "2015-05-02T20:25:18-06:00"
draft = false
title = "Platform Considerations"
slug = "platform_considerations"
comments = true

series = [ "About this site" ]

+++

**The following information encapsulates much of my thinking regarding how to power this site.  It is based on experimentation and observations as of 2015-05-02.**

## Architectural/Philosophical Considerations

**Static Site Generation** - I didn't want a full CMS like <a href="http://www.drupal.org">Drupal</a>, a hybrid  CMS like <a href="https://wordpress.org/">WordPress</a> or even a static file CMS like <a href="http://getkirby.com/">Kirby</a> or <a href="http://picocms.org/">Pico</a>.  I wanted something with a minimum amount of overhead that would allow me to host static files in places like <a href="https://pages.github.com/">GitHub Pages</a>.  Ultimately, <a href="https://www.staticgen.com/">StaticGen</a> maintains one of the more interesting lists of static generators, so if you want a comprehensive view of the space, look there, but listed below are thoughts and observations from my own foray into this space.  

**Language** - While there was some temptation to scratch an itch with regard to learning new languages, I wasn't intrigued with the prospects of going overboard there.  I like the idea of using node.js -- a lot.  I used to be intrigued with Python, but decided against it for this project.  Despite being very popular in this space, I decided to avoid Ruby.  I wanted to avoid anything based on .Net too.  Oddly, I couldn't find much intriguing in the PHP space, but would have found that workable.  

**Data** - Ultimately, I want a tool that will allow me to augment simple site markdown files with data from an array of sources. I could just render everything down to markdown or html files, but I wanted to use data sources that would allow me to more flexibly manipulate what gets rendered.  JSON was a requirement for me, but I'm becoming a fan of YAML and TOML.   They are a bit more conveninent to work with in some situations and I may consider switching to one of them for some data sources I create.

**Features** - Basic support for themeing, templating, and partials are requirements for me.  Live reload is a "nice to have" feature, but not that important in this case.  It could help for some iteration, but given the scale I hope to operate at, I'm resigned to the belief that it isn't going to be practical for use on the site I'm developing.  The prospects for leveraging SASS/LESS are very attractive, but aren't a defining characteristic for me.  Pagination and classification (through tagging and/or taxonomy) were some of the key features I hoped to leverage.

**Performance** - I need something sufficently performant.  Knowing the end-product (the rendered site) would be fast, throughput for site generation would be a luxury, an added convenience, but not a defining characteristic.  

**Open Source** -  I didn't want to use any site generator that wasn't open source even if it was free/inexpensive.  I hope to find ways to contribute back to the systems I leverage.

## Platform Summary

My search primarily focused on the following platforms.  I've highlighted a few of the features that were key to my own consideration. I ruled out Jekyll due to its dependency on Ruby, but included it here due it is prominence in the marketplace.  

<table class="table table-striped table-bordered dataTableSimple dt-responsive" style="width: 100%;">
  <thead>
    <tr>
      <th>Tech</th>
      <th>Language</th>
      <th>Status</th>
      <th>Tagging</th>
      <th>Pagination</th>
      <th>Data</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td scope="row"><a href="#harp">Harp</a></th>
      <td clue="lang"><span class="label label-success">Node.js</span></td>
      <td clue="lang"><span class="label label-warning">Stalled</span></td>
      <td clue="tagging"><span class="label label-danger">Unsupported</span></td>
      <td clue="pagination"><span class="label label-danger">Unsupported</span></td>
      <td clue="data"><span class="label label-warning">Potential</span></td>
    </tr>
    <tr>
      <td scope="row"><a href="#hexo">Hexo</a></th>
      <td clue="lang"><span class="label label-success">Node.js</span></td>
      <td clue="lang"><span class="label label-success">Active</span></td>
      <td clue="tagging"><span class="label label-success">Supported</span></td>
      <td clue="pagination"><span class="label label-success">Supported</span></td>
      <td clue="data"><span class="label label-warning">Potential</span></td>
    </tr>
    <tr>
      <td scope="row"><a href="#hugo">Hugo</a></th>
      <td clue="lang"><span class="label label-warning">Go</span></td>
      <td clue="lang"><span class="label label-success">Active</span></td>
      <td clue="tagging"><span class="label label-success">Supported</span></td>
      <td clue="pagination"><span class="label label-success">Supported</span></td>
      <td clue="data"><span class="label label-warning">Potential</span></td>
    </tr>
    <tr>
      <td scope="row"><a href="#jekyll">Jekyll</a></th>
      <td clue="lang"><span class="label label-danger">Ruby</span></td>
      <td clue="lang"><span class="label label-success">Active</span></td>
      <td clue="tagging"><span class="label label-success">Supported</span></td>
      <td clue="pagination"><span class="label label-success">Supported</span></td>
      <td clue="data"><span class="label label-warning">Unknown</span></td>
    </tr>
  </tbody>
</table>


<a id="harp"></a>
### Harp
http://harpjs.com/

I really like Harp, but consider it a last resort option at this stage.  More than anything else, the need to host a metadata file in json to generate the site isn't attractive for the scale I want to use for this project.  For smaller sites that don't need pagination and classification, it would be great.

<table class="table table-striped table-bordered dataTableSimple dt-responsive">
        <thead>
          <tr>
            <th>Feature</th>
            <th>Status</th>
            <th>Notes</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td scope="row">Status</th>
            <td><span class="label label-warning">Stalled</span></td>
            <td>Activity has waned as of 2015/05/02</td>
          </tr>
          <tr>
            <td scope="row">Pagination</th>
            <td><span class="label label-danger">Unsupported</span></td>
            <td>It doesn't natively support pagination. I could find alternate routes by using data files, but the level of effort would be signficant.</td>
          </tr>
          <tr>
            <td scope="row">Tagging</th>
            <td><span class="label label-danger">Unsupported</span></td>
            <td>A reasonable path forward could be found in the use of data files</td>
          </tr>

          <tr>
            <td scope="row">Data</th>
            <td><span class="label label-warning">Possible?</span></td>
            <td>My needs could be supoprted w/ data files per "node", but haven't investigated it at this stage.</td>
          </tr>
        </tbody>
      </table>

<a id="hexo"></a>
### Hexo
https://hexo.io/

I really wanted to like Hexo, but abandoned it very quickly.  I couldn't handle the data files that I'd already tried with Hugo, so I decided to skip investigating it more deeply.  

<table class="table table-striped table-bordered dataTableSimple dt-responsive">
  <thead>
    <tr>
      <th>Feature</th>
      <th>Status</th>
      <th>Notes</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td scope="row">Status</th>
      <td><span class="label label-success">Active</span></td>
      <td>It seemed to be reasonably active</td>
    </tr>
    <tr>
      <td scope="row">Pagination</th>
      <td><span class="label label-success">Supported</span></td>
      <td>It natively supports pagination, but didn't explore it deeply.</td>
    </tr>
    <tr>
      <td scope="row">Tagging</th>
      <td><span class="label label-success">Supported</span></td>
      <td>It natively supports tagging, but didn't explore it deeply.</td>
    </tr>

    <tr>
      <td scope="row">Data</th>
      <td><span class="label label-warning">Possible?</span></td>
      <td>It natively supports use of secondary data files, but after attempting to use it with a large collection of data,  Hexo proved unresponsive, so I abandoned.</td>
    </tr>
  </tbody>
</table>



<a id="hugo"></a>
### Hugo
https://hugo.io

**Hugo is very intriguing.**  Before hitting some boundaries with data, it was extremely fast.  The only thing missing from my wish list right now is SASS/LESS support and I think that's on the backlog.  The Go Templating system is a little foreign to me, but I've had no problems navigating it so far.  EJS was far more familiar to me, but given everything else it does well, this is a reasonable trade-off.  With node.js based systems, my learning curve for contributing back would be much smaller.  If I continue progressing forward with Hugo, I'll have to consider other ways to contribute, but I may break down and immerse myself more deeply in Go if Hugo proves a durable solution for me.

<table class="table table-striped table-bordered dataTableSimple dt-responsive" style="width: 100%;">
  <thead>
    <tr>
      <th>Feature</th>
      <th>Status</th>
      <th>Notes</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td scope="row">Status</th>
      <td><span class="label label-success">Active</span></td>
      <td>It seemed to be reasonably active and the support channel was quite responsive for the one issue I'd submitted.</td>
    </tr>
    <tr>
      <td scope="row">Pagination</th>
      <td><span class="label label-success">Supported</span></td>
      <td>It natively supports pagination.</td>
    </tr>
    <tr>
      <td scope="row">Tagging</th>
      <td><span class="label label-success">Supported</span></td>
      <td>It natively supports tagging.  I'm still working through it.  Not sure if pagination is supported at the tag level yet.</td>
    </tr>

    <tr>
      <td scope="row">Data</th>
      <td><span class="label label-warning">Possible?</span></td>
      <td>It natively supports use of secondary data files.  It eventually collapses under the weight of large amounts of data.  See my bug report at <a href="https://github.com/spf13/hugo/issues/1065">https://github.com/spf13/hugo/issues/1065</a> for more information.  I may try switching to a Linux VM to see if results vary there, but it didn't sound promising.</td>
    </tr>
  </tbody>
</table>

<a id="jekyll"></a>
### Jekyll
http://jekyllrb.com/

Jekyll is one of the most popular static site generators available.  Ultimately, I didn't want to use a Ruby based system, so I didn't pursue it.  

## Conclusion

At this stage, I'm pressing forward with Hugo, but I'll continue to keep an eye out on alternative platforms.  Until something else captures my attention, I think it is well suited to drive the site if I make some sacrifices on the data to work around the bug I highlighted above.
