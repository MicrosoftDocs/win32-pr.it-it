---
title: Errore TabIndex del contenitore ARIA
description: Errore TabIndex del contenitore ARIA
ms.assetid: CCEA9490-903D-423D-B9FD-641E8B7D3E0B
keywords:
- AriaContainerTabIndexErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b6af684b401627181aaef656215240a312393f2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396714"
---
# <a name="aria-container-tabindex-error"></a><span data-ttu-id="9fa73-104">Errore TabIndex del contenitore ARIA</span><span class="sxs-lookup"><span data-stu-id="9fa73-104">ARIA Container Tabindex Error</span></span>

## <a name="text"></a><span data-ttu-id="9fa73-105">Testo</span><span class="sxs-lookup"><span data-stu-id="9fa73-105">Text</span></span>

<span data-ttu-id="9fa73-106">L'elemento è un contenitore focalizzabile con discendenti attivi definiti, ma senza valore **TabIndex** maggiore o uguale a 0.</span><span class="sxs-lookup"><span data-stu-id="9fa73-106">Element is a focusable container with active descendants defined but without **tabindex** value greater or equal to 0.</span></span>

## <a name="type"></a><span data-ttu-id="9fa73-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="9fa73-107">Type</span></span>

<span data-ttu-id="9fa73-108">Errore</span><span class="sxs-lookup"><span data-stu-id="9fa73-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="9fa73-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9fa73-109">Description</span></span>

<span data-ttu-id="9fa73-110">Questo errore si verifica per gli elementi che hanno l'attributo **aria-activedescendant** , non sono disabilitati e l'attributo **TabIndex** non è impostato su un valore maggiore o uguale a 0.</span><span class="sxs-lookup"><span data-stu-id="9fa73-110">This error applies to elements that have the **aria-activedescendant** attribute, are not disabled, and do not have the **tabindex** attribute set to a value that is greater than or equal to 0.</span></span> <span data-ttu-id="9fa73-111">Questi elementi devono essere in ordine di tabulazione perché sono responsabili della gestione degli eventi di tastiera per i relativi elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="9fa73-111">These elements must be in tab order because they are responsible for handling keyboard events for their child elements.</span></span>

<span data-ttu-id="9fa73-112">Per correggere l'errore, impostare l'attributo **TabIndex** su un valore maggiore o uguale a 0.</span><span class="sxs-lookup"><span data-stu-id="9fa73-112">To fix this error, set the **tabindex** attribute to a value that is greater than or equal to 0.</span></span>

## <a name="example"></a><span data-ttu-id="9fa73-113">Esempio</span><span class="sxs-lookup"><span data-stu-id="9fa73-113">Example</span></span>


```HTML
<div role="listbox" id="listbox1" tabindex="0" aria-activedescendant="listbox1-1"> 
       <div role="option" id="listbox1-1" class="selected">Item 1</div> 
       <div role="option" id="listbox1-2">Item 2</div> 

       <div role="option" id="listbox1-3">Item 3</div>
      ... 
<div>
```



## <a name="related-topics"></a><span data-ttu-id="9fa73-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9fa73-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9fa73-115">Errore TabIndex del ruolo contenitore ARIA (senza discendente attivo)</span><span class="sxs-lookup"><span data-stu-id="9fa73-115">ARIA Container Role (without active descendant) Tabindex Error</span></span>](aria-container--no-active-descendant--tabindex.md)
</dt> </dl>

 

 




