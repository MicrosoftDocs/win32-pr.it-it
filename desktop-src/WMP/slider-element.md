---
title: Elemento SLIDER
description: Elemento SLIDER
ms.assetid: f1da8987-5430-46ef-b7d7-ac92f34a2185
keywords:
- Windows Media Player skin, elemento SLIDER
- skins,slider - elemento
- Elemento SLIDER
- informazioni di riferimento per le skin, elemento SLIDER
- elementi,SLIDER
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 140c84f6bec826b34ff4e1c5a4a3365d44ba9aa67ca9504cea642aba25f076d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118569089"
---
# <a name="slider-element"></a>Elemento SLIDER

**L'elemento SLIDER** consente di creare e modificare un semplice controllo dispositivo di scorrimento orizzontale o verticale. Supporta gli attributi e i gestori eventi seguenti. Gli elementi **SLIDER** predefiniti vengono forniti anche per praticità.

**L'elemento SLIDER** supporta gli attributi seguenti.



| Attributo                                                 | Descrizione                                                                                                       |
|-----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [Backgroundcolor](slider-backgroundcolor.md)             | Specifica o recupera il colore di sfondo del controllo dispositivo di scorrimento.                                                |
| [backgroundEndColor](slider-backgroundendcolor.md)       | Specifica o recupera il colore finale dello sfondo del controllo dispositivo di scorrimento.                                         |
| [backgroundHoverImage](slider-backgroundhoverimage.md)   | Specifica o recupera l'immagine di sfondo del dispositivo di scorrimento visualizzato quando si passa il mouse su di essa.      |
| [backgroundImage](slider-backgroundimage.md)             | Specifica o recupera l'immagine di sfondo predefinita del dispositivo di scorrimento.                                                |
| [borderSize](slider-bordersize.md)                       | Specifica o recupera le dimensioni del bordo in pixel.                                                                 |
| [cursor](slider-cursor.md)                               | Specifica o recupera un valore che indica il tipo di cursore visualizzato quando il mouse viene posizionato sul controllo dispositivo di scorrimento. |
| [direction](slider-direction.md)                         | Specifica o recupera la direzione in cui vengono disposti i dispositivi di scorrimento.                                             |
| [disabledColor](slider-disabledcolor.md)                 | Specifica o recupera il colore disabilitato del controllo dispositivo di scorrimento.                                                  |
| [disabledImage](slider-disabledimage.md)                 | Specifica o recupera l'immagine del dispositivo di scorrimento visualizzata quando il controllo è disabilitato.                         |
| [foregroundColor](slider-foregroundcolor.md)             | Specifica o recupera il colore di primo piano del controllo dispositivo di scorrimento.                                                |
| [foregroundEndColor](slider-foregroundendcolor.md)       | Specifica o recupera il colore finale in primo piano del controllo dispositivo di scorrimento.                                         |
| [foregroundHoverImage](slider-foregroundhoverimage.md)   | Specifica o recupera l'immagine in primo piano del dispositivo di scorrimento visualizzata quando si passa il mouse su di essa.      |
| [foregroundImage](slider-foregroundimage.md)             | Specifica o recupera l'immagine in primo piano predefinita del dispositivo di scorrimento.                                                |
| [foregroundProgress](slider-foregroundprogress.md)       | Specifica o recupera la posizione corrente dell'indicatore di stato in primo piano come percentuale dell'area del dispositivo di scorrimento.    |
| [max](slider-max.md)                                     | Specifica o recupera il valore massimo dell'intervallo definito dal controllo dispositivo di scorrimento.                              |
| [min](slider-min.md)                                     | Specifica o recupera il valore minimo dell'intervallo definito dal controllo dispositivo di scorrimento.                              |
| [Diapositiva](slider-slide.md)                                 | Specifica o recupera un valore che indica se l'immagine in primo piano scorre sull'immagine di sfondo.          |
| [thumbDisabledImage](slider-thumbdisabledimage.md)       | Specifica o recupera l'immagine del dispositivo di scorrimento disabilitata del dispositivo di scorrimento.                                            |
| [thumbDownImage](slider-thumbdownimage.md)               | Specifica o recupera l'immagine che rappresenta lo stato verso il basso della casella di scorrimento.                                        |
| [thumbHoverImage](slider-thumbhoverimage.md)             | Specifica o recupera l'immagine della casella di scorrimento visualizzata quando si posiziona il puntatore del mouse su di essa.                  |
| [thumbImage](slider-thumbimage.md)                       | Specifica o recupera l'immagine che verrà utilizzata per rappresentare la posizione corrente del dispositivo di scorrimento.               |
| [Piastrellati](slider-tiled.md)                                 | Specifica o recupera un valore che indica se le immagini del dispositivo di scorrimento verranno affiancate.                                |
| [Descrizione comandi](slider-tooltip.md)                             | Specifica o recupera il testo della descrizione comando per il controllo dispositivo di scorrimento.                                                   |
| [transparencyColor](slider-transparencycolor.md)         | Specifica o recupera il colore trasparente delle immagini del dispositivo di scorrimento.                                                |
| [useForegroundProgress](slider-useforegroundprogress.md) | Specifica o recupera un valore che indica se verrà utilizzato l'indicatore di stato in primo piano.                       |
| [value](slider-value.md)                                 | Specifica e recupera la posizione corrente del dispositivo di scorrimento.                                                       |



 

**L'elemento SLIDER** può implementare i gestori eventi seguenti.



| Gestore di evento                                   | Descrizione                                                                                                          |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [onDragBegin](slider-ondragbegin.md)           | Gestisce un evento che si verifica quando l'utente fa clic e tiene premuto il pulsante sinistro del mouse e inizia a trascinare il mouse. |
| [onDragEnd](slider-ondragend.md)               | Gestisce un evento che si verifica quando il pulsante sinistro del mouse viene rilasciato dopo un'operazione di trascinamento.                      |
| [onPositionChange](slider-onpositionchange.md) | Gestisce un evento che si verifica quando la posizione del dispositivo di scorrimento cambia in seguito al clic o al trascinamento dell'utente.   |



 

**L'elemento SLIDER** supporta gli attributi di ambiente e può implementare i gestori eventi di ambiente. Per altre informazioni, vedere [Attributi di ambiente e](ambient-attributes.md) Gestori eventi di [ambiente](ambient-event-handlers.md).

I dispositivi di scorrimento predefiniti sono normali **elementi SLIDER** con diverse impostazioni di attributi comuni specificate per impostazione predefinita. Sono disponibili i dispositivi di scorrimento predefiniti seguenti.



| DISPOSITIVO DI SCORRIMENTO predefinito                  | Descrizione                                                    |
|------------------------------------|----------------------------------------------------------------|
| [BALANCESLIDER](balanceslider.md) | SLIDER **usato** per impostare il bilanciamento dell'audio.                        |
| [SEEKSLIDER](seekslider.md)       | Slider **usato** per cercare qualsiasi posizione all'interno di un file multimediale. |
| [VOLUMILIDER](volumeslider.md)   | Slider **usato** per impostare il volume audio.                         |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni di riferimento sulla programmazione dell'interfaccia**](skin-programming-reference.md)
</dt> </dl>

 

 




