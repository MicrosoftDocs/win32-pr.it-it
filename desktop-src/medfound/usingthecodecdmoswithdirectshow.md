---
description: Uso dei codec multimediali della finestra in DirectShow
ms.assetid: 5b930447-6bf2-4bb3-8dfb-05f4c1e7cd64
title: Uso dei codec multimediali della finestra in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 495a2675335474351da80b9845fba67f9e967d637d7c9d9c749ffc2f12ce3ea4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012181"
---
# <a name="using-the-window-media-codecs-in-directshow"></a>Uso dei codec multimediali della finestra in DirectShow

Gli Windows codificatori e decodificatori audio e video multimediali sono stati originariamente progettati e ottimizzati per l'utilizzo con il formato del contenitore di file ASF e Windows Media Format SDK. Gli oggetti codec funzionano DirectShow per determinati scenari, ad esempio CBR a un passaggio e codifica VBR basata sulla qualità dei flussi video. Tuttavia, se si sta valutando l'uso degli oggetti codec direttamente in DirectShow usando contenitori di file diversi da ASF, esistono alcuni comportamenti e problemi di cui è necessario tenere conto in anticipo.

> [!Note]  
> Se si intende usare codec autonomi con DirectShow, è probabile che si voglia usarli solo come DMO. In altre parole, si usa [**l'interfaccia IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) anziché [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform).

 

## <a name="wm-audio-in-avi-files"></a>Audio WM in file AVI

È possibile usare DirectShow per codificare i flussi WMA in qualsiasi formato di contenitore di file per cui si dispone di un filtro multiplexer. Tuttavia, le interfacce codec audio e video di Windows Media non supportano WMA nei file AVI perché non è possibile, usando i filtri di riproduzione AVI DirectShow predefiniti, mantenere la sincronizzazione audio-video in un file AVI con un flusso WMA. Per altre informazioni, vedere [Archiviazione di supporti compressi in file AVI](storingcompressedmediainavifiles.md).

Il codificatore audio DMO esempi di durata variabile, anche in modalità "velocità in bit costante". Funziona quindi meglio con i formati dei contenitori di file che usano timestamp. I file AVI non forniscono un timestamp per ogni campione audio o gruppo di campioni. In DirectShow, il filtro AVI Splitter produce timestamp per ogni gruppo di campioni (ogni fotogramma audio) in base al valore **nAvgBytesPerSec** nella struttura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) nell'intestazione del flusso AVI.

Il presupposto alla base di questo calcolo è che tutti i campioni audio nel flusso siano di uguale durata; Tuttavia, gli esempi restituiti dal DMO non sono di uguale durata e quindi i timestamp applicati dalla barra di divisione AVI non sono accurati. Pertanto, non è possibile, senza modificare lo splitter AVI o il DMO del decodificatore audio, usare qualsiasi applicazione basata su DirectShow per riprodurre i file AVI con flussi audio e video sincronizzati. Il codec Windows Media Audio 9 Voice funzionerà in alcuni casi, ma anche questo perderà la sincronizzazione dopo qualsiasi operazione di ricerca, quindi non può essere considerato una soluzione praticabile.

Se si dispone di un codificatore MP3, è possibile creare file AVI con WMV e MP3 per il flusso audio. Tali file verranno riprodotti e cercati correttamente in Windows Media Player e in altre applicazioni basate su DirectShow, perché lo splitter AVI contiene codice di gestione speciale per i flussi MP3. Un'altra opzione è usare l'audio PCM non compresso, anche se ovviamente le dimensioni del file risultanti saranno molto più grandi rispetto a quelle di un flusso audio compresso. Poiché l'DirectShow di esempio crea file AVI, non illustra come usare il codificatore audio DMO.

## <a name="one-pass-encoding"></a>Codifica con un solo passaggio

Il codificatore video DMO funziona facilmente DirectShow due modalità di codifica: CBR e VBR basato sulla qualità. Purché si segua l'ordine corretto delle operazioni durante la compilazione del grafico dei filtri, come illustrato nell'applicazione di esempio, è relativamente semplice inserire il contenuto WMV in un file AVI usando AVI Multiplexer e File Writer.

## <a name="two-pass-encoding"></a>Codifica a due passi

Le modalità di codifica a due passi richiedono un approccio più complesso alla compilazione e allo streaming di grafi per impedire al DMO di scaricare il contenuto dal primo passaggio prima di iniziare il secondo passaggio. Nella codifica a due passaggi è necessario eseguire il grafo una sola volta in modo che il DMO possa eseguire l'analisi di pre-elaborazione dei dati del file e quindi riavvolgere il grafo ed eseguirlo di nuovo in modo che il DMO possa eseguire la codifica effettiva.

Quando il grafico passa allo stato di esecuzione per il secondo passaggio, il wrapper DMO imposta il flag DISCONTINUITY nel primo esempio, perché il timestamp non è sequenziale con l'ultimo timestamp nel primo passaggio. Quando il DMO, che non è stato progettato per funzionare in DirectShow in questo modo, riceve il flag DISCONTINUITY, esegue uno scaricamento e perde i dati archiviati dal primo passaggio. Per risolvere questo problema, la soluzione migliore è probabilmente scrivere un filtro wrapper DMO personalizzato che non imposta il flag DISCONTINUITY quando il grafo viene cercato dopo il primo passaggio. L'esempio Video for Windows (VfW) in questo SDK illustra come eseguire la codifica a due passi.

## <a name="interlaced-content"></a>Contenuto interlacciato

L'DMO codificatore WMV è in grado di codificare il contenuto interlacciato mantenendo l'interlacciamento, utile per il contenuto acquisito da un TV e che potrebbe anche essere riprodotto su un TV. Tuttavia, non è possibile mantenere l'interlacciamento usando il wrapper DMO predefinito, perché tale filtro non supporta [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) nei relativi esempi di input.

Il DMO usa tale interfaccia per ottenere le impostazioni interlacciate per ogni campione ricevuto. Se l'interfaccia non viene trovata, come nel caso del wrapper DMO, il DMO considera semplicemente gli esempi di input come non interlacciati. Per eseguire la codifica interlacciata DirectShow, sono disponibili diverse alternative. L'approccio più semplice consiste probabilmente nell'usare Windows Media Format 9 Series SDK direttamente o usando il filtro DirectShow WM ASF Writer per creare un file ASF interlacciato. È quindi possibile transcodificare il file in un altro formato. Se si transcodifica in AVI, si avrà un file interlacciato, ma i filtri di riproduzione AVI standard DirectShow non lo riconosceranno perché non supportano [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2). Un altro approccio consiste nello scrivere un filtro DMO wrapper personalizzato che supporti [**l'interfaccia INSSBuffer.**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso degli oggetti DMO codec](workingwithcodecdmos.md)
</dt> </dl>

 

 
