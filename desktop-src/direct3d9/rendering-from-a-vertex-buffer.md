---
description: "Per il rendering dei dati del vertice da un buffer vertex sono necessari alcuni passaggi. Per prima cosa, è necessario impostare l'origine del flusso chiamando il metodo IDirect3DDevice9:: SetStreamSource, come illustrato nell'esempio seguente."
ms.assetid: a0435a3d-e1dd-4365-904d-8e5713e379ce
title: Rendering da un buffer vertex (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cebb68c5395a827a9aee4ea1f8465257c436bb7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123429"
---
# <a name="rendering-from-a-vertex-buffer-direct3d-9"></a>Rendering da un buffer vertex (Direct3D 9)

Per il rendering dei dati del vertice da un buffer vertex sono necessari alcuni passaggi. Per prima cosa, è necessario impostare l'origine del flusso chiamando il metodo [**IDirect3DDevice9:: SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) , come illustrato nell'esempio seguente.


```
d3dDevice->SetStreamSource( 0, g_pVB, 0, sizeof(CUSTOMVERTEX) );
```



Il primo parametro di [**IDirect3DDevice9:: SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) indica a Direct3D l'origine del flusso di dati del dispositivo. Il secondo parametro è il buffer vertex da associare al flusso di dati. Il terzo parametro è l'offset dall'inizio del flusso all'inizio dei dati del vertice, espresso in byte. Il quarto parametro è lo stride del componente, in byte. Nel codice di esempio precedente, la dimensione di un oggetto CUSTOMVERTEX viene utilizzata per lo stride del componente.

Il passaggio successivo consiste nell'informare Direct3D quale vertex shader utilizzare chiamando il metodo [**IDirect3DDevice9:: SetVertexShader**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) . Il codice di esempio seguente imposta un codice FVF per il vertex shader. Questo informa Direct3D dei tipi di vertici che sta occupando.


```
d3dDevice->SetFVF( D3DFVF_CUSTOMVERTEX );
```



Dopo aver impostato l'origine del flusso e il vertex shader, tutti i metodi di creazione utilizzeranno il buffer dei vertici. Nell'esempio di codice seguente viene illustrato come eseguire il rendering dei vertici da un buffer vertex con il metodo [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) .


```
d3dDevice->DrawPrimitive( D3DPT_TRIANGLELIST, 0, 1 );
```



Il secondo parametro che [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) accetta è l'indice del primo vettore nel buffer del vertice da caricare.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Buffer vertici](vertex-buffers.md)
</dt> <dt>

[Rendering dai buffer di Vertex e index (Direct3D 9)](rendering-from-vertex-and-index-buffers.md)
</dt> </dl>

 

 
