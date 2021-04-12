---
title: Gestori eventi di ambiente
description: Gestori eventi di ambiente
ms.assetid: ec806b92-a66d-499d-9bb3-cea7e82676bb
keywords:
- Interfacce di Media Player Windows, gestori eventi di ambiente
- interfacce, gestori eventi di ambiente
- riferimento per le interfacce, i gestori eventi di ambiente
- gestori eventi di ambiente
- eventi, ambiente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dc05cf90956464afbb030f3cd5dc4af194b0da2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395538"
---
# <a name="ambient-event-handlers"></a>Gestori eventi di ambiente

I gestori eventi seguenti possono essere implementati per la maggior parte degli elementi di interfaccia. Gli attributi dell'evento di ambiente a cui si accede con la parola chiave **Event** possono essere utilizzati all'interno di un gestore eventi per determinare lo stato della tastiera e del mouse al momento dell'evento.



| Gestore di evento                                   | Descrizione                                                                                                                                                                                                                   |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [*attributo* \_ OnChange](attribute-onchange.md) | Quando un attributo Skin cambia valore, si verifica un evento che può essere gestito da un gestore eventi. Il nome del gestore eventi è il nome dell'attributo seguito da un carattere di sottolineatura e da "onChange", ad esempio "valore \_ OnChange". |
| [onblur](onblur.md)                            | Gestisce un evento che si verifica quando l'elemento perde lo stato attivo della tastiera.                                                                                                                                                       |
| [OnClick](onclick.md)                          | Gestisce un evento che si verifica quando l'utente fa clic sull'elemento.                                                                                                                                                                |
| [ondblclick](ondblclick.md)                    | Gestisce un evento che si verifica quando l'utente fa doppio clic sull'elemento.                                                                                                                                                         |
| [onendalphablend](onendalphablend.md)          | Gestisce un evento che si verifica quando un elemento completa un'operazione **alphaBlendTo** .                                                                                                                                         |
| [onendmove](onendmove.md)                      | Gestisce un evento che si verifica quando un elemento completa un'operazione **MoveTo** .                                                                                                                                                |
| [onfocus](onfocus.md)                          | Gestisce un evento che si verifica quando l'elemento riceve lo stato attivo della tastiera.                                                                                                                                                    |
| [OnKeyDown](onkeydown.md)                      | Gestisce un evento che si verifica quando viene premuto un tasto.                                                                                                                                                                           |
| [OnKeyPress](onkeypress.md)                    | Gestisce un evento che si verifica quando l'utente preme un tasto alfanumerico.                                                                                                                                                       |
| [OnKeyUp](onkeyup.md)                          | Gestisce un evento che si verifica quando viene rilasciato un tasto.                                                                                                                                                                          |
| [OnMouseDown](onmousedown.md)                  | Gestisce un evento che si verifica quando l'utente fa clic su un pulsante del mouse.                                                                                                                                                             |
| [OnMouseMove](onmousemove.md)                  | Gestisce un evento che si verifica quando l'utente sposta il puntatore del mouse mentre è posizionato su un elemento.                                                                                                                               |
| [onmouseout](onmouseout.md)                    | Gestisce un evento che si verifica quando l'utente sposta il puntatore del mouse sull'elemento.                                                                                                                                                 |
| [onmouseover](onmouseover.md)                  | Gestisce un evento che si verifica quando l'utente posiziona il puntatore del mouse sull'elemento.                                                                                                                                         |
| [OnMouseUp](onmouseup.md)                      | Gestisce un evento che si verifica quando l'utente rilascia un pulsante del mouse mentre il puntatore è posizionato sull'elemento.                                                                                                                     |
| [OnResize](onresize.md)                        | Gestisce un evento che si verifica quando un controllo viene ridimensionato.                                                                                                                                                                          |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Attributi dell'evento di ambiente**](ambient-event-attributes.md)
</dt> <dt>

[**Informazioni di riferimento sulla programmazione dell'interfaccia**](skin-programming-reference.md)
</dt> </dl>

 

 




