---
description: Il sink multimediale ASF è il componente finale della pipeline di codifica che consente a un'applicazione di scrivere un file ASF.
ms.assetid: 65bb8822-5eb0-46a3-ab9e-c55ae466e982
title: Sink di supporti ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d6bcd3e6b91403185342607e8c4374eb32069c7
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320692"
---
# <a name="asf-media-sinks"></a>Sink di supporti ASF

Il sink multimediale ASF è il componente finale della pipeline di codifica che consente a un'applicazione di scrivere un file ASF.

Media Foundation fornisce due tipi di sink di supporti ASF:

-   Il *sink di file ASF* viene usato per archiviare i dati del supporto ASF in un file.
-   Il *sink di streaming ASF* viene usato per scrivere contenuto ASF in un flusso di byte che può essere trasmesso attraverso la rete.

I sink multimediali ASF contengono uno o più sink di flusso, che rappresentano i dati da scrivere per ogni flusso nel file ASF di output. Per la codifica di applicazioni eseguite in Windows Vista, è necessario configurare manualmente la topologia di codifica tramite la creazione e la configurazione del sink multimediale ASF e quindi l'aggiunta alla topologia. In Windows 7, se si utilizzano gli oggetti transcode veloci per creare la topologia, non è necessario creare direttamente il sink multimediale e l'applicazione non chiama alcun metodo sul sink multimediale o su uno dei sink di flusso. Gli oggetti Fast transcode creano un'istanza dei sink multimediali necessari e li aggiungono alla topologia prima di restituire un riferimento all'applicazione chiamante. Per gli oggetti di transcodifica rapida, tuttavia, esistono alcune restrizioni che si applicano a seconda del tipo di codifica.

-   [Modello a oggetti del sink multimediale ASF](#asf-media-sink-object-model)
-   [Sink di file ASF](#asf-file-sink)
-   [Argomenti correlati](#related-topics)

## <a name="asf-media-sink-object-model"></a>Modello a oggetti del sink multimediale ASF

I sink multimediali ASF implementano l'interfaccia [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) ed espone le interfacce seguenti. Un'applicazione può ottenere un riferimento a queste interfacce chiamando [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sul sink multimediale ASF usato per generare esempi di output.



| Interfaccia                                                  | Descrizione                                                                                                                                                                                            |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)                       | Obbligatorio per tutti i sink di supporto.                                                                                                                                                                          |
| [**IMFFinalizableMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imffinalizablemediasink) | Implementato dal sink di file ASF che scrive il contenuto multimediale generato in un file. È possibile utilizzare i metodi su questa interfaccia per svuotare i dati e aggiornare l'oggetto intestazione ASF del file di output finale. |
| [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)             | Riceve notifiche di modifica dello stato dal clock della presentazione.                                                                                                                                       |
| [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo)             | L'oggetto di un oggetto ContentInfo ASF è un oggetto a livello di WMContainer che archivia principalmente le informazioni sull'oggetto intestazione ASF. Viene utilizzato per creare i sink di supporto ASF.                                                     |
| [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata)                         | Utilizzato per descrivere i metadati per il file ASF.                                                                                                                                                        |
| [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider)         | Recupera una raccolta di metadati per un'intera presentazione o per un flusso nella presentazione.                                                                                          |



 

## <a name="asf-file-sink"></a>Sink di file ASF

Il sink di file ASF è un'implementazione di [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) fornita da Media Foundation che un'applicazione può usare per archiviare i dati del supporto ASF in un file.

È necessario creare, configurare e chiamare metodi sul sink di file o su uno dei relativi sink di flusso se si usano gli oggetti livello pipeline per scrivere un nuovo file ASF. Dopo aver configurato il sink di file, è possibile aggiungerlo alla pipeline di codifica.

Ecco i passaggi generali per l'uso del sink di file ASF:

1.  Creare il sink di file in-process o out-of-process.
2.  Configurare il sink di file con tutti i flussi, le proprietà di codifica e le informazioni sui metadati.
3.  Associare il sink di file al nodo della topologia di output enumerando i sink del flusso o tenendo traccia dei numeri di flusso con nel sink.

Negli argomenti seguenti sono incluse informazioni dettagliate sull'utilizzo del sink di file ASF:

-   [Creazione del sink di file ASF](creating-the-asf-file-sink.md)
-   [Aggiunta di informazioni sul flusso al sink di file ASF](adding-stream-information-to-the-asf-file-sink.md)
-   [Impostazione delle proprietà nel sink di file](setting-properties-in-the-file-sink.md)
-   [Aggiunta di metadati al sink di file](adding-metadata-to-the-file-sink.md)
-   [Modello di buffer di bucket a perdita](the-leaky-bucket-buffer-model.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Componenti ASF a livello pipeline](pipeline-layer-asf-components.md)
</dt> <dt>

[Supporto ASF in Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 
