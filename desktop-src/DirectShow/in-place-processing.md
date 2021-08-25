---
description: In-Place elaborazione
ms.assetid: 61e5c12c-e42a-42d8-ac5b-e60afaceda82
title: In-Place elaborazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b1a72b6bad2311a9c96bdd94e7e63acdc7e4961b51e106324dbe38de9510ad2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117818796"
---
# <a name="in-place-processing"></a>In-Place elaborazione

Alcune trasformazioni dei dati possono essere completate modificando direttamente i dati. Questa operazione viene *chiamata elaborazione sul* posto. In questo modo è possibile eseguire molti effetti audio e video. Se un DMO supporta l'elaborazione sul posto, espone [**l'interfaccia IMediaObjectInPlace.**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobjectinplace) L'elaborazione sul posto è in genere più efficiente rispetto all'uso di buffer separati per l'output. Una delle principali eccezioni è quando il buffer si trova nella memoria video. In questo caso, le operazioni di lettura sono molto più lente delle operazioni di scrittura, quindi l'elaborazione sul posto non è consigliata.

Per elaborare i dati sul posto, il client effettua una singola chiamata al metodo [**IMediaObjectInPlace::P rocess, anziché**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobjectinplace-process) separare le chiamate a **ProcessInput** e **ProcessOutput.** Il **metodo Process** è sincrono. tutta l'elaborazione avviene all'interno della chiamata. Inoltre, l'elaborazione sul posto non usa **oggetti IMediaBuffer.** Il **metodo Process** accetta un puntatore direttamente al buffer di memoria.

Un DMO che supporta l'elaborazione sul posto deve comunque implementare **l'interfaccia IMediaObject,** inclusi **i metodi ProcessInput** **e ProcessOutput.** Il client può scegliere se usare l'elaborazione sul posto o buffer separati. Tuttavia, non combinare i due tipi di elaborazione. Se si chiama **Process**, non chiamare **ProcessInput** o **ProcessOutput** e viceversa.

**Code degli effetti**

Un'operazione sul DMO potrebbe creare un output aggiuntivo dopo l'arresto dell'input. Questa operazione è detta *coda dell'effetto.* Ad esempio, un effetto di riverbero continua quando l'input raggiunge il silenzio. Se è presente un effetto tail, il **metodo Process** restituisce S \_ FALSE. Dopo che l'applicazione ha elaborato tutti i dati, può generare l'effetto tail inviando buffer vuoti al **metodo Process.**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Hosting diretto di un DMO](directly-hosting-a-dmo.md)
</dt> </dl>

 

 



