---
title: Lettura di file con il lettore asincrono
description: Lettura di file con il lettore asincrono
ms.assetid: 3cc72f8d-bf1f-416d-bc90-21dfb92a55aa
keywords:
- Windows Media Format SDK, lettura di file
- Windows Media Format SDK, Reader asincroni
- ASF (Advanced Systems Format), Reader asincroni
- ASF (formato avanzato dei sistemi), Reader asincroni
- Formato di sistemi avanzati (ASF), lettura di file
- ASF (Advanced Systems Format), lettura di file
- Reader asincroni, interfaccia IWMReaderCallback
- IWMReaderCallback, lettori asincroni
- Reader asincroni, lettura di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0807c0701dd596f943010ad613b08ef9fe2c415c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104398555"
---
# <a name="reading-files-with-the-asynchronous-reader"></a>Lettura di file con il lettore asincrono

Il lettore asincrono legge il contenuto dai file ASF usando più thread e chiamate asincrone. Le funzionalità supportate dal reader asincrono lo rendono particolarmente adatto per le applicazioni che eseguono il rendering del contenuto agli utenti finali.

La maggior parte delle funzionalità di base dell'oggetto Reader può essere suddivisa nei passaggi seguenti. In questa procedura "l'applicazione" si riferisce al programma scritto usando Windows Media Format SDK.

1.  L'applicazione implementa l'interfaccia [**IWMReaderCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback) per gestire i messaggi dal reader. Sono inclusi due metodi di callback: **OnStatus**, che riceve i messaggi relativi allo stato di diversi aspetti del Reader e **OnSample**, che riceve campioni non compressi dal reader.
2.  L'applicazione passa al lettore il nome di un file da leggere. Quando il lettore apre il file, assegna un numero di output a ogni flusso. Se il file usa l'esclusione reciproca, il lettore assegna un singolo output per tutti i flussi che si escludono a vicenda.
3.  L'applicazione ottiene informazioni sulla configurazione dei vari output dal reader. Le informazioni raccolte consentiranno all'applicazione di eseguire correttamente il rendering degli esempi di supporti.
4.  L'applicazione indica al lettore di iniziare a leggere i dati dal file. Il lettore inizia a inviare campioni non compressi al callback **OnSample** uno alla volta nei buffer racchiusi tra oggetti buffer. Gli esempi recapitati dal reader sono ordinati in base alla fase di presentazione. Il lettore continuerà a consegnare gli esempi fino a quando non verrà interrotto dall'applicazione o fino al raggiungimento della fine del file.
5.  L'applicazione è responsabile del rendering dei dati dopo che sono stati recapitati dal lettore. Windows Media Format SDK non fornisce routine di rendering. In genere, le applicazioni utilizzeranno altri SDK per eseguire il rendering dei dati, ad esempio Microsoft DirectX® SDK, o le funzioni multimediali di Microsoft Windows Platform SDK.
6.  Al termine della lettura, l'applicazione indica al lettore di chiudere il file.

Questi passaggi sono illustrati nell'applicazione di esempio AudioPlayer, tra gli altri. Per altre informazioni, vedere [applicazioni di esempio](sample-applications.md).

Il lettore supporta inoltre funzionalità più avanzate. Il lettore consente di eseguire le operazioni seguenti:

-   Sospendere la riproduzione di un file.
-   Recuperare le statistiche sulle prestazioni del lettore.
-   Controllare la selezione del flusso per i flussi che si escludono a vicenda.
-   Allocare manualmente i buffer per l'output.
-   Fornire il proprio clock.
-   Recuperare lo stato delle operazioni su file (memorizzazione nel buffer, download o salvataggio).
-   Aprire un file utilizzando l'interfaccia COM standard, **IStream**.
-   Consente di cercare punti specifici in un file ASF.
-   Leggere i dati di profilo dall'intestazione del file.

Nelle sezioni seguenti viene descritto in dettaglio l'utilizzo dell'oggetto Reader.

-   [Per implementare i messaggi del lettore nel callback OnStatus](to-implement-reader-messages-in-the-onstatus-callback.md)
-   [Per implementare il callback OnSample](to-implement-the-onsample-callback.md)
-   [Per creare un reader e aprire un file](to-create-a-reader-and-open-a-file.md)
-   [Per recuperare esempi di supporti con il Reader asincrono](to-retrieve-media-samples-with-the-asynchronous-reader.md)
-   [Per eseguire ricerche in base al tempo tramite il Reader asincrono](to-seek-by-time-using-the-asynchronous-reader.md)
-   [Per eseguire la ricerca in base al numero di frame utilizzando il Reader asincrono](to-seek-by-frame-number-using-the-asynchronous-reader.md)
-   [Per eseguire la ricerca in base al codice ora SMPTE usando il Reader asincrono](to-seek-by-smpte-time-code-using-the-asynchronous-reader.md)
-   [Per cercare i marcatori](to-seek-to-markers.md)
-   [Per sospendere o arrestare la riproduzione](to-pause-or-stop-playback.md)
-   [Per ottenere le statistiche sulle prestazioni del lettore](to-get-reader-performance-statistics.md)
-   [Per usare la selezione del flusso manuale](to-use-manual-stream-selection.md)
-   [Per recapitare esempi compressi con il lettore asincrono](to-deliver-compressed-samples-with-the-asynchronous-reader.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Lettura di file ASF**](reading-asf-files.md)
</dt> <dt>

[**Oggetto Lettore**](reader-object.md)
</dt> </dl>

 

 




