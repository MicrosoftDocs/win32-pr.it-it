---
title: Configurazione di audio Flussi
description: Configurazione di audio Flussi
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
- flussi, formati audio a basso ritardo
- flussi audio, formati audio a basso ritardo
- codec, formati audio a basso ritardo
- flussi, velocità in bit variabile (VBR)
- flussi audio, velocità in bit variabile (VBR)
- codec, velocità in bit variabile (VBR)
- velocità in bit variabile (VBR), configurazione
- VBR (velocità in bit variabile),configurazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e28c32e9d0e237e72f693bded74c7620d33845261a6137afdf58b04f35f441f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119548031"
---
# <a name="configuring-audio-streams"></a>Configurazione di audio Flussi

I flussi audio sono in genere i più semplici da configurare. Ottenere una configurazione del flusso dal codec usando i metodi di [**IWMCodecInfo,**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo) come descritto in Ottenere informazioni di [configurazione del flusso dai codec](getting-stream-configuration-information-from-codecs.md). Nella maggior parte dei casi, è consigliabile non modificare le impostazioni da quelle recuperate.

Il formato del codec selezionato tra quelli enumerati dipende dall'uso previsto dei file ASF effettuati con il profilo. La descrizione del formato del codec recuperata da [**IWMCodecInfo2::GetCodecFormatDesc**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo2-getcodecformatdesc) riepiloga le caratteristiche del formato. Se l'applicazione non visualizza le descrizioni da scegliere, è possibile chiamare **QueryInterface** [**sull'interfaccia IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig) del formato codec per ottenere l'interfaccia [**IWMMediaProps.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops) È quindi possibile recuperare la [**struttura WM \_ MEDIA \_ TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) chiamando [**IWMMediaProps::GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype). Esaminando la **struttura WM MEDIA \_ \_ TYPE** e la struttura [**WAVEFORMATEX**](/previous-versions/windows/desktop/legacy/dd757720(v=vs.85)) a cui punta, è possibile determinare le impostazioni del formato codec e confrontarle con le proprie esigenze.

## <a name="getting-audio-formats-for-av-synchronization"></a>Recupero di formati audio per la sincronizzazione A/V

Il Windows codec Media Audio e Windows Codec Professional Media Audio supportano sia i formati per i file solo audio che per i file audio/video. I formati solo audio sono ottimizzati per i file contenenti solo dati audio, mentre i formati audio/video sono ottimizzati per l'audio contenuto in un file con un flusso video. Quando si enumerano i formati di codec per questi codec, i formati audio/video vengono dopo i formati solo audio. Le descrizioni del formato audio/video contengono tutte la stringa "(A/V)". È possibile identificare i formati progettati per la sincronizzazione audio/video a livello di codice controllando il numero di pacchetti al secondo. I formati per la sincronizzazione hanno 5 o più pacchetti al secondo se la velocità in bit è maggiore o uguale a 32.000 bit al secondo. I formati con velocità in bit inferiori a 32.000 bit al secondo possono essere usati con video sincronizzati se usano 3 o più pacchetti al secondo. L'esempio di codice [nell'argomento To Find Audio Formats](to-find-audio-formats.md) contiene il codice necessario per eseguire questo controllo:


```C++
if((pWave->nAvgBytesPerSec / pWave->nBlockAlign) >= 
       ((pWave->nAvgBytesPerSec >= 4000) ? 5.0 : 3.0))
{
    // Set this stream configuration as the new best match.
}
```



## <a name="getting-low-delay-audio-formats"></a>Recupero Low-Delay formati audio

Il codec Windows Media 9.1 e il codec Windows Media Audio 9.1 Professional supportano entrambi formati a basso ritardo. Questi formati hanno una finestra del buffer più piccola rispetto ad altri formati audio. L'audio a basso ritardo è progettato per migliorare le prestazioni negli scenari in cui i file o i flussi verranno cambiati di frequente. ad esempio un'applicazione che elenca una serie di brani per lo streaming nell'interfaccia utente e consente agli utenti di passare arbitrariamente da un brano all'altro.

I formati a ritardo ridotto sono disponibili solo in modalità CBR (un passaggio o due passi). Le descrizioni del formato a basso ritardo contengono tutte la stringa "Low Delay". È possibile identificare i formati a livello di codice controllando il valore della velocità in bit del formato. Ai formati a basso ritardo vengono assegnate velocità in bit inferiori di 1 kilobit rispetto alle velocità in bit del formato normale equivalente. Ad esempio, il codec Windows Media Audio 9.1 supporta un formato CBR a singolo passaggio con una velocità in bit di 192 kbps. Il formato a ritardo basso equivalente ha una velocità in bit di 191 kbps. Inoltre, ad eccezione del formato mono a 5 kbps supportato dal codec Windows Media Audio 9.1, i formati a basso ritardo sono gli unici formati con un valore di velocità in bit dispari.

## <a name="configuring-variable-bit-rate-audio"></a>Configurazione dell'audio a velocità in bit variabile

Quando è necessario un formato VBR (Variable Bit Rate) per uno dei codec audio di Windows Media, è possibile ottenerlo impostando le impostazioni di enumerazione nel metodo [**IWMCodecInfo3::SetCodecEnumerationSetting.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-setcodecenumerationsetting) Impostare g \_ wszVBREnabled su True e g wszNumPasses su 1 per vbr basato sulla qualità o 2 per VBR a due passi (vincolato o non \_ vincolato). Se si usa vbr a due passi vincolato, è necessario impostare manualmente la velocità in bit massima e la finestra del buffer per il flusso usando i metodi di [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) come descritto in Configurazione di [VBR Flussi](configuring-vbr-streams.md).

Nei profili VBR basati sulla qualità, il membro **nAvgBytesPerSec** della struttura **WAVEFORMATEX** contiene il livello di qualità (da 1 a 100) nel byte meno significativo e i tre byte di ordine superiore sono impostati su 0x7fffff. Non tentare di modificare l'impostazione di qualità modificando manualmente questo valore. È necessario usare il formato così come viene recuperato dal codec. Per usare un valore di qualità diverso, è necessario enumerare i formati fino a trovare uno che soddisfi le proprie esigenze. Inoltre, **nAvgBytesPerSec** non verrà mantenuto nel file ASF. Quando si ottiene la struttura **WAVEFORMATEX** per un file aperto con l'oggetto reader, **nAvgBytesPerSec** contiene un valore approssimativo che rappresenta il numero medio di byte al secondo.

> [!Note]  
> Quando si configurano flussi audio, non è mai necessario avere un valore della finestra del buffer audio maggiore del valore per tutti i flussi video nel file. In genere questo non è un problema, perché i valori della finestra del buffer audio devono essere compresi tra 1,5 e 3 secondi e i valori video devono essere compresi tra 3 e 5 secondi. Se una finestra del buffer audio è maggiore di una finestra del buffer video, il file verrà riprodotto con i flussi leggermente fuori sincronizzazione.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Configurazione comune a tutti i Flussi**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Configurazione di Flussi**](configuring-streams.md)
</dt> <dt>

[**Per trovare formati audio**](to-find-audio-formats.md)
</dt> </dl>

 

 