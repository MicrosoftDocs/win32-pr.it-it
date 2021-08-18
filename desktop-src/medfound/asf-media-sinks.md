---
description: Il sink multimediale ASF è il componente finale nella pipeline di codifica che consente a un'applicazione di scrivere un file ASF.
ms.assetid: 65bb8822-5eb0-46a3-ab9e-c55ae466e982
title: Sink di supporti ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50af8530b1c2b8d9131243cafa67e841289cbbe0691cfcb499b57df68b60b141
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118744212"
---
# <a name="asf-media-sinks"></a>Sink di supporti ASF

Il sink multimediale ASF è il componente finale nella pipeline di codifica che consente a un'applicazione di scrivere un file ASF.

Media Foundation fornisce due tipi di sink multimediali ASF:

-   *Il sink di file ASF* viene usato per archiviare i dati multimediali asf in un file.
-   *Il sink di streaming ASF* viene usato per scrivere contenuto ASF in un flusso di byte che può essere trasmesso in rete.

I sink multimediali ASF contengono uno o più sink di flusso, che rappresenta i dati da scrivere per ogni flusso nel file ASF di output. Per le applicazioni di codifica eseguite in Windows Vista, è necessario configurare manualmente la topologia di codifica creando e configurando il sink di supporto ASF e quindi aggiungendolo alla topologia. In Windows 7, se si usano gli oggetti di transcodifica rapida per creare la topologia, il sink multimediale non è stato creato direttamente e l'applicazione non chiama metodi sul sink di supporto o sui sink di flusso. Gli oggetti di transcodifica rapida creano un'istanza dei sink multimediali necessari e lo aggiungono alla topologia prima di restituire un riferimento all'applicazione chiamante. Tuttavia, per gli oggetti di transcodifica rapida, esistono alcune restrizioni che si applicano a seconda del tipo di codifica.

-   [Modello a oggetti sink multimediale ASF](#asf-media-sink-object-model)
-   [ASF File Sink](#asf-file-sink)
-   [Argomenti correlati](#related-topics)

## <a name="asf-media-sink-object-model"></a>Modello a oggetti sink multimediale ASF

I sink multimediali ASF implementano [**l'interfaccia IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) ed espongono le interfacce seguenti. Un'applicazione può ottenere un riferimento a queste interfacce chiamando [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sul sink multimediale ASF che usa per generare esempi di output.



| Interfaccia                                                  | Descrizione                                                                                                                                                                                            |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)                       | Obbligatorio per tutti i sink multimediali.                                                                                                                                                                          |
| [**IMFFinalizableMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imffinalizablemediasink) | Implementato dal sink di file ASF che scrive il contenuto multimediale generato in un file. È possibile usare i metodi in questa interfaccia per scaricare i dati e aggiornare l'oggetto intestazione ASF del file di output finale. |
| [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)             | Riceve le notifiche di modifica dello stato dall'orologio della presentazione.                                                                                                                                       |
| [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo)             | L'oggetto ContentInfo asf è un oggetto a livello WMContainer che archivia principalmente le informazioni sull'oggetto intestazione ASF. Viene usato per creare sink multimediali ASF.                                                     |
| [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata)                         | Usato per descrivere i metadati per il file ASF.                                                                                                                                                        |
| [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider)         | Recupera una raccolta di metadati, per un'intera presentazione o per un flusso nella presentazione.                                                                                          |



 

## <a name="asf-file-sink"></a>ASF File Sink

Il sink di file ASF è un'implementazione di [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) fornita da Media Foundation che un'applicazione può usare per archiviare i dati multimediali asf in un file.

È necessario creare, configurare e chiamare metodi sul sink di file o su uno dei relativi sink di flusso se si usano gli oggetti del livello pipeline per scrivere un nuovo file ASF. Dopo aver configurato il sink di file, è possibile aggiungerlo alla pipeline di codifica.

Ecco i passaggi generali per l'uso del sink di file ASF:

1.  Creare il sink di file in-process o out-of-process.
2.  Configurare il sink di file con tutti i flussi, le proprietà di codifica e le informazioni sui metadati.
3.  Associare il sink di file al nodo della topologia di output enumerando i sink di flusso o tenendo traccia dei numeri di flusso con nel sink.

Gli argomenti seguenti contengono informazioni dettagliate sull'uso del sink di file ASF:

-   [Creazione del sink di file ASF](creating-the-asf-file-sink.md)
-   [Aggiunta di informazioni sul flusso al sink di file ASF](adding-stream-information-to-the-asf-file-sink.md)
-   [Impostazione delle proprietà nel sink di file](setting-properties-in-the-file-sink.md)
-   [Aggiunta di metadati al sink di file](adding-metadata-to-the-file-sink.md)
-   [Modello di buffer bucket persa](the-leaky-bucket-buffer-model.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Componenti ASF del livello pipeline](pipeline-layer-asf-components.md)
</dt> <dt>

[Supporto di ASF in Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 
