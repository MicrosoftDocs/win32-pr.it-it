---
title: Errore di accessibilità della tastiera del ruolo contenitore ARIA (senza discendente attivo)
description: Errore di accessibilità della tastiera del ruolo contenitore ARIA (senza discendente attivo)
ms.assetid: 15EDD3CC-FC2A-42FC-95DD-B04D9AF3515E
keywords:
- AriaContainerWithoutActiveDescendantKeyboardAccessiblityId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d9e30e0194f156426e2b61aa774ac1f3e0f5b91
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856118"
---
# <a name="aria-container-role-without-active-descendant-keyboard-accessibility-error"></a><span data-ttu-id="019d1-104">Errore di accessibilità della tastiera del ruolo contenitore ARIA (senza discendente attivo)</span><span class="sxs-lookup"><span data-stu-id="019d1-104">ARIA Container Role (without active descendant) Keyboard Accessibility Error</span></span>

## <a name="text"></a><span data-ttu-id="019d1-105">Testo</span><span class="sxs-lookup"><span data-stu-id="019d1-105">Text</span></span>

<span data-ttu-id="019d1-106">L'elemento è un contenitore attivabile senza un discendente attivo definito e senza **OnKeyDown** / **OnKeyPress** /  gestori eventi (né nel contenitore né in uno degli elementi figlio).</span><span class="sxs-lookup"><span data-stu-id="019d1-106">Element is a focusable container without active descendant defined and without **OnKeyDown**/**OnKeyPress**/**OnKeyUp** event handlers (neither on container nor on one of child elements).</span></span>

## <a name="type"></a><span data-ttu-id="019d1-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="019d1-107">Type</span></span>

<span data-ttu-id="019d1-108">Errore</span><span class="sxs-lookup"><span data-stu-id="019d1-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="019d1-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="019d1-109">Description</span></span>

<span data-ttu-id="019d1-110">Questo errore si verifica per gli elementi che hanno un ruolo contenitore, non hanno un attributo **aria-activedescendant** e non sono disabilitati.</span><span class="sxs-lookup"><span data-stu-id="019d1-110">This error applies to elements that have a container role, do not have an **aria-activedescendant** attribute, and are not disabled.</span></span> <span data-ttu-id="019d1-111">Questi elementi implementano la navigazione da tastiera tra gli elementi figlio utilizzando il concetto noto come *Indice itinerante*.</span><span class="sxs-lookup"><span data-stu-id="019d1-111">These elements implement keyboard navigation among child elements by using the concept known as *roving index*.</span></span> <span data-ttu-id="019d1-112">In questo concetto, gli attributi **TabIndex** degli elementi figlio vengono mantenuti in modo dinamico, assicurando che in ogni momento un solo elemento figlio sia in ordine di tabulazione.</span><span class="sxs-lookup"><span data-stu-id="019d1-112">In this concept, the **tabindex** attributes of child elements are maintained dynamically, ensuring that at all times only one child element is in tab order.</span></span>

<span data-ttu-id="019d1-113">Questo errore indica che un elemento contenitore che non dispone dell'attributo **aria-activedescendant** , e che non è disabilitato, non è accessibile agli utenti della tastiera.</span><span class="sxs-lookup"><span data-stu-id="019d1-113">This error indicates that a container element that does not have the **aria-activedescendant** attribute, and that is not disabled, is not accessible to keyboard users.</span></span> <span data-ttu-id="019d1-114">Il problema è dovuto al fatto che il contenitore non contiene i gestori eventi di tastiera necessari (**KeyDown**, **KeyUp** o **KeyPress**) e nessuno degli elementi figlio del contenitore.</span><span class="sxs-lookup"><span data-stu-id="019d1-114">The problem exists because the container does not have the needed keyboard event handlers (**keydown**, **keyup**, or **keypress**), and neither do any of the container's child elements.</span></span>

<span data-ttu-id="019d1-115">Per correggere l'errore, definire un gestore eventi **KeyDown**, **KeyUp** o **KeyPress** per il contenitore o uno dei relativi elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="019d1-115">To fix this error, define a **keydown**, **keyup**, or **keypress** event handler for the container or one of its child elements.</span></span>

## <a name="example"></a><span data-ttu-id="019d1-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="019d1-116">Example</span></span>


```HTML
<div role="listbox" id="listbox1" >
  <div role="option" id="listbox1-1" tabindex="0" class="selected">Item 1</div>
  <div role="option" id="listbox1-2">Item 2</div>
  <div role="option" id="listbox1-3">Item 3</div>
  ...
<div>

<script>

  ...

  listbox1.addEventListener('keyup', function(e) {
    var itm = e.srcElement;
    var prev = itm.previousElementSibling;
    var next = itm.nextElementSibling;

    if (e.keyCode == 38 && prev) {
      // On arrow up move focus to the previous item.
      itm.setAttribute('tabindex', '-1');
      prev.setAttribute('tabindex','0');
      prev.focus();
    }

    else if (e.keyCode == 40 && next) {
      // On arrow down move focus to the next item.
      itm.setAttribute('tabindex', '-1');
      next.setAttribute('tabindex','0');
      next.focus();
    }
  });

</script>
```



## <a name="related-topics"></a><span data-ttu-id="019d1-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="019d1-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="019d1-118">Errore di accessibilità tastiera ruolo contenitore ARIA</span><span class="sxs-lookup"><span data-stu-id="019d1-118">ARIA Container Role Keyboard Accessibility Error</span></span>](aria-container-keyboard-events.md)
</dt> </dl>

 

 




