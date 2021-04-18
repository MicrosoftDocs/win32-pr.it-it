---
title: Per utilizzare il controllo intervallo dinamico
description: Per utilizzare il controllo intervallo dinamico
ms.assetid: 719658c1-952f-4e8f-a3ea-bdf89a0a7268
keywords:
- Windows Media Format SDK, controllo intervallo dinamico
- Windows Media Format SDK, il codec Windows Media Audio 9 Professional
- Windows Media Format SDK, Windows Media Audio 9 codec lossless
- Codec ASF (Advanced Systems Format), Windows Media Audio 9 Professional
- ASF (Advanced Systems Format), Windows Media Audio 9 Professional codec
- ASF (Advanced Systems Format), codec Windows Media Audio 9 Lossless
- ASF (Advanced Systems Format), Windows Media Audio 9 codec lossless
- ASF (Advanced Systems Format), controllo intervallo dinamico
- ASF (formato avanzato dei sistemi), controllo intervallo dinamico
- controllo intervallo dinamico
- codecs, Windows Media Audio 9 codec lossless
- codec, codec Windows Media Audio 9 Professional
- Codec Windows Media Audio 9 Lossless, controllo intervallo dinamico
- Codec Windows Media Audio 9 Professional, controllo intervallo dinamico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 077ebc0052d0154aec395f371a5c2dc3ffd46c67
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "106299391"
---
# <a name="to-use-dynamic-range-control"></a>Per utilizzare il controllo intervallo dinamico

L'intervallo dinamico di un frammento di contenuto audio è fondamentalmente la differenza tra il volume più basso e il volume massimo. Se l'intervallo dinamico del contenuto è troppo elevato, gli utenti potrebbero ritrovarsi a modificare il volume ripetutamente durante la riproduzione. Ad esempio, i film hanno spesso un intervallo dinamico elevato. Spesso, quando il volume viene regolato in modo che sia possibile comprendere la finestra di dialogo durante le situazioni di silenzio, altre parti del film con musica o effetti audio sono più potenti del necessario.

I codec Windows Media Audio 9 Professional e Windows Media Audio 9 Lossless supportano una funzionalità denominata controllo dinamico degli intervalli. Al momento della codifica, il codec calcola i valori di picco e di ampiezza media nel contenuto e l'oggetto writer archivia questi valori nei metadati per il flusso al termine della codifica. Facoltativamente, un'applicazione può anche scrivere valori di "destinazione" come metadati che le applicazioni del lettore e il decodificatore possono usare come hint per la riproduzione del file. Al momento della riproduzione, un'applicazione può specificare il livello di controllo intervallo dinamico da applicare al flusso audio.

Windows Media Player implementa il controllo intervallo dinamico come funzionalità di modalità non interattiva.

## <a name="when-to-use-dynamic-range-control"></a>Quando usare il controllo dinamico degli intervalli

Il controllo intervallo dinamico può modificare il suono del contenuto. Per questo motivo, non è consigliabile configurare l'applicazione in modo che utilizzi automaticamente il controllo dinamico degli intervalli. Al contrario, fornire agli utenti la possibilità di attivare o disattivare il controllo dinamico degli intervalli in base alle esigenze.

## <a name="using-dynamic-range-control"></a>Uso del controllo intervallo dinamico

Al momento della riproduzione, il controllo intervallo dinamico viene attivato utilizzando l'impostazione di output g \_ wszDynamicRangeControl. Usare [**IWMReaderAdvanced2:: SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) per configurare l'impostazione. Il valore zero (impostazione predefinita) indica che l'intervallo dinamico non deve essere modificato. Il valore 1 o 2 segnala al codec di eseguire un controllo dell'intervallo dinamico, dove 1 è un livello moderato di compressione dell'intervallo dinamico e 2 è un livello elevato di compressione dinamica degli intervalli.

Al momento della codifica o del tempo di riproduzione, è possibile assegnare al codec i valori PCM di destinazione per i livelli Peak e Average impostando rispettivamente gli attributi [**WM/WMADRCPeakTarget**](wm-wmadrcpeaktarget.md) e [**WM/WMADRCAverageTarget**](wm-wmadrcaveragetarget.md) . Questi valori vengono archiviati come attributi di metadati ed è necessario accedervi utilizzando i metodi dell'interfaccia [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) . Quando si codifica un flusso audio usando il codec Professional o senza perdita di dati, gli attributi [**WM/WMADRCPeakReference**](wm-wmadrcpeakreference.md) e [**WM/WMADRCAverageReference**](wm-wmadrcaveragereference.md) vengono impostati automaticamente sui livelli di picco e medio del contenuto originale. Per impostazione predefinita, i valori di destinazione sono impostati sugli stessi valori dei riferimenti.

Il decodificatore al momento della riproduzione calcola l'intervallo dinamico in base al livello selezionato di controllo intervallo dinamico e ai valori di destinazione (se specificati). Gli intervalli possibili sono illustrati nella tabella seguente.



| Impostazioni                                                                | Intervallo di audio recapitato                                                                                                     |
|-------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| g \_ wszDynamicRangeControl = 0 (qualsiasi valore di destinazione)                       | Stesso intervallo del contenuto originale.                                                                                          |
| g \_ wszDynamicRangeControl = 1 (valori di destinazione uguali ai valori di riferimento) | Il livello medio viene mantenuto e i picchi sono limitati alla media + 12 dB.                                                    |
| g \_ wszDynamicRangeControl = 2 (valori di destinazione uguali ai valori di riferimento) | Il livello medio viene mantenuto e i picchi sono limitati alla media di + 6 dB.                                                     |
| g \_ wszDynamicRangeControl = 1 (valori di destinazione specificati)                 | Il livello medio è impostato sul valore medio di destinazione e i picchi sono limitati al valore di picco di destinazione.                                   |
| g \_ wszDynamicRangeControl = 2 (valori di destinazione specificati)                 | Il livello medio è impostato sul valore medio di destinazione e i picchi sono limitati alla mediana della media di destinazione e ai valori di picco di destinazione. |



 

Si noti che il controllo intervallo dinamico è una funzionalità di decodifica solo ed esiste solo come metadati nel file stesso. Queste impostazioni non hanno effetto sul contenuto archiviato nel file, a meno che non si indichi in modo specifico il decodificatore per usarle. Windows Media Format SDK non fornisce metodi per la modifica dell'intervallo dinamico dei dati audio al momento della codifica.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Argomenti avanzati**](advanced-topics.md)
</dt> </dl>

 

 




