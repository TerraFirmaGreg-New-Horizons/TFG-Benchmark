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
<img src="https://quickchart.io/chart?w=400&h=30&c={
  type: 'horizontalBar',
  data: {
    datasets: [
      {label:      'MODS:', data: [125.27]},
      {label: 'FML stuff:', data: [ 94.16]}
    ]
  },
  options: {
    scales: {
      xAxes: [{display: false,stacked: true}],
      yAxes: [{display: false,stacked: true}],
    },
    elements: {rectangle: {borderWidth: 2}},
    legend: {display: false,},
    plugins: {datalabels: {color: 'white',formatter: (value, context) =>
      [context.dataset.label, value].join(' ')
    }}
  }
}"/>
</p>

<br>

# Mods Loading Time
<p align="center">
<img src="https://quickchart.io/chart?w=400&h=300&c={
  type: 'outlabeledPie',
  options: {
    cutoutPercentage: 25,
    plugins: {
      legend: !1,
      outlabels: {
        stretch: 5,
        padding: 1,
        text: (v,i)=>[
          v.labels[v.dataIndex],' ',
          (v.percent*1000|0)/10,
          String.fromCharCode(37)].join('')
      }
    }
  },
  data: {...
`
518ba8  18.04s Charset;
219e4d  17.34s Just Stargate Mod;
436e17  11.98s Had Enough Items;
3C6315   4.50s Had Enough Items (Plugins);
813e4d  10.48s GroovyScript;
8f6c30   8.41s Dynamic Surroundings;
813e81   5.92s OpenComputers;
2c9e21   2.96s GregTech;
6aba3e   2.94s Galacticraft;
6e2717   2.23s Extra Planets;
8f308f   1.91s JourneyMap;
306e8f   1.60s Custom Loading Screen;
5161a8   1.18s CraftTweaker2;
495797   0.37s CraftTweaker2 (Script Loading);
3e68ba   1.46s AE2 Unofficial Extended Life;
6e176c   1.40s TerraFirmaCraft;
308f7e   1.28s Quark: RotN Edition;
8f3087   0.84s Forge Mod Loader;
cd872c   0.78s LittleTiles;
a85181   0.77s TFC Florae;
842ccd   0.65s CodeChicken Lib;
8f3033   0.62s Oxygen Core;
444444   0.00s 0 Other mods;
333333  30.47s 140 'Fast' mods (load 1.0s - 0.1s);
222222   0.81s 23 'Instant' mods (load %3C 0.1s)
`
    .split(';').reduce((a, l) => {
      l.match(/(\w{6}) *(\d*\.\d*)s (.*)/)
      .slice(1).map((a, i) => [[String.fromCharCode(35),a].join(''), parseFloat(a), a][i])
      .forEach((s, i) => 
        [a.datasets[0].backgroundColor, a.datasets[0].data, a.labels][i].push(s)
      );
      return a
    }, {
      labels: [],
      datasets: [{
        backgroundColor: [],
        data: [],
        borderColor: 'rgba(22,22,22,0.3)',
        borderWidth: 1
      }]
    })
  }
}"/>
</p>

<br>

# Top Mods Details (except JEI, FML and Forge)
<p align="center">
<img src="https://quickchart.io/chart?w=400&h=450&c={
  options: {
    scales: {
      xAxes: [{stacked: true}],
      yAxes: [{stacked: true}],
    },
    plugins: {
      datalabels: {
        anchor: 'end',
        align: 'top',
        color: 'white',
        backgroundColor: 'rgba(46, 140, 171, 0.6)',
        borderColor: 'rgba(41, 168, 194, 1.0)',
        borderWidth: 0.5,
        borderRadius: 3,
        padding: 0,
        font: {size:10},
        formatter: (v,ctx) => 
          ctx.datasetIndex!=ctx.chart.data.datasets.length-1 ? null
            : [((ctx.chart.data.datasets.reduce((a,b)=>a- -b.data[ctx.dataIndex],0)*10)|0)/10,'s'].join('')
      },
      colorschemes: {
        scheme: 'office.Damask6'
      }
    }
  },
  type: 'bar',
  data: {...(() => {
    let a = { labels: [], datasets: [] };
`
1: Construction;
2: Loading Resources;
3: PreInitialization;
4: Initialization;
5: InterModComms$IMC;
6: PostInitialization;
7: LoadComplete;
8: ModIdMapping
`
    .split(';')
      .map(l => l.match(/\d: (.*)/).slice(1))
      .forEach(([name]) => a.datasets.push({ label: name, data: [] }));
`
                                 1      2      3      4      5      6      7      8  ;
Charset                      |  0.02|  0.00|  0.47|  0.14|  0.00| 17.39|  0.02|  0.00;
Just Stargate Mod            |  0.26|  0.01|  0.57|  0.20|  0.00| 16.29|  0.02|  0.00;
GroovyScript                 |  0.87|  0.01|  0.02|  0.02|  0.00|  9.54|  0.02|  0.00;
Dynamic Surroundings         |  0.17|  0.01|  0.12|  0.07|  0.00|  0.03|  8.02|  0.00;
OpenComputers                |  0.12|  0.02|  4.58|  1.10|  0.06|  0.02|  0.02|  0.00;
GregTech                     |  0.27|  0.02|  1.53|  0.46|  0.00|  0.66|  0.02|  0.00;
Galacticraft                 |  0.14|  0.01|  1.42|  1.24|  0.00|  0.11|  0.02|  0.00;
Extra Planets                |  0.28|  0.01|  1.47|  0.26|  0.00|  0.19|  0.02|  0.00;
JourneyMap                   |  0.03|  0.01|  0.04|  1.22|  0.00|  0.59|  0.02|  0.00;
Custom Loading Screen        |  1.52|  0.00|  0.02|  0.02|  0.00|  0.02|  0.02|  0.00;
CraftTweaker2                |  0.39|  0.00|  1.04|  0.02|  0.00|  0.08|  0.02|  0.00;
AE2 Unofficial Extended Life |  0.09|  0.01|  0.98|  0.12|  0.01|  0.23|  0.02|  0.00
`
    .split(';').slice(1)
      .map(l => l.split('|').map(s => s.trim()))
      .forEach(([name, ...arr], i) => {
        a.labels.push(name);
        arr.forEach((v, j) => a.datasets[j].data[i] = v)
      }); return a
  })()}
}"/>
</p>

<br>

# TOP JEI Registered Plugis
<p align="center">
<img src="https://quickchart.io/chart?w=700&c={
  options: {
    elements: { rectangle: { borderWidth: 1 } },
    legend: false
  },
  type: 'horizontalBar',
    data: {...(() => {
      let a = {
        labels: [], datasets: [{
          backgroundColor: 'rgba(0, 99, 132, 0.5)',
          borderColor: 'rgb(0, 99, 132)',
          data: []
        }]
      };
`
  1.33: li.cil.oc.integration.jei.ModPluginOpenComputers;
  1.05: gregtech.integration.jei.GTJeiPlugin;
  1.03: net.dries007.tfc.compat.jei.TFCJEIPlugin;
  0.24: mezz.jei.plugins.vanilla.VanillaPlugin;
  0.17: com.mjr.extraplanets.jei.ExtraPlanetsJEI;
  0.09: micdoodle8.mods.galacticraft.planets.mars.client.jei.GalacticraftMarsJEI;
  0.06: micdoodle8.mods.galacticraft.core.client.jei.GalacticraftJEI;
  0.05: micdoodle8.mods.galacticraft.planets.asteroids.client.jei.GalacticraftAsteroidsJEI;
  0.04: tfcflorae.compat.jei.TFCFJEIPlugin;
  0.04: tfcflorae.compat.firmalife.jei.JEIPluginFLCompat;
  0.04: tfctech.compat.jei.TechJEIPlugin;
  0.03: com.eerussianguy.firmalife.compat.jei.JEIPluginFL;
  0.03: tauri.dev.jsg.integration.jei.JEIIntegration;
  0.03: se.gory_moon.horsepower.jei.HorsePowerPlugin;
  0.03: crafttweaker.mods.jei.JEIAddonPlugin;
  0.24: Other 30 Plugins
`
        .split(';')
        .map(l => l.split(':'))
        .forEach(([time, name]) => {
          a.labels.push(name);
          a.datasets[0].data.push(time)
        })
        ; return a
    })()
  }
}"/>
</p>

<br>

# FML Stuff
<p align="center">
<img src="https://quickchart.io/chart?w=500&h=400&c={
  options: {
    rotation: Math.PI,
    cutoutPercentage: 55,
    plugins: {
      legend: !1,
      outlabels: {
        stretch: 5,
        padding: 1,
        text: (v)=>v.labels
      },
      doughnutlabel: {
        labels: [
          {
            text: 'FML stuff:',
            color: 'rgba(128, 128, 128, 0.5)',
            font: {size: 18}
          },
          {
            text: [ 94.16,'s'].join(''),
            color: 'rgba(128, 128, 128, 1)',
            font: {size: 22}
          }
        ]
      },
    }
  },
  type: 'outlabeledPie',
  data: {...(() => {
    let a = {
      labels: [],
      datasets: [{
        backgroundColor: [],
        data: [],
        borderColor: 'rgba(22,22,22,0.3)',
        borderWidth: 2
      }]
    };
`
993A00   1.86s Loading sounds;
994400   1.89s Loading Resource - SoundHandler;
994F00  10.31s ModelLoader: blocks;
995900   4.59s ModelLoader: items;
996300   6.19s ModelLoader: baking;
996D00   0.02s Applying remove furnace recipe actions;
997700   0.45s Indexing ingredients;
998200   3.16s Indexing ingredients;
444444  65.69s Other
`
    .split(';')
      .map(l => l.match(/(\w{6}) *(\d*\.\d*)s (.*)/))
      .forEach(([, col, time, name]) => {
        a.labels.push([name, ' ', time, 's'].join(''));
        a.datasets[0].data.push(parseFloat(time));
        a.datasets[0].backgroundColor.push([String.fromCharCode(35), col].join(''))
      })
      ; return a
  })()}
}"/>
</p>

<br>
