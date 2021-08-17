---
title: Errore del ruolo ARIA per gli elementi con gestori eventi
description: Errore del ruolo ARIA per gli elementi con gestori eventi
ms.assetid: 20BB874A-874B-4266-9C7B-49C07D4146DA
keywords:
- AriaContainerRoleErrorMessage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cebaa2e6f4526d0a1e820e60adc1d28439d3f361c7ffb58a0c4d855861ea46d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133994"
---
# <a name="aria-role-error-for-elements-with-event-handlers"></a>Errore del ruolo ARIA per gli elementi con gestori eventi

## <a name="text"></a>Testo

L'elemento ha un gestore eventi, ma il ruolo WAI-ARIA valido non è definito.

## <a name="type"></a>Tipo

Errore

## <a name="description"></a>Descrizione

Questo errore si applica agli elementi che non hanno un ruolo IMPLICIT WEB Accessibility Initiative - Accessible Rich Internet Applications (WAI-ARIA).

Questo errore indica che un elemento ha un gestore eventi del mouse o della tastiera **(clic,** **mousedown,** **mouseup, mousemove,** [](https://developer.mozilla.org/docs/Web/HTML/Reference) **mouseout,** **mouseover, keyup,** **keydown** o **keypress),** ma non ha l'attributo role impostato e non è uno dei tag HTML con un ruolo WAI-ARIA implicito (ad **esempio,**, un pulsante **,** **img**, **input**, **select** e così via). 

L'impostazione dell'attributo role per gli elementi interattivi che non hanno un ruolo implicito ,ad esempio un tag **div,** è necessaria per esporre i modelli di comportamento dell'elemento alle utilità per la lettura dello schermo e ad altre tecnologie di assistive technology. [](https://developer.mozilla.org/docs/Web/HTML/Reference)

Per correggere l'errore, impostare l'attributo [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) su un ruolo WAI-ARIA valido più adatto ai modelli di comportamento di questo elemento e agli attributi obbligatori. Ad esempio, se un tag **div** funziona come pulsante, impostare l'attributo role su "button".

## <a name="example"></a>Esempio


```HTML
<!-- Setting role attribute allows screen readers to know it can be clicked -->
<div role="button" tabindex="0" aria-label="Back" onclick="mouseAction(event)" onkeyup="keyAction(event)" >
```



 

 




