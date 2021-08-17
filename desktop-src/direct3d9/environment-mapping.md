---
description: Il mapping dell'ambiente è una tecnica che simula superfici altamente riflettenti senza usare il ray tracing.
ms.assetid: vs|directx_sdk|~\environment_mapping.htm
title: Mapping dell'ambiente (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8a07d53028e200d273206f149ea12c07afa6dbc4ad47f8232e64cddf7582a09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119122224"
---
# <a name="environment-mapping-direct3d-9"></a>Mapping dell'ambiente (Direct3D 9)

Il mapping dell'ambiente è una tecnica che simula superfici altamente riflettenti senza usare il ray tracing. In pratica, il mapping dell'ambiente applica all'oggetto stesso una mappa di trama speciale che contiene un'immagine della scena che circonda un oggetto. Il risultato approssima l'aspetto di una superficie riflettente, abbastanza vicina da ingannare l'occhio, senza incorrere in calcoli complessi coinvolti nella traccia dei raggi.

La figura seguente illustra un tipo di mapping dell'ambiente denominato mapping dell'ambiente sferico. Per informazioni dettagliate, vedere [Mapping dell'ambiente sferico](spherical-environment-mapping.md).

![illustrazione di una teiera con una trama applicata che riflette l'ambiente circostante](images/spheremapped-teapot.png)

La teiera in questa immagine sembra riflettere l'ambiente circostante; si tratta in realtà di una trama applicata all'oggetto . Poiché il mapping dell'ambiente usa una trama, combinata con coordinate di trama appositamente calcolate, può essere eseguita in tempo reale.

In questa sezione vengono fornite informazioni sull'esecuzione di due tipi comuni di mapping dell'ambiente con Direct3D. Esistono molti tipi di mapping dell'ambiente in uso in tutto il settore della grafica, ma gli argomenti seguenti sono relativi alle due forme più comuni: mapping dell'ambiente cubico e mapping dell'ambiente sferico.

-   [Mapping dell'ambiente cubico](cubic-environment-mapping.md)
-   [Mapping dell'ambiente sferico](spherical-environment-mapping.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pixel Pipeline](pixel-pipeline.md)
</dt> </dl>

 

 



