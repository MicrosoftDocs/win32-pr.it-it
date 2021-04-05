---
title: Elemento BUTTON (WMP)
description: Elemento BUTTON
ms.assetid: 2818ff6a-4fc5-4150-9ff9-ff143feb9204
keywords:
- Windows Media Player Skin, elemento BUTTON
- Skin, elemento BUTTON
- Elemento BUTTON
- riferimento per le interfacce, elemento BUTTON
- elementi, pulsante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c069207e15be62e06b4d2b18f13c052026932dc
ms.sourcegitcommit: 6f7576b297d54c0b8f9c79e02c912b83041aa4fb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/09/2019
ms.locfileid: "103719606"
---
# <a name="button-element"></a>Elemento BUTTON

L'elemento **Button** fornisce un modo per creare un pulsante all'interno di un'interfaccia. Gli attributi seguenti possono essere usati per personalizzare il comportamento di un pulsante oppure è possibile usare un pulsante predefinito per praticità.

L'elemento **Button** supporta gli attributi seguenti.



| Attributo                                         | Descrizione                                                                                                                                      |
|---------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [cursor](button-cursor.md)                       | Specifica o Recupera il cursore visualizzato quando il puntatore del mouse viene posizionato sul **pulsante**.                                                |
| [disabledImage](button-disabledimage.md)         | Specifica o recupera l'immagine visualizzata quando il **pulsante** è disabilitato.                                                                  |
| [giù](button-down.md)                           | Specifica o recupera un valore che indica se il **pulsante** si trova nella posizione verso l'alto o verso il basso.                                                  |
| [downImage](button-downimage.md)                 | Specifica o recupera l'immagine che rappresenta lo stato di inattività del **pulsante**.                                                                  |
| [downToolTip](button-downtooltip.md)             | Specifica o Recupera il testo della descrizione comando visualizzato quando il mouse è posizionato sul **pulsante** e il **pulsante** si trova nello stato premuto o premuto. |
| [hoverDownImage](button-hoverdownimage.md)       | Specifica o recupera l'immagine visualizzata quando il **pulsante** è nello stato di inattività e l'utente passa il puntatore del mouse su di esso.          |
| [hoverImage](button-hoverimage.md)               | Specifica o recupera l'immagine visualizzata quando il **pulsante** si trova nello stato attivo e l'utente passa su di esso con il puntatore del mouse.            |
| [image](button-image.md)                         | Specifica o recupera l'immagine predefinita del **pulsante**.                                                                                      |
| [permanenti](button-sticky.md)                       | Specifica o recupera un valore che indica se il **pulsante** è un interruttore, ovvero se si tratta di un pulsante a due Stati o a stato singolo.         |
| [piastrellati](button-tiled.md)                         | Specifica o recupera un valore che indica se l'immagine del **pulsante** verrà affiancata.                                                            |
| [transparencyColor](button-transparencycolor.md) | Specifica o Recupera il colore che sarà trasparente nell'immagine del **pulsante** .                                                               |
| [Descrizione comando](button-uptooltip.md)                 | Specifica o Recupera il testo della descrizione comando visualizzato quando il mouse è posizionato sul **pulsante** e il **pulsante** si trova nello stato attivo.                |



 

L'elemento **Button** supporta gli attributi di ambiente e può implementare i gestori eventi di ambiente. Per altre informazioni, vedere [attributi di ambiente](ambient-attributes.md) e [gestori di eventi di ambiente](ambient-event-handlers.md).

I pulsanti predefiniti sono elementi **pulsante** normali con diverse impostazioni degli attributi comuni specificati per impostazione predefinita. Sono disponibili i seguenti pulsanti predefiniti.



| PULSANTE predefinito                    | Descrizione                                                                        |
|--------------------------------------|------------------------------------------------------------------------------------|
| [CLOSEBUTTON](closebutton.md)       | **Pulsante** utilizzato per chiudere il lettore.                                             |
| [FFWDBUTTON](ffwdbutton.md)         | **Pulsante** con una chiamata incorporata a **Player. Controls. fastForward** quando si fa clic su. |
| [IMAGEBUTTON](imagebutton.md)       | **Pulsante** utilizzato per visualizzare un'immagine.                                             |
| [MINIMIZEBUTTON](minimizebutton.md) | **Pulsante** utilizzato per ridurre al minimo il lettore.                                          |
| [MUTEBUTTON](mutebutton.md)         | **Pulsante** usato per disattivare e disattivare l'audio.                                   |
| [NEXTBUTTON](nextbutton.md)         | **Pulsante** con una chiamata incorporata a **Player. Controls. Next** quando si fa clic su.        |
| [PAUSEBUTTON](pausebutton.md)       | **Pulsante** con una chiamata incorporata a **Player. Controls. pause** quando si fa clic su di essa.       |
| [PLAYBUTTON](playbutton.md)         | **Pulsante** con una chiamata incorporata a **Player. Controls. Play** quando si fa clic su.        |
| [PREVBUTTON](prevbutton.md)         | **Pulsante** con una chiamata incorporata a **Player. Controls. Previous** quando si fa clic su.    |
| [REPEATBUTTON](repeatbutton.md)     | **Pulsante** che consente di impostare o disabilitare l'opzione Ripeti.                                       |
| [RETURNBUTTON](returnbutton.md)     | **Pulsante** che restituisce Media Player di Windows al centro multimediale.                |
| [REWBUTTON](rewbutton.md)           | **Pulsante** con una chiamata incorporata a **Player. Controls. fastReverse** quando si fa clic su. |
| [SHUFFLEBUTTON](shufflebutton.md)   | **Pulsante** che consente di impostare o disabilitare l'opzione Shuffle.                                      |
| [STOPBUTTON](stopbutton.md)         | **Pulsante** con una chiamata incorporata a **Player. Controls. Stop** quando si fa clic su.        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni di riferimento sulla programmazione dell'interfaccia**](skin-programming-reference.md)
</dt> </dl>

 

 




