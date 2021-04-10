---
title: ElementsChildHasDifferentParent
description: ElementsChildHasDifferentParent
ms.assetid: 2347A33C-8FBD-4C30-8B40-9CB35F121C8E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 843ea0f0ec7708f91d407f1fa7a55fa59a813234
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332655"
---
# <a name="elementschildhasdifferentparent"></a><span data-ttu-id="2a71f-103">ElementsChildHasDifferentParent</span><span class="sxs-lookup"><span data-stu-id="2a71f-103">ElementsChildHasDifferentParent</span></span>

## <a name="text"></a><span data-ttu-id="2a71f-104">Testo</span><span class="sxs-lookup"><span data-stu-id="2a71f-104">Text</span></span>

<span data-ttu-id="2a71f-105">L'elemento figlio () dell'elemento {0} ha un {1} elemento padre () diverso</span><span class="sxs-lookup"><span data-stu-id="2a71f-105">Element's child({0}) has different parent({1}) than element</span></span>

## <a name="type"></a><span data-ttu-id="2a71f-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="2a71f-106">Type</span></span>

<span data-ttu-id="2a71f-107">Errore</span><span class="sxs-lookup"><span data-stu-id="2a71f-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="2a71f-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2a71f-108">Description</span></span>

<span data-ttu-id="2a71f-109">Questo errore indica che, quando viene chiamato il metodo [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) sugli elementi figlio dell'elemento target, gli elementi figlio non segnalano un elemento padre coerente.</span><span class="sxs-lookup"><span data-stu-id="2a71f-109">This error indicates that, when [**get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) is called on the children of the target element, the children do not report a consistent parent.</span></span>

![esempio di elementi figlio di un elemento che segnala un padre incoerente](images/accchecker-inconsistent-parent.png)

<span data-ttu-id="2a71f-111">Questo problema può causare problemi di navigazione per gli strumenti automatici perché l'attraversamento degli elementi potrebbe essere irregolare e imprevedibile.</span><span class="sxs-lookup"><span data-stu-id="2a71f-111">This issue can cause navigation problems for automated tools because traversing elements might be erratic and unpredictable.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="2a71f-112">Possibili cause</span><span class="sxs-lookup"><span data-stu-id="2a71f-112">Possible causes</span></span>

<span data-ttu-id="2a71f-113">Implementazione MSAA non corretta o non valida.</span><span class="sxs-lookup"><span data-stu-id="2a71f-113">An incorrect or invalid MSAA implementation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2a71f-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2a71f-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a71f-115">**AccessibleChildren**</span><span class="sxs-lookup"><span data-stu-id="2a71f-115">**AccessibleChildren**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren)
</dt> </dl>

 

 




