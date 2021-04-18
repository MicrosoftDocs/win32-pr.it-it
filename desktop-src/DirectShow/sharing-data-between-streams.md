---
description: Condivisione di dati tra flussi
ms.assetid: e18eecf8-9475-420a-9a60-4b1b5f8fd43a
title: Condivisione di dati tra flussi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee0b2f53fe1952bbc16711f7c7e39c3182ba94a7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481973"
---
# <a name="sharing-data-between-streams"></a>Condivisione di dati tra flussi

> [!Note]  
> Queste API sono deprecate. Le applicazioni devono usare il filtro [**grabber di esempio**](sample-grabber-filter.md) o implementare un filtro personalizzato per ottenere i dati da un grafico filtro DirectShow.

 

L'elaborazione dei dati multimediali richiede in genere una grande quantità di risorse di sistema. Pertanto, è consigliabile evitare di copiare i dati laddove possibile. L'architettura di streaming supporta gli esempi di flussi condivisi, un meccanismo che sposta i dati da un flusso a un altro senza copiarli. Questo buffer consente il trasporto efficiente di dati tra due flussi anche se il flusso di destinazione non supporta in modo specifico il formato dati sottostante.

Si supponga, ad esempio, che si disponga di un flusso multimediale con tre flussi di dati: video e audio e che il timestamp dei dati dell'URL corrisponda al contenuto video. Si vuole scrivere un'applicazione che aggiunga un avviso sul copyright a ogni fotogramma video e scriva i dati in un altro flusso per l'archiviazione, ma l'applicazione non comprende i formati di dati ad eccezione del flusso video. Per il flusso video, viene creato un esempio collegato alla superficie DirectDraw desiderata. È quindi possibile creare un flusso di output chiamando il metodo [**IDirectDrawMediaStream:: CreateSample**](/previous-versions/windows/desktop/api/ddstream/nf-ddstream-idirectdrawmediastream-createsample) con tale puntatore alla stessa area o [**IMediaStream:: CreateSharedSample**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imediastream-createsharedsample). In entrambi i casi, i flussi di input e di output condividono la superficie DirectDraw. Poiché si comprende il formato video, è possibile accedere a questa superficie in base alle esigenze.

Per recuperare gli altri puntatori del flusso di origine (audio e URL), enumerare il flusso del contenitore di origine e selezionare i puntatori ai flussi non video. A ognuno di questi flussi di origine è associato un flusso di output nel contenitore del flusso di output. Recuperare questi puntatori di output chiamando il metodo [**IMultiMediaStream:: GetMediaStream**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imultimediastream-getmediastream) sul contenitore di output con ognuno dei puntatori del flusso di origine. Questo processo è descritto nella seguente procedura.

1.  Chiamare [**IMultiMediaStream:: EnumMediaStreams**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imultimediastream-enummediastreams) per recuperare un puntatore a un flusso di origine. Assicurarsi che non sia il flusso video, perché l'applicazione ne è già in grado di comprendere il formato.
2.  Chiamare [**IMultiMediaStream:: GetMediaStream**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imultimediastream-getmediastream) nel flusso del contenitore di output con il puntatore del passaggio 1. Viene restituito un puntatore al flusso di output desiderato.
3.  Chiamare [**AllocateSample**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imediastream-allocatesample) nel flusso di origine.
4.  Chiamare [**CreateSharedSample**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imediastream-createsharedsample) nel flusso di output.
5.  Chiamare [**Update**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-istreamsample-update) nel flusso di origine per leggere i dati.
6.  Chiamare [**Update**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-istreamsample-update) nel flusso di output per scrivere i dati.

Ripetere questi passaggi per ogni flusso il cui formato non è supportato. Quando entrambi gli esempi terminano l'aggiornamento, il flusso di output contiene tutti i dati del flusso di origine e l'operazione è terminata.

 

 



