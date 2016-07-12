---
layout: post
title: Dynamics CRM Metadata To C# Constants Files
bigimg: /img/BridgeOverDepotBay.jpg
---

Intellisense is great for many things, and clean code is one of them. When I write my C# plugins for Dynamics CRM, I like to include several contants files so that I don't accidentally mistype something. It just makes my life a little easier when so many other things don't work the way they should.

So I wrote a small tool that will take the customizations.xml file from an exported solution and build the constants file for me. It even includes the Option Sets.

[Metadata To Constants](https://github.com/sarahch/MetadataToConstants)

To get the file this tool will read:
1. Export your customizations file from Dynamics CRM (be sure to include the fields when you built your solution in 2016!)
2. Save the zip file to a directory
3. Extract the solution files
4. Make note of the path to the directory that the customizations.xml file is in for the tool.

In my c# projects, I create a Constants folder, so that's where I put the output files. I've run a few tests, but I haven't used it with a client yet, so there are probably a few bugs I haven't found yet or assumptions I didn't respect.

I decided to share it with the community beause I haven't found anything like it, even though it's a pretty simple thing to write, and I wish I'd had it years ago.