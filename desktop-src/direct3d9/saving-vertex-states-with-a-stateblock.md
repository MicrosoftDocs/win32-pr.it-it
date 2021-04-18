---
description: Un blocco di stato può essere usato per acquisire solo lo stato del vertice (vedere lo stato di salvataggio e ripristino di blocchi di stato (Direct3D 9)).
ms.assetid: cb898228-dc45-4a2a-a82e-8d64523e9b85
title: Salvataggio degli Stati dei vertici con StateBlock (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81c6bc7fd291a2609ef60709f05a04fe8d27f8eb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304379"
---
# <a name="saving-vertex-states-with-a-stateblock-direct3d-9"></a>Salvataggio degli Stati dei vertici con StateBlock (Direct3D 9)

Un blocco di stato può essere usato per acquisire solo lo stato del vertice (vedere lo stato di [salvataggio e ripristino di blocchi di stato (Direct3D 9)](state-blocks-save-and-restore-state.md)). Lo stato seguente è Vertex state:

-   Stato di rendering vertici (vedere [pipeline Vertex: stato di rendering](#vertex-pipeline-render-state)).
-   Stato campionatore vertici (vedere [pipeline Vertex: stato campionatore](#vertex-pipeline-sampler-state)).
-   Stato trama vertice (vedere [pipeline Vertex: stato trama](#vertex-pipeline-texture-state)).
-   I segmenti in modalità NPatch di [**IDirect3DDevice9:: SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode).
-   Ogni luce di [**IDirect3DDevice9:: selight**](/windows/desktop/api), nonché se la luce è abilitata con [**IDirect3DDevice9:: alleggerible**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-lightenable).
-   Vertex shader corrente e ognuna delle costanti vertex shader.
-   Per ogni flusso di vertici, archiviare il valore del divisore da [**IDirect3DDevice9:: SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq).
-   Dichiarazione del vertice corrente.

Per acquisire lo stato del vertice con un blocco di stato, specificare D3DSBT \_ VERTEXSTATE quando si chiama [**IDirect3DDevice9:: CreateStateBlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createstateblock).

## <a name="vertex-pipeline-render-state"></a>Pipeline Vertex: stato di rendering

Gli Stati di rendering del dispositivo influiscono sul comportamento di quasi tutte le parti della pipeline. Gli Stati di rendering vengono impostati chiamando [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate).

Nella tabella seguente sono inclusi tutti gli Stati di rendering che configurano lo stato dei vertici:



| Stati di rendering                           | Valore predefinito          |
|-----------------------------------------|------------------------|
| \_CULLMODE D3DRS                         | D3DCULL \_ CCW           |
| \_FogColor D3DRS                         | 0                      |
| \_FOGTABLEMODE D3DRS                     | D3DFOG \_ None           |
| \_FOGSTART D3DRS                         | 0                      |
| \_FOGEND D3DRS                           | 1                      |
| \_FOGDENSITY D3DRS                       | 1                      |
| \_RANGEFOGENABLE D3DRS                   | **FALSE**              |
| \_Ambiente D3DRS                          | 0                      |
| \_COLORVERTEX D3DRS                      | **TRUE**               |
| \_FOGVERTEXMODE D3DRS                    | D3DFOG \_ None           |
| Ritaglio D3DRS \_                         | **TRUE**               |
| \_Illuminazione D3DRS                         | **TRUE**               |
| \_LOCALVIEWER D3DRS                      | **TRUE**               |
| \_EMISSIVEMATERIALSOURCE D3DRS           | \_Materiale D3DMCS       |
| \_AMBIENTMATERIALSOURCE D3DRS            | \_Materiale D3DMCS       |
| \_DIFFUSEMATERIALSOURCE D3DRS            | \_COLOR1 D3DMCS         |
| \_SPECULARMATERIALSOURCE D3DRS           | \_Color2 D3DMCS         |
| \_VERTEXBLEND D3DRS                      | \_Disabilitazione D3DVBF        |
| \_CLIPPLANEENABLE D3DRS                  | 0                      |
| \_POINTSIZE D3DRS                        | Dipendente dal driver       |
| D3DRS \_ POINTSIZE \_ min                   | 1                      |
| \_POINTSPRITEENABLE D3DRS                | **FALSE**              |
| \_POINTSCALEENABLE D3DRS                 | **FALSE**              |
| D3DRS \_ POINTSCALE \_ A                    | 1                      |
| D3DRS \_ POINTSCALE \_ B                    | 0                      |
| D3DRS \_ POINTSCALE \_ C                    | 0                      |
| \_MULTISAMPLEANTIALIAS D3DRS             | **TRUE**               |
| \_MULTISAMPLEMASK D3DRS                  | 0xFFFFFFFF             |
| \_PATCHEDGESTYLE D3DRS                   | D3DPATCHEDGE \_ discreto |
| D3DRS \_ POINTSIZE \_ Max                   | 1                      |
| \_INDEXEDVERTEXBLENDENABLE D3DRS         | **FALSE**              |
| \_TWEENFACTOR D3DRS                      | 0                      |
| \_POSITIONDEGREE D3DRS                   | \_Cubi D3DDEGREE       |
| \_NORMALDEGREE D3DRS                     | D3DDEGREE \_ lineare      |
| \_MINTESSELLATIONLEVEL D3DRS             | 1                      |
| \_MAXTESSELLATIONLEVEL D3DRS             | 1                      |
| D3DRS \_ ADAPTIVETESS \_ X                  | 0                      |
| D3DRS \_ ADAPTIVETESS \_ Y                  | 0                      |
| D3DRS \_ ADAPTIVETESS \_ Z                  | 1                      |
| D3DRS \_ ADAPTIVETESS \_ W                  | 0                      |
| D3DRS \_ ENABLEADAPTIVETESSELLATION "/> | **FALSE**              |



 

## <a name="vertex-pipeline-sampler-state"></a>Pipeline Vertex: stato campionatore

Gli Stati del campionatore controllano argomenti correlati al campionamento, ad esempio le modalità di filtro, affiancamento e coordinate di trama. Usare [**IDirect3DDevice9:: SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) per impostare lo stato del campionatore (incluso quello usato nell'unità mosaico per campionare le mappe di spostamento). Gli Stati del campionatore sono stati rinominati con un \_ prefisso "D3DSAMP" per abilitare il rilevamento degli errori in fase di compilazione durante il trasferimento da DirectX 8.

La tabella seguente include tutti gli Stati del campionatore che configurano lo stato dei vertici:



| Stati campionatore      | Valore predefinito |
|---------------------|---------------|
| \_DMAPOFFSET D3DSAMP | 256           |



 

## <a name="vertex-pipeline-texture-state"></a>Pipeline Vertex: stato trama

Gli Stati della trama controllano le operazioni di blending del Blender a più trame. Usare [**IDirect3DDevice9:: SetTextureStageState**](/windows/desktop/api) per impostare gli Stati della trama. Usare [**IDirect3DDevice9:: Setrame**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) per associare una trama a una fase del campionatore.

La tabella seguente include tutti gli Stati di trama che configurano lo stato dei vertici:



| Stati di trama                | Valore predefinito    |
|-------------------------------|------------------|
| \_TEXCOORDINDEX D3DTSS         | 0                |
| \_TEXTURETRANSFORMFLAGS D3DTSS | \_Disabilitazione D3DTTFF |



 

D3DTSS \_ TEXCOORDINDEX è uno stato di elaborazione Vertex della funzione fissa. Se viene usato un vertex shader programmabile, questo stato viene ignorato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Stato di salvataggio e ripristino del blocco di stato](state-blocks-save-and-restore-state.md)
</dt> </dl>

 

 
