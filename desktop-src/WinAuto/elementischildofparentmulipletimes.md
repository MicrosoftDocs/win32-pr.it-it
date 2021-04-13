---
title: ElementIsChildOfParentMulipleTimes
description: ElementIsChildOfParentMulipleTimes
ms.assetid: B966ABE0-5109-4DAD-8125-EB4A3B3A5F61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da27c66027f7948dfa794c85dace015565d636c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104222123"
---
# <a name="elementischildofparentmulipletimes"></a><span data-ttu-id="7a01c-103">ElementIsChildOfParentMulipleTimes</span><span class="sxs-lookup"><span data-stu-id="7a01c-103">ElementIsChildOfParentMulipleTimes</span></span>

## <a name="text"></a><span data-ttu-id="7a01c-104">Testo</span><span class="sxs-lookup"><span data-stu-id="7a01c-104">Text</span></span>

<span data-ttu-id="7a01c-105">AccParent dell'elemento è ( {0} ), ma l'elemento originale è un {1} tempo figlio</span><span class="sxs-lookup"><span data-stu-id="7a01c-105">Element's accParent is ({0}), but original element is a child {1} times</span></span>

## <a name="type"></a><span data-ttu-id="7a01c-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="7a01c-106">Type</span></span>

<span data-ttu-id="7a01c-107">Errore</span><span class="sxs-lookup"><span data-stu-id="7a01c-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="7a01c-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7a01c-108">Description</span></span>

<span data-ttu-id="7a01c-109">Quando viene chiamato il metodo [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) sull'elemento target, questo viene segnalato come figlio dello stesso padre più volte.</span><span class="sxs-lookup"><span data-stu-id="7a01c-109">When [**get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) is called on the target element, it reports being a child of the same parent multiple times.</span></span>

<span data-ttu-id="7a01c-110">Questo problema può causare problemi di navigazione per gli strumenti automatici perché l'attraversamento degli elementi potrebbe essere irregolare e imprevedibile.</span><span class="sxs-lookup"><span data-stu-id="7a01c-110">This issue can cause navigation problems for automated tools because traversing elements might be erratic and unpredictable.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="7a01c-111">Possibili cause</span><span class="sxs-lookup"><span data-stu-id="7a01c-111">Possible causes</span></span>

<span data-ttu-id="7a01c-112">Implementazione MSAA non corretta o non valida.</span><span class="sxs-lookup"><span data-stu-id="7a01c-112">An incorrect or invalid MSAA implementation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7a01c-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7a01c-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a01c-114">**IAccessible:: Get \_ accParent**</span><span class="sxs-lookup"><span data-stu-id="7a01c-114">**IAccessible::get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)
</dt> </dl>

 

 




