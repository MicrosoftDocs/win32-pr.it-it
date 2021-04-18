---
title: Errore del ruolo ARIA
description: Errore del ruolo ARIA
ms.assetid: FEEB4F28-4A71-4417-A2F9-ABCB86B44F0F
keywords:
- AriaRoleErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df04ad94d68ae1e8e2e8d3352aa349834a2389fa
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "106300631"
---
# <a name="aria-role-error"></a><span data-ttu-id="bd336-104">Errore del ruolo ARIA</span><span class="sxs-lookup"><span data-stu-id="bd336-104">ARIA Role Error</span></span>

## <a name="text"></a><span data-ttu-id="bd336-105">Testo</span><span class="sxs-lookup"><span data-stu-id="bd336-105">Text</span></span>

<span data-ttu-id="bd336-106">L'elemento ha un ruolo WAI-ARIA non valido.</span><span class="sxs-lookup"><span data-stu-id="bd336-106">Element has invalid WAI-ARIA role.</span></span>

## <a name="type"></a><span data-ttu-id="bd336-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="bd336-107">Type</span></span>

<span data-ttu-id="bd336-108">Errore</span><span class="sxs-lookup"><span data-stu-id="bd336-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="bd336-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bd336-109">Description</span></span>

<span data-ttu-id="bd336-110">Questo errore si applica a tutti gli elementi che hanno l'attributo [**Role**](https://developer.mozilla.org/docs/Web/HTML/Reference) .</span><span class="sxs-lookup"><span data-stu-id="bd336-110">This error applies to all elements that have the [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) attribute.</span></span> <span data-ttu-id="bd336-111">Indica che l'attributo **Role** non è un valore di ruolo di Web Accessibility Initiative (Wai-aria) accessibile per Internet, come definito dalla specifica Wai-aria.</span><span class="sxs-lookup"><span data-stu-id="bd336-111">It indicates that the **role** attribute is not a valid Web Accessibility Initiative - Accessible Rich Internet Applications (WAI-ARIA) role value as defined by the WAI-ARIA specification.</span></span> <span data-ttu-id="bd336-112">L'impostazione di un ruolo valido consente di garantire che l'elemento venga interpretato correttamente dalle utilità per la lettura dello schermo e da altri strumenti di Assistive Technology.</span><span class="sxs-lookup"><span data-stu-id="bd336-112">Setting a valid role helps ensure that the element is correctly interpreted by screen readers and other assistive technology tools.</span></span>

<span data-ttu-id="bd336-113">Per correggere l'errore, impostare l'attributo [**Role**](https://developer.mozilla.org/docs/Web/HTML/Reference) su un valore del ruolo Wai-aria valido.</span><span class="sxs-lookup"><span data-stu-id="bd336-113">To fix this error, set the [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) attribute to a valid WAI-ARIA role value.</span></span> <span data-ttu-id="bd336-114">Si noti che i ruoli di WAI-ARIA astratti non sono validi.</span><span class="sxs-lookup"><span data-stu-id="bd336-114">Note that abstract WAI-ARIA roles are not valid.</span></span>

## <a name="example"></a><span data-ttu-id="bd336-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="bd336-115">Example</span></span>


```HTML
<!—The invalid role will not expose this element as a button. -->
<div role="backbutton" tabindex="0" aria-label="Back" onclick="mouseAction(event)" onkeyup="keyAction(event)" >

<!—Setting the correct role will expose this as a button that can be clicked. -->
<div role="button" tabindex="0" aria-label="Back" onclick="mouseAction(event)" onkeyup="keyAction(event)" >
```



## <a name="related-topics"></a><span data-ttu-id="bd336-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bd336-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd336-117">Errore del ruolo del contenitore ARIA</span><span class="sxs-lookup"><span data-stu-id="bd336-117">ARIA Container Role Error</span></span>](aria-container-role.md)
</dt> </dl>

 

 




