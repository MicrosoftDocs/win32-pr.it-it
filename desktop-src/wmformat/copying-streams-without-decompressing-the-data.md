---
title: Copia Flussi senza decomprimere i dati
description: Copia Flussi senza decomprimere i dati
ms.assetid: c268ce44-a09d-4304-bc39-8b6657da2bdb
keywords:
- Windows MEDIA Format SDK, copia di flussi
- Advanced Systems Format (ASF), copia di flussi
- ASF (Advanced Systems Format), copia di flussi
- flussi, copia senza decompressione dei dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2387861c25ad565298fb2731300f6da8ccc00c26c5f7c82c36fede1bb7f62f9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931561"
---
# <a name="copying-streams-without-decompressing-the-data"></a>Copia Flussi senza decomprimere i dati

Il modo più semplice e più comune per copiare un flusso da un file a un altro è recuperare gli esempi nello stato compresso e quindi scriverli nel nuovo file senza decomprimerli e ricomprimerli. Gli esempi ottenuti da un file nello stato compresso sono detti esempi di flusso, perché non vengono modificati dalla relativa rappresentazione nel flusso. È consigliabile usare sempre gli esempi di flusso per copiare i flussi, perché la decompressione e la ricompressione dei dati multimediali digitali peggiorano la qualità. Se è necessario copiare un flusso da dati decompressi, vedere Copia di Flussi [usando esempi decompressi](copying-streams-using-decompressed-samples.md).

È possibile concatenare due o più flussi in un singolo flusso usando esempi compressi, ma solo se le velocità in bit sono identiche. Il processo è essenzialmente lo stesso dei passaggi descritti di seguito, ad eccezione del fatto che è necessario leggere più file originali per ottenere tutto il contenuto necessario. Tuttavia, è possibile scrivere esempi compressi da più file in un unico flusso solo se le strutture **WM \_ MEDIA \_ TYPE** (inclusi tutti i membri della struttura **pbFormat)** di tutti i flussi compressi sono identiche. Per combinare dati da più flussi che non hanno lo stesso formato, è necessario decomprimere il contenuto e ricomprimerlo nel flusso di destinazione. Inoltre, quando si combinano dati da due o più flussi in un singolo flusso, è necessario aggiungere i valori della finestra del buffer per tutti i flussi insieme per ottenere la finestra del buffer per il nuovo flusso. Ciò è dovuto al fatto che non è possibile determinare la quantità di buffer utilizzata alla fine di un flusso e all'inizio di un altro.

È possibile recuperare gli esempi di flusso con il lettore asincrono [**usando IWMReaderAdvanced::SetReceiveStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setreceivestreamsamples). Gli esempi di flusso vengono recapitati [**a IWMReaderCallbackAdvanced::OnStreamSample,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample)non a [**IWMReaderCallback::OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample). Se si legge un file e si recuperano alcuni flussi compressi e alcuni decompressi, è necessario implementare entrambi i metodi di callback.

Il lettore sincrono offre maggiore flessibilità per il recupero degli esempi. È possibile passare liberamente da esempi compressi a campioni decompressi durante la riproduzione [**usando IWMSyncReader::SetReadStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setreadstreamsamples).

Per copiare un intero flusso da un file ASF in un nuovo file ASF, seguire questa procedura. Questi passaggi usano il lettore sincrono perché è molto più semplice da usare per questo tipo di operazione.

1.  Creare un oggetto lettore sincrono chiamando la [**funzione WMCreateSyncReader.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader)
2.  Aprire un file nel lettore con una chiamata a [**IWMSyncReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-open).
3.  Ottenere un puntatore [**all'interfaccia IWMProfile**](iwmprofile.md) dell'oggetto lettore sincrono chiamando **IWMSyncReader::QueryInterface**.
4.  Recuperare le proprietà del flusso desiderato chiamando [**IWMProfile::GetStreamByNumber**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber). Verrà recuperato un puntatore [**all'interfaccia IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig) dell'oggetto di configurazione del flusso per il flusso desiderato.
5.  Ottenere una copia della [**struttura WM \_ MEDIA \_ TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) per il flusso. Effettuare due chiamate a [**IWMMediaProps::GetMediaType:**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype)la prima per ottenere le dimensioni della struttura, la seconda per ottenere la struttura stessa.
6.  Creare un oggetto di gestione del profilo chiamando la [**funzione WMCreateProfileManager.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager)
7.  Chiamare [**IWMProfileManager::CreateEmptyProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile) per creare un nuovo profilo o aprire un profilo esistente a cui si vuole aggiungere il flusso. Chiamare [**IWMProfile::AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream) nel nuovo profilo per aggiungere il flusso dal file esistente. Quando si aggiunge il flusso, usare il **puntatore IWMStreamConfig** ottenuto nel passaggio 4.
8.  Creare un oggetto writer con una chiamata alla [**funzione WMCreateWriter.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) Impostare il profilo appena creato come profilo attivo nel writer chiamando [**IWMWriter::SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile). Creare un file per l'output chiamando [**IWMWriter::SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename).
9.  Per ogni input associato al flusso o ai flussi da copiare, chiamare [**IWMWriter::SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops), passando **NULL** per l'interfaccia [**IWMInputMediaProps.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) Ciò informa l'oggetto writer che non è necessario convalidare i dati che si stanno passando. È necessario eseguire questa chiamata prima di **chiamare BeginWriting** (passaggio 14), in caso contrario un oggetto di lettura potrebbe non essere in grado di decodificare il contenuto.
10. Impostare il lettore sincrono per fornire esempi di flussi compressi per il flusso selezionato chiamando [**IWMSyncReader::SetReadStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setreadstreamsamples) con il *parametro fCompressed* impostato su True.
11. Ottenere informazioni sul codec per ogni flusso copiato e aggiungere le informazioni sul codec all'intestazione prima della scrittura. Per ottenere le informazioni sul codec, chiamare [**IWMHeaderInfo2::GetCodecInfoCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfocount) e [**IWMHeaderInfo2::GetCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfo) per enumerare i codec associati al file nel lettore. Selezionare le informazioni sul codec che corrispondono alla configurazione del flusso. Impostare quindi le informazioni sul codec nel writer chiamando [**IWMHeaderInfo3::AddCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addcodecinfo), passando le informazioni ottenute dal lettore.
12. Ottenere un puntatore [**all'interfaccia IWMWriterAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced) chiamando **IWMWriter::QueryInterface**.
13. Impostare il writer sulla modalità di scrittura chiamando [**IWMWriter::BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).
14. Effettuare chiamate ripetute a [**IWMSyncReader::GetNextSample,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample)specificando il numero di flusso desiderato. Quando vengono ricevuti esempi, passarli al writer con chiamate a [**IWMWriterAdvanced::WriteStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-writestreamsample). Per i flussi video, è necessario controllare i flag (se presenti) impostati dal writer in ogni chiamata a **GetNextSample**. Se WM SF CLEANPOINT è impostato, è necessario impostarlo anche \_ \_ nella chiamata a **WriteStreamSample**.
15. Al termine della lettura, chiamare [**IWMWriter::EndWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-endwriting). Il flusso deve essere trasferito.

> [!Note]  
> I flussi di immagini non possono essere copiati da un file a un altro usando esempi di flusso. Per copiare i dati del flusso di immagini, recuperare gli esempi non compressi e quindi elaborarli tramite il writer come si farebbe normalmente.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Copia di dati da un file a un altro**](copying-data-from-one-file-to-another.md)
</dt> <dt>

[**Copia Flussi usando esempi decompressi**](copying-streams-using-decompressed-samples.md)
</dt> </dl>

 

 




