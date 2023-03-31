## Minecraft load time benchmark


---

<p align="center" style="font-size:160%;">
MC total load time:<br>
219.42 sec
<br>
<sup><sub>(
3:39 min
)</sub></sup>
</p>

<br>


<p align="center">
<img src="https://quickchart.io/chart?w=400&h=30&c={%20type:%20'horizontalBar',%20data:%20{%20datasets:%20[%20{label:%20'MODS:',%20data:%20[125.27]},%20{label:%20'FML%20stuff:',%20data:%20[%2094.16]}%20]%20},%20options:%20{%20scales:%20{%20xAxes:%20[{display:%20false,stacked:%20true}],%20yAxes:%20[{display:%20false,stacked:%20true}],%20},%20elements:%20{rectangle:%20{borderWidth:%202}},%20legend:%20{display:%20false,},%20plugins:%20{datalabels:%20{color:%20'white',formatter:%20(value,%20context)%20=>%20[context.dataset.label,%20value].join('%20')%20}}%20}%20}"/>
</p>

<br>

# Mods Loading Time
<p align="center">
<img src="https://quickchart.io/chart?w=400&h=300&c={%20type:%20'outlabeledPie',%20options:%20{%20cutoutPercentage:%2025,%20plugins:%20{%20legend:%20!1,%20outlabels:%20{%20stretch:%205,%20padding:%201,%20text:%20(v,i)=>[%20v.labels[v.dataIndex],'%20',%20(v.percent*1000|0)/10,%20String.fromCharCode(37)].join('')%20}%20}%20},%20data:%20{...%20`%20518ba8%2018.04s%20Charset;%20219e4d%2017.34s%20Just%20Stargate%20Mod;%20436e17%2011.98s%20Had%20Enough%20Items;%203C6315%204.50s%20Had%20Enough%20Items%20(Plugins);%20813e4d%2010.48s%20GroovyScript;%208f6c30%208.41s%20Dynamic%20Surroundings;%20813e81%205.92s%20OpenComputers;%202c9e21%202.96s%20GregTech;%206aba3e%202.94s%20Galacticraft;%206e2717%202.23s%20Extra%20Planets;%208f308f%201.91s%20JourneyMap;%20306e8f%201.60s%20Custom%20Loading%20Screen;%205161a8%201.18s%20CraftTweaker2;%20495797%200.37s%20CraftTweaker2%20(Script%20Loading);%203e68ba%201.46s%20AE2%20Unofficial%20Extended%20Life;%206e176c%201.40s%20TerraFirmaCraft;%20308f7e%201.28s%20Quark:%20RotN%20Edition;%208f3087%200.84s%20Forge%20Mod%20Loader;%20cd872c%200.78s%20LittleTiles;%20a85181%200.77s%20TFC%20Florae;%20842ccd%200.65s%20CodeChicken%20Lib;%208f3033%200.62s%20Oxygen%20Core;%20444444%200.00s%200%20Other%20mods;%20333333%2030.47s%20140%20'Fast'%20mods%20(load%201.0s%20-%200.1s);%20222222%200.81s%2023%20'Instant'%20mods%20(load%20%3C%200.1s)%20`%20.split(';').reduce((a,%20l)%20=>%20{%20l.match(/(\w{6})%20*(\d*\.\d*)s%20(.*)/)%20.slice(1).map((a,%20i)%20=>%20[[String.fromCharCode(35),a].join(''),%20parseFloat(a),%20a][i])%20.forEach((s,%20i)%20=>%20[a.datasets[0].backgroundColor,%20a.datasets[0].data,%20a.labels][i].push(s)%20);%20return%20a%20},%20{%20labels:%20[],%20datasets:%20[{%20backgroundColor:%20[],%20data:%20[],%20borderColor:%20'rgba(22,22,22,0.3)',%20borderWidth:%201%20}]%20})%20}%20}"/>
</p>

<br>

# Top Mods Details (except JEI, FML and Forge)
<p align="center">
<img src="https://quickchart.io/chart?w=400&h=450&c={%20options:%20{%20scales:%20{%20xAxes:%20[{stacked:%20true}],%20yAxes:%20[{stacked:%20true}],%20},%20plugins:%20{%20datalabels:%20{%20anchor:%20'end',%20align:%20'top',%20color:%20'white',%20backgroundColor:%20'rgba(46,%20140,%20171,%200.6)',%20borderColor:%20'rgba(41,%20168,%20194,%201.0)',%20borderWidth:%200.5,%20borderRadius:%203,%20padding:%200,%20font:%20{size:10},%20formatter:%20(v,ctx)%20=>%20ctx.datasetIndex!=ctx.chart.data.datasets.length-1%20?%20null%20:%20[((ctx.chart.data.datasets.reduce((a,b)=>a-%20-b.data[ctx.dataIndex],0)*10)|0)/10,'s'].join('')%20},%20colorschemes:%20{%20scheme:%20'office.Damask6'%20}%20}%20},%20type:%20'bar',%20data:%20{...(()%20=>%20{%20let%20a%20=%20{%20labels:%20[],%20datasets:%20[]%20};%20`%201:%20Construction;%202:%20Loading%20Resources;%203:%20PreInitialization;%204:%20Initialization;%205:%20InterModComms$IMC;%206:%20PostInitialization;%207:%20LoadComplete;%208:%20ModIdMapping%20`%20.split(';')%20.map(l%20=>%20l.match(/\d:%20(.*)/).slice(1))%20.forEach(([name])%20=>%20a.datasets.push({%20label:%20name,%20data:%20[]%20}));%20`%201%202%203%204%205%206%207%208%20;%20Charset%20|%200.02|%200.00|%200.47|%200.14|%200.00|%2017.39|%200.02|%200.00;%20Just%20Stargate%20Mod%20|%200.26|%200.01|%200.57|%200.20|%200.00|%2016.29|%200.02|%200.00;%20GroovyScript%20|%200.87|%200.01|%200.02|%200.02|%200.00|%209.54|%200.02|%200.00;%20Dynamic%20Surroundings%20|%200.17|%200.01|%200.12|%200.07|%200.00|%200.03|%208.02|%200.00;%20OpenComputers%20|%200.12|%200.02|%204.58|%201.10|%200.06|%200.02|%200.02|%200.00;%20GregTech%20|%200.27|%200.02|%201.53|%200.46|%200.00|%200.66|%200.02|%200.00;%20Galacticraft%20|%200.14|%200.01|%201.42|%201.24|%200.00|%200.11|%200.02|%200.00;%20Extra%20Planets%20|%200.28|%200.01|%201.47|%200.26|%200.00|%200.19|%200.02|%200.00;%20JourneyMap%20|%200.03|%200.01|%200.04|%201.22|%200.00|%200.59|%200.02|%200.00;%20Custom%20Loading%20Screen%20|%201.52|%200.00|%200.02|%200.02|%200.00|%200.02|%200.02|%200.00;%20CraftTweaker2%20|%200.39|%200.00|%201.04|%200.02|%200.00|%200.08|%200.02|%200.00;%20AE2%20Unofficial%20Extended%20Life%20|%200.09|%200.01|%200.98|%200.12|%200.01|%200.23|%200.02|%200.00%20`%20.split(';').slice(1)%20.map(l%20=>%20l.split('|').map(s%20=>%20s.trim()))%20.forEach(([name,%20...arr],%20i)%20=>%20{%20a.labels.push(name);%20arr.forEach((v,%20j)%20=>%20a.datasets[j].data[i]%20=%20v)%20});%20return%20a%20})()}%20}"/>
</p>

<br>

# TOP JEI Registered Plugis
<p align="center">
<img src="https://quickchart.io/chart?w=700&c={%20options:%20{%20elements:%20{%20rectangle:%20{%20borderWidth:%201%20}%20},%20legend:%20false%20},%20type:%20'horizontalBar',%20data:%20{...(()%20=>%20{%20let%20a%20=%20{%20labels:%20[],%20datasets:%20[{%20backgroundColor:%20'rgba(0,%2099,%20132,%200.5)',%20borderColor:%20'rgb(0,%2099,%20132)',%20data:%20[]%20}]%20};%20`%201.33:%20li.cil.oc.integration.jei.ModPluginOpenComputers;%201.05:%20gregtech.integration.jei.GTJeiPlugin;%201.03:%20net.dries007.tfc.compat.jei.TFCJEIPlugin;%200.24:%20mezz.jei.plugins.vanilla.VanillaPlugin;%200.17:%20com.mjr.extraplanets.jei.ExtraPlanetsJEI;%200.09:%20micdoodle8.mods.galacticraft.planets.mars.client.jei.GalacticraftMarsJEI;%200.06:%20micdoodle8.mods.galacticraft.core.client.jei.GalacticraftJEI;%200.05:%20micdoodle8.mods.galacticraft.planets.asteroids.client.jei.GalacticraftAsteroidsJEI;%200.04:%20tfcflorae.compat.jei.TFCFJEIPlugin;%200.04:%20tfcflorae.compat.firmalife.jei.JEIPluginFLCompat;%200.04:%20tfctech.compat.jei.TechJEIPlugin;%200.03:%20com.eerussianguy.firmalife.compat.jei.JEIPluginFL;%200.03:%20tauri.dev.jsg.integration.jei.JEIIntegration;%200.03:%20se.gory_moon.horsepower.jei.HorsePowerPlugin;%200.03:%20crafttweaker.mods.jei.JEIAddonPlugin;%200.24:%20Other%2030%20Plugins%20`%20.split(';')%20.map(l%20=>%20l.split(':'))%20.forEach(([time,%20name])%20=>%20{%20a.labels.push(name);%20a.datasets[0].data.push(time)%20})%20;%20return%20a%20})()%20}%20}"/>
</p>

<br>

# FML Stuff
<p align="center">
<img src="https://quickchart.io/chart?w=500&h=400&c={%20options:%20{%20rotation:%20Math.PI,%20cutoutPercentage:%2055,%20plugins:%20{%20legend:%20!1,%20outlabels:%20{%20stretch:%205,%20padding:%201,%20text:%20(v)=>v.labels%20},%20doughnutlabel:%20{%20labels:%20[%20{%20text:%20'FML%20stuff:',%20color:%20'rgba(128,%20128,%20128,%200.5)',%20font:%20{size:%2018}%20},%20{%20text:%20[%2094.16,'s'].join(''),%20color:%20'rgba(128,%20128,%20128,%201)',%20font:%20{size:%2022}%20}%20]%20},%20}%20},%20type:%20'outlabeledPie',%20data:%20{...(()%20=>%20{%20let%20a%20=%20{%20labels:%20[],%20datasets:%20[{%20backgroundColor:%20[],%20data:%20[],%20borderColor:%20'rgba(22,22,22,0.3)',%20borderWidth:%202%20}]%20};%20`%20993A00%201.86s%20Loading%20sounds;%20994400%201.89s%20Loading%20Resource%20-%20SoundHandler;%20994F00%2010.31s%20ModelLoader:%20blocks;%20995900%204.59s%20ModelLoader:%20items;%20996300%206.19s%20ModelLoader:%20baking;%20996D00%200.02s%20Applying%20remove%20furnace%20recipe%20actions;%20997700%200.45s%20Indexing%20ingredients;%20998200%203.16s%20Indexing%20ingredients;%20444444%2065.69s%20Other%20`%20.split(';')%20.map(l%20=>%20l.match(/(\w{6})%20*(\d*\.\d*)s%20(.*)/))%20.forEach(([,%20col,%20time,%20name])%20=>%20{%20a.labels.push([name,%20'%20',%20time,%20's'].join(''));%20a.datasets[0].data.push(parseFloat(time));%20a.datasets[0].backgroundColor.push([String.fromCharCode(35),%20col].join(''))%20})%20;%20return%20a%20})()}%20}"/>
</p>

<br>
