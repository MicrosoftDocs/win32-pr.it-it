---
title: Errore del ruolo ARIA per gli elementi con gestori eventi
description: Errore del ruolo ARIA per gli elementi con gestori eventi
ms.assetid: 20BB874A-874B-4266-9C7B-49C07D4146DA
keywords:
- AriaContainerRoleErrorMessage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eede416392e8b4cb644938242a9975238118ff07
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "104399864"
---
# <a name="aria-role-error-for-elements-with-event-handlers"></a>Errore del ruolo ARIA per gli elementi con gestori eventi

## <a name="text"></a>Testo

L'elemento ha un gestore eventi ma il ruolo WAI-ARIA valido non è definito.

## <a name="type"></a>Tipo

Errore

## <a name="description"></a>Descrizione

Questo errore si verifica per gli elementi che non dispongono di un ruolo di applicazioni Internet (WAI-ARIA) accessibile da Web Accessibility Initiative.

Questo errore indica che un elemento ha un gestore eventi mouse o tastiera (**clic**, **MouseDown**, **MouseUp**, **MouseMove**, **mouse**, **MouseOver**, **KeyUp**, **KeyDown** o **KeyPress**), ma non ha l'attributo [**Role**](https://developer.mozilla.org/docs/Web/HTML/Reference) impostato e non è uno dei tag HTML con un ruolo Wai-aria implicito (ad esempio, **un** **pulsante**, **IMG**, **input**, **Select** e così via).

È necessario impostare l'attributo [**Role**](https://developer.mozilla.org/docs/Web/HTML/Reference) per gli elementi interattivi che non dispongono di un ruolo implicito, ad esempio un tag **div** , per esporre i modelli di comportamento dell'elemento alle utilità per la lettura dello schermo e ad altre tecnologie per l'accesso facilitato.

Per correggere l'errore, impostare l'attributo [**Role**](https://developer.mozilla.org/docs/Web/HTML/Reference) su un ruolo Wai-aria valido che meglio si adatta ai modelli di comportamento di questo elemento e agli attributi obbligatori. Se, ad esempio, un tag **div** funziona come un pulsante, impostare l'attributo Role su "button".

## <a name="example"></a>Esempio


```HTML
<!-- Setting role attribute allows screen readers to know it can be clicked -->
<div role="button" tabindex="0" aria-label="Back" onclick="mouseAction(event)" onkeyup="keyAction(event)" >
```



 

 




