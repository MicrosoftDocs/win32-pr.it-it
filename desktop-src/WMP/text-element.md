---
title: Elemento TEXT (Windows Media Player SDK)
description: Elemento TEXT
ms.assetid: 4523fe7a-a77a-4bf2-9195-3943bff0eb21
keywords:
- Interfacce Media Player di Windows, elemento di testo
- Skin, elemento di testo
- Elemento TEXT
- riferimento per le interfacce, elemento di testo
- elementi, testo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acdad737fda44cc0e090eb13fb20c765b447ccbd
ms.sourcegitcommit: 40a1246849dba8ececf54c716b2794b99c96ad50
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/12/2019
ms.locfileid: "104335428"
---
# <a name="text-element"></a>Elemento TEXT

L'elemento di **testo** fornisce un modo per creare e controllare l'aspetto del testo all'interno di un'interfaccia utilizzando gli attributi seguenti. Gli elementi di **testo** predefiniti sono inoltre disponibili per praticità.

L'elemento di **testo** supporta i seguenti attributi.



| Attributo                                                   | Descrizione                                                                                                 |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [backgroundColor](text-backgroundcolor.md)                 | Specifica o Recupera il colore di sfondo per il controllo di testo.                                           |
| [cursor](text-cursor.md)                                   | Specifica o recupera un valore che indica quale cursore viene visualizzato quando il mouse è posizionato sul controllo di testo.     |
| [disabledBackgroundColor](text-disabledbackgroundcolor.md) | Specifica o Recupera il colore di sfondo utilizzato per il controllo di testo quando è disabilitato.                  |
| [disabledFontStyle](text-disabledfontstyle.md)             | Specifica o recupera lo stile del carattere utilizzato per il controllo di testo quando è disabilitato.                        |
| [disabledForegroundColor](text-disabledforegroundcolor.md) | Specifica o Recupera il colore del testo utilizzato quando il controllo testo è disabilitato.                               |
| [fontFace](text-fontface.md)                               | Specifica o Recupera il carattere tipografico per il controllo di testo.                                                   |
| [fontSize](text-fontsize.md)                               | Specifica o recupera le dimensioni del carattere per il controllo di testo.                                                  |
| [fontSmoothing](text-fontsmoothing.md)                     | Specifica o recupera un valore che indica se la smussatura dei caratteri è abilitata.                                |
| [fontStyle](text-fontstyle.md)                             | Specifica o recupera lo stile del carattere per il controllo di testo.                                                 |
| [foregroundColor](text-foregroundcolor.md)                 | Specifica o Recupera il colore del testo per il controllo di testo.                                                 |
| [hoverBackgroundColor](text-hoverbackgroundcolor.md)       | Specifica o Recupera il colore di sfondo utilizzato per il controllo di testo quando il cursore del mouse viene posizionato su di esso. |
| [hoverFontStyle](text-hoverfontstyle.md)                   | Specifica o recupera lo stile del carattere utilizzato per il controllo di testo quando il cursore del mouse viene posizionato su di esso.       |
| [hoverForegroundColor](text-hoverforegroundcolor.md)       | Specifica o Recupera il colore del testo utilizzato per il controllo di testo quando il cursore del mouse viene posizionato su di esso.       |
| [giustificazione](text-justification.md)                     | Specifica o recupera l'allineamento del testo all'interno del controllo di testo.                                   |
| [scorrimento](text-scrolling.md)                             | Specifica o recupera un valore che indica se lo scorrimento del testo viene eseguito.                                         |
| [scrollingAmount](text-scrollingamount.md)                 | Specifica o Recupera il numero di pixel spostati dal testo durante ogni spostamento dello scorrimento.             |
| [scrollingDelay](text-scrollingdelay.md)                   | Specifica o recupera l'intervallo di tempo tra i movimenti di scorrimento.                                          |
| [scrollingDirection](text-scrollingdirection.md)           | Specifica o recupera la direzione del testo di scorrimento.                                                 |
| [textWidth](text-textwidth.md)                             | Recupera la larghezza in pixel della stringa contenuta nell'attributo **value** .                           |
| [Descrizione comando](text-tooltip.md)                                 | Specifica o Recupera il testo della descrizione comando per il controllo di testo.                                               |
| [value](text-value.md)                                     | Specifica o Recupera il testo visualizzato nel controllo di testo.                                      |
| [wordWrap](text-wordwrap.md)                               | Specifica o recupera un valore che indica se il ritorno a capo automatico è abilitato o disabilitato.                     |



 

L'elemento di **testo** supporta gli attributi di ambiente e può implementare i gestori eventi di ambiente. Per altre informazioni, vedere [attributi di ambiente](ambient-attributes.md) e [gestori di eventi di ambiente](ambient-event-handlers.md).

Gli elementi di testo predefiniti sono elementi di **testo** normali con diverse impostazioni degli attributi comuni specificati per impostazione predefinita. Sono disponibili gli elementi di testo predefiniti seguenti.



| TESTO predefinito                                | Descrizione                                                                                |
|------------------------------------------------|--------------------------------------------------------------------------------------------|
| [CURRENTPOSITIONTEXT](currentpositiontext.md) | Elemento di **testo** con un listener incorporato per **Player. Controls. currentPositionString**. |
| [DURATIONTEXT](durationtext.md)               | Elemento di **testo** con un listener incorporato per **Player. currentMedia. DurationString**.    |
| [STATUSTEXT](statustext.md)                   | Elemento di **testo** con un listener incorporato per **Player. status**.                         |
| [TRACKNAMETEXT](tracknametext.md)             | Elemento di **testo** con un listener incorporato per **Player.currentMedia.Name**.              |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni di riferimento sulla programmazione dell'interfaccia**](skin-programming-reference.md)
</dt> </dl>

 

 




