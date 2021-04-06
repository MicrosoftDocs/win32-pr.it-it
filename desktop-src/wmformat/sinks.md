---
title: Sink
description: Sink
ms.assetid: 6781a326-a30a-4d4d-96db-332d0f681a31
keywords:
- Windows Media Format SDK, sink
- Windows Media Format SDK, sink di file
- ASF (Advanced Systems Format), sink
- ASF (formato avanzato dei sistemi), sink
- ASF (Advanced Systems Format), sink di file
- ASF (formato avanzato dei sistemi), sink di file
- Windows Media Format SDK, sink di rete
- Windows Media Format SDK, sink di push
- ASF (Advanced Systems Format), sink di rete
- ASF (formato avanzato dei sistemi), sink di rete
- ASF (Advanced Systems Format), sink di push
- ASF (formato avanzato dei sistemi), sink di push
- sink, informazioni
- sink di file, informazioni
- sink di rete
- sink di push
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a62548f159172f58d4f52b0289c5adbfef02f55
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104046332"
---
# <a name="sinks"></a>Sink

L'oggetto writer di Windows Media Format SDK recapita contenuto elaborato a sink. Ogni sink è un oggetto che recapita i dati. Il punto di distribuzione dipende dal tipo di sink. Sono disponibili tre tipi di sink: sink di file, sink di rete e sink di push.

## <a name="file-sinks"></a>Sink di file

I sink di file scrivono contenuto ASF in un file in un'unità locale o di rete. Quando si usa l'oggetto writer per scrivere un file senza aggiungere esplicitamente un sink di file, il writer ne creerà uno usando il nome passato a [**IWMWriter:: SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename). È possibile assegnare più sink di file a un oggetto writer per scrivere il contenuto in più file contemporaneamente.

Utilizzando un sink di file, è possibile controllare molti aspetti del file. Le funzionalità seguenti sono disponibili tramite un sink di file.

-   Monitoraggio delle statistiche di file. È possibile monitorare le dimensioni e la durata del file durante la creazione.
-   Creazione di file di contenuto parziale. I sink di file possono essere configurati per iniziare a scrivere contenuto in un momento specifico e terminare la scrittura in un momento specifico. In questo modo è possibile creare più file contenenti sezioni diverse dello stesso contenuto nello stesso passaggio di scrittura.

## <a name="network-sinks"></a>Sink di rete

I sink di rete trasmettono contenuto a un indirizzo di rete. La lettura dei client può connettersi all'indirizzo per ricevere la trasmissione.

## <a name="push-sinks"></a>Sink di push

I sink di push recapitano il contenuto dal writer a un server che esegue Servizi Windows Media. I sink di push vengono in genere utilizzati negli scenari in cui un computer codifica contenuto Live e lo recapita a uno o più server per la distribuzione estesa. L'uso di un sink di push consente di dedicare i computer a attività specifiche, risparmiando la larghezza di banda e la potenza di elaborazione in ogni server.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Funzionalità di scrittura di file**](file-writing-features.md)
</dt> <dt>

[**Utilizzo dei sink di writer**](working-with-writer-sinks.md)
</dt> </dl>

 

 




