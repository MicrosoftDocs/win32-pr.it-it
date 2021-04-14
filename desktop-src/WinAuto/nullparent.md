---
title: NullParent
description: NullParent
ms.assetid: F9563D73-66EF-4C66-8783-B034AA7A212E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 765217f8d2d46645358d590c5a93310b04da01b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329655"
---
# <a name="nullparent"></a><span data-ttu-id="afaf7-103">NullParent</span><span class="sxs-lookup"><span data-stu-id="afaf7-103">NullParent</span></span>

## <a name="text"></a><span data-ttu-id="afaf7-104">Testo</span><span class="sxs-lookup"><span data-stu-id="afaf7-104">Text</span></span>

<span data-ttu-id="afaf7-105">Elements Parent è NULL</span><span class="sxs-lookup"><span data-stu-id="afaf7-105">Elements parent is NULL</span></span>

## <a name="type"></a><span data-ttu-id="afaf7-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="afaf7-106">Type</span></span>

<span data-ttu-id="afaf7-107">Errore</span><span class="sxs-lookup"><span data-stu-id="afaf7-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="afaf7-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="afaf7-108">Description</span></span>

<span data-ttu-id="afaf7-109">Viene restituito NULL quando viene chiamato il metodo [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) sull'elemento.</span><span class="sxs-lookup"><span data-stu-id="afaf7-109">NULL is returned when [**get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) is called on the element.</span></span> <span data-ttu-id="afaf7-110">Il metodo **get \_ accParent** deve restituire null solo quando viene chiamato sull'elemento radice della destinazione di verifica.</span><span class="sxs-lookup"><span data-stu-id="afaf7-110">The **get\_accParent** method should return NULL only when called on the root element of the verification target.</span></span>

<span data-ttu-id="afaf7-111">Questo problema può causare problemi di navigazione per gli strumenti automatici perché l'attraversamento degli elementi potrebbe essere irregolare e imprevedibile.</span><span class="sxs-lookup"><span data-stu-id="afaf7-111">This issue can cause navigation problems for automated tools because traversing elements might be erratic and unpredictable.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="afaf7-112">Possibili cause</span><span class="sxs-lookup"><span data-stu-id="afaf7-112">Possible causes</span></span>

<span data-ttu-id="afaf7-113">Implementazione MSAA non corretta o non valida.</span><span class="sxs-lookup"><span data-stu-id="afaf7-113">An incorrect or invalid MSAA implementation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="afaf7-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="afaf7-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="afaf7-115">**IAccessible:: accNavigate**</span><span class="sxs-lookup"><span data-stu-id="afaf7-115">**IAccessible::accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
</dt> <dt>

[<span data-ttu-id="afaf7-116">**IAccessible:: Get \_ accParent**</span><span class="sxs-lookup"><span data-stu-id="afaf7-116">**IAccessible::get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)
</dt> </dl>

 

 




