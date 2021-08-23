---
description: L'esempio PRTDemo e il simulatore PRTCmdLine inclusi in DirectX SDK rappresentano vettori di trasferimento ai vertici di una mesh.
ms.assetid: cee049e8-3245-4fce-ab2f-ba251eacc72a
title: Rappresentazione di PRT con trame (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e827e24258d75a91aa75c9eb51ed6563d476ab16f75fedc31a7071bca28a4a78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118797925"
---
# <a name="representing-prt-with-textures-direct3d-9"></a>Rappresentazione di PRT con trame (Direct3D 9)

L'esempio PRTDemo e il simulatore PRTCmdLine inclusi in DirectX SDK rappresentano vettori di trasferimento ai vertici di una mesh. Per rappresentare in modo accurato il segnale PRT, possono essere necessari tesserli che potrebbero risultare poco pratico per i giochi correnti. La rappresentazione dei vettori di trasferimento nelle mappe di trama è un approccio alternativo che ha lo stesso costo dei dati indipendentemente dalla complessità della mesh. Esistono diversi modi per generare mappe di trame vettoriali di trasferimento usando la libreria PRT D3DX.

## <a name="precomputing-transfer-vectors"></a>Pre-ricalcolo dei vettori di trasferimento

Un approccio consiste nel modificare gli esempi PRTDemo e PRTCmdLine per calcolare un vettore di trasferimento a ogni texel in una parametrizzazione di una superficie. Per eseguire questa operazione:

1.  Modificare la chiamata a [**D3DXCreatePRTEngine**](d3dxcreateprtengine.md) per estrarre le coordinate della trama dalla mesh (ExtractUVs deve essere **TRUE)**
2.  Sostituire [**le chiamate D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md) con [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md) usando le stesse dimensioni della trama.

Tutti i metodi ID3DXPRTEngine funzionano con simulazioni per texel ad eccezione di ComputeBounceAdaptive, ComputeSSAdaptive, ComputeSS e ComputeDirectLightingSHAdaptive. Anche se la simulazione dello spazio trame genererà il risultato corretto, spesso può essere piuttosto lenta perché molto probabilmente calcola i vettori di trasferimento ad alta densità.

Un altro approccio consiste nel calcolare una simulazione PRT adattiva per vertice (con coordinate di trama che verranno usate per i dati per texel) e quindi chiamare [**ID3DXPRTEngine::ResampleBuffer**](id3dxprtengine--resamplebuffer.md) (usando un buffer di output creato con [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md) alla risoluzione appropriata). Funziona con tutte le funzionalità PRT D3DX nell'SDK e spesso può essere molto più efficiente rispetto al calcolo diretto di un buffer di trasferimento per texel.

## <a name="runtime-calculations"></a>Calcoli di runtime

Se viene usato un singolo cluster, i risultati possono essere filtrati e mappati mip come qualsiasi altra trama e il pixel shader è identico al codice vertex shader fornito con PRTDemo.

Se la compressione genera più cluster, non è possibile filtrare o modificare il mapping dei dati perché gli indici di clustering non sono continui. Ecco alcune alternative per la gestione dei dati multi-cluster:

-   Eseguire tutti i filtri manualmente nel pixel shader. Sfortunatamente, questo non è in genere pratico per motivi di prestazioni.
-   Se le trame sono trame non mappate a mip a bassa risoluzione (ad esempio, mappe di luce), è molto più efficiente calcolare l'illuminazione direttamente nello spazio della trama, in cui non verrà eseguito alcun filtro, ed eseguire il rendering dell'oggetto con una trama ombreggiata. Si tratta essenzialmente di una mappa di luce dinamica creata interamente sulla GPU.
-   Se si usa un at atlas di trama (vedere Uso di [UVAtlas (Direct3D 9)](using-uvatlas.md)), è possibile creare manualmente un cluster della scena facendo in modo che tutti i vettori di trasferimento in un componente connesso nello spazio della trama siano nello stesso cluster. In questo modo è possibile filtrare la trama perché tutti i texel a cui si accede verrebbero nello stesso cluster in base alla costruzione. L'ID cluster per un viso specificato può essere propagato dal vertex shader.

I pixel shader hanno un numero molto inferiore di registri costanti che non possono essere indicizzati, quindi pixel shader è leggermente diverso dal vertex shader. L'archiviazione del lavoro per cluster in una trama dinamica a bassa risoluzione e l'uso di caricamenti di trama sarebbe il modo più efficiente per eseguire il rendering quando si usano più cluster.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Trasferimento di radiance pre-ricalcolato](precomputed-radiance-transfer.md)
</dt> <dt>

[Esempio demo PRT](https://msdn.microsoft.com/library/Ee418763(v=VS.85).aspx)
</dt> <dt>

[Simulatore PRT (prtcmdline.exe)](https://msdn.microsoft.com/library/Ee418766(v=VS.85).aspx)
</dt> </dl>

 

 



