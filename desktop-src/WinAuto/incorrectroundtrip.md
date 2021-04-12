---
title: IncorrectRoundTrip
description: IncorrectRoundTrip
ms.assetid: 244537EB-E7DC-49E4-BEAF-CFE3ED25E0B2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1f154c0ccc0fff9bb654b94ef9d0807aa459d4b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221801"
---
# <a name="incorrectroundtrip"></a><span data-ttu-id="e3d8d-103">IncorrectRoundTrip</span><span class="sxs-lookup"><span data-stu-id="e3d8d-103">IncorrectRoundTrip</span></span>

## <a name="text"></a><span data-ttu-id="e3d8d-104">Testo</span><span class="sxs-lookup"><span data-stu-id="e3d8d-104">Text</span></span>

<span data-ttu-id="e3d8d-105">Chiamata a accNavigate ((fare clic su Snooze per ricordarsi di nuovo in:), 1, NAVDIR \_ successivo), quindi accNavigate ((Open), 2, NAVDIR \_ precedente), dovrebbe avere restituito clic su Snooze per ricordarsi di nuovo in: (childID = 1), ma restituito fare clic su Snooze per ricordarlo di nuovo in:</span><span class="sxs-lookup"><span data-stu-id="e3d8d-105">Call to accNavigate((Click Snooze to be reminded again in:), 1, NAVDIR\_NEXT), then accNavigate((Open), 2, NAVDIR\_PREVIOUS), should have returned Click Snooze to be reminded again in:(ChildId=1), but returned Click Snooze to be reminded again in:</span></span>

## <a name="type"></a><span data-ttu-id="e3d8d-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="e3d8d-106">Type</span></span>

<span data-ttu-id="e3d8d-107">Errore</span><span class="sxs-lookup"><span data-stu-id="e3d8d-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="e3d8d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e3d8d-108">Description</span></span>

<span data-ttu-id="e3d8d-109">l'uso di [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) per attraversare l'albero degli elementi della destinazione di verifica non restituisce lo stesso elemento iniziale quando la direzione di attraversamento è invertita.</span><span class="sxs-lookup"><span data-stu-id="e3d8d-109">using [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) to traverse the element tree of the verification target does not return the same starting element when the direction of traversal is reversed.</span></span>

![esempio di implementazione MSAA non valida che ha causato una navigazione non corretta del round trip](images/accchecker-invalid-round-trip.png)

<span data-ttu-id="e3d8d-111">Questo problema può causare problemi di navigazione per gli strumenti automatici perché l'attraversamento degli elementi potrebbe essere irregolare e imprevedibile.</span><span class="sxs-lookup"><span data-stu-id="e3d8d-111">This issue can cause navigation problems for automated tools because traversing elements might be erratic and unpredictable.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="e3d8d-112">Possibili cause</span><span class="sxs-lookup"><span data-stu-id="e3d8d-112">Possible causes</span></span>

<span data-ttu-id="e3d8d-113">Implementazione MSAA non corretta o non valida.</span><span class="sxs-lookup"><span data-stu-id="e3d8d-113">An incorrect or invalid MSAA implementation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e3d8d-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e3d8d-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3d8d-115">**IAccessible:: accNavigate**</span><span class="sxs-lookup"><span data-stu-id="e3d8d-115">**IAccessible::accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
</dt> </dl>

 

 




