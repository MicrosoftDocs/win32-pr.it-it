---
title: Errore del ruolo del contenitore ARIA
description: Errore del ruolo del contenitore ARIA
ms.assetid: AF207293-1172-43D0-B92C-C3070876DF54
keywords:
- AriaContainerRoleErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d02554c868816c05981fa9f008c8f79f0a3eb0f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955778"
---
# <a name="aria-container-role-error"></a><span data-ttu-id="e13d0-104">Errore del ruolo del contenitore ARIA</span><span class="sxs-lookup"><span data-stu-id="e13d0-104">ARIA Container Role Error</span></span>

## <a name="text"></a><span data-ttu-id="e13d0-105">Testo</span><span class="sxs-lookup"><span data-stu-id="e13d0-105">Text</span></span>

<span data-ttu-id="e13d0-106">L'elemento con un **discendente attivo** definito non dispone di un ruolo contenitore (**casella combinata**, **griglia**, **ListBox**, **menu**, **barra** dei menu, **radiogruppo**, **albero**, **Treegrid**, in **particolare**, **riga**).</span><span class="sxs-lookup"><span data-stu-id="e13d0-106">Element with **active-descendant** defined does not have a container role (**combobox**, **grid**, **listbox**, **menu**, **menubar**, **radiogroup**, **tree**, **treegrid**, **tablist**, **row**).</span></span>

## <a name="type"></a><span data-ttu-id="e13d0-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="e13d0-107">Type</span></span>

<span data-ttu-id="e13d0-108">Errore</span><span class="sxs-lookup"><span data-stu-id="e13d0-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="e13d0-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e13d0-109">Description</span></span>

<span data-ttu-id="e13d0-110">Questo errore si applica agli elementi con l'attributo **aria-activedescendant** .</span><span class="sxs-lookup"><span data-stu-id="e13d0-110">This error applies to elements that have the **aria-activedescendant** attribute.</span></span>

<span data-ttu-id="e13d0-111">Un elemento sembra essere un contenitore in cui è impostato l'attributo **aria-activedescendant** , ma l'attributo Role dell'elemento non dispone di un valore valido per un contenitore.</span><span class="sxs-lookup"><span data-stu-id="e13d0-111">An element appears to be a container that has the **aria-activedescendant** attribute set, but the element's role attribute doesn’t have a value that is valid for a container.</span></span>

<span data-ttu-id="e13d0-112">Per correggere l'errore, impostare l'attributo **Role** su un valore del ruolo Web Accessibility Initiative (Wai-aria) accessibile da Internet, che è valido per un elemento contenitore: **ComboBox**, **Grid**, **ListBox**, **menu**, **barra** dei menu, **RadioGroup**, in **particolare**, **Tree** o **Treegrid**.</span><span class="sxs-lookup"><span data-stu-id="e13d0-112">To fix this error, set the **role** attribute to a Web Accessibility Initiative - Accessible Rich Internet Applications (WAI-ARIA) role value that is valid for a container element: **combobox**, **grid**, **listbox**, **menu**, **menubar**, **radiogroup**, **tablist**, **tree**, or **treegrid**.</span></span>

## <a name="example"></a><span data-ttu-id="e13d0-113">Esempio</span><span class="sxs-lookup"><span data-stu-id="e13d0-113">Example</span></span>


```HTML
<div role="listbox" id="listbox1" tabindex="0" aria-activedescendant="listbox1-1">
  <div role="option" id="listbox1-1" class="selected">Item 1</div>
  <div role="option" id="listbox1-2">Item 2</div>
  <div role="option" id="listbox1-3">Item 3</div>
  ...
<div>
```



## <a name="related-topics"></a><span data-ttu-id="e13d0-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e13d0-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e13d0-115">Errore del ruolo ARIA</span><span class="sxs-lookup"><span data-stu-id="e13d0-115">ARIA Role Error</span></span>](aria-role-invalid.md)
</dt> </dl>

 

 




