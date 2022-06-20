# Interschutz Hackathon LiveReader Challenge

This is a starter repo for the [Interschutz Hackathon LiveReader Challenge](https://spell-plattform.de/hackathon/challenges/) and contains useful ressources for the participants.  
This includes links to Docs, Code examples and even some Templates for [Graphly D3](https://graphly-d3.livereader.com).

## The Challenge

Visualization as the key to collaboration between man and machine (AI).

The management of complex crises and emergencies goes hand in hand with the management of a flood of information. A wide variety of data is available from a large number of sources, which are combined in a semantic platform in SPELL and can be used to assess the situation. Support can then be provided by specialized AI services, which are used on the platform for evaluations and for implementing specific subtasks.

AI will therefore provide far-reaching support in the SPELL project, but this must also be communicated to the people who have to assess the respective situation and make decisions. To deal with the large number of variations of different events and emergencies, information can be visualized in a graph representation. However, in order to reduce the complexity here and still convey a meaningful situation picture, an expressive and self-explanatory symbolism is needed.

For example, how can...

-   an imminent event such as a flood, a storm, or the like be gainfully depicted in the context of an emergency?
-   a drone during a reconnaissance flight be depicted and integrated into an emergency response?
-   a traffic disruption with influence on travel times and possibly uncertainty factors of emergency vehicles can be visualized?
-   and much more.

The starting point for this challenge is the open source project Graphly-D3, which offers an easy entry with an existing library and sample code and yet allows an impressive implementation of an own idea within the framework of the hackathon. Which situation, which facts, which details do you want to represent compactly and intuitively in order to enable efficient collaboration between humans and AI?

## Graphly D3

Since the challenge is all about Human Computer Interaction, we provide our open source graph visualization library [Graphly D3](https://graphly-d3.livereader.com) as a starting point.  
It empowers you to develop outstanding graph visualizations with easy by developing intuitive and easy to understand Templates.

Check out the [Graphly D3 Documentation](https://graphly-d3.livereader.com/) to learn more about the library and how to develop your own Templates.

## Graphly D3 in Vue

If you use Vue for your project, you can easily use our [Graphly D3 Vue](https://github.com/LiveReader/graphly-d3-vue) component instead of the standard Graphly D3 library.

Just run `npm install @livereader/graphly-d3-vue` and then import the component.

```shell
<template>
  <GraphlyD3 ref="graphly" />
</template>

<script setup>
	import { onMounted } from "vue";
	import { GraphlyD3 } from "@livereader/graphly-d3-vue";
	import "@livereader/graphly-d3-vue/style.css";

	const graphly = ref(null);

	onMounted(() => {
		const simulation = graphly.value.simulation;
		simulation.render({
			nodes: [],
			links: [],
		})
	});
</script>
```

More details in its [ReadMe](https://github.com/LiveReader/graphly-d3-vue).

## Templates

In this Repo are 6 of our already developed Templates which are also used in the SPELL demonstrator for example. – You can take a look at the demonstrator on the Interschutz in Hall 16 Booth F26 :eyes:

You can use them in your hackathon project and take inspiration for your own Templates.

-   Operation
-   Affected Person
-   Affected Object
-   Emergency Reporter
-   Emergency Action
-   Emergency Ressource
