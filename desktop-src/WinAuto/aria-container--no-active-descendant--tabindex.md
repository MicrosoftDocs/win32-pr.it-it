---
title: Errore TabIndex del ruolo contenitore ARIA (senza discendente attivo)
description: Errore TabIndex del ruolo contenitore ARIA (senza discendente attivo)
ms.assetid: E3CCA500-7104-4163-927C-94EA8F1E89D8
keywords:
- AriaContainerWithoutActiveDescendantTabIndexErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a01d3391d93b7e7f146f379bcfecd629e14bce7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221464"
---
# <a name="aria-container-role-without-active-descendant-tabindex-error"></a><span data-ttu-id="f1f69-104">Errore TabIndex del ruolo contenitore ARIA (senza discendente attivo)</span><span class="sxs-lookup"><span data-stu-id="f1f69-104">ARIA Container Role (without active descendant) Tabindex Error</span></span>

## <a name="text"></a><span data-ttu-id="f1f69-105">Testo</span><span class="sxs-lookup"><span data-stu-id="f1f69-105">Text</span></span>

<span data-ttu-id="f1f69-106">L'elemento è un contenitore attivabile senza un discendente attivo definito, ma nessun elemento figlio ha un **TabIndex** maggiore o uguale a 0.</span><span class="sxs-lookup"><span data-stu-id="f1f69-106">Element is a focusable container without active descendant defined, but no child element has **tabindex** greater or equal to 0.</span></span>

## <a name="type"></a><span data-ttu-id="f1f69-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="f1f69-107">Type</span></span>

<span data-ttu-id="f1f69-108">Errore</span><span class="sxs-lookup"><span data-stu-id="f1f69-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="f1f69-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f1f69-109">Description</span></span>

<span data-ttu-id="f1f69-110">Questo errore si verifica per gli elementi che hanno un ruolo contenitore, non hanno un attributo **aria-activedescendant** e non sono disabilitati.</span><span class="sxs-lookup"><span data-stu-id="f1f69-110">This error applies to elements that have a container role, do not have an **aria-activedescendant** attribute, and are not disabled.</span></span> <span data-ttu-id="f1f69-111">Questi elementi implementano la navigazione da tastiera tra gli elementi figlio utilizzando il concetto noto come *Indice itinerante*.</span><span class="sxs-lookup"><span data-stu-id="f1f69-111">These elements implement keyboard navigation among child elements by using the concept known as *roving index*.</span></span> <span data-ttu-id="f1f69-112">In questo concetto, gli attributi **TabIndex** degli elementi figlio vengono mantenuti in modo dinamico, assicurando che in ogni momento un solo elemento figlio sia in ordine di tabulazione.</span><span class="sxs-lookup"><span data-stu-id="f1f69-112">In this concept, the **tabindex** attributes of child elements are maintained dynamically, ensuring that at all times only one child element is in tab order.</span></span>

<span data-ttu-id="f1f69-113">Per correggere l'errore, impostare l'attributo **TabIndex** di uno degli elementi figlio su un valore maggiore o uguale a 0.</span><span class="sxs-lookup"><span data-stu-id="f1f69-113">To fix this error, set the **tabindex** attribute of one of the child elements to a value equal to or greater than 0.</span></span>

## <a name="example"></a><span data-ttu-id="f1f69-114">Esempio</span><span class="sxs-lookup"><span data-stu-id="f1f69-114">Example</span></span>


```HTML
<div id="listbox" role="listbox1">
  <div role="option" id="listbox1-1" tabindex="0" class="selected">Item 1</div>
  <div role="option" id="listbox1-2">Item 2</div>
  <div role="option" id="listbox1-3">Item 3</div>
</div>

<script>

  ...

  listbox1.addEventListener('keyup', function(e) {
    var itm = e.srcElement;
    var prev = itm.previousElementSibling;
    var next = itm.nextElementSibling;

    if (e.keyCode == 38 && prev) {
      // Arrow up to move focus to the previous item.
      itm.setAttribute('tabindex', '-1');
      prev.setAttribute('tabindex','0');
      prev.focus();
    } 

    else if (e.keyCode == 40 && next) {
      // Arrow down to move focus to the next item.
      itm.setAttribute('tabindex', '-1');
      next.setAttribute('tabindex','0');
      next.focus();
    }
  });

</script>
```



## <a name="related-topics"></a><span data-ttu-id="f1f69-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f1f69-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1f69-116">Errore TabIndex del contenitore ARIA</span><span class="sxs-lookup"><span data-stu-id="f1f69-116">ARIA Container Tabindex Error</span></span>](aria-container-tabindex.md)
</dt> </dl>

 

 




