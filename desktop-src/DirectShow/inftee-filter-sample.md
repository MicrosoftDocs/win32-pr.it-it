---
description: Esempio di filtro InfTee
ms.assetid: ba401528-9706-41fb-99d1-2bc3ffc05f1a
title: Esempio di filtro InfTee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bd0bbbb4df30f549a8ea0ba15d33696dcb7c108cbeffa6658bbb1842291517d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118398019"
---
# <a name="inftee-filter-sample"></a>Esempio di filtro InfTee

## <a name="description"></a>Descrizione

Il filtro InfTee fornisce un'implementazione di esempio del DirectShow [Infinite Pin Tee.](infinite-pin-tee-filter.md) Il filtro ha un pin di input e un numero dinamico di pin di output. Tutti i campioni multimediali inviati al filtro vengono recapitati contemporaneamente da tutti i pin di output.

Questo filtro viene visualizzato in GraphEdit sotto il nome "Sample Infinite Pin Tee", per distinguerlo dal filtro Infinite Pin Tee standard fornito in DirectShow.

## <a name="usage"></a>Utilizzo

Poiché questo filtro non modifica i dati ricevuti, tutti i pin devono accettare lo stesso tipo di supporto. Durante il processo di connessione, il filtro potrebbe riconnettere alcuni pin per fare in modo che i tipi di supporti corrispondano.

I dati in arrivo al pin di input non vengono copiati prima di essere inviati ai pin di output. Il filtro garantisce inoltre che i dati siano recapitati ai filtri downstream, per garantire che entrambi gli output ricevano un servizio in tempo reale. In particolare, se uno degli output può bloccarsi nella funzione membro [**COutputQueue::Receive,**](coutputqueue-receive.md) il tee attiva un thread per distribuire l'esempio. Se non è presente alcun thread per distribuire l'esempio, il thread che recapita il campione al pin di input tee potrebbe passare i dati a un filtro downstream; A questo punto, potrebbe bloccarsi, mantenendo i dati dell'altro filtro downstream per lunghi periodi di tempo.

## <a name="downloading-the-sample"></a>Download dell'esempio

Per scaricare gli esempi DirectShow SDK, installare la versione più recente di [Windows SDK.](https://msdn.microsoft.com/windowsvista/bb980924.aspx)

Questo esempio viene installato nel percorso seguente: *\[ SDK Root \]* Samples Multimedia DirectShow Filters \\ \\ \\ \\ \\ InfTee.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow Campioni](directshow-samples.md)
</dt> </dl>

 

 



