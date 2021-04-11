---
title: Impostazioni di output
description: Impostazioni di output
ms.assetid: effe6c07-e6df-45b0-b865-2a025c466d6f
keywords:
- Windows Media Format SDK, costanti globali
- Advanced Systems Format (ASF), costanti globali
- ASF (formato avanzato dei sistemi), costanti globali
- costanti globali, elenco di
- Windows Media Format SDK, costanti
- Advanced Systems Format (ASF), costanti
- ASF (formato avanzato dei sistemi), costanti
- costanti, elenco di
- Windows Media Format SDK, impostazioni di output
- ASF (Advanced Systems Format), impostazioni di output
- ASF (formato avanzato dei sistemi), impostazioni di output
- impostazioni di output
- lettori sincroni, impostazioni di output
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f5a02d508f76057dd72e34558a7ca8d29de4847
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104117343"
---
# <a name="output-settings"></a>Impostazioni di output

Le costanti globali seguenti vengono utilizzate per identificare le impostazioni di output per il Reader e l'oggetto Reader sincrono.



| Costante globale                | tipo di dati \_ attr WMT \_  | Descrizione di *pValue*                                                                                                                                                                                                                                                                                                    |
|--------------------------------|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| g \_ wszAllowInterlacedOutput    | **\_tipo WMT \_ bool**  | Se true, il lettore fornirà frame interlacciati, se supportati dall'output.                                                                                                                                                                                                                                            |
| g \_ wszDedicatedDeliveryThread  | **\_tipo WMT \_ bool**  | Se true, l'output disporrà di un thread dedicato creato per il recapito degli esempi. Non supportato nel lettore sincrono.                                                                                                                                                                                            |
| g \_ wszDeliverOnReceive         | **\_tipo WMT \_ bool**  | Se true, gli esempi per questo output verranno recapitati non appena sono disponibili dal reader. Ciò può comportare il recapito degli esempi di questo output in ordine non ordinato e prima dei campioni corrispondenti da altri output.                                                                                            |
| g \_ wszDynamicRangeControl      | **WMT \_ tipo \_ DWORD** | Specifica il livello di controllo intervallo dinamico da usare per l'output. Impostare su un valore compreso tra 0 e 2, dove 0 indica nessun controllo intervallo dinamico (impostazione predefinita) e 2 è il livello massimo di controllo intervallo dinamico (intervallo dinamico più piccolo).                                                                                |
| g \_ wszEarlyDataDelivery        | **WMT \_ tipo \_ DWORD** | Tempo, in millisecondi, che specifica la quantità di tempo precedente per il recapito degli esempi. Se maggiore di zero, gli esempi di questo output verranno recuperati e decodificati in modo che gli esempi vengano recapitati prima degli esempi per altri output. In genere, il lettore fornisce esempi in ordine di tempo di presentazione.         |
| g \_ wszEnableDiscreteOutput     | **\_tipo WMT \_ bool**  | Se true, il lettore Abilita l'output audio multicanale ad alta definizione. Questa impostazione è valida solo per i flussi audio codificati con il codec Windows Media Audio 9 Professional. Se questa impostazione è impostata su true, è necessario specificare anche la configurazione del relatore del computer client impostando g \_ wszSpeakerConfig. |
| g \_ wszEnableFrameInterpolation | **\_tipo WMT \_ bool**  | Se true, il codec fornirà il flusso video a una [*frequenza di frame*](wmformat-glossary.md)superiore, interpolando i frame algoritmicamente.                                                                                                                                                          |
| g \_ wszJustInTimeDecode         | **\_tipo WMT \_ bool**  | Se true, i dati devono essere decodificati il più tardi possibile. Non supportato nel lettore sincrono.                                                                                                                                                                                                                            |
| g \_ wszNeedsPreviousSample      | **\_tipo WMT \_ bool**  | Se true, per l'esempio è necessario decomprimere l'esempio precedente. Questa impostazione si applica solo ai frame Delta nel video compresso ed è di sola lettura.                                                                                                                                                                       |
| g \_ wszScrambledAudio           | **\_tipo WMT \_ bool**  | Se true, questo output utilizzerà lo schema di occultamento degli errori audio codificati. Questa impostazione è valida solo per gli output audio.                                                                                                                                                                                                |
| g \_ wszSingleOutputBuffer       | **\_tipo WMT \_ bool**  | Se è true, è necessario usare un singolo buffer di output, ad esempio un buffer video di DirectDraw®. Non supportato nel lettore sincrono.                                                                                                                                                                                           |
| g \_ wszSoftwareScaling          | **\_tipo WMT \_ bool**  | Se false, il video non viene ridimensionato. (Non è necessario modificare la risoluzione).                                                                                                                                                                                                                                                |
| g \_ wszSpeakerConfig            | **WMT \_ tipo \_ DWORD** | Se la decodifica audio multicanale è abilitata impostando g \_ wszEnableDiscreteOutput, questa impostazione specifica la configurazione dell'altoparlante del computer client. Impostare su una delle costanti di configurazione dell'altoparlante DirectSound.                                                                                                   |
| g \_ wszStreamLanguage           | **WMT \_ digitare \_ Word**  | Indice nell'elenco di lingue della lingua da recapitare per questo output. Usato per gli output che rappresentano i flussi che si escludono a vicenda per lingua.                                                                                                                                                                      |
| g \_ wszVideoSampleDurations     | **\_tipo WMT \_ bool**  | Se true, il lettore fornirà durate di campionamento accurate.                                                                                                                                                                                                                                                                |
| g \_ wszEnableWMAProSPDIFOutput  | **\_tipo WMT \_ bool**  | Se true, il lettore includerà il formato di interfaccia digitale (S/PDIF) Sony/Phillips nei tipi di output enumerati.                                                                                                                                                                                                       |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IWMReaderAdvanced2::GetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getoutputsetting)
</dt> <dt>

[**IWMReaderAdvanced2::SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting)
</dt> <dt>

[**IWMSyncReader::GetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputsetting)
</dt> <dt>

[**IWMSyncReader::SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setoutputsetting)
</dt> </dl>

 

 




