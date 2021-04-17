---
title: Errore di accessibilità tastiera ruolo contenitore ARIA
description: Errore di accessibilità tastiera ruolo contenitore ARIA
ms.assetid: 364F26D7-7B65-418B-9DA5-F3B7B59284F7
keywords:
- AriaContainerKeyboardAccessibilityErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 085591e4f4834e8088b5ca199918d621f518e678
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330943"
---
# <a name="aria-container-role-keyboard-accessibility-error"></a><span data-ttu-id="945ff-104">Errore di accessibilità tastiera ruolo contenitore ARIA</span><span class="sxs-lookup"><span data-stu-id="945ff-104">ARIA Container Role Keyboard Accessibility Error</span></span>

## <a name="text"></a><span data-ttu-id="945ff-105">Testo</span><span class="sxs-lookup"><span data-stu-id="945ff-105">Text</span></span>

<span data-ttu-id="945ff-106">L'elemento è un contenitore con funzionalità del mouse attive discendenti e personalizzate ma senza la corrispondente funzionalità della tastiera: gestori eventi JavaScript per **OnKeyDown** o **OnKeyPress**.</span><span class="sxs-lookup"><span data-stu-id="945ff-106">Element is a container with active descendant and custom mouse functionality but without the corresponding keyboard functionality: JavaScript event handlers for **OnKeyDown** or **OnKeyPress**.</span></span>

## <a name="type"></a><span data-ttu-id="945ff-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="945ff-107">Type</span></span>

<span data-ttu-id="945ff-108">Errore</span><span class="sxs-lookup"><span data-stu-id="945ff-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="945ff-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="945ff-109">Description</span></span>

<span data-ttu-id="945ff-110">Questo errore si applica agli elementi con l'attributo **aria-activedescendant** .</span><span class="sxs-lookup"><span data-stu-id="945ff-110">This error applies to elements that have the **aria-activedescendant** attribute.</span></span> <span data-ttu-id="945ff-111">Questi elementi hanno uno o più gestori di eventi del mouse (**MouseMove**, **MouseDown** o **MouseUp**), ma mancano i gestori eventi di tastiera equivalenti (**KeyDown**, **KeyUp** o **KeyPress**).</span><span class="sxs-lookup"><span data-stu-id="945ff-111">These elements have one or more mouse event handlers (**mousemove**, **mousedown** or **mouseup**), but are missing the equivalent keyboard event handlers (**keydown**, **keyup** or **keypress**).</span></span> <span data-ttu-id="945ff-112">I gestori degli eventi della tastiera sono necessari per garantire che l'utente possa richiamare la funzionalità dell'elemento tramite la tastiera e per assicurarsi che l'elemento mantenga l'attributo **aria-activedescendant** .</span><span class="sxs-lookup"><span data-stu-id="945ff-112">The keyboard event handlers are needed to ensure that the user can invoke the element's functionality by using the keyboard, and to ensure that the element maintains the **aria-activedescendant** attribute.</span></span>

<span data-ttu-id="945ff-113">Per correggere l'errore, implementare uno dei gestori di eventi della tastiera.</span><span class="sxs-lookup"><span data-stu-id="945ff-113">To fix this error, implement one of the keyboard event handlers.</span></span>

## <a name="example"></a><span data-ttu-id="945ff-114">Esempio</span><span class="sxs-lookup"><span data-stu-id="945ff-114">Example</span></span>


```HTML
<div role="listbox" id="listbox1" tabindex="0" aria-activedescendant="listbox1-1"> 
  <div role="option" id="listbox1-1" class="selected">Item 1</div>
  <div role="option" id="listbox1-2">Item 2</div>
  <div role="option" id="listbox1-3">Item 3</div>
</div>

<script>

   ...

  listbox1.addEventListener('keyup', function(e) {
    var itm = document.getElementById(this.getAttribute('aria-activedescendant'));
    var prev = itm.previousElementSibling;
    var next = itm.nextElementSibling;
    
    if ( e.keyCode  38 && prev ) {
      // Arrow up to move active descendant to the previous item
      itm.removeAttribute('class’);
      prev.setAttribute("class", "selected");
      this.setAttribute ('aria-activedescendant', prev.id)
    } 

    else if ( e.keyCode == 40 && next) {
      // Arrow down to move focus to the next item
      itm.removeAttribute('class’);
      next.setAttribute("class", "selected");
      this.setAttribute ('aria-activedescendant', next.id)
    }
  });      

</script>
```



## <a name="related-topics"></a><span data-ttu-id="945ff-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="945ff-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="945ff-116">Errore di accessibilità della tastiera del ruolo contenitore ARIA (senza discendente attivo)</span><span class="sxs-lookup"><span data-stu-id="945ff-116">ARIA Container Role (without active descendant) Keyboard Accessibility Error</span></span>](aria-container--no-active-descendants--keyboard-events.md)
</dt> </dl>

 

 




