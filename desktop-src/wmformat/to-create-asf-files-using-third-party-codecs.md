---
title: Per creare file ASF usando codec di terze parti
description: Per creare file ASF usando codec di terze parti
ms.assetid: 5cd348ca-1f86-429d-92ee-4eab4ced8571
keywords:
- Windows Media Format SDK, creazione di file ASF
- Windows MEDIA Format SDK, codec di terze parti
- Advanced Systems Format (ASF), creazione di file
- ASF (Advanced Systems Format), creazione di file
- Advanced Systems Format (ASF), codec di terze parti
- ASF (Advanced Systems Format), codec di terze parti
- codec di terze parti
- codec, terze parti
- codec, creazione di file ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d1eeeb891037581a550d8c15c2f2b4cefa14f81f20d0d55623d382d0e933e95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118197080"
---
# <a name="to-create-asf-files-using-third-party-codecs"></a>Per creare file ASF usando codec di terze parti

È possibile usare l'SDK Windows Media Format per creare file ASF contenenti file multimediali digitali codificati con qualsiasi codec scelto. Quando si usa un codec diverso da quello incluso in questo SDK, è necessario eseguire la procedura seguente.

1.  Codificare il contenuto con il codec desiderato.
2.  Trovare o creare un valore GUID per identificare il contenuto codificato con il codec usato nel passaggio 1.
3.  Creare un nuovo profilo o modificarne uno esistente da usare con il contenuto codificato.
    -   Creare un flusso per il contenuto codificato con il tipo principale appropriato. Per altre informazioni sui tipi di supporti principali, vedere [Tipi di supporti.](media-types.md) Usare il GUID identificato nel passaggio 2 come sottotipo di supporto.
    -   Impostare la frequenza in bit e la finestra del buffer per il flusso su valori che non comportano un overflow del buffer. Dovrebbe essere possibile ottenere questi valori dal codec al momento della codifica. I componenti di runtime dell'SDK controllano i valori della finestra della velocità in bit/buffer ed eliminano gli esempi, se necessario, per adattare i dati specificati a questi valori. Se si impostano i valori in modo non corretto, il file non verrà trasmesso correttamente, con conseguente scarsa riproduzione.
    -   Per i flussi video, è necessario impostare il membro **biCompression** della struttura **BITMAPINFOHEADER** contenuta nella struttura [**WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader) sul valore FOURCC appropriato per il contenuto. Questo valore deve essere uguale ai primi quattro byte del GUID del sottotipo. Ad esempio, se **biCompression** è MAKEFOURCC('T','E','S','T')=0x54455354, il GUID del sottotipo inizierà come segue: 54455354-XXXX-XXXX-XXXX-XXXXXXXXXXXXXX.
4.  Creare un oggetto writer e caricare il profilo creato nel passaggio precedente. Per altre informazioni sulla scrittura di file, vedere [Scrittura di file ASF.](writing-asf-files.md)
5.  Scorrere gli input del file e assegnare le proprietà di input per ognuno come di consueto. Per altre informazioni sugli input, vedere [Uso degli input.](working-with-inputs.md) Per il flusso codificato con un codec di terze parti, impostare il puntatore di interfaccia [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) su **NULL** prima di chiamare [**IWMWriter::BeginWriting.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting)
6.  Usare il nuovo profilo creato nel passaggio precedente per scrivere il file. Passare gli esempi compressi [**usando IWMWriterAdvanced::WriteStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-writestreamsample) anziché [**IWMWriter::WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample). Per i video, è necessario specificare quali campioni sono fotogrammi chiave passando WM \_ SF \_ CLEANPOINT come *parametro dwFlags.*

Per elaborare e decomprimere il flusso codificato con un codec di terze parti, è necessario leggere gli esempi di flusso compresso. L'applicazione di lettura deve gestire anche la decompressione di esempio per il flusso.

## <a name="putting-mpeg-2-streams-into-asf"></a>Inserimento di flussi MPEG-2 in ASF

> [!Note]  
> Questo argomento si applica alle applicazioni che usano Windows Media Format SDK per inserire MPEG-2 (o altri formati di compressione che usano frame B) nel contenitore di file ASF.

 

L'oggetto writer richiede che tutti i campioni di input siano contrassegnati con timestamp e presuppone che ogni esempio di input abbia un'ora di presentazione successiva a quella precedente. Anche se praticamente tutti i video non compressi e anche alcuni flussi video compressi soddisfano queste condizioni, i flussi MPEG-2 non lo soddisfano. In MPEG-2 non tutti i campioni sono contrassegnati con timestamp e, quando sono presenti fotogrammi B, l'ordine di decodifica dei campioni non corrisponde all'ordine di rendering. Quando l'oggetto writer rileva campioni non in ordine, li riorganizza nell'ordine "corretto". Pertanto, per archiviare i flussi MPEG-2 in modo nativo (non decodificato) in un contenitore ASF, è necessario seguire questa procedura:

Quando si scrive il file:

1.  Aggiungere un'estensione per unità dati a dimensione fissa (DUE) a ogni esempio di input che contenerà una struttura contenente i valori effettivi dell'ora di inizio del timestamp MPEG e dell'ora di arresto per l'esempio. Usare -1 per questi valori se l'esempio non ha un timestamp.
2.  Assegnare all'oggetto writer timestamp di input "fittizi" che aumentano sempre in modo da scrivere gli esempi nel file esattamente nello stesso ordine in cui vengono ricevuti. I timestamp fittizi devono corrispondere approssimativamente agli orari di presentazione effettivi, come indicato nella media nel tempo. I timestamp fittizi formeranno la sequenza temporale di ricerca, quindi se divergono rispetto ai timestamp in tempo reale, le operazioni di ricerca sul file produrranno risultati imprevisti. Tuttavia, una quantità limitata di instabilità tra i tempi di campionamento non influirà in modo grave sulle operazioni di ricerca.

Durante la lettura del file:

-   Per ogni esempio letto dal file, esaminare due. Se contiene un'ora di inizio maggiore o uguale a zero, copiare tale valore nel timestamp dell'esempio di output prima che venga recapitato al decodificatore. Impostare tutti gli altri timestamp sugli esempi di output su **NULL.** In DirectShow questa operazione viene eseguita chiamando **IMediaSample::SetTime**(**NULL**,**NULL**).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Buffering del contenuto**](buffering-content.md)
</dt> <dt>

[**Interfaccia IWMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[**Interfaccia IWMWriterAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[**Per distribuire esempi compressi con il lettore asincrono**](to-deliver-compressed-samples-with-the-asynchronous-reader.md)
</dt> <dt>

[**Per recuperare esempi di flusso con il lettore sincrono**](to-retrieve-stream-samples-with-the-synchronous-reader.md)
</dt> <dt>

[**WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader)
</dt> <dt>

[**Uso dei profili**](working-with-profiles.md)
</dt> <dt>

[**Scrittura di file ASF**](writing-asf-files.md)
</dt> </dl>

 

 




