---
title: Lettura di file con il lettore sincrono
description: Lettura di file con il lettore sincrono
ms.assetid: 18c6c0cd-478f-4325-b23e-571c33779a96
keywords:
- Windows MEDIA Format SDK, lettura di file
- Windows Media Format SDK, lettori sincroni
- Advanced Systems Format (ASF), lettori sincroni
- ASF (Advanced Systems Format), lettori sincroni
- Advanced Systems Format (ASF), lettura di file
- ASF (Advanced Systems Format), lettura di file
- lettori sincroni, interfaccia IWMReaderCallback
- IWMReaderCallback, lettori sincroni
- lettori sincroni, lettura di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c30ed2f9af78c9643f269adb24f740f2fe9227bc2e5b8a36d5c9d29606564176
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118197473"
---
# <a name="reading-files-with-the-synchronous-reader"></a>Lettura di file con il lettore sincrono

È possibile usare il lettore sincrono per leggere un file ASF usando chiamate sincrone anziché i metodi asincroni nell'oggetto reader. L'uso di chiamate sincrone riduce il numero di thread necessari per leggere un file. Il lettore asincrono usa più thread per l'elaborazione dei flussi. Per i file con più flussi, il numero di thread usati può diventare molto elevato. Il lettore sincrono usa un solo thread.

Il lettore sincrono è stato progettato per soddisfare le esigenze delle applicazioni di creazione e modifica di file del contenuto. È possibile usare il lettore sincrono per altre applicazioni, ma la relativa funzionalità è limitata.

Il lettore sincrono può aprire file locali o file in una rete usando il nome di percorso UNC (ad esempio " \\ \\ \\ someshare \\ somedirectory somefile.wmv"). Non è possibile trasmettere file al lettore sincrono o aprire file da un percorso Internet. Il lettore sincrono fornisce anche il supporto per l'uso **dell'interfaccia** COM IStream come origine.

Il lettore sincrono offre maggiore versatilità per il recupero di esempi da un file ASF rispetto al lettore asincrono. Il lettore sincrono può distribuire esempi in base al numero di flusso e all'output. Gli esempi forniti dal numero di flusso possono essere compressi o non compressi. Il lettore sincrono può anche passare dalla distribuzione compressa alla distribuzione non compressa durante la riproduzione. Questa funzionalità è nota come "modifica rapida". Questa funzionalità consente a un'applicazione di modifica di leggere Windows contenuto basato su supporti e passarlo direttamente al writer fino a quando non viene raggiunto un frame desiderato. A questo punto l'applicazione può indicare al lettore di iniziare a distribuire contenuto non compresso, che l'applicazione può quindi modificare e passare al writer per la ricompressione. Al termine della modifica dei frame specificati, l'applicazione può indicare al lettore di iniziare a distribuire nuovamente i frame compressi.

La funzionalità più semplice dell'oggetto lettore sincrono può essere suddivisa nei passaggi seguenti. In questi passaggi "l'applicazione" si riferisce al programma scritto usando Windows Media Format SDK.

1.  L'applicazione passa al lettore sincrono il nome di un file da leggere. Quando il lettore sincrono apre il file, assegna un numero di output a ogni flusso. Se il file usa l'esclusione reciproca, il lettore assegna un singolo output per tutti i flussi che si escludono a vicenda.
2.  L'applicazione ottiene informazioni sulla configurazione dei vari output dal lettore. Le informazioni raccolte consentiranno all'applicazione di eseguire correttamente il rendering degli esempi multimediali.
3.  L'applicazione inizia a richiedere campioni, uno alla volta, dal lettore sincrono. Il lettore sincrono recapita ogni esempio in un oggetto buffer per il quale fornisce [**l'interfaccia INSSBuffer.**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer)
4.  L'applicazione è responsabile del rendering dei dati dopo che sono stati recapitati dal lettore. L Windows Media Format SDK non fornisce routine di rendering. In genere, le applicazioni usano altri SDK per eseguire il rendering dei dati, ad esempio Microsoft Direct X SDK o le funzioni multimediali di Microsoft Windows Platform SDK.

Questi passaggi sono illustrati nell'applicazione di esempio WMSyncReader. Per altre informazioni, vedere [Applicazioni di esempio.](sample-applications.md)

Il lettore sincrono supporta anche funzionalità più avanzate. Il lettore sincrono consente di eseguire le operazioni seguenti:

-   Specificare un intervallo di campioni da recuperare in base all'ora o al numero di fotogramma.
-   Controllare la selezione del flusso per i flussi che si escludono a vicenda.
-   Aprire un file usando l'interfaccia COM standard, **IStream.**
-   Legge i dati del profilo dall'intestazione del file.
-   Legge i metadati dall'intestazione del file.
-   Passare da un flusso all'altro e da un esempio di output all'altro durante la riproduzione.
-   Passare da campioni di flusso compressi a campioni non compressi durante la riproduzione.

Nelle sezioni seguenti viene descritto in dettaglio l'utilizzo dell'oggetto lettore sincrono.

-   [Per creare un lettore sincrono e aprire un file](to-create-a-synchronous-reader-and-open-a-file.md)
-   [Per trovare i numeri di flusso e i numeri di output](to-find-stream-numbers-and-output-numbers.md)
-   [Per recuperare esempi di file multimediali con il lettore sincrono](to-retrieve-media-samples-with-the-synchronous-reader.md)
-   [Per eseguire la ricerca in base all'ora usando il lettore sincrono](to-seek-by-time-using-the-synchronous-reader.md)
-   [Per cercare in base al numero di fotogramma usando il lettore sincrono](to-seek-by-frame-number-using-the-synchronous-reader.md)
-   [Per eseguire la ricerca in base al codice temporale SMPTE usando il lettore sincrono](to-seek-by-smpte-time-code-using-the-synchronous-reader.md)
-   [Per recuperare esempi di flusso con il lettore sincrono](to-retrieve-stream-samples-with-the-synchronous-reader.md)
-   [Per recuperare esempi compressi con il lettore sincrono](to-retrieve-compressed-samples-with-the-synchronous-reader.md)

**Codice di esempio**

Il codice di esempio seguente illustra come leggere esempi da un file ASF usando il lettore sincrono. Specifica in base al numero di fotogramma un intervallo di campioni da distribuire.


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

 

 




