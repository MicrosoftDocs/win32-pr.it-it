---
description: "In questo argomento vengono fornite due viste di alto livello dell'architettura di Direct3D:"
ms.assetid: ed08b4c8-fdd9-46fb-a2be-c2fb15af2dc6
title: Architettura Direct3D (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e557b7a36aadcaa8b96899047a721741ecef2156
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124500"
---
# <a name="direct3d-architecture-direct3d-9"></a>Architettura Direct3D (Direct3D 9)

In questo argomento vengono fornite due viste di alto livello dell'architettura di Direct3D:

-   [Pipeline grafica Direct3D](#direct3d-graphics-pipeline) : vista dell'architettura di elaborazione interna del sistema di rendering Direct3D.
-   [Integrazione del sistema Direct3D](#direct3d-system-integration) : una vista del modo in cui Direct3D intermedia tra un'applicazione e l'hardware grafico.

## <a name="direct3d-graphics-pipeline"></a>Pipeline grafica Direct3D

La pipeline grafica offre la potenza per elaborare ed eseguire in modo efficiente le scene Direct3D in una visualizzazione, sfruttando i vantaggi dell'hardware disponibile. Il diagramma seguente illustra i blocchi predefiniti della pipeline:

![diagramma della pipeline grafica Direct3D](images/blockdiag-graphics.png)



| Componente pipeline  | Descrizione                                                                                                                                                                                      | Argomenti correlati                                                                                                                                                                                             |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Dati dei vertici         | I vertici del modello non trasformati vengono archiviati nei buffer di memoria dei vertici.                                                                                                                                | [Buffer vertex (Direct3D 9)](vertex-buffers.md), [ **IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)                                                                                                |
| Dati primitivi      | Le primitive geometriche, tra cui punti, linee, triangoli e poligoni, fanno riferimento ai dati dei vertici con buffer di indice.                                                                    | [Buffer di indice (Direct3D 9)](index-buffers.md), [**IDirect3DIndexBuffer9**](/windows/desktop/api), [primitive](primitives.md), [primitive di ordine superiore (Direct3D 9)](higher-order-primitives.md) |
| Suddivisione a mosaico        | L'unità Tesselator converte le primitive di ordine superiore, le mappe di spostamento e le patch mesh in posizioni dei vertici e archivia tali posizioni nei buffer dei vertici.                                      | [Suddivisione a mosaico (Direct3D 9)](tessellation.md)                                                                                                                                                              |
| Elaborazione vertici   | Le trasformazioni Direct3D vengono applicate ai vertici archiviati nel buffer dei vertici.                                                                                                                    | [Pipeline Vertex (Direct3D 9)](vertex-pipeline.md)                                                                                                                                                        |
| Elaborazione Geometry | Il ritaglio, l'abbattimento delle facce posteriori, la valutazione degli attributi e la rasterizzazione vengono applicati ai vertici trasformati.                                                                                    | [Pipeline pixel (Direct3D 9)](pixel-pipeline.md)                                                                                                                                                          |
| Superficie con trama    | Le coordinate di trama per le superfici Direct3D vengono fornite a Direct3D tramite l'interfaccia [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) .                                                         | [Trame Direct3D (Direct3D 9)](direct3d-textures.md), [ **IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)                                                                                                    |
| Campionatore trama     | Per i valori di trama di input viene applicato il filtro del livello di dettaglio della trama.                                                                                                                            | [Trame Direct3D (Direct3D 9)](direct3d-textures.md)                                                                                                                                                    |
| Elaborazione pixel    | Le operazioni pixel shader usano i dati geometrici per modificare i dati di trama e vertice di input, restituendo i valori dei colori del pixel di output.                                                                           | [Pipeline pixel (Direct3D 9)](pixel-pipeline.md)                                                                                                                                                          |
| Rendering pixel     | I processi di rendering finali modificano i valori dei colori pixel con test alfa, profondità o stencil oppure applicando la fusione o la nebbia Alpha. Tutti i valori pixel risultanti vengono presentati alla visualizzazione dell'output. | [Pipeline pixel (Direct3D 9)](pixel-pipeline.md)                                                                                                                                                          |



 

## <a name="direct3d-system-integration"></a>Integrazione del sistema Direct3D

Il diagramma seguente illustra le relazioni tra un'applicazione finestra, Direct3D, GDI e l'hardware:

![diagramma della relazione tra Direct3D e altri componenti di sistema](images/d3dsysint.png)

Direct3D espone un'interfaccia indipendente dal dispositivo a un'applicazione. Le applicazioni Direct3D possono esistere insieme alle applicazioni GDI ed entrambi hanno accesso all'hardware grafico del computer tramite il driver di dispositivo per la scheda grafica. Diversamente da GDI, Direct3D può sfruttare le funzionalità hardware creando un dispositivo Hal.

Un dispositivo Hal fornisce l'accelerazione hardware alle funzioni della pipeline grafica, in base al set di funzionalità supportato dalla scheda grafica. Sono disponibili metodi Direct3D per recuperare le funzionalità di visualizzazione del dispositivo in fase di esecuzione. Vedere [**IDirect3DDevice9:: GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps). Se una funzionalità non viene fornita dall'hardware, l'HAL non lo segnala come funzionalità hardware.

Per altre informazioni sui dispositivi HAL e di riferimento supportati da Direct3D, vedere [tipi di dispositivi (Direct3D 9)](device-types.md).

## <a name="related-topics"></a>Argomenti correlati

[Per iniziare](getting-started.md)
