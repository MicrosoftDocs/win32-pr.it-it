---
description: Calcolo dei valori dei parametri
ms.assetid: cc3c26ed-a007-4350-99be-0ebd94953689
title: Calcolo dei valori dei parametri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89dac0767d7d19bc4331e1a9ee032ec5b3eaae2e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304140"
---
# <a name="calculating-parameter-values"></a>Calcolo dei valori dei parametri

Potenzialmente, un buffer di input potrebbe essere molto grande. Idealmente, quando DMO elabora il buffer, i parametri seguiranno esattamente le curve nell'intero batch di dati. Tuttavia, un DMO presenta un certo margine di manovra per il calcolo di tali valori.

-   L'approccio più accurato consiste nel calcolare il valore esatto per ogni unità di dati atomica. ad esempio, ogni esempio di audio. Questo approccio è il più costoso dal punto di vista del calcolo.
-   Un altro approccio consiste nel sezionare i dati in unità più piccole di alcune dimensioni fisse, ad esempio 100 esempi. Questo approccio crea un effetto "scale-stepping". Per alcuni parametri, questo potrebbe essere accettabile. Negli effetti audio, potrebbe creare artefatti udibili.
-   Un compromesso consiste nell'utilizzare la tecnica precedente, ma all'interno di ogni batch eseguire un'interpolazione lineare del valore del parametro per ogni campione.

Questi problemi sono particolarmente importanti per l'elaborazione audio. Un secondo di audio potrebbe contenere 48.000 campioni audio per canale, che è un numero elevato di calcoli da eseguire, ma l'orecchio è sensibile agli artefatti, ad esempio l'aliasing.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Parametri dei supporti](media-parameters.md)
</dt> </dl>

 

 



