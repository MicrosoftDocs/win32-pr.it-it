---
description: Elaborazione In-Place
ms.assetid: 61e5c12c-e42a-42d8-ac5b-e60afaceda82
title: Elaborazione In-Place
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ba0aa5c50fc000eadadc0f121db6f954a57c338
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304138"
---
# <a name="in-place-processing"></a>Elaborazione In-Place

Alcune trasformazioni dei dati possono essere eseguite modificando direttamente i dati. Questa operazione è denominata elaborazione *sul posto* . Molti effetti audio e video possono essere eseguiti in questo modo. Se un DMO supporta l'elaborazione sul posto, espone l'interfaccia [**IMediaObjectInPlace**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobjectinplace) . L'elaborazione sul posto è in genere più efficiente rispetto all'uso di buffer distinti per l'output. (Un'eccezione principale è quando il buffer risiede nella memoria video. In tal caso, le operazioni di lettura sono molto più lente delle operazioni di scrittura, pertanto l'elaborazione sul posto non è consigliata.

Per elaborare i dati sul posto, il client effettua una singola chiamata al metodo [**IMediaObjectInPlace::P rocess**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobjectinplace-process) , anziché a chiamate separate a **ProcessInput** e **ProcessOutput**. Il metodo **Process** è sincrono; tutte le operazioni di elaborazione avvengono all'interno della chiamata. Inoltre, l'elaborazione sul posto non usa gli oggetti **IMediaBuffer** . Il metodo **Process** accetta un puntatore direttamente al buffer di memoria.

Un DMO che supporta l'elaborazione sul posto deve comunque implementare l'interfaccia **IMediaObject** , inclusi i metodi **ProcessInput** e **ProcessOutput** . Il client può scegliere se usare l'elaborazione sul posto o usare buffer distinti. Tuttavia, non combinare i due tipi di elaborazione. Se si chiama il **Metodo Process**, non chiamare **ProcessInput** o **ProcessOutput** e viceversa.

**Effetti della coda**

Una DMO sul posto potrebbe creare un output aggiuntivo dopo l'arresto dell'input. Questa operazione è detta *coda effetto*. Un effetto di riverbero continua, ad esempio, dopo che l'input raggiunge il silenzio. Se è presente un effetto Tail, il metodo **Process** restituisce S \_ false. Una volta che l'applicazione ha elaborato tutti i dati, può generare la coda degli effetti inviando buffer vuoti al metodo **Process** .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Hosting diretto di un DMO](directly-hosting-a-dmo.md)
</dt> </dl>

 

 



