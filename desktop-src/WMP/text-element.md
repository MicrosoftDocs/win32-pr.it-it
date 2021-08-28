---
title: Elemento TEXT (Windows Media Player SDK)
description: Elemento TEXT
ms.assetid: 4523fe7a-a77a-4bf2-9195-3943bff0eb21
keywords:
- Windows Media Player skin, elemento TEXT
- skins,elemento TEXT
- Elemento TEXT
- riferimento per le skin, elemento TEXT
- elementi,TEXT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 333c0d30393ef4fdeb62061ee58b0c7bd2f3f58bd685945e62c0e8062f22d881
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122851"
---
# <a name="text-element"></a>Elemento TEXT

**L'elemento TEXT** consente di creare e controllare l'aspetto del testo all'interno di un'interfaccia usando gli attributi seguenti. Gli elementi **TEXT predefiniti** vengono forniti anche per praticità.

**L'elemento TEXT** supporta gli attributi seguenti.



| Attributo                                                   | Descrizione                                                                                                 |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [Backgroundcolor](text-backgroundcolor.md)                 | Specifica o recupera il colore di sfondo per il controllo Text.                                           |
| [cursor](text-cursor.md)                                   | Specifica o recupera un valore che indica quale cursore viene visualizzato quando il mouse si trova sul controllo Text.     |
| [disabledBackgroundColor](text-disabledbackgroundcolor.md) | Specifica o recupera il colore di sfondo utilizzato per il controllo Text quando è disabilitato.                  |
| [disabledFontStyle](text-disabledfontstyle.md)             | Specifica o recupera lo stile del carattere utilizzato per il controllo Text quando è disabilitato.                        |
| [disabledForegroundColor](text-disabledforegroundcolor.md) | Specifica o recupera il colore del testo utilizzato quando il controllo Text è disabilitato.                               |
| [fontFace](text-fontface.md)                               | Specifica o recupera il carattere tipografico per il controllo Text.                                                   |
| [Fontsize](text-fontsize.md)                               | Specifica o recupera le dimensioni del carattere per il controllo Text.                                                  |
| [fontSmoothing](text-fontsmoothing.md)                     | Specifica o recupera un valore che indica se l'arrotondamento del carattere è abilitato.                                |
| [Fontstyle](text-fontstyle.md)                             | Specifica o recupera lo stile del carattere per il controllo Text.                                                 |
| [foregroundColor](text-foregroundcolor.md)                 | Specifica o recupera il colore del testo per il controllo Text.                                                 |
| [hoverBackgroundColor](text-hoverbackgroundcolor.md)       | Specifica o recupera il colore di sfondo utilizzato per il controllo Text quando il cursore del mouse viene posizionato su di esso. |
| [hoverFontStyle](text-hoverfontstyle.md)                   | Specifica o recupera lo stile del carattere utilizzato per il controllo Text quando il cursore del mouse viene posizionato su di esso.       |
| [hoverForegroundColor](text-hoverforegroundcolor.md)       | Specifica o recupera il colore del testo utilizzato per il controllo Text quando il cursore del mouse viene posizionato su di esso.       |
| [Giustificazione](text-justification.md)                     | Specifica o recupera l'allineamento del testo all'interno del controllo Text.                                   |
| [Scorrimento](text-scrolling.md)                             | Specifica o recupera un valore che indica se il testo scorre.                                         |
| [scrollingAmount](text-scrollingamount.md)                 | Specifica o recupera il numero di pixel che il testo sposta durante ogni movimento di scorrimento.             |
| [scrollingDelay](text-scrollingdelay.md)                   | Specifica o recupera il ritardo temporale tra i movimenti di scorrimento.                                          |
| [scrollingDirection](text-scrollingdirection.md)           | Specifica o recupera la direzione del testo a scorrimento.                                                 |
| [textWidth](text-textwidth.md)                             | Recupera la larghezza in pixel della stringa contenuta **nell'attributo value.**                           |
| [Descrizione comandi](text-tooltip.md)                                 | Specifica o recupera il testo della descrizione comando per il controllo testo.                                               |
| [value](text-value.md)                                     | Specifica o recupera il testo visualizzato nel controllo Text.                                      |
| [Wordwrap](text-wordwrap.md)                               | Specifica o recupera un valore che indica se il ritorno a capo automatico è abilitato o disabilitato.                     |



 

**L'elemento TEXT** supporta gli attributi di ambiente e può implementare i gestori eventi di ambiente. Per altre informazioni, vedere [Attributi di ambiente](ambient-attributes.md) e Gestori eventi di [ambiente](ambient-event-handlers.md).

Gli elementi di testo predefiniti sono normali **elementi TEXT** con diverse impostazioni di attributi comuni specificate per impostazione predefinita. Sono disponibili gli elementi di testo predefiniti seguenti.



| TESTO predefinito                                | Descrizione                                                                                |
|------------------------------------------------|--------------------------------------------------------------------------------------------|
| [CURRENTPOSITIONTEXT](currentpositiontext.md) | Elemento **TEXT** con un listener predefinito per **player.controls.currentPositionString.** |
| [DURATIONTEXT](durationtext.md)               | Elemento **TEXT** con un listener predefinito per **player.currentMedia.DurationString**.    |
| [STATUSTEXT](statustext.md)                   | Elemento **TEXT** con un listener predefinito per **player.status.**                         |
| [TRACKNAMETEXT](tracknametext.md)             | Elemento **TEXT** con un listener predefinito **per** player.currentMedia.name .              |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni di riferimento sulla programmazione dell'interfaccia**](skin-programming-reference.md)
</dt> </dl>

 

 




