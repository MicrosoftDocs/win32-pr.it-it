---
title: AccNavigate_ReturnedElementWithIncorrectParent
description: '\_ReturnedElementWithIncorrectParent AccNavigate'
ms.assetid: 44447E47-04D5-4784-B5E9-E8C62A9834CE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a3bdff54c9c594cde4e6e57fe1886a900c913eb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104557694"
---
# <a name="accnavigate_returnedelementwithincorrectparent"></a><span data-ttu-id="ad3c3-103">\_ReturnedElementWithIncorrectParent AccNavigate</span><span class="sxs-lookup"><span data-stu-id="ad3c3-103">AccNavigate\_ReturnedElementWithIncorrectParent</span></span>

## <a name="text"></a><span data-ttu-id="ad3c3-104">Testo</span><span class="sxs-lookup"><span data-stu-id="ad3c3-104">Text</span></span>

<span data-ttu-id="ad3c3-105">La chiamata a accNavigate ((Live Search), 0, NAVDIR \_ FIRSTCHILD) che ha restituito (x-Gadget:///gadget.html) ha restituito un elemento padre non corretto ( \[ null \] ) e non (ricerca in tempo reale)</span><span class="sxs-lookup"><span data-stu-id="ad3c3-105">Calling accNavigate((Live Search), 0, NAVDIR\_FIRSTCHILD) which returned (x-gadget:///gadget.html) returned the incorrect parent(\[NULL\]) and not (Live Search)</span></span>

## <a name="type"></a><span data-ttu-id="ad3c3-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="ad3c3-106">Type</span></span>

<span data-ttu-id="ad3c3-107">Errore</span><span class="sxs-lookup"><span data-stu-id="ad3c3-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="ad3c3-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ad3c3-108">Description</span></span>

<span data-ttu-id="ad3c3-109">Quando [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) viene chiamato sull'elemento figlio restituito da [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) (usando le \_ costanti di navigazione NAVDIR FIRSTCHILD o NAVDIR \_ LastChild), l'elemento padre restituito non corrisponde all'elemento padre specificato nella chiamata **accNavigate** .</span><span class="sxs-lookup"><span data-stu-id="ad3c3-109">When [**get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) is called on the child element returned by [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) (using either the NAVDIR\_FIRSTCHILD or NAVDIR\_LASTCHILD navigation constants), the parent element returned does not match the parent element specified in the **accNavigate** call.</span></span>

![esempio di implementazione MSAA non valida che restituisce un elemento padre non corretto.](images/accchecker-invalid-msaa-parent.png)

<span data-ttu-id="ad3c3-111">Questo problema può causare problemi di navigazione per gli strumenti automatici perché l'attraversamento degli elementi potrebbe essere irregolare e imprevedibile.</span><span class="sxs-lookup"><span data-stu-id="ad3c3-111">This issue can cause navigation problems for automated tools because traversing elements might be erratic and unpredictable.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="ad3c3-112">Possibili cause</span><span class="sxs-lookup"><span data-stu-id="ad3c3-112">Possible causes</span></span>

<span data-ttu-id="ad3c3-113">Implementazione MSAA non corretta o non valida.</span><span class="sxs-lookup"><span data-stu-id="ad3c3-113">An incorrect or invalid MSAA implementation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ad3c3-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ad3c3-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ad3c3-115">**IAccessible:: accNavigate**</span><span class="sxs-lookup"><span data-stu-id="ad3c3-115">**IAccessible::accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
</dt> <dt>

[<span data-ttu-id="ad3c3-116">**IAccessible:: Get \_ accParent**</span><span class="sxs-lookup"><span data-stu-id="ad3c3-116">**IAccessible::get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)
</dt> </dl>

 

 




