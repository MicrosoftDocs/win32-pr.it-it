---
title: Creazione di esempi di immagini video
description: Creazione di esempi di immagini video
ms.assetid: 1d375186-230a-4a18-a995-b331c72a76e7
keywords:
- ASF (Advanced Systems Format), scrittura di esempi di immagini video
- ASF (Advanced Systems Format), scrittura di esempi di immagini video
- immagini video, scrittura di esempi
- flussi, scrittura di esempi di immagini video
- codec, scrittura di esempi di immagini video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fbac644d7938477ba3d2e8b21ebb6e631a47708
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104336297"
---
# <a name="writing-video-image-samples"></a>Creazione di esempi di immagini video

Un flusso di immagini video è un video che contiene una serie di immagini ancora. Le immagini possono essere spostate all'interno del frame e ogni immagine può essere fusa nella successiva. I flussi di immagini video vengono codificati con il codec Windows Media Video 9 image V2. Il video di output è simile a quello creato dal codec Windows Media Video 9.

Per creare un profilo che contiene un flusso di immagini video, iniziare con l'enumerazione dei codec video, come descritto in [recupero delle informazioni di configurazione del flusso dai codec](getting-stream-configuration-information-from-codecs.md). Cercare il codec che supporta il \_ sottotipo WVP2 di WMMEDIASUBTYPE.

Dopo aver impostato il profilo sull'oggetto writer, chiamare [**IWMWriter:: GetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops) per ottenere le proprietà del supporto per il flusso di input dell'immagine video. Ottenere il tipo di supporto dall'oggetto proprietà del supporto, chiamando [**IWMMediaProps:: GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype)e impostare il sottotipo su WMMEDIASUBTYPE \_ VIDEOIMAGE. È necessario impostare la larghezza e l'altezza del video sulle dimensioni massime necessarie per includere le immagini che verranno aggiunte al flusso. Chiamare quindi [**IWMMediaProps:: SetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-setmediatype) con il tipo di input modificato. A questo punto è possibile iniziare a inviare esempi all'oggetto writer.

Ogni esempio deve iniziare con una struttura **WMT \_ VIDEOIMAGE \_ SAMPLE2** . Inoltre, gli esempi possono contenere immagini bitmap. Un'immagine è associata solo a un esempio per il primo frame in cui viene visualizzata. Tutti i frame aggiuntivi che usano tale immagine necessitano solo di informazioni nella struttura. Le bitmap di input devono essere formattate come RGB, 24 bit per pixel.

I file bitmap archiviano i dati dell'immagine in modo che i dati di ogni riga dell'immagine accettino un numero di byte divisibile per quattro. Questa operazione è denominata stride della bitmap. Questa operazione impone l'inizio di ogni riga di video a un limite **DWORD** , rendendo più efficiente la copia. Se le righe dell'immagine non sono divisibile in modo uniforme per quattro, la riga viene riempita al multiplo più alto successivo di quattro byte. Quando si allineano i dati dell'immagine, è necessario rimuovere qualsiasi riempimento presente alla fine dei dati per ogni riga.

Il codec Windows Media Video 9 image V2 gestisce fino a due immagini in memoria alla volta. Queste immagini sono denominate immagine precedente e immagine corrente. Ogni immagine include un set di membri nella struttura **WMT \_ VIDEOIMAGE \_ SAMPLE2** , che determinano la modalità di presentazione dell'immagine nel frame. È possibile aggiungere un'immagine impostando il membro dwControlFlags di **WMT \_ VIDEOIMAGE \_ SAMPLE2** su WMT \_ VIDEOIMAGE \_ Sample \_ input \_ frame. Quando si passa un frame di input al codec, l'immagine diventa l'immagine corrente. L'immagine che rappresenta l'immagine corrente nell'esempio precedente viene in genere convertita nell'immagine precedente e l'immagine precedente nell'esempio precedente viene eliminata. È possibile configurare il codec in modo che mantenga la vecchia immagine precedente impostando il membro **bKeepPrevImage** su **true**. In tal caso, l'immagine che rappresenta l'immagine corrente nell'esempio precedente viene eliminata.

La composizione di base di un frame di immagini video è determinata da due fattori per ogni immagine, ovvero l'area di interesse e il coefficiente di Blend. L'area di interesse per un'immagine è definita da un punto di origine, una larghezza e un'altezza. La parte di un'immagine descritta dall'area di interesse riempie il frame di output. Se l'area di interesse ha dimensioni diverse rispetto al frame di output, il codec lo ridimensiona. Il coefficiente di Blend dell'immagine determina la fusione delle due immagini. I coefficienti di Blend per le immagini correnti e precedenti devono essere totali di 1,0. Ad esempio, se **fCurrBlendCoef** è impostato su 0,5 e **fPrevBlendCoef** è impostato su 0,5, il frame di output è costituito da una combinazione uguale delle aree di interesse di entrambe le immagini.

Modificando l'area di interesse per un'immagine, è possibile creare effetti di zoom e panning. I coefficienti di Blend consentono di dissolvenza incrociata (dissolvenza) tra le immagini. Oltre a questi effetti, è possibile usare una delle transizioni predefinite per creare frame più complessi. Le transizioni disponibili sono descritte nella sezione [transizioni di immagini video](video-image-transitions.md) di questa documentazione. Quando si usa una transizione, è necessario configurare ogni frame. Il modo più semplice per eseguire questa operazione consiste nel creare una funzione che modifichi in modo incrementale i membri della struttura **WMT \_ VIDEOIMAGE \_ SAMPLE2** per un effetto completo.

Per ulteriori informazioni sui valori da impostare per le deformazioni, vedere [**WMT \_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2).

**Nota** Se si vuole includere audio in un file con un flusso di immagini video, è necessario usare l'input audio non compresso. Per combinare un flusso di immagini video con un flusso audio compresso esistente, è necessario decomprimere l'audio e passare gli esempi in non compressi. Se si passano esempi compressi al writer durante la scrittura di un flusso di immagini video, si verificherà un errore, causando l'eliminazione di campioni dal video.

Inoltre, i file di immagine video compressi senza flussi audio possono contenere diversi frame video molto piccoli e altamente compressi in un unico pacchetto ASF, che può comportare un'esperienza di riproduzione insufficiente nelle versioni precedenti di Windows Media Player. Per evitare questo problema, la soluzione migliore consiste nell'inserire un flusso audio invisibile all'utente nel file, anche se ciò aumenterà anche le dimensioni del file.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Immagine video**](video-image.md)
</dt> <dt>

[**Scrittura di file ASF**](writing-asf-files.md)
</dt> </dl>

 

 




