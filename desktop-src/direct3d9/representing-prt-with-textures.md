---
description: L'esempio PRTDemo e il simulatore PRTCmdLine incluso in DirectX SDK rappresentano i vettori di trasferimento ai vertici di una rete mesh.
ms.assetid: cee049e8-3245-4fce-ab2f-ba251eacc72a
title: Rappresentazione di PRT con trame (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4647cfc85451ede9507e007ed556a203a3cd890a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104225472"
---
# <a name="representing-prt-with-textures-direct3d-9"></a>Rappresentazione di PRT con trame (Direct3D 9)

L'esempio PRTDemo e il simulatore PRTCmdLine incluso in DirectX SDK rappresentano i vettori di trasferimento ai vertici di una rete mesh. Per rappresentare accuratamente il segnale PRT, può essere necessario tassellature che può risultare poco pratico per i giochi correnti. Rappresenta un approccio alternativo con lo stesso costo dei dati indipendente dalla complessità della rete. Esistono diversi modi per generare mappe di trame vettori di trasferimento usando la libreria PRT D3DX.

## <a name="precomputing-transfer-vectors"></a>Vettori di trasferimento per il precalcolo

Un approccio consiste nel modificare gli esempi di PRTDemo e PRTCmdLine per calcolare un vettore di trasferimento a ogni Texel in una parametrizzazione di una superficie. Per eseguire questa operazione:

1.  Modificare la chiamata a [**D3DXCreatePRTEngine**](d3dxcreateprtengine.md) per estrarre le coordinate di trama dalla mesh (ExtractUVs deve essere **true**)
2.  Sostituire le chiamate [**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md) con [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md) usando le stesse dimensioni della trama.

Tutti i metodi ID3DXPRTEngine funzionano con le simulazioni per Texel, ad eccezione di: ComputeBounceAdaptive, ComputeSSAdaptive, ComputeSS e ComputeDirectLightingSHAdaptive. Anche se la simulazione dello spazio di trama genera il risultato corretto, spesso può essere piuttosto lento poiché probabilmente sarà il calcolo dei vettori di trasferimento a densità elevata.

Un altro approccio consiste nel calcolare una simulazione di PRT per un vertice adattivo (con coordinate di trama che verranno usate per i dati per Texel) e quindi chiamare [**ID3DXPRTEngine:: ResampleBuffer**](id3dxprtengine--resamplebuffer.md) (usando un buffer di output creato con [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md) alla risoluzione appropriata). Funziona con tutte le funzionalità di D3DX PRT nell'SDK e spesso può essere molto più efficiente rispetto al calcolo diretto di un buffer di trasferimento per Texel.

## <a name="runtime-calculations"></a>Calcoli di runtime

Se viene usato un singolo cluster, i risultati possono essere filtrati e con mapping MIP come qualsiasi altra trama e il pixel shader è identico al codice del vertex shader fornito con PRTDemo.

Se la compressione genera più cluster, non è possibile filtrare o mipmap i dati perché gli indici clustering non sono continui. Di seguito sono riportate alcune alternative per la gestione dei dati multicluster:

-   Eseguire tutte le operazioni di filtro nel pixel shader. Sfortunatamente, questa operazione è in genere poco pratica per motivi di prestazioni.
-   Se le trame sono trame con mapping non MIP a bassa risoluzione (ad esempio, mappe luminose), è più probabile che si calcoli semplicemente l'illuminazione direttamente nello spazio di trama, in cui non si verificherà alcun filtro e il rendering dell'oggetto con una trama ombreggiata. Si tratta essenzialmente di una mappa chiara dinamica che viene creata interamente nella GPU.
-   Se viene usato un Atlante di trama (vedere [uso di UVAtlas (Direct3D 9)](using-uvatlas.md)), è possibile raggruppare manualmente la scena perché tutti i vettori di trasferimento in un componente connesso nello spazio di trama si trovino nello stesso cluster. In questo modo è possibile filtrare la trama perché tutti i Texel a cui si accede si trovino nello stesso cluster per costruzione. L'ID cluster per una determinata faccia può essere propagato dal vertex shader.

I pixel shader hanno un numero molto inferiore di registri costanti che non possono essere indicizzati, pertanto il pixel shader è leggermente diverso da quello del vertex shader. L'archiviazione dei singoli cluster funziona in una trama dinamica a bassa risoluzione e l'uso di caricamenti di trama costituisce il modo più efficiente per eseguire il rendering quando si usano più cluster.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Trasferimento Radiance pre-calcolato](precomputed-radiance-transfer.md)
</dt> <dt>

[Esempio di demo PRT](https://msdn.microsoft.com/library/Ee418763(v=VS.85).aspx)
</dt> <dt>

[Simulatore PRT (prtcmdline.exe)](https://msdn.microsoft.com/library/Ee418766(v=VS.85).aspx)
</dt> </dl>

 

 



