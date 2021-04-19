---
description: Uso dei codec di Windows Media in DirectShow
ms.assetid: 5b930447-6bf2-4bb3-8dfb-05f4c1e7cd64
title: Uso dei codec di Windows Media in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb521c0e3897dc2415fbd613f97b755a146657d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308980"
---
# <a name="using-the-window-media-codecs-in-directshow"></a>Uso dei codec di Windows Media in DirectShow

Il codificatore Windows Media Audio e video e gli oggetti decodificatore sono stati originariamente progettati e ottimizzati per funzionare con il formato del contenitore di file ASF e Windows Media Format SDK. Gli oggetti codec funzionano in modo ottimale in DirectShow per determinati scenari, ovvero la codifica VBR e la qualità dei flussi video con una sola passata. Tuttavia, se si sta valutando l'uso di oggetti codec direttamente in DirectShow usando contenitori di file diversi da ASF, esistono alcuni comportamenti e problemi che è necessario conoscere in anticipo.

> [!Note]  
> Se si prevede di usare codec autonomi con DirectShow, è consigliabile usarli solo come DMOs. In altre parole, si utilizzerà l'interfaccia [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) anziché [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform).

 

## <a name="wm-audio-in-avi-files"></a>Audio WM nei file AVI

È possibile utilizzare DirectShow per codificare i flussi WMA in qualsiasi formato di contenitore di file per il quale si dispone di un filtro multiplexer. Tuttavia, le interfacce Windows Media Audio e codec video non supportano WMA nei file AVI perché è impossibile, usando i filtri di riproduzione DirectShow AVI predefiniti, per gestire la sincronizzazione audio-video in un file AVI con un flusso WMA. Per ulteriori informazioni, vedere [archiviazione di supporti compressi nei file AVI](storingcompressedmediainavifiles.md).

Il codificatore audio DMO restituisce esempi di durata variabile, anche in modalità "velocità in bit costante". Quindi, funziona meglio con i formati di contenitori di file che usano i timestamp. I file AVI non forniscono un timestamp per ogni campione audio o gruppo di campioni. In DirectShow il filtro del separatore AVI produce timestamp per ogni gruppo di campioni (ogni frame audio) in base al valore **nAvgBytesPerSec** nella struttura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) nell'intestazione del flusso AVI.

Il presupposto sottostante a questo calcolo è che tutti gli esempi audio nel flusso hanno una durata uguale. Tuttavia, gli esempi restituiti da DMO non sono di uguale durata, quindi i timestamp applicati dal separatore AVI non sono accurati. Pertanto, non è possibile, senza modificare il separatore AVI o il decodificatore audio DMO, per usare qualsiasi applicazione basata su DirectShow per riprodurre file AVI con flussi audio e video sincronizzati. Il codec Windows Media Audio 9 Voice funzionerà in alcuni casi, ma anche questa funzione perderà la sincronizzazione dopo qualsiasi operazione di ricerca, pertanto non può essere considerata una soluzione valida.

Se si ha un codificatore MP3, è possibile creare file AVI con WMV e MP3 per il flusso audio. Tali file vengono riprodotti e cercati correttamente in Windows Media Player e in altre applicazioni basate su DirectShow, perché il separatore AVI contiene codice di gestione speciale per i flussi MP3. Un'altra opzione consiste nell'usare audio PCM non compresso, sebbene ovviamente le dimensioni dei file risultanti saranno molto più grandi rispetto a un flusso audio compresso. Poiché l'applicazione di esempio DirectShow crea file AVI, non illustra come usare il codificatore audio DMO.

## <a name="one-pass-encoding"></a>Codifica a passaggio singolo

Il codificatore video DMO funziona facilmente in DirectShow per due modalità di codifica, ovvero CBR e la VBR basata sulla qualità. Se si segue l'ordine corretto delle operazioni durante la creazione del grafico di filtro, come illustrato nell'applicazione di esempio, è relativamente semplice inserire il contenuto di WMV in un file AVI usando il multiplexer AVI e il writer di file.

## <a name="two-pass-encoding"></a>Codifica a due passaggi

Le modalità di codifica a due passaggi richiedono un approccio più complesso alla compilazione e al flusso di grafici per impedire a DMO di scaricare il contenuto dal primo passaggio prima di iniziare il secondo passaggio. Nella codifica a due passaggi è necessario eseguire il grafo una volta in modo che DMO possa eseguire l'analisi di pre-elaborazione dei dati del file, quindi riavvolgere il grafo ed eseguirlo di nuovo in modo che DMO possa eseguire la codifica effettiva.

Quando il grafico entra in uno stato di esecuzione per il secondo passaggio, il wrapper DMO imposta il flag di discontinuità sul primo campione, perché il timestamp non è sequenziale con l'ultimo timestamp del primo passaggio. Quando DMO, che non è stato progettato per funzionare in DirectShow in questo modo, riceve il flag di discontinuità, esegue uno scaricamento e perde i dati archiviati dal primo passaggio. Per ovviare a questo problema, è probabile che la soluzione migliore scriva un filtro wrapper DMO personalizzato che non imposta il flag di discontinuità quando il grafico viene ricercato dopo il primo passaggio. Nell'esempio video for Windows (VfW) in questo SDK viene illustrato come eseguire la codifica a due passaggi.

## <a name="interlaced-content"></a>Contenuto interlacciato

Il codificatore di WMV DMO è in grado di codificare il contenuto interlacciato conservando il interlacciamento, utile per il contenuto acquisito da un televisore e potrebbe essere riprodotto anche in un televisore. Tuttavia, non è possibile mantenere l'interlacciamento utilizzando il wrapper DMO predefinito, perché tale filtro non supporta [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) nei relativi esempi di input.

DMO utilizza tale interfaccia per ottenere le impostazioni interlacciate per ogni campione ricevuto. Se l'interfaccia non viene trovata, come nel caso del wrapper DMO, DMO considera semplicemente gli esempi di input come non interlacciati. Per eseguire la codifica interlacciata in DirectShow, esistono diverse alternative. L'approccio più semplice è probabilmente usare Windows Media Format 9 Series SDK direttamente o usando il filtro DirectShow del writer WM ASF, per creare un file ASF interlacciato. È quindi possibile transcodificare il file in un altro formato. Se si esegue la transcodifica in AVI, sarà presente un file interlacciato, ma i filtri di riproduzione standard DirectShow AVI non lo riconoscono perché non supportano [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2). Un altro approccio consiste nel scrivere un filtro wrapper DMO che supporta l'interfaccia [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di codec DMOs](workingwithcodecdmos.md)
</dt> </dl>

 

 
