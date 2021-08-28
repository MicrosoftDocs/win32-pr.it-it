---
description: "In questo argomento vengono fornite due visualizzazioni di alto livello dell'architettura di Direct3D:"
ms.assetid: ed08b4c8-fdd9-46fb-a2be-c2fb15af2dc6
title: Architettura Direct3D (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d288cbf7896b276824f358364bede519e778375d1d3f8c9915108cbfadf8486
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119791492"
---
# <a name="direct3d-architecture-direct3d-9"></a>Architettura Direct3D (Direct3D 9)

In questo argomento vengono fornite due visualizzazioni di alto livello dell'architettura di Direct3D:

-   [Pipeline grafica Direct3D:](#direct3d-graphics-pipeline) visualizzazione dell'architettura di elaborazione interna del sistema di rendering Direct3D.
-   [Integrazione del sistema Direct3D:](#direct3d-system-integration) visualizzazione della mediazione di Direct3D tra un'applicazione e l'hardware grafico.

## <a name="direct3d-graphics-pipeline"></a>Pipeline grafica Direct3D

La pipeline grafica offre la potenza per elaborare ed eseguire in modo efficiente il rendering di scene Direct3D su uno schermo, sfruttando l'hardware disponibile. Il diagramma seguente illustra i blocchi predefiniti della pipeline:

![Diagramma della pipeline grafica direct3d](images/blockdiag-graphics.png)



| Componente pipeline  | Descrizione                                                                                                                                                                                      | Argomenti correlati                                                                                                                                                                                             |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Dati sui vertici         | I vertici del modello non trasformati vengono archiviati nei buffer di memoria dei vertici.                                                                                                                                | [Vertex Buffer (Direct3D 9),](vertex-buffers.md) [ **IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)                                                                                                |
| Dati primitivi      | Le primitive geometriche, inclusi punti, linee, triangoli e poligoni, vengono referenziate nei dati dei vertici con buffer di indice.                                                                    | [Buffer di indice (Direct3D 9),](index-buffers.md) [**IDirect3DIndexBuffer9,**](/windows/desktop/api) [primitive,](primitives.md) [primitive di ordine superiore (Direct3D 9)](higher-order-primitives.md) |
| Suddivisione a mosaico        | L'unità a tesselator converte primitive di ordine superiore, mappe di spostamento e patch di mesh in posizioni dei vertici e archivia tali posizioni nei buffer dei vertici.                                      | [A tessellazione (Direct3D 9)](tessellation.md)                                                                                                                                                              |
| Elaborazione dei vertici   | Le trasformazioni Direct3D vengono applicate ai vertici archiviati nel vertex buffer.                                                                                                                    | [Pipeline vertice (Direct3D 9)](vertex-pipeline.md)                                                                                                                                                        |
| Elaborazione geometry | Ai vertici trasformati vengono applicati il ritaglio, l'culling del viso posteriore, la valutazione degli attributi e la rasterizzazione.                                                                                    | [Pipeline pixel (Direct3D 9)](pixel-pipeline.md)                                                                                                                                                          |
| Superficie con trama    | Le coordinate di trama per le superfici Direct3D vengono fornite a Direct3D tramite [**l'interfaccia IDirect3DTexture9.**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)                                                         | [Trame Direct3D (Direct3D 9),](direct3d-textures.md) [ **IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)                                                                                                    |
| Campionatore di trame     | Il filtro del livello di dettaglio della trama viene applicato ai valori di trama di input.                                                                                                                            | [Trame Direct3D (Direct3D 9)](direct3d-textures.md)                                                                                                                                                    |
| Elaborazione pixel    | Le operazioni pixel shader usano i dati geometry per modificare i dati di vertice e trama di input, producendo valori di colore pixel di output.                                                                           | [Pipeline pixel (Direct3D 9)](pixel-pipeline.md)                                                                                                                                                          |
| Pixel Rendering     | I processi di rendering finali modificano i valori dei colori dei pixel con test alfa, profondità o stencil oppure applicando la fusione alfa o la sfumatura. Tutti i valori in pixel risultanti vengono presentati alla visualizzazione di output. | [Pipeline pixel (Direct3D 9)](pixel-pipeline.md)                                                                                                                                                          |



 

## <a name="direct3d-system-integration"></a>Integrazione del sistema Direct3D

Il diagramma seguente illustra le relazioni tra un'applicazione Window, Direct3D, GDI e l'hardware:

![diagramma della relazione tra direct3d e altri componenti di sistema](images/d3dsysint.png)

Direct3D espone un'interfaccia indipendente dal dispositivo a un'applicazione. Le applicazioni Direct3D possono esistere insieme alle applicazioni GDI ed entrambe hanno accesso all'hardware grafico del computer tramite il driver di dispositivo per la scheda grafica. A differenza di GDI, Direct3D può sfruttare le funzionalità hardware creando un dispositivo hal.

Un dispositivo hal fornisce l'accelerazione hardware alle funzioni della pipeline grafica, in base al set di funzionalità supportato dalla scheda grafica. Vengono forniti metodi Direct3D per recuperare le funzionalità di visualizzazione dei dispositivi in fase di esecuzione. Vedere [**IDirect3DDevice9::GetDeviceCaps.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) Se l'hardware non fornisce una funzionalità, l'hal non la segnala come funzionalità hardware.

Per altre informazioni sui dispositivi hal e di riferimento supportati da Direct3D, vedere Tipi di [dispositivo (Direct3D 9).](device-types.md)

## <a name="related-topics"></a>Argomenti correlati

[Per iniziare](getting-started.md)
