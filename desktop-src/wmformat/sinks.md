---
title: Sink
description: Sink
ms.assetid: 6781a326-a30a-4d4d-96db-332d0f681a31
keywords:
- Windows MEDIA Format SDK, sink
- Windows Media Format SDK, sink di file
- Advanced Systems Format (ASF), sink
- ASF (Advanced Systems Format), sink
- Advanced Systems Format (ASF), sink di file
- ASF (Advanced Systems Format), sink di file
- Windows MEDIA Format SDK, sink di rete
- Windows MEDIA Format SDK, sink push
- Advanced Systems Format (ASF), sink di rete
- ASF (Advanced Systems Format),sink di rete
- Advanced Systems Format (ASF), sink push
- ASF (Advanced Systems Format), sink push
- sink, informazioni
- sink di file, informazioni
- sink di rete
- sink push
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb72479a231c3db508efcea7db54528c0b1bf9635afba8b842a4c23add0456cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807901"
---
# <a name="sinks"></a>Sink

L'oggetto writer di Windows Media Format SDK recapita il contenuto elaborato ai sink. Ogni sink è un oggetto che recapita i dati. Il punto di recapito dipende dal tipo di sink. Esistono tre tipi di sink: sink di file, sink di rete e sink push.

## <a name="file-sinks"></a>Sink di file

I sink di file scrivono contenuto ASF in un file in un'unità locale o di rete. Quando si usa l'oggetto writer per scrivere un file senza aggiungere in modo esplicito un sink di file, il writer ne creerà uno usando il nome passato a [**IWMWriter::SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename). È possibile assegnare più sink di file a un oggetto writer per scrivere il contenuto in più file contemporaneamente.

Usando un sink di file, è possibile controllare molti aspetti del file. Le funzionalità seguenti sono disponibili tramite un sink di file.

-   Monitoraggio delle statistiche dei file. È possibile monitorare le dimensioni e la durata del file durante la creazione.
-   Creazione parziale del file di contenuto. I sink di file possono essere configurati per iniziare a scrivere contenuto in un momento specifico e terminare la scrittura in un momento specifico. In questo modo è possibile creare più file contenenti sezioni diverse dello stesso contenuto nello stesso passaggio di scrittura.

## <a name="network-sinks"></a>Sink di rete

I sink di rete tras broadcast del contenuto a un indirizzo di rete. I client di lettura possono connettersi all'indirizzo per ricevere la trasmissione.

## <a name="push-sinks"></a>Sink di push

I sink di push recapitare il contenuto dal writer a un server che esegue Servizi Windows Media. I sink push vengono in genere usati negli scenari in cui un computer codifica il contenuto live e lo recapita a uno o più server per un'ampia distribuzione. L'uso di un sink push consente di dedicare i computer ad attività specifiche, risparmiando larghezza di banda ed potenza di elaborazione in ogni server.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Funzionalità di scrittura di file**](file-writing-features.md)
</dt> <dt>

[**Uso dei sink del writer**](working-with-writer-sinks.md)
</dt> </dl>

 

 




