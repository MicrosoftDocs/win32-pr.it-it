---
description: Il mapping dell'ambiente è una tecnica che simula superfici altamente riflettenti senza usare l'analisi dei raggi.
ms.assetid: vs|directx_sdk|~\environment_mapping.htm
title: Mapping dell'ambiente (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 686f15b2f097550206f9c02cfc4104e7c9f6c030
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745951"
---
# <a name="environment-mapping-direct3d-9"></a>Mapping dell'ambiente (Direct3D 9)

Il mapping dell'ambiente è una tecnica che simula superfici altamente riflettenti senza usare l'analisi dei raggi. In pratica, il mapping dell'ambiente applica una mappa di trama speciale che contiene un'immagine della scena che circonda un oggetto per l'oggetto stesso. Il risultato è simile all'aspetto di una superficie riflettente, sufficientemente vicino da ingannare l'occhio, senza incorrere in alcun calcolo complesso implicato nella traccia dei raggi.

Nella figura seguente viene illustrato un tipo di mapping dell'ambiente denominato mapping di ambienti sferici. Per informazioni dettagliate, vedere [mapping di ambienti sferici](spherical-environment-mapping.md).

![illustrazione di una teiera con una trama applicata che riflette gli ambienti](images/spheremapped-teapot.png)

La teiera in questa immagine sembra rifletterne gli ambienti; si tratta in realtà di una trama applicata all'oggetto. Poiché il mapping dell'ambiente usa una trama, combinata con coordinate di trama calcolate in modo specifico, può essere eseguita in tempo reale.

In questa sezione vengono fornite informazioni sull'esecuzione di due tipi comuni di mapping dell'ambiente con Direct3D. Sono disponibili molti tipi di mapping dell'ambiente in uso nel settore della grafica, ma gli argomenti seguenti sono destinati alle due forme più comuni: mapping dell'ambiente cubico e mapping di ambienti sferici.

-   [Mapping dell'ambiente cubico](cubic-environment-mapping.md)
-   [Mapping di ambienti sferici](spherical-environment-mapping.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pipeline pixel](pixel-pipeline.md)
</dt> </dl>

 

 



