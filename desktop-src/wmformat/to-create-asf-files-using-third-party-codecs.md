---
title: Per creare file ASF con codec di terze parti
description: Per creare file ASF con codec di terze parti
ms.assetid: 5cd348ca-1f86-429d-92ee-4eab4ced8571
keywords:
- Windows Media Format SDK, creazione di file ASF
- Windows Media Format SDK, codec di terze parti
- ASF (Advanced Systems Format), creazione di file
- ASF (Advanced Systems Format), creazione di file
- ASF (Advanced Systems Format), codec di terze parti
- ASF (Advanced Systems Format), codec di terze parti
- codec di terze parti
- codec, terze parti
- codec, creazione di file ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d6c057f1785ed50e328ac6094ff7dbe078e98fc
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "104336634"
---
# <a name="to-create-asf-files-using-third-party-codecs"></a>Per creare file ASF con codec di terze parti

È possibile utilizzare Windows Media Format SDK per creare file ASF contenenti supporti digitali codificati con i codec scelti. Quando si usa un codec diverso da uno incluso in questo SDK, è necessario eseguire i passaggi seguenti.

1.  Codificare il contenuto con il codec desiderato.
2.  Trovare o creare un valore GUID per identificare il contenuto codificato con il codec usato nel passaggio 1.
3.  Creare un nuovo profilo o modificare un profilo esistente da usare con il contenuto codificato.
    -   Creare un flusso per il contenuto codificato con il tipo principale appropriato. Per ulteriori informazioni sui tipi di supporti principali, vedere [tipi di supporti](media-types.md). Usare il GUID identificato nel passaggio 2 come sottotipo di supporto.
    -   Impostare la velocità in bit e la finestra del buffer per il flusso su valori che non comporteranno un overflow del buffer. Dovrebbe essere possibile ottenere questi valori dal codec al momento della codifica. I componenti Runtime SDK controllano i valori della finestra bitrate/buffer ed eliminano gli esempi, se necessario, per adattare i dati specificati con questi valori. Se si impostano i valori in modo errato, il file non viene trasmesso correttamente, causando una riproduzione insufficiente.
    -   Per i flussi video, è necessario impostare il membro della **bicompressione** della struttura **BITMAPINFOHEADER** contenuto nella struttura [**WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader) sul valore FourCC appropriato per il contenuto. Questo valore deve essere uguale ai primi quattro byte del GUID del sottotipo. Se, ad esempio, la funzione **biCompression** è MAKEFOURCC (' T',' È,',' t') = 0x54455354, il GUID del sottotipo inizierà come segue: 54455354-XXXX-XXXX-XXXX-XXXXXXXXXXXX.
4.  Creare un oggetto writer e caricare il profilo creato nel passaggio precedente. Per ulteriori informazioni sulla scrittura di file, vedere la pagina relativa alla [scrittura di file ASF](writing-asf-files.md).
5.  Scorrere gli input del file e assegnare le proprietà di input per ognuno di essi normalmente. Per ulteriori informazioni sugli input, vedere [utilizzo degli input](working-with-inputs.md). Per il flusso codificato con un codec di terze parti, impostare il puntatore all'interfaccia [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) su **null** prima di chiamare [**IWMWriter:: BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).
6.  Usare il nuovo profilo creato nel passaggio precedente per scrivere il file. Passare gli esempi compressi usando [**IWMWriterAdvanced:: WriteStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-writestreamsample) anziché [**IWMWriter:: WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample). Per il video, è necessario specificare quali esempi sono fotogrammi chiave passando WM \_ SF \_ CLEANPOINT come parametro *dwFlags* .

Per elaborare e decomprimere il flusso codificato con un codec di terze parti, è necessario leggere gli esempi di flussi compressi. L'applicazione di lettura deve gestire anche la decompressione di esempio per il flusso.

## <a name="putting-mpeg-2-streams-into-asf"></a>Inserimento di flussi MPEG-2 in ASF

> [!Note]  
> Questo argomento si applica alle applicazioni che usano Windows Media Format SDK per inserire MPEG-2 (o altri formati di compressione che usano i frame B) nel contenitore di file ASF.

 

Per l'oggetto writer è necessario che tutti gli esempi di input abbiano timestamp e che ogni esempio di input abbia un tempo di presentazione successivo a quello che lo precede. Sebbene praticamente tutti i video non compressi e anche alcuni flussi video compressi soddisfino queste condizioni, i flussi MPEG-2 non lo sono. In MPEG-2 non tutti gli esempi hanno timestamp e quando sono presenti frame B, l'ordine di decodifica di esempio non corrisponde all'ordine di rendering. Quando l'oggetto writer rileva gli esempi non ordinati, li riorganizza nell'ordine "corretto". Per archiviare i flussi MPEG-2 in modalità nativa (non decodificata) in un contenitore ASF, è pertanto necessario eseguire i passaggi seguenti:

Quando si scrive il file:

1.  Aggiungere un'estensione di unità dati a dimensione fissa (a causa) a ogni esempio di input che conterrà una struttura che contiene i valori effettivi dell'ora di inizio e dell'ora di inizio del timestamp MPEG per l'esempio. Utilizzare-1 per questi valori se per l'esempio non è presente alcun timestamp.
2.  Assegnare all'oggetto writer i timestamp di input "fittizi" che aumentano sempre in modo da scrivere gli esempi nel file esattamente nello stesso ordine in cui vengono ricevuti. I timestamp fittizi devono corrispondere approssimativamente ai tempi di presentazione effettivi, calcolati in media nel tempo. I timestamp fittizi saranno costituiti dalla sequenza temporale di ricerca, pertanto se si differenziano in base ai timestamp in tempo reale, le operazioni di ricerca nel file produrranno risultati imprevisti. Tuttavia, una quantità limitata di jitter tra i tempi di campionamento non influirà seriamente sulle operazioni di ricerca.

Durante la lettura del file:

-   Per ogni esempio letto dal file, esaminare la causa. Se contiene un'ora di inizio maggiore o uguale a zero, copiare tale valore nel timestamp per l'esempio di output prima che venga recapitato al decodificatore. Impostare tutti gli altri timestamp sugli esempi di output su **null**. In DirectShow questa operazione viene eseguita chiamando **IMediaSample:: setime**(**null**,**null**).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Contenuto del buffer**](buffering-content.md)
</dt> <dt>

[**Interfaccia IWMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[**Interfaccia IWMWriterAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[**Per recapitare esempi compressi con il lettore asincrono**](to-deliver-compressed-samples-with-the-asynchronous-reader.md)
</dt> <dt>

[**Per recuperare esempi di flusso con il lettore sincrono**](to-retrieve-stream-samples-with-the-synchronous-reader.md)
</dt> <dt>

[**WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader)
</dt> <dt>

[**Utilizzo dei profili**](working-with-profiles.md)
</dt> <dt>

[**Scrittura di file ASF**](writing-asf-files.md)
</dt> </dl>

 

 




