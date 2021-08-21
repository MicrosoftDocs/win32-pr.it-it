---
description: Condivisione dei dati tra Flussi
ms.assetid: e18eecf8-9475-420a-9a60-4b1b5f8fd43a
title: Condivisione dei dati tra Flussi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4137d56a9d90f524ee2e5c67b6a4d726d9478e824513d0fe7879c95ce094af1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072565"
---
# <a name="sharing-data-between-streams"></a>Condivisione dei dati tra Flussi

> [!Note]  
> Queste API sono deprecate. Le applicazioni devono usare il [**filtro Grabber**](sample-grabber-filter.md) di esempio o implementare un filtro personalizzato per ottenere dati da un DirectShow di filtro.

 

L'elaborazione dei dati multimediali richiede in genere una grande quantità di risorse di sistema. Pertanto, è consigliabile evitare di copiare i dati quando possibile. L'architettura di streaming supporta esempi di flussi condivisi, un meccanismo che sposta i dati da un flusso a un altro senza copiarli. Questo buffer consente il trasporto efficiente dei dati tra due flussi anche se il flusso di destinazione non supporta in modo specifico il formato dati sottostante.

Si supponga, ad esempio, di avere un flusso multimediale con tre flussi di dati: video e audio e dati URL con timestamp corrispondente al contenuto video. Si vuole scrivere un'applicazione che aggiunge un avviso di copyright su ogni fotogramma video e scrive i dati in un altro flusso per l'archiviazione, ma l'applicazione non comprende alcun formato di dati tranne il flusso video. Per il flusso video, si crea un esempio collegato alla superficie DirectDraw desiderata. È quindi possibile creare un flusso di output chiamando il metodo [**IDirectDrawMediaStream::CreateSample**](/previous-versions/windows/desktop/api/ddstream/nf-ddstream-idirectdrawmediastream-createsample) con tale puntatore alla stessa superficie oppure [**IMediaStream::CreateSharedSample**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imediastream-createsharedsample). In entrambi i casi, i flussi di input e di output condividono l'area DirectDraw. Poiché si comprende il formato video, è possibile accedere a questa superficie in base alle esigenze.

Per recuperare gli altri puntatori al flusso di origine (audio e URL), enumerare il flusso del contenitore di origine e recuperare i puntatori ai flussi nonvideo. A ognuno di questi flussi di origine è associato un flusso di output nel contenitore del flusso di output. Recuperare questi puntatori di output chiamando il metodo [**IMultiMediaStream::GetMediaStream**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imultimediastream-getmediastream) nel contenitore di output con ognuno dei puntatori del flusso di origine. Questo processo è descritto nella seguente procedura.

1.  Chiamare [**IMultiMediaStream::EnumMediaStreams**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imultimediastream-enummediastreams) per recuperare un puntatore a un flusso di origine. Assicurarsi che non sia il flusso video, perché l'applicazione ne comprende già il formato.
2.  Chiamare [**IMultiMediaStream::GetMediaStream**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imultimediastream-getmediastream) sul flusso del contenitore di output con il puntatore del passaggio 1. Verrà restituito un puntatore al flusso di output desiderato.
3.  Chiamare [**AllocateSample**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imediastream-allocatesample) nel flusso di origine.
4.  Chiamare [**CreateSharedSample nel**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imediastream-createsharedsample) flusso di output.
5.  Chiamare [**Update**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-istreamsample-update) nel flusso di origine per leggere i dati.
6.  Chiamare [**Update**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-istreamsample-update) nel flusso di output per scrivere i dati.

Ripetere questi passaggi per ogni flusso il cui formato non è supportato. Al termine dell'aggiornamento di entrambi gli esempi, il flusso di output include tutti i dati del flusso di origine e l'operazione è stata completata.

 

 



