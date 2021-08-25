---
description: Enumerazione dei tipi audio per modalità di codifica specifiche
ms.assetid: d44960eb-da5e-4379-ba9d-cb804559dc53
title: Enumerazione dei tipi audio per modalità di codifica specifiche (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ec311c9ac4d879f8834d50353913e7fad1b6e50a9292a44444bc45376247636
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828241"
---
# <a name="enumerating-audio-types-for-specific-encoding-modes-microsoft-media-foundation"></a>Enumerazione dei tipi audio per modalità di codifica specifiche (Microsoft Media Foundation)

I tipi di supporti di input e output accettati dal codificatore audio sono molto strutturati. È necessario ottenere i tipi di output supportati chiamando **il metodo IMediaObject::GetOutputType** o **IMFTransform::GetOutputType**. Dopo aver restituito un tipo di output, non è necessario modificarlo.

Se si vuole usare una modalità di codifica diversa da CBR a un passaggio, è necessario impostare la modalità e quindi enumerare i tipi di output per tale modalità. il codificatore modifica i tipi di output supportati a seconda della modalità impostata. Le proprietà che controllano la modalità di codifica [**sono MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) e [**MFPKEY \_ PASSESUSED.**](mfpkey-passesusedproperty.md) Quando la modalità è impostata nel codificatore, è necessario enumerare e selezionare un tipo di output, usandolo senza alterazione, come con CBR.

## <a name="identifying-quality-based-vbr-types"></a>Identificazione dei tipi VBR basati sulla qualità

La procedura per identificare i tipi VBR basati sulla qualità dipende dal fatto che il codificatore agirà come oggetto multimediale DirectX (DMO) o come una trasformazione Media Foundation (MFT). Per informazioni su quando un codificatore funge da DMO o MFT, vedere le singole pagine di riferimento del codec in [Codec Objects (Oggetti codec).](codecobjects.md)

Quando un codificatore audio funge da DMO e si configura il codificatore per l'uso di VBR a un passaggio, enumera tutti i tipi di output supportati. Tuttavia, in genere è necessario selezionare un tipo VBR a un passaggio in base al parametro quality. Il codificatore inserisce il valore di qualità per i tipi di output VBR a un passaggio nel membro **nAvgBytesPerSec** della struttura **WAVEFORMATEX** a cui punta **DMO MEDIA \_ \_ TYPE.pbFormat**.

Questo valore viene archiviato nel formato seguente: 0x7FFFFFXX, dove XX è il valore di qualità (da 0 a 100). Ad esempio, il **valore nAvgBytesPerSec** di 0x7FFFFF62 specifica il livello di qualità 98 (0x62 = 98).

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



Quando il codificatore funge da MFT ed enumera un tipo di output in una chiamata a **GetAvailableOutputType,** è possibile eseguire una query su MFT per la proprietà **MFPKEY \_ MOST RECENTLY \_ \_ ENUMERATED \_ VBRQUALITY.** Il valore restituito indica la qualità VBR del tipo di supporto di output restituito più di recente. È quindi possibile usare tale valore per impostare la [**proprietà MFPKEY \_ DESIRED \_ VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md) del codificatore.

## <a name="setting-peak-constraints"></a>Impostazione dei vincoli di picco

Per vbr basato sulla qualità (one-pass) e VBR a due passaggi non vincolato, non sono necessarie impostazioni aggiuntive dopo il recupero del tipo di output. Per usare vbr con vincoli di picco, recuperare un tipo di output con VBR abilitato e due passaggi impostati. Questo tipo, senza modifica, descrive le impostazioni vbr senza vincoli. Per impostare i vincoli di picco, impostare le [proprietà MFPKEY \_ RMAX](mfpkey-rmaxproperty.md) e [MFPKEY \_ BMAX.](mfpkey-bmaxproperty.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Configurazione della codifica audio](configuringaudioencoding.md)
</dt> <dt>

[Ricerca dei tipi di output del codificatore audio](findingaudioencoderoutputtypes.md)
</dt> <dt>

[Uso Two-Pass codifica](usingtwoencodingpasses.md)
</dt> <dt>

[Uso della codifica VBR](usingvbrencoding.md)
</dt> </dl>

 

 



