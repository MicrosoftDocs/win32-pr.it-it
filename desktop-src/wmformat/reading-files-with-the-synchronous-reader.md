---
title: Lettura di file con il lettore sincrono
description: Lettura di file con il lettore sincrono
ms.assetid: 18c6c0cd-478f-4325-b23e-571c33779a96
keywords:
- Windows Media Format SDK, lettura di file
- Windows Media Format SDK, lettori sincroni
- ASF (Advanced Systems Format), lettori sincroni
- ASF (formato avanzato dei sistemi), lettori sincroni
- Formato di sistemi avanzati (ASF), lettura di file
- ASF (Advanced Systems Format), lettura di file
- lettori sincroni, interfaccia IWMReaderCallback
- IWMReaderCallback, lettori sincroni
- lettori sincroni, lettura di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 893a1bd324cdc91968e423f2084bfdba5ef57c8e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104398554"
---
# <a name="reading-files-with-the-synchronous-reader"></a>Lettura di file con il lettore sincrono

È possibile utilizzare il lettore sincrono per leggere un file ASF utilizzando chiamate sincrone anziché i metodi asincroni nell'oggetto Reader. L'utilizzo di chiamate sincrone riduce il numero di thread necessari per la lettura di un file. Il lettore asincrono usa più thread per l'elaborazione dei flussi. Per i file con più flussi, il numero di thread usati può diventare molto grande. Il lettore sincrono utilizza un solo thread.

Il lettore sincrono è stato progettato per soddisfare le esigenze di creazione di contenuti e di applicazioni di modifica di file. È possibile utilizzare il lettore sincrono per altre applicazioni, ma la sua funzionalità è limitata.

Il lettore sincrono può aprire file locali o file in una rete usando il nome del percorso UNC (ad esempio " \\ \\ someshare \\ somedirectory \\ somefile. wmv"). Non è possibile trasmettere file al lettore sincrono o aprire file da un percorso Internet. Il lettore sincrono fornisce inoltre supporto per l'utilizzo dell'interfaccia com **IStream** come origine.

Il lettore sincrono offre maggiore versatilità per il recupero di esempi da un file ASF rispetto al lettore asincrono. Il lettore sincrono può recapitare campioni per numero di flusso e per output. Gli esempi recapitati dal numero di flusso possono essere compressi o decompressi. Il lettore sincrono può anche passare da un recapito compresso a quello non compresso durante la riproduzione. Questa funzionalità è nota come "modifica rapida". Questa funzionalità consente a un'applicazione di modifica di leggere contenuto basato su Windows Media e passarlo direttamente al writer fino a quando non viene raggiunto un frame desiderato. A questo punto, l'applicazione può indicare al lettore di iniziare a consegnare contenuto non compresso, che l'applicazione può quindi modificare e passare al writer per la ricompressione. Quando l'applicazione ha terminato di modificare i frame specificati, può indicare al lettore di iniziare a consegnare nuovamente i frame compressi.

La maggior parte delle funzionalità di base dell'oggetto Reader sincrono può essere suddivisa nei passaggi seguenti. In questa procedura "l'applicazione" si riferisce al programma scritto usando Windows Media Format SDK.

1.  L'applicazione passa al lettore sincrono il nome di un file da leggere. Quando il lettore sincrono apre il file, assegna un numero di output a ogni flusso. Se il file usa l'esclusione reciproca, il lettore assegna un singolo output per tutti i flussi che si escludono a vicenda.
2.  L'applicazione ottiene informazioni sulla configurazione dei vari output dal reader. Le informazioni raccolte consentiranno all'applicazione di eseguire correttamente il rendering degli esempi di supporti.
3.  L'applicazione inizia a richiedere gli esempi, uno alla volta, dal lettore sincrono. Il lettore sincrono recapita ogni esempio in un oggetto buffer per il quale viene distribuita l'interfaccia [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) .
4.  L'applicazione è responsabile del rendering dei dati dopo che sono stati recapitati dal lettore. Windows Media Format SDK non fornisce routine di rendering. In genere, le applicazioni utilizzeranno altri SDK per eseguire il rendering dei dati, ad esempio Microsoft Direct X SDK, o le funzioni multimediali di Microsoft Windows Platform SDK.

Questi passaggi sono illustrati nell'applicazione di esempio WMSyncReader. Per altre informazioni, vedere [applicazioni di esempio](sample-applications.md).

Il lettore sincrono supporta inoltre funzionalità più avanzate. Il lettore sincrono consente di eseguire le operazioni seguenti:

-   Consente di specificare un intervallo di campioni da recuperare in base all'ora o al numero di frame.
-   Controllare la selezione del flusso per i flussi che si escludono a vicenda.
-   Aprire un file utilizzando l'interfaccia COM standard, **IStream**.
-   Leggere i dati di profilo dall'intestazione del file.
-   Leggere i metadati dall'intestazione del file.
-   Passa tra gli esempi di flusso e di output durante la riproduzione.
-   Passare da un campione compresso a un flusso non compresso durante la riproduzione.

Nelle sezioni seguenti viene descritto in dettaglio l'utilizzo dell'oggetto Reader sincrono.

-   [Per creare un reader sincrono e aprire un file](to-create-a-synchronous-reader-and-open-a-file.md)
-   [Per trovare i numeri di flusso e i numeri di output](to-find-stream-numbers-and-output-numbers.md)
-   [Per recuperare esempi di supporti con il lettore sincrono](to-retrieve-media-samples-with-the-synchronous-reader.md)
-   [Per eseguire ricerche in base al tempo tramite il lettore sincrono](to-seek-by-time-using-the-synchronous-reader.md)
-   [Per eseguire la ricerca in base al numero di frame utilizzando il lettore sincrono](to-seek-by-frame-number-using-the-synchronous-reader.md)
-   [Per eseguire la ricerca in base al codice ora SMPTE usando il lettore sincrono](to-seek-by-smpte-time-code-using-the-synchronous-reader.md)
-   [Per recuperare esempi di flusso con il lettore sincrono](to-retrieve-stream-samples-with-the-synchronous-reader.md)
-   [Per recuperare esempi compressi con il lettore sincrono](to-retrieve-compressed-samples-with-the-synchronous-reader.md)

**Codice di esempio**

Nell'esempio di codice seguente viene illustrato come leggere esempi da un file ASF utilizzando il lettore sincrono. Specifica in base al numero di frame un intervallo di campioni da recapitare.


```C++
IWMSyncReader* pSyncReader = NULL;
INSSBuffer*    pMyBuffer   = NULL;

QWORD cnsSampleTime = 0;
QWORD cnsSampleDuration = 0;
DWORD dwFlags = 0;
DWORD dwOutputNumber;
HRESULT hr = S_OK;

// Initialize COM.
hr = CoInitialize(NULL);

// Create a synchronous reader.
hr = WMCreateSyncReader(NULL, WMT_RIGHT_PLAYBACK, &pSyncReader);

// Open an ASF file.
hr = pSyncReader->Open(L"c:\\somefile.wmv");

// TODO: Identify the properties for each output. This works 
// exactly as it does with the asynchronous reader.

// Specify a playback range from frame number 100 of the video 
// stream to the end of the file. Assume that the video stream 
// is stream number 2.
hr = pSyncReader->SetRangeByFrame(2, 100, 0);

// Loop through all the samples in the specified range.
do
{
   // Get the next sample, regardless of its stream number.
   hr = pSyncReader->GetNextSample(0,
                                   &pMyBuffer,
                                   &cnsSampleTime,
                                   &cnsSampleDuration,
                                   &dwFlags,
                                   &dwOutputNumber,
                                   NULL);

   if(SUCCEEDED(hr))
   {
      // TODO: Process the sample in whatever way is appropriate 
      // to your application. When finished, clean up.
      pMyBuffer->Release();
      pMyBuffer = NULL;
      cnsSampleTime     = 0;
      cnsSampleDuration = 0;
      dwFlags           = 0;
      dwOutputNumber    = 0;
   }
} 
while (SUCCEEDED(hr));

pSyncReader->Release();
pSyncReader = NULL;

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Lettura di file ASF**](reading-asf-files.md)
</dt> <dt>

[**Oggetto lettore sincrono**](synchronous-reader-object.md)
</dt> </dl>

 

 




