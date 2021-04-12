---
title: ElementIsNotChildOfElementsParent
description: ElementIsNotChildOfElementsParent
ms.assetid: DFD5CC2A-B5F4-49F2-B3EF-2CD447A575E2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c5a3d62a6ae656bffffca442ed3cbb9b85be8dc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396955"
---
# <a name="elementisnotchildofelementsparent"></a><span data-ttu-id="f07ce-103">ElementIsNotChildOfElementsParent</span><span class="sxs-lookup"><span data-stu-id="f07ce-103">ElementIsNotChildOfElementsParent</span></span>

## <a name="text"></a><span data-ttu-id="f07ce-104">Testo</span><span class="sxs-lookup"><span data-stu-id="f07ce-104">Text</span></span>

<span data-ttu-id="f07ce-105">L'elemento non è un elemento figlio del padre</span><span class="sxs-lookup"><span data-stu-id="f07ce-105">Element is not a child of it's parent</span></span>

## <a name="type"></a><span data-ttu-id="f07ce-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="f07ce-106">Type</span></span>

<span data-ttu-id="f07ce-107">Errore</span><span class="sxs-lookup"><span data-stu-id="f07ce-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="f07ce-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f07ce-108">Description</span></span>

<span data-ttu-id="f07ce-109">Quando [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) viene chiamato sull'elemento figlio restituito da [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) (usando le \_ costanti di navigazione NAVDIR FIRSTCHILD o NAVDIR \_ LastChild), l'elemento padre restituito non corrisponde all'elemento padre specificato nella chiamata **accNavigate** .</span><span class="sxs-lookup"><span data-stu-id="f07ce-109">When [**get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) is called on the child element returned by [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) (using either the NAVDIR\_FIRSTCHILD or NAVDIR\_LASTCHILD navigation constants), the parent element returned does not match the parent element specified in the **accNavigate** call.</span></span>

<span data-ttu-id="f07ce-110">Questo problema può causare problemi di navigazione per gli strumenti automatici perché l'attraversamento degli elementi potrebbe essere irregolare e imprevedibile.</span><span class="sxs-lookup"><span data-stu-id="f07ce-110">This issue can cause navigation problems for automated tools because traversing elements might be erratic and unpredictable.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="f07ce-111">Possibili cause</span><span class="sxs-lookup"><span data-stu-id="f07ce-111">Possible causes</span></span>

<span data-ttu-id="f07ce-112">Implementazione MSAA non corretta o non valida.</span><span class="sxs-lookup"><span data-stu-id="f07ce-112">An incorrect or invalid MSAA implementation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f07ce-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f07ce-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f07ce-114">**IAccessible:: accNavigate**</span><span class="sxs-lookup"><span data-stu-id="f07ce-114">**IAccessible::accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
</dt> <dt>

[<span data-ttu-id="f07ce-115">**IAccessible:: Get \_ accParent**</span><span class="sxs-lookup"><span data-stu-id="f07ce-115">**IAccessible::get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)
</dt> </dl>

 

 




