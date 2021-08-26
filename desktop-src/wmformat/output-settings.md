---
title: Impostazioni di output
description: Impostazioni di output
ms.assetid: effe6c07-e6df-45b0-b865-2a025c466d6f
keywords:
- Windows Media Format SDK, costanti globali
- Advanced Systems Format (ASF), costanti globali
- ASF (Advanced Systems Format), costanti globali
- costanti globali, elenco di
- Windows Media Format SDK,costanti
- Advanced Systems Format (ASF), costanti
- ASF (Advanced Systems Format), costanti
- costanti, elenco di
- Windows Media Format SDK, impostazioni di output
- Advanced Systems Format (ASF), impostazioni di output
- ASF (Advanced Systems Format), impostazioni di output
- impostazioni di output
- lettori sincroni,impostazioni di output
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 966cd350d379170f9f19c44967ef932bf41a15cb1910b865432ce499b006161e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119929941"
---
# <a name="output-settings"></a>Impostazioni di output

Le costanti globali seguenti vengono usate per identificare le impostazioni di output per il lettore e l'oggetto lettore sincrono.



| Costante globale                | TIPO DI \_ DATI WMT ATTR \_  | Descrizione di *pValue*                                                                                                                                                                                                                                                                                                    |
|--------------------------------|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| g \_ wszAllowInterlacedOutput    | **TIPO WMT \_ \_ BOOL**  | Se True, il lettore consegnerà fotogrammi interlacciati, se supportato dall'output.                                                                                                                                                                                                                                            |
| g \_ wszDedicatedDeliveryThread  | **TIPO WMT \_ \_ BOOL**  | Se True, questo output avrà un thread dedicato creato per il recapito dei relativi esempi. Non supportato nel lettore sincrono.                                                                                                                                                                                            |
| g \_ wszDeliverOnReceive         | **TIPO WMT \_ \_ BOOL**  | Se True, gli esempi per questo output verranno recapitati non appena saranno disponibili dal lettore. In questo modo, gli esempi di questo output vengono recapitati in ordine e prima degli esempi corrispondenti di altri output.                                                                                            |
| g \_ wszDynamicRangeControl      | **DWORD \_ DI TIPO \_ WMT** | Specifica il livello di controllo dell'intervallo dinamico da utilizzare per l'output. Impostare su un valore compreso tra 0 e 2, dove 0 indica nessun controllo di intervallo dinamico (impostazione predefinita) e 2 è il livello massimo di controllo dell'intervallo dinamico (l'intervallo dinamico più piccolo).                                                                                |
| g \_ wszEarlyDataDelivery        | **DWORD \_ DI TIPO \_ WMT** | Tempo, espresso in millisecondi, che specifica quanto prima per distribuire gli esempi. Se è maggiore di zero, gli esempi di questo output verranno recuperati e decodificati in modo che gli esempi siano forniti prima degli esempi per altri output. In genere il lettore fornisce esempi in ordine di tempo di presentazione.         |
| g \_ wszEnableDiscreteOutput     | **TIPO WMT \_ \_ BOOL**  | Se True, il lettore abiliterà l'output audio multicanale ad alta definizione. Questa impostazione è valida solo per i flussi audio codificati con il codec Windows Media Audio 9 Professional. Se questa impostazione è impostata su true, è necessario specificare anche la configurazione del parlante del computer client impostando g \_ wszSpeakerConfig. |
| g \_ wszEnableFrameInterpolation | **TIPO WMT \_ \_ BOOL**  | Se True, il codec consegnerà il flusso video a una [*frequenza di fotogrammi*](wmformat-glossary.md)superiore, interpolando i fotogrammi in modo algoritmico.                                                                                                                                                          |
| g \_ wszJustInTimeDecode         | **TIPO WMT \_ \_ BOOL**  | Se True, i dati devono essere decodificati il più tardi possibile. Non supportato nel lettore sincrono.                                                                                                                                                                                                                            |
| g \_ wszNeedsPreviousSample      | **TIPO WMT \_ \_ BOOL**  | Se true, l'esempio richiede che l'esempio precedente sia decompresso. Questa impostazione si applica solo ai fotogrammi differenziali nel video compresso ed è di sola lettura.                                                                                                                                                                       |
| g \_ wszScrambledAudio           | **TIPO WMT \_ \_ BOOL**  | Se True, questo output userà lo schema di mascheramento degli errori audio non codificati. Si tratta di un'impostazione valida solo per gli output audio.                                                                                                                                                                                                |
| g \_ wszSingleOutputBuffer       | **TIPO WMT \_ \_ BOOL**  | Se True, è necessario usare un singolo buffer di output, ad esempio un buffer video DirectDraw® video. Non supportato nel lettore sincrono.                                                                                                                                                                                           |
| g \_ wszSoftwareScaling          | **TIPO WMT \_ \_ BOOL**  | Se False, il video non viene ridimensionato. Non deve essere apportata alcuna modifica alla risoluzione.                                                                                                                                                                                                                                                |
| g \_ wszSpeakerConfig            | **DWORD \_ DI TIPO \_ WMT** | Se la decodifica audio multicanale è abilitata impostando g wszEnableDiscreteOutput, questa impostazione specifica la configurazione del parlante \_ del computer client. Impostare su una delle costanti di configurazione della voce DirectSound.                                                                                                   |
| g \_ wszStreamLanguage           | **WMT \_ TYPE \_ WORD**  | Indice nell'elenco di lingue della lingua da recapitare per questo output. Usato per gli output che rappresentano flussi che si escludono a vicenda in base al linguaggio.                                                                                                                                                                      |
| g \_ wszVideoSampleDurations     | **TIPO WMT \_ \_ BOOL**  | Se True, il lettore consegnerà durate di campionamento accurate.                                                                                                                                                                                                                                                                |
| g \_ wszEnableWMAProSPDIFOutput  | **TIPO WMT \_ \_ BOOL**  | Se True, il lettore includerà il formato S/PDIF (Digital Interface Format) di Sony/Philips nei tipi di output enumerati.                                                                                                                                                                                                       |



 

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

 

 




