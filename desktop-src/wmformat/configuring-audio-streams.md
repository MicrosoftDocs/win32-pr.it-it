---
title: Configurazione di flussi audio
description: Configurazione di flussi audio
ms.assetid: 6ddd9bc1-3fde-4098-afce-fdda461ced62
keywords:
- flussi, configurazione di flussi audio
- codec, configurazione di flussi audio
- flussi audio, configurazione
- codec, formati
- flussi, interfaccia IWMCodecInfo
- IWMCodecInfo, flussi audio
- flussi, sincronizzazione A/V
- flussi audio, sincronizzazione A/V
- Sincronizzazione A/V
- flussi, sincronizzazione A/V
- flussi audio, sincronizzazione A/V
- flussi, formati audio a ritardo ridotto
- flussi audio, formati audio a ritardo ridotto
- codec, formati audio a ritardo ridotto
- flussi, velocità in bit variabile (VBR)
- flussi audio, velocità in bit variabile (VBR)
- codec, velocità in bit variabile (VBR)
- velocità in bit variabile (VBR), configurazione
- VBR (velocità in bit variabile), configurazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ad3931ec41e73c125417d39cdd177dc16056e9e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300232"
---
# <a name="configuring-audio-streams"></a>Configurazione di flussi audio

I flussi audio sono in genere i più semplici da configurare. Ottenere una configurazione di flusso dal codec usando i metodi di [**IWMCodecInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo) , come descritto in [recupero delle informazioni di configurazione dei flussi dai codec](getting-stream-configuration-information-from-codecs.md). Nella maggior parte dei casi, non è consigliabile modificare le impostazioni da quelle recuperate.

Il formato di codec selezionato da quello enumerato dipende dall'uso previsto dei file ASF creati con il profilo. La descrizione del formato di codec recuperata da [**IWMCodecInfo2:: GetCodecFormatDesc**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo2-getcodecformatdesc) riepiloga le caratteristiche del formato. Se l'applicazione non Visualizza le descrizioni per sceglierle, è possibile chiamare **QueryInterface** sull'interfaccia [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig) del formato codec per ottenere l'interfaccia [**IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops) . È quindi possibile recuperare la struttura del [**\_ \_ tipo di supporto WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) chiamando [**IWMMediaProps:: GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype). Esaminando la struttura **del \_ \_ tipo di supporto WM** e la struttura [**WAVEFORMATEX**](/previous-versions/windows/desktop/legacy/dd757720(v=vs.85)) a cui punta, è possibile determinare le impostazioni del formato di codec e confrontarle con i requisiti.

## <a name="getting-audio-formats-for-av-synchronization"></a>Recupero di formati audio per la sincronizzazione A/V

Il codec Windows Media Audio e il codec Windows Media Audio Professional supportano entrambi i formati per i file audio e video. I formati solo audio sono ottimizzati per i file contenenti solo dati audio, mentre i formati audio/video sono ottimizzati per l'audio in un file con un flusso video. Quando si enumerano i formati di codec per questi codec, i formati audio/video sono disponibili solo per i formati audio. Le descrizioni del formato audio/video contengono tutte la stringa "(A/V)". È possibile identificare i formati progettati per la sincronizzazione audio/video a livello di programmazione controllando il numero di pacchetti al secondo. I formati per la sincronizzazione contengono 5 o più pacchetti al secondo se la velocità in bit è maggiore o uguale a 32.000 bit al secondo. I formati con velocità in bit inferiori a 32.000 bit al secondo possono essere usati con video sincronizzato se usano 3 o più pacchetti al secondo. L'esempio di codice nell'argomento [to find audio formats](to-find-audio-formats.md) contiene il codice necessario per eseguire questo controllo:


```C++
if((pWave->nAvgBytesPerSec / pWave->nBlockAlign) >= 
       ((pWave->nAvgBytesPerSec >= 4000) ? 5.0 : 3.0))
{
    // Set this stream configuration as the new best match.
}
```



## <a name="getting-low-delay-audio-formats"></a>Acquisizione di Low-Delay formati audio

Il codec Windows Media 9,1 e il codec Windows Media Audio 9,1 Professional supportano entrambi i formati a ritardo ridotto. Questi formati hanno una finestra buffer più piccola rispetto ad altri formati audio. L'audio a basso ritardo è progettato per migliorare le prestazioni negli scenari in cui i file o i flussi verranno scambiati di frequente; ad esempio, un'applicazione che elenca diversi brani per lo streaming nell'interfaccia utente e consente agli utenti di spostarsi arbitrariamente tra loro.

I formati a ritardo ridotto sono disponibili solo in modalità CBR (un passaggio o due passaggi). Le descrizioni del formato a ritardo basso contengono tutte la stringa "ritardo basso". È possibile identificare i formati a livello di programmazione controllando il valore della velocità in bit del formato. Ai formati a basso ritardo vengono assegnate velocità in bit pari a 1 kilobit inferiore rispetto alla velocità in bit del formato normale equivalente. Ad esempio, il codec Windows Media Audio 9,1 supporta un formato CBR a passaggio singolo con una velocità in bit di 192 kbps. Il formato a basso ritardo equivalente ha una velocità in bit di 191 kbps. Inoltre, con l'eccezione del formato mono a 5 kbps supportato dal codec Windows Media Audio 9,1, i formati a basso ritardo sono gli unici formati che hanno un valore di velocità in bit dispari.

## <a name="configuring-variable-bit-rate-audio"></a>Configurazione dell'audio della velocità in bit variabile

Quando è necessario un formato di velocità in bit variabile (VBR) per uno dei codec audio di Windows Media, è possibile ottenerlo impostando le impostazioni di enumerazione nel metodo [**IWMCodecInfo3:: SetCodecEnumerationSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-setcodecenumerationsetting) . Impostare g \_ wszVBREnabled su true e impostare g \_ wszNumPasses su 1 per VBR basato sulla qualità o 2 per VBR a due passaggi (vincolato o non vincolato). Se si usa un VBR a due passaggi vincolato, è necessario impostare manualmente la velocità in bit massima e la finestra del buffer per il flusso usando i metodi di [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) , come descritto in [configurazione dei flussi VBR](configuring-vbr-streams.md).

Nei profili VBR basati sulla qualità, il membro **nAvgBytesPerSec** della struttura **WAVEFORMATEX** contiene il livello di qualità (da 1 a 100) nel byte di ordine inferiore e i tre byte più significativi sono impostati su 0x7fffff. Non tentare di modificare l'impostazione di qualità modificando manualmente questo valore. è necessario usare il formato così come viene recuperato dal codec. Per usare un valore di qualità diverso, è necessario enumerare i formati fino a trovare uno che soddisfi le proprie esigenze. Inoltre, **nAvgBytesPerSec** non verrà mantenuto nel file ASF; Quando si ottiene la struttura **WAVEFORMATEX** per un file aperto con l'oggetto Reader, **nAvgBytesPerSec** contiene un valore approssimativo che rappresenta il numero medio di byte al secondo.

> [!Note]  
> Quando si configurano i flussi audio, non è mai necessario avere un valore della finestra buffer audio maggiore del valore per tutti i flussi video nel file. In genere non si tratta di un problema, poiché i valori della finestra buffer audio devono essere compresi tra 1,5 e 3 secondi e i valori video devono essere compresi tra 3 e 5 secondi. Se una finestra buffer audio è maggiore di una finestra buffer video, il file verrà riprodotto con i flussi leggermente fuori dalla sincronizzazione.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Configurazione comune a tutti i flussi**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Configurazione di flussi**](configuring-streams.md)
</dt> <dt>

[**Per trovare i formati audio**](to-find-audio-formats.md)
</dt> </dl>

 

 