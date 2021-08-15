---
description: Il rendering dei dati dei vertici da un buffer dei vertici richiede alcuni passaggi. Per prima cosa, è necessario impostare l'origine del flusso chiamando il metodo IDirect3DDevice9::SetStreamSource, come illustrato nell'esempio seguente.
ms.assetid: a0435a3d-e1dd-4365-904d-8e5713e379ce
title: Rendering da un vertex buffer (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87ee3d477fc812d2dabed765e28bb14452a6badf746a331a13283108ef46b47c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118520072"
---
# <a name="rendering-from-a-vertex-buffer-direct3d-9"></a>Rendering da un vertex buffer (Direct3D 9)

Il rendering dei dati dei vertici da un buffer dei vertici richiede alcuni passaggi. Per prima cosa, è necessario impostare l'origine del flusso chiamando il metodo [**IDirect3DDevice9::SetStreamSource,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) come illustrato nell'esempio seguente.


```
d3dDevice->SetStreamSource( 0, g_pVB, 0, sizeof(CUSTOMVERTEX) );
```



Il primo parametro di [**IDirect3DDevice9::SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) indica a Direct3D l'origine del flusso di dati del dispositivo. Il secondo parametro è il buffer dei vertici da associare al flusso di dati. Il terzo parametro è l'offset dall'inizio del flusso all'inizio dei dati del vertice, in byte. Il quarto parametro è lo stride del componente, in byte. Nel codice di esempio precedente vengono usate le dimensioni di CUSTOMVERTEX per lo stride del componente.

Il passaggio successivo consiste nell'informare Direct3D del vertex shader da usare chiamando il [**metodo IDirect3DDevice9::SetVertexShader.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) Il codice di esempio seguente imposta un codice FVF per il vertex shader. Questo informa Direct3D dei tipi di vertici con cui si sta occupando.


```
d3dDevice->SetFVF( D3DFVF_CUSTOMVERTEX );
```



Dopo aver impostato l'origine del flusso e il vertex shader, tutti i metodi di disegno useranno il buffer dei vertici. L'esempio di codice seguente illustra come eseguire il rendering dei vertici da un vertex buffer con il metodo [**IDirect3DDevice9::D rawPrimitive.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)


```
d3dDevice->DrawPrimitive( D3DPT_TRIANGLELIST, 0, 1 );
```



Il secondo parametro accettato [**da IDirect3DDevice9::D rawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) è l'indice del primo vettore nel buffer dei vertici da caricare.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Vertex buffer](vertex-buffers.md)
</dt> <dt>

[Rendering da vertex buffer e index buffer (Direct3D 9)](rendering-from-vertex-and-index-buffers.md)
</dt> </dl>

 

 
