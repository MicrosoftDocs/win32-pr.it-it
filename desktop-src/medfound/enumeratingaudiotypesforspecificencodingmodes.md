---
description: Enumerazione dei tipi audio per modalità di codifica specifiche
ms.assetid: d44960eb-da5e-4379-ba9d-cb804559dc53
title: Enumerazione dei tipi audio per modalità di codifica specifiche (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a16a8b97afdd48cb1d7828f80778aa9fcf8dc1ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401533"
---
# <a name="enumerating-audio-types-for-specific-encoding-modes-microsoft-media-foundation"></a>Enumerazione dei tipi audio per modalità di codifica specifiche (Microsoft Media Foundation)

I tipi di supporto di input e di output accettati dal codificatore audio sono molto strutturati. È necessario ottenere i tipi di output supportati chiamando il metodo **IMediaObject:: GetOutputType** o **IMFTransform:: GetOutputType**. Una volta ottenuto un tipo di output, non è necessario modificarlo.

Se si vuole usare una modalità di codifica diversa da un CBR a un passaggio, è necessario impostare la modalità e quindi enumerare i tipi di output per tale modalità; il codificatore modifica i tipi di output supportati a seconda della modalità impostata. Le proprietà che controllano la modalità di codifica sono [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) e [**MFPKEY \_ PASSESUSED**](mfpkey-passesusedproperty.md). Quando la modalità è impostata nel codificatore, è necessario enumerare e selezionare un tipo di output, usandolo senza modifiche, come per CBR.

## <a name="identifying-quality-based-vbr-types"></a>Identificazione di tipi VBR basati sulla qualità

La procedura per identificare i tipi VBR basati sulla qualità varia a seconda che il codificatore funga da oggetto DMO (DirectX Media Object) o funga da Media Foundation Transform (MFT). Per informazioni su quando un codificatore funge da DMO o da un MFT, vedere le pagine di riferimento del singolo codec in [oggetti codec](codecobjects.md).

Quando un codificatore audio funge da DMO e si configura il codificatore per l'uso di un VBR con un solo passaggio, vengono enumerati tutti i tipi di output supportati. Tuttavia, in genere si vuole selezionare un tipo VBR a un passaggio basato sul parametro Quality. Il codificatore inserisce il valore di qualità per i tipi di output VBR a un passaggio nel membro **nAvgBytesPerSec** della struttura **WAVEFORMATEX** a cui fa riferimento **DMO \_ media \_ Type. pbFormat**.

Questo valore viene archiviato nel formato seguente: 0x7FFFFFXX, dove XX è il valore qualitativo (compreso tra 0 e 100). Il valore **nAvgBytesPerSec** di 0x7FFFFF62, ad esempio, specifica il livello di qualità 98 (0x62 = 98).

Nell'esempio seguente viene illustrato come controllare il livello di qualità di un formato quando il codificatore funge da DMO.


```
void ShowQuality(WAVEFORMATEX* pWave)
{
    // Store the average bytes per second in a local variable
    // with a more manageable name.
    DWORD dwBps = pWave->nAvgBytesPerSec;

    // Verify that the value is a VBR quality level by using 
    // a bitmask to check for the bit pattern 0x7FFFFFXX. 
    if(dwBps & 0x7FFFFF00 == 0x7FFFFF00)
        printf("VBR Quality: %d%%\n",(dwBps & 0x000000FF));
    else // Not a valid VBR quality value.
        printf("Not a valid one-pass VBR audio format.\n");
}
```



Quando il codificatore funge da MFT ed enumera un tipo di output in una chiamata a **GetAvailableOutputType**, è possibile eseguire una query su MFT per la **proprietà \_ \_ \_ \_ VBRQUALITY enumerata più di recente MFPKEY** . Il valore restituito indica la qualità VBR del tipo di supporto di output restituito più di recente. È quindi possibile usare tale valore per impostare la [**proprietà \_ \_ VBRQUALITY desiderata MFPKEY**](mfpkey-desired-vbrqualityproperty.md) del codificatore.

## <a name="setting-peak-constraints"></a>Impostazione di vincoli di picco

Per la qualità VBR (One-Pass) e il VBR con due passaggi non vincolati, non sono necessarie impostazioni aggiuntive dopo il recupero del tipo di output. Per usare un VBR con vincoli di picco, recuperare un tipo di output con VBR abilitato e due set di sessioni. Questo tipo, senza modifiche, descrive le impostazioni VBR non vincolate. Per impostare i vincoli di picco, impostare le proprietà [MFPKEY \_ Rmax](mfpkey-rmaxproperty.md) e [MFPKEY \_ BMAX](mfpkey-bmaxproperty.md) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Configurazione della codifica audio](configuringaudioencoding.md)
</dt> <dt>

[Ricerca di tipi di output del codificatore audio](findingaudioencoderoutputtypes.md)
</dt> <dt>

[Uso della codifica Two-Pass](usingtwoencodingpasses.md)
</dt> <dt>

[Uso della codifica VBR](usingvbrencoding.md)
</dt> </dl>

 

 



