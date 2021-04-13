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
# <a name="aria-role-error-for-elements-with-event-handlers"></a><span data-ttu-id="38fd2-104">Errore del ruolo ARIA per gli elementi con gestori eventi</span><span class="sxs-lookup"><span data-stu-id="38fd2-104">ARIA Role Error for elements with event handlers</span></span>

## <a name="text"></a><span data-ttu-id="38fd2-105">Testo</span><span class="sxs-lookup"><span data-stu-id="38fd2-105">Text</span></span>

<span data-ttu-id="38fd2-106">L'elemento ha un gestore eventi ma il ruolo WAI-ARIA valido non è definito.</span><span class="sxs-lookup"><span data-stu-id="38fd2-106">Element has an event handler but valid WAI-ARIA role is not defined.</span></span>

## <a name="type"></a><span data-ttu-id="38fd2-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="38fd2-107">Type</span></span>

<span data-ttu-id="38fd2-108">Errore</span><span class="sxs-lookup"><span data-stu-id="38fd2-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="38fd2-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="38fd2-109">Description</span></span>

<span data-ttu-id="38fd2-110">Questo errore si verifica per gli elementi che non dispongono di un ruolo di applicazioni Internet (WAI-ARIA) accessibile da Web Accessibility Initiative.</span><span class="sxs-lookup"><span data-stu-id="38fd2-110">This error applies to elements that do not have an implicit Web Accessibility Initiative - Accessible Rich Internet Applications (WAI-ARIA) role.</span></span>

<span data-ttu-id="38fd2-111">Questo errore indica che un elemento ha un gestore eventi mouse o tastiera (**clic**, **MouseDown**, **MouseUp**, **MouseMove**, **mouse**, **MouseOver**, **KeyUp**, **KeyDown** o **KeyPress**), ma non ha l'attributo [**Role**](https://developer.mozilla.org/docs/Web/HTML/Reference) impostato e non è uno dei tag HTML con un ruolo Wai-aria implicito (ad esempio, **un** **pulsante**, **IMG**, **input**, **Select** e così via).</span><span class="sxs-lookup"><span data-stu-id="38fd2-111">This error indicates that an element has a mouse or keyboard event handler (**click**, **mousedown**, **mouseup**, **mousemove**, **mouseout**, **mouseover**, **keyup**, **keydown**, or **keypress**), but doesn’t have the [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) attribute set, and is not one of the HTML tags that has an implicit WAI-ARIA role (for example, **a**, **button**, **img**, **input**, **select** and so on).</span></span>

<span data-ttu-id="38fd2-112">È necessario impostare l'attributo [**Role**](https://developer.mozilla.org/docs/Web/HTML/Reference) per gli elementi interattivi che non dispongono di un ruolo implicito, ad esempio un tag **div** , per esporre i modelli di comportamento dell'elemento alle utilità per la lettura dello schermo e ad altre tecnologie per l'accesso facilitato.</span><span class="sxs-lookup"><span data-stu-id="38fd2-112">Setting the [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) attribute for interactive elements that have no implicit role (such as a **div** tag) is necessary to expose the element's behavior patterns to screen readers and other assistive technologies.</span></span>

<span data-ttu-id="38fd2-113">Per correggere l'errore, impostare l'attributo [**Role**](https://developer.mozilla.org/docs/Web/HTML/Reference) su un ruolo Wai-aria valido che meglio si adatta ai modelli di comportamento di questo elemento e agli attributi obbligatori.</span><span class="sxs-lookup"><span data-stu-id="38fd2-113">To fix this error, set the [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) attribute to a valid WAI-ARIA role that best fits this element's behavior patterns and required attributes.</span></span> <span data-ttu-id="38fd2-114">Se, ad esempio, un tag **div** funziona come un pulsante, impostare l'attributo Role su "button".</span><span class="sxs-lookup"><span data-stu-id="38fd2-114">For example, if a **div** tag functions as a button, set the role attribute to "button".</span></span>

## <a name="example"></a><span data-ttu-id="38fd2-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="38fd2-115">Example</span></span>


```HTML
<!-- Setting role attribute allows screen readers to know it can be clicked -->
<div role="button" tabindex="0" aria-label="Back" onclick="mouseAction(event)" onkeyup="keyAction(event)" >
```



 

 




