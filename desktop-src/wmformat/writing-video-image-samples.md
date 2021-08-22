---
title: Scrittura di esempi di immagini video
description: Scrittura di esempi di immagini video
ms.assetid: 1d375186-230a-4a18-a995-b331c72a76e7
keywords:
- Advanced Systems Format (ASF), scrittura di esempi di immagini video
- ASF (Advanced Systems Format), scrittura di esempi di immagini video
- immagini video, scrittura di esempi
- flussi, scrittura di esempi di immagini video
- codec, scrittura di esempi di immagini video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7c05bbcc9239eede97f4ea7ca0df34004b1fb7facc0c36c8f38098c42e86fce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119704821"
---
# <a name="writing-video-image-samples"></a>Scrittura di esempi di immagini video

Un flusso di immagini video è un video che contiene una serie di immagini fisse. Le immagini possono essere spostate all'interno del frame e ogni immagine può essere confusa alla successiva. I flussi di immagini video vengono codificati usando Windows codec Media Video 9 Image v2. Il video di output è simile a quello creato dal codec Windows Media Video 9.

Per creare un profilo che contiene un flusso di immagini video, iniziare enumerando i codec video come descritto in [Getting Stream Configuration Information from Codecs](getting-stream-configuration-information-from-codecs.md). Cercare il codec che supporta il sottotipo WMMEDIASUBTYPE \_ WVP2.

Dopo aver impostato il profilo nell'oggetto writer, chiamare [**IWMWriter::GetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops) per ottenere le proprietà multimediali per il flusso di input dell'immagine video. Ottenere il tipo di supporto dall'oggetto delle proprietà multimediali chiamando [**IWMMediaProps::GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype)e modificare il sottotipo in WMMEDIASUBTYPE \_ VIDEOIMAGE. È consigliabile impostare la larghezza e l'altezza del video alle dimensioni massime necessarie per includere le immagini da aggiungere al flusso. Chiamare quindi [**IWMMediaProps::SetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-setmediatype) con il tipo di input modificato. A questo punto è possibile iniziare a inviare esempi all'oggetto writer.

Ogni esempio deve iniziare con una **struttura WMT \_ VIDEOIMAGE \_ SAMPLE2.** Inoltre, gli esempi possono contenere immagini bitmap. Un'immagine è collegata solo a un campione per il primo frame in cui viene visualizzata. Tutti i fotogrammi aggiuntivi che usano tale immagine necessitano solo di informazioni nella struttura . Le bitmap di input devono essere formattate come RGB, 24 bit per pixel.

I file bitmap archiviano i dati dell'immagine in modo che i dati per ogni riga dell'immagine accettano un numero di byte divisibile per quattro. Questo è detto stride della bitmap. In questo modo l'inizio di ogni riga di video viene forzato su un **limite DWORD,** in modo da rendere più efficiente la copia. Se le righe dell'immagine non sono divisibile in modo uniforme per quattro, la riga viene riempita fino al successivo multiplo più alto di quattro byte. Quando si collegano dati immagine, è necessario rimuovere qualsiasi spaziatura interna presente alla fine dei dati per ogni riga.

Il codec Windows Media Video 9 Image v2 mantiene fino a due immagini in memoria alla volta. Queste immagini sono denominate immagine precedente e immagine corrente. Ogni immagine ha un set di membri nella struttura **WMT \_ VIDEOIMAGE \_ SAMPLE2,** che determinano il modo in cui l'immagine viene presentata nel fotogramma. È possibile aggiungere un'immagine impostando il membro dwControlFlags di **WMT \_ VIDEOIMAGE \_ SAMPLE2** su WMT \_ VIDEOIMAGE \_ SAMPLE INPUT \_ \_ FRAME. Quando si passa un frame di input al codec, tale immagine diventa l'immagine corrente. L'immagine che era l'immagine corrente nell'esempio precedente diventa in genere l'immagine precedente e l'immagine che era l'immagine precedente nell'esempio precedente viene eliminata. È possibile configurare il codec per mantenere l'immagine precedente impostando il membro **bKeepPrevImage** su **TRUE.** In tal caso, l'immagine che era l'immagine corrente nell'esempio precedente viene eliminata.

La composizione di base di un fotogramma immagine video è determinata da due fattori per ogni immagine: area di interesse e coefficiente di fusione. L'area di interesse per un'immagine è definita da un punto di origine, una larghezza e un'altezza. La parte di un'immagine descritta dall'area di interesse riempie il frame di output. Se l'area di interesse è di dimensioni diverse rispetto al frame di output, il codec la ridimensiona. Il coefficiente di fusione dell'immagine determina la fusione delle due immagini. I coefficienti di blend per le immagini correnti e precedenti devono essere totali di 1,0. Ad esempio, se **fCurrBlendCoef** è impostato su 0,5 e **fPrevBlendCoef** è impostato su 0,5, il frame di output è composto da una combinazione uguale delle aree di interesse da entrambe le immagini.

Modificando l'area di interesse per un'immagine, è possibile creare effetti di panoramica e zoom. I coefficienti di fusione consentono di eseguire la dissolvenza incrociata (dissolvenza) tra le immagini. Oltre a questi effetti, è possibile usare una delle transizioni predefinite per creare frame più complessi. Le transizioni disponibili sono descritte nella [sezione Transizioni di immagini](video-image-transitions.md) video di questa documentazione. Quando si usa una transizione, è necessario configurare ogni fotogramma. Il modo più semplice per eseguire questa operazione è creare una funzione che modifica in modo incrementale i membri della struttura **WMT \_ VIDEOIMAGE \_ SAMPLE2** per ottenere un effetto completo.

Per altre informazioni sui valori da impostare per le datazioni, vedere [**WMT \_ VIDEOIMAGE \_ SAMPLE2.**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2)

**Nota** Se si vuole includere audio in un file con un flusso di immagini video, è necessario usare l'input audio non compresso. Per combinare un flusso di immagini video con un flusso audio compresso esistente, è necessario decomprimere l'audio e passare gli esempi non compressi. Se si passano esempi compressi al writer durante la scrittura di un flusso di immagini video, si verificherà un errore, causando l'eserema di campioni dal video.

Inoltre, i file di immagine video compressi senza flussi audio possono contenere diversi fotogrammi video molto piccoli e altamente compressi in un singolo pacchetto ASF, con un'esperienza di riproduzione non ottimale nelle versioni precedenti di Windows Media Player. Per evitare questo problema, la soluzione migliore consiste nell'inserire un flusso audio invisibile all'utente nel file, anche se ciò aumenterà anche le dimensioni del file.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Immagine video**](video-image.md)
</dt> <dt>

[**Scrittura di file ASF**](writing-asf-files.md)
</dt> </dl>

 

 




