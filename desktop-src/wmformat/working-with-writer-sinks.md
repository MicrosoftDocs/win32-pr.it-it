---
title: Uso dei sink del writer
description: Uso dei sink del writer
ms.assetid: 1ad28684-47d2-4ddb-bf18-22310f0392a0
keywords:
- Advanced Systems Format (ASF), sink writer
- ASF (Advanced Systems Format),sink writer
- Advanced Systems Format (ASF), sink
- ASF (Advanced Systems Format), sink
- sink, sink writer
- sink writer, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 407e5bf2e87bfbf3084d19f75170a12be693d804d4d902f919096dca5aeab057
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118194868"
---
# <a name="working-with-writer-sinks"></a>Uso dei sink del writer

L'oggetto writer dell'SDK Windows Media Format elabora i dati multimediali di input in un flusso di bit. Tuttavia, l'oggetto writer non recapita il flusso di bit alla destinazione finale (a un file o a un percorso di rete). Per scrivere il contenuto asf in un formato utilizzabile, è necessario usare i sink del writer.

L'oggetto writer supporta tre tipi di sink: sink di file, sink di rete e sink push. Un sink di file scrive il contenuto di ASF in un file ASF su disco. Un sink di rete trasmette il contenuto asf da un indirizzo di rete. Un sink push recapita i dati a un server che esegue Servizi Windows Media in modo che il server possa rendere disponibile il contenuto ai destinatari. È anche possibile creare sink personalizzati per distribuire i dati ASF nel modo richiesto dall'applicazione. Per informazioni sui sink di rete e i sink push, vedere [Invio di dati ASF in una rete.](sending-asf-data-over-a-network.md) Nella parte restante di questa sezione vengono illustrati i sink del writer.

È possibile configurare uno o più sink per ogni istanza del writer in uso. Ogni sink gestisce una sola destinazione. Ad esempio, se si desidera scrivere tre file contemporaneamente, è necessario creare e configurare un sink di file separato per ognuno.

Nelle sezioni seguenti viene descritto l'utilizzo dei sink del writer.



| Sezione                                                                      | Descrizione                                                                      |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [Aggiunta di sink al writer](adding-sinks-to-the-writer.md)                 | Viene descritto come aggiungere sink al writer.                                        |
| [Enumerazione di sink](enumerating-sinks.md)                                   | Viene descritto come enumerare i sink aggiunti al writer.         |
| [Recupero di messaggi di errore da un sink](getting-error-messages-from-a-sink.md) | Viene descritto come configurare i sink per recapitare messaggi di stato all'applicazione. |
| [Uso di file sink](using-file-sinks.md)                                     | Viene descritto come usare un sink di file writer per creare un file ASF su disco.           |
| [Uso di sink personalizzati](using-custom-sinks.md)                                 | Viene descritto come creare e usare sink personalizzati per distribuire dati ASF.       |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia IWMWriterAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[**Interfaccia IWMWriterSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink)
</dt> <dt>

[**Scrittura di file ASF**](writing-asf-files.md)
</dt> </dl>

 

 




