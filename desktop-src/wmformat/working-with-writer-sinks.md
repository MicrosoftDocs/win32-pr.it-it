---
title: Utilizzo dei sink di writer
description: Utilizzo dei sink di writer
ms.assetid: 1ad28684-47d2-4ddb-bf18-22310f0392a0
keywords:
- ASF (Advanced Systems Format), sink writer
- ASF (formato avanzato dei sistemi), sink writer
- ASF (Advanced Systems Format), sink
- ASF (formato avanzato dei sistemi), sink
- sink, sink di writer
- sink writer, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d5b690d9e1ab25d15f7c1e8612bf20e32f87c81
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723367"
---
# <a name="working-with-writer-sinks"></a>Utilizzo dei sink di writer

L'oggetto writer di Windows Media Format SDK elabora i dati multimediali di input in un flusso di bit. Tuttavia, l'oggetto writer non distribuisce il flusso di bit alla destinazione finale, ovvero in un file o in un percorso di rete. Per scrivere il contenuto ASF in un formato utilizzabile, è necessario utilizzare i sink del writer.

L'oggetto Writer supporta tre tipi di sink: sink di file, sink di rete e sink di push. Un sink di file scrive il contenuto ASF in un file ASF su disco. Un sink di rete trasmette contenuto ASF da un indirizzo di rete. Un sink di push recapita i dati a un server che esegue Servizi Windows Media, in modo che il server possa rendere il contenuto disponibile ai destinatari desiderati. È anche possibile creare sink personalizzati per distribuire i dati ASF nel modo desiderato per l'applicazione. Per informazioni sui sink di rete e sui sink di push, vedere [invio di dati ASF in una rete](sending-asf-data-over-a-network.md). Nella parte restante di questa sezione vengono illustrati i sink di writer.

È possibile configurare uno o più sink per ogni istanza del writer usato. Ogni sink gestisce solo una singola destinazione. Se ad esempio si desidera scrivere tre file in una sola volta, è necessario creare e configurare un sink di file separato per ciascuno di essi.

Le sezioni seguenti descrivono l'uso di sink di writer.



| Sezione                                                                      | Descrizione                                                                      |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [Aggiunta di sink al writer](adding-sinks-to-the-writer.md)                 | Viene descritto come aggiungere sink al writer.                                        |
| [Enumerazione dei sink](enumerating-sinks.md)                                   | Viene descritto come enumerare i sink aggiunti al writer.         |
| [Recupero di messaggi di errore da un sink](getting-error-messages-from-a-sink.md) | Viene descritto come configurare i sink per inviare messaggi di stato all'applicazione. |
| [Uso di file sink](using-file-sinks.md)                                     | Viene descritto come utilizzare un sink di file del writer per creare un file ASF su disco.           |
| [Uso di sink personalizzati](using-custom-sinks.md)                                 | Viene descritto come creare e utilizzare i sink personalizzati per fornire dati ASF.       |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia IWMWriterAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[**Interfaccia IWMWriterSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink)
</dt> <dt>

[**Scrittura di file ASF**](writing-asf-files.md)
</dt> </dl>

 

 




