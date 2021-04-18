---
description: Esempio di filtro InfTee
ms.assetid: ba401528-9706-41fb-99d1-2bc3ffc05f1a
title: Esempio di filtro InfTee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cd0fc5a1d550e0327da0d0d3dd47c8847ffafee
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304179"
---
# <a name="inftee-filter-sample"></a>Esempio di filtro InfTee

## <a name="description"></a>Descrizione

Il filtro InfTee fornisce un'implementazione di esempio del filtro del [Pin Tee infinito](infinite-pin-tee-filter.md) DirectShow. Il filtro ha un pin di input e un numero dinamico di pin di output. Tutti gli esempi di supporti inviati al filtro vengono distribuiti simultaneamente da tutti i pin di output.

Questo filtro viene visualizzato in GraphEdit sotto il nome "Sample uninfinito Pin Tee" per distinguerlo dal filtro standard infinito Pin Tee fornito in DirectShow.

## <a name="usage"></a>Utilizzo

Poiché questo filtro non modifica i dati ricevuti, tutti i pin devono accettare lo stesso tipo di supporto. Durante il processo di connessione, il filtro potrebbe riconnettere alcuni pin per fare in modo che i tipi di supporto corrispondano.

I dati che arrivano al pin di input non vengono copiati prima di essere inviati ai pin di output. Il filtro garantisce inoltre che i dati vengano recapitati ai filtri downstream, per garantire che entrambi gli output ricevano un servizio tempestivo. In particolare, se uno degli output può essere bloccato nella funzione membro [**COutputQueue:: Receive**](coutputqueue-receive.md) , il tee gira un thread per recapitare l'esempio. Se non è presente alcun thread per recapitare l'esempio, il thread che recapita l'esempio al pin di input Tee potrebbe passare i dati a un filtro downstream; a questo punto, potrebbe bloccarsi, mantenendo i dati dall'altro filtro downstream per lunghi periodi di tempo.

## <a name="downloading-the-sample"></a>Download dell'esempio

Per scaricare gli esempi di DirectShow SDK, installare la versione più recente del [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

Questo esempio viene installato nel percorso seguente: esempi *\[ radice \] SDK* \\ \\ \\ filtri DirectShow multimediali \\ \\ InfTee.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempi di DirectShow](directshow-samples.md)
</dt> </dl>

 

 



