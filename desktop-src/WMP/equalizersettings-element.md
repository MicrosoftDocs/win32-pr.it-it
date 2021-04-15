---
title: Elemento EQUALIZERSETTINGS
description: Elemento EQUALIZERSETTINGS
ms.assetid: 521f1c95-7904-4085-a8bc-5399d667dfb1
keywords:
- Windows Media Player Skin, elemento EQUALIZERSETTINGS
- interfacce, elemento EQUALIZERSETTINGS
- Elemento EQUALIZERSETTINGS
- riferimento per le interfacce, elemento EQUALIZERSETTINGS
- elementi, EQUALIZERSETTINGS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae20500dfba656450c3102ee80b4a06e089fe8ff
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515781"
---
# <a name="equalizersettings-element"></a>Elemento EQUALIZERSETTINGS

L'elemento **EQUALIZERSETTINGS** fornisce un modo per modificare il equalizzatore grafico e altre impostazioni audio di Windows Media Player usando gli attributi e il metodo elencati qui.

L'elemento **EQUALIZERSETTINGS** supporta i seguenti attributi.



| Attributo                                                          | Descrizione                                                                                             |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [bande](equalizersettings-bands.md)                               | Recupera il numero di bande di frequenza supportate.                                                      |
| [bypass](equalizersettings-bypass.md)                             | Specifica o recupera un valore che indica se il filtro dell'equalizzatore viene ignorato nel grafico del filtro. |
| [crossFade](equalizersettings-crossfade.md)                       | Specifica o recupera un valore che indica se la dissolvenza incrociata è abilitata.                                |
| [crossFadeWindow](equalizersettings-crossfadewindow.md)           | Specifica o recupera la quantità di sovrapposizione tra dissolvenza incrociata in millisecondi.                                |
| [currentPreset](equalizersettings-currentpreset.md)               | Specifica o recupera l'indice del set di impostazioni corrente.                                                 |
| [currentPresetTitle](equalizersettings-currentpresettitle.md)     | Recupera il titolo del set di impostazioni corrente.                                                              |
| [currentSpeakerName](equalizersettings-currentspeakername.md)     | Recupera il nome dell'impostazione del relatore corrente.                                                      |
| [enableSplineTension](equalizersettings-enablesplinetension.md)   | Specifica o recupera un valore che indica se la tensione spline è abilitata o disabilitata.                |
| [enhancedAudio](equalizersettings-enhancedaudio.md)               | Specifica o recupera un valore che indica se l'audio avanzato è attivato.                          |
| [gainLevels](equalizersettings-gainlevels.md)                     | Specifica o Recupera il livello di guadagno della banda corrispondente all'indice fornito.                  |
| [gainLevel1](equalizersettings-gainlevel1.md)                     | Specifica o Recupera il livello di guadagno della banda 1.                                                        |
| [gainLevel2](equalizersettings-gainlevel2.md)                     | Specifica o Recupera il livello di guadagno della banda 2.                                                        |
| [gainLevel3](equalizersettings-gainlevel3.md)                     | Specifica o Recupera il livello di guadagno della banda 3.                                                        |
| [gainLevel4](equalizersettings-gainlevel4.md)                     | Specifica o Recupera il livello di guadagno della banda 4.                                                        |
| [gainLevel5](equalizersettings-gainlevel5.md)                     | Specifica o Recupera il livello di guadagno della banda 5.                                                        |
| [gainLevel6](equalizersettings-gainlevel6.md)                     | Specifica o Recupera il livello di guadagno della banda 6.                                                        |
| [gainLevel7](equalizersettings-gainlevel7.md)                     | Specifica o Recupera il livello di guadagno della banda 7.                                                        |
| [gainLevel8](equalizersettings-gainlevel8.md)                     | Specifica o Recupera il livello di guadagno della banda 8.                                                        |
| [gainLevel9](equalizersettings-gainlevel9.md)                     | Specifica o Recupera il livello di guadagno della banda 9.                                                        |
| [gainLevel10](equalizersettings-gainlevel10.md)                   | Specifica o Recupera il livello di guadagno della banda 10.                                                       |
| [normalizzazione](equalizersettings-normalization.md)               | Specifica o recupera un valore che indica se la normalizzazione è abilitata.                             |
| [normalizationAverage](equalizersettings-normalizationaverage.md) | Recupera il valore di normalizzazione medio.                                                              |
| [normalizationPeak](equalizersettings-normalizationpeak.md)       | Recupera il valore di normalizzazione del picco.                                                                 |
| [presetCount](equalizersettings-presetcount.md)                   | Recupera il numero di set di impostazioni disponibili.                                                              |
| [speakerSize](equalizersettings-speakersize.md)                   | Specifica o recupera l'indice della dimensione del relatore corrente.                                           |
| [splineTension](equalizersettings-splinetension.md)               | Specifica o recupera la tensione della spline per il controllo dell'equalizzatore.                                    |
| [truBassLevel](equalizersettings-trubasslevel.md)                 | Specifica o Recupera il livello di TruBass SRS.                                                           |
| [wowLevel](equalizersettings-wowlevel.md)                         | Specifica o Recupera il livello di effetto SRS WOW.                                                        |



 

L'elemento **EQUALIZERSETTINGS** supporta i metodi seguenti.



| Metodo                                                 | Descrizione                                                          |
|--------------------------------------------------------|----------------------------------------------------------------------|
| [nextPreset](equalizersettings-nextpreset.md)         | Applica il set di impostazioni di equalizzatore successivo.                                   |
| [presetTitle](equalizersettings-presettitle.md)       | Recupera il nome del set di impostazioni dell'equalizzatore con l'indice specificato. |
| [previousPreset](equalizersettings-previouspreset.md) | Applica il set di impostazioni di equalizzatore precedente.                               |
| [reset](equalizersettings-reset.md)                   | Reimposta i livelli di guadagno di tutte le bande su zero decibel.                |



 

L'elemento **EQUALIZERSETTINGS** può implementare i gestori eventi [ \_ OnChange dell'attributo](attribute-onchange.md) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni di riferimento sulla programmazione dell'interfaccia**](skin-programming-reference.md)
</dt> </dl>

 

 




