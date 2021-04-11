---
title: Elemento SLIDER
description: Elemento SLIDER
ms.assetid: f1da8987-5430-46ef-b7d7-ac92f34a2185
keywords:
- Interfacce Media Player Windows, elemento SLIDER
- Skin, elemento SLIDER
- Elemento SLIDER
- riferimento per interfacce, elemento SLIDER
- elementi, dispositivo di scorrimento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34607c8706fccc8f416ebc83ae483c98a784c08b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330540"
---
# <a name="slider-element"></a>Elemento SLIDER

L'elemento **Slider** fornisce un modo per creare e modificare un semplice controllo dispositivo di scorrimento orizzontale o verticale. Supporta i seguenti attributi e gestori eventi. Gli elementi del **dispositivo di scorrimento** predefiniti sono inoltre disponibili per praticità.

L'elemento **Slider** supporta gli attributi seguenti.



| Attributo                                                 | Descrizione                                                                                                       |
|-----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [backgroundColor](slider-backgroundcolor.md)             | Specifica o Recupera il colore di sfondo del controllo dispositivo di scorrimento.                                                |
| [backgroundEndColor](slider-backgroundendcolor.md)       | Specifica o Recupera il colore finale dello sfondo del controllo dispositivo di scorrimento.                                         |
| [backgroundHoverImage](slider-backgroundhoverimage.md)   | Consente di specificare o recuperare l'immagine di sfondo del dispositivo di scorrimento visualizzato quando si passa il mouse su di essa.      |
| [backgroundImage](slider-backgroundimage.md)             | Specifica o recupera l'immagine di sfondo predefinita del dispositivo di scorrimento.                                                |
| [borderSize](slider-bordersize.md)                       | Specifica o recupera le dimensioni del bordo in pixel.                                                                 |
| [cursor](slider-cursor.md)                               | Specifica o recupera un valore che indica il tipo di cursore visualizzato quando il mouse è posizionato sul controllo dispositivo di scorrimento. |
| [direction](slider-direction.md)                         | Specifica o recupera la direzione in cui sono disposte le immagini del dispositivo di scorrimento.                                             |
| [disabledColor](slider-disabledcolor.md)                 | Specifica o Recupera il colore disabilitato del controllo dispositivo di scorrimento.                                                  |
| [disabledImage](slider-disabledimage.md)                 | Specifica o recupera l'immagine del dispositivo di scorrimento visualizzato quando il controllo è disabilitato.                         |
| [foregroundColor](slider-foregroundcolor.md)             | Specifica o Recupera il colore di primo piano del controllo dispositivo di scorrimento.                                                |
| [foregroundEndColor](slider-foregroundendcolor.md)       | Specifica o Recupera il colore finale in primo piano del controllo dispositivo di scorrimento.                                         |
| [foregroundHoverImage](slider-foregroundhoverimage.md)   | Specifica o recupera l'immagine in primo piano del dispositivo di scorrimento visualizzato quando si passa il mouse su di esso.      |
| [foregroundImage](slider-foregroundimage.md)             | Specifica o recupera l'immagine in primo piano predefinita del dispositivo di scorrimento.                                                |
| [foregroundProgress](slider-foregroundprogress.md)       | Specifica o recupera la posizione corrente dell'indicatore di stato in primo piano come percentuale dell'area del dispositivo di scorrimento.    |
| [max](slider-max.md)                                     | Specifica o Recupera il valore massimo dell'intervallo definito dal controllo dispositivo di scorrimento.                              |
| [min](slider-min.md)                                     | Specifica o Recupera il valore minimo dell'intervallo definito dal controllo dispositivo di scorrimento.                              |
| [diapositiva](slider-slide.md)                                 | Specifica o recupera un valore che indica se l'immagine in primo piano scorre sull'immagine di sfondo.          |
| [thumbDisabledImage](slider-thumbdisabledimage.md)       | Specifica o recupera l'immagine Thumb disabilitata del controllo dispositivo di scorrimento.                                            |
| [thumbDownImage](slider-thumbdownimage.md)               | Specifica o recupera l'immagine che rappresenta lo stato di inattività del cursore.                                        |
| [thumbHoverImage](slider-thumbhoverimage.md)             | Specifica o recupera l'immagine del cursore visualizzato quando si passa il mouse su di essa.                  |
| [thumbImage](slider-thumbimage.md)                       | Specifica o recupera l'immagine che verrà utilizzata per rappresentare la posizione corrente del dispositivo di scorrimento.               |
| [piastrellati](slider-tiled.md)                                 | Specifica o recupera un valore che indica se le immagini del dispositivo di scorrimento verranno affiancate.                                |
| [Descrizione comando](slider-tooltip.md)                             | Specifica o Recupera il testo della descrizione comando per il controllo dispositivo di scorrimento.                                                   |
| [transparencyColor](slider-transparencycolor.md)         | Specifica o Recupera il colore trasparente delle immagini del dispositivo di scorrimento.                                                |
| [useForegroundProgress](slider-useforegroundprogress.md) | Specifica o recupera un valore che indica se verrà utilizzato l'indicatore di stato in primo piano.                       |
| [value](slider-value.md)                                 | Specifica e recupera la posizione corrente del dispositivo di scorrimento.                                                       |



 

L'elemento **Slider** può implementare i gestori eventi seguenti.



| Gestore di evento                                   | Descrizione                                                                                                          |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [onDragBegin](slider-ondragbegin.md)           | Gestisce un evento che si verifica quando l'utente fa clic e mantiene premuto il pulsante sinistro del mouse e inizia a trascinare il mouse. |
| [onDragEnd](slider-ondragend.md)               | Gestisce un evento che si verifica quando viene rilasciato il pulsante sinistro del mouse dopo un'operazione di trascinamento.                      |
| [onPositionChange](slider-onpositionchange.md) | Gestisce un evento che si verifica quando la posizione del dispositivo di scorrimento viene modificata in seguito alla selezione o al trascinamento dell'utente.   |



 

L'elemento **Slider** supporta gli attributi di ambiente e può implementare i gestori eventi di ambiente. Per altre informazioni, vedere [attributi di ambiente](ambient-attributes.md) e [gestori di eventi di ambiente](ambient-event-handlers.md).

I dispositivi di scorrimento predefiniti sono elementi di **scorrimento** normali con diverse impostazioni degli attributi comuni specificati per impostazione predefinita. Sono disponibili i dispositivi di scorrimento predefiniti seguenti.



| Dispositivo di scorrimento predefinito                  | Descrizione                                                    |
|------------------------------------|----------------------------------------------------------------|
| [BALANCESLIDER](balanceslider.md) | **Dispositivo di scorrimento** utilizzato per impostare il bilanciamento audio.                        |
| [SEEKSLIDER](seekslider.md)       | **Dispositivo di scorrimento** utilizzato per cercare in qualsiasi posizione all'interno di un file multimediale. |
| [VOLUMESLIDER](volumeslider.md)   | **Dispositivo di scorrimento** utilizzato per impostare il volume audio.                         |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni di riferimento sulla programmazione dell'interfaccia**](skin-programming-reference.md)
</dt> </dl>

 

 




