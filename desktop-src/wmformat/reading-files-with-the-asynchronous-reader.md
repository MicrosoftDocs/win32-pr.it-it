---
title: Lettura di file con il lettore asincrono
description: Lettura di file con il lettore asincrono
ms.assetid: 3cc72f8d-bf1f-416d-bc90-21dfb92a55aa
keywords:
- Windows MEDIA Format SDK, lettura di file
- Windows Media Format SDK, lettori asincroni
- Advanced Systems Format (ASF), lettori asincroni
- ASF (Advanced Systems Format),lettori asincroni
- Advanced Systems Format (ASF), lettura di file
- ASF (Advanced Systems Format), lettura di file
- lettori asincroni,interfaccia IWMReaderCallback
- IWMReaderCallback, lettori asincroni
- lettori asincroni, lettura di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bea24a8f09cff8fe3e4a1f1cfb383f5569e968200bbbe6f25f2c8f225b3c18f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119084508"
---
# <a name="reading-files-with-the-asynchronous-reader"></a>Lettura di file con il lettore asincrono

Il lettore asincrono legge il contenuto dai file ASF usando più thread e chiamate asincrone. Le funzionalità supportate dal lettore asincrono lo rendono particolarmente adatto per le applicazioni che eseguono il rendering del contenuto agli utenti finali.

La funzionalità più semplice dell'oggetto reader può essere suddivisa nei passaggi seguenti. In questi passaggi "l'applicazione" si riferisce al programma scritto usando Windows Media Format SDK.

1.  L'applicazione implementa [**l'interfaccia IWMReaderCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback) per gestire i messaggi dal lettore. Sono inclusi due metodi di callback: **OnStatus**, che riceve i messaggi relativi allo stato dei vari aspetti del lettore e **OnSample,** che riceve esempi non compressi dal lettore.
2.  L'applicazione passa al lettore il nome di un file da leggere. Quando il lettore apre il file, assegna un numero di output a ogni flusso. Se il file usa l'esclusione reciproca, il lettore assegna un singolo output per tutti i flussi che si escludono a vicenda.
3.  L'applicazione ottiene informazioni sulla configurazione dei vari output dal lettore. Le informazioni raccolte consentiranno all'applicazione di eseguire correttamente il rendering degli esempi multimediali.
4.  L'applicazione indica al lettore di iniziare a leggere i dati dal file. Il lettore inizia a recapitare campioni non compressi al callback **OnSample** uno alla volta in buffer di cui è stato eseguito il wrapping in oggetti buffer. Gli esempi forniti dal lettore sono nell'ordine del tempo di presentazione. Il lettore continuerà a fornire esempi fino a quando non viene arrestato dall'applicazione o fino a quando non viene raggiunta la fine del file.
5.  L'applicazione è responsabile del rendering dei dati dopo che sono stati recapitati dal lettore. L Windows Media Format SDK non fornisce routine di rendering. In genere, le applicazioni usano altri SDK per eseguire il rendering dei dati, ad esempio Microsoft DirectX® SDK o le funzioni multimediali di Microsoft Windows Platform SDK.
6.  Al termine della lettura, l'applicazione indica al lettore di chiudere il file.

Questi passaggi sono illustrati, tra gli altri, nell'applicazione di esempio AudioPlayer. Per altre informazioni, vedere [Applicazioni di esempio.](sample-applications.md)

Il lettore supporta anche funzionalità più avanzate. Il lettore consente di eseguire le operazioni seguenti:

-   Sospendere la riproduzione di un file.
-   Recuperare le statistiche sulle prestazioni del lettore.
-   Controllare la selezione del flusso per i flussi che si escludono a vicenda.
-   Allocare manualmente i buffer per l'output.
-   Specificare il proprio orologio.
-   Recuperare lo stato delle operazioni sui file (memorizzazione nel buffer, download o salvataggio).
-   Aprire un file usando l'interfaccia COM standard, **IStream.**
-   Cercare punti specifici in un file ASF.
-   Legge i dati del profilo dall'intestazione del file.

Nelle sezioni seguenti viene descritto in dettaglio l'utilizzo dell'oggetto reader.

-   [Per implementare i messaggi del lettore nel callback OnStatus](to-implement-reader-messages-in-the-onstatus-callback.md)
-   [Per implementare il callback OnSample](to-implement-the-onsample-callback.md)
-   [Per creare un lettore e aprire un file](to-create-a-reader-and-open-a-file.md)
-   [Per recuperare esempi multimediali con il lettore asincrono](to-retrieve-media-samples-with-the-asynchronous-reader.md)
-   [Per eseguire la ricerca in base all'ora usando il lettore asincrono](to-seek-by-time-using-the-asynchronous-reader.md)
-   [Per cercare in base al numero di fotogramma usando il lettore asincrono](to-seek-by-frame-number-using-the-asynchronous-reader.md)
-   [Per eseguire la ricerca in base al codice temporale SMPTE usando il lettore asincrono](to-seek-by-smpte-time-code-using-the-asynchronous-reader.md)
-   [Per cercare marcatori](to-seek-to-markers.md)
-   [Per sospendere o arrestare la riproduzione](to-pause-or-stop-playback.md)
-   [Per ottenere statistiche sulle prestazioni del lettore](to-get-reader-performance-statistics.md)
-   [Per usare la selezione manuale del flusso](to-use-manual-stream-selection.md)
-   [Per distribuire esempi compressi con il lettore asincrono](to-deliver-compressed-samples-with-the-asynchronous-reader.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Lettura di file ASF**](reading-asf-files.md)
</dt> <dt>

[**Oggetto Lettore**](reader-object.md)
</dt> </dl>

 

 




