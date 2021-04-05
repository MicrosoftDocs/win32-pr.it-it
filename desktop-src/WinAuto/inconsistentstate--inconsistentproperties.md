---
title: InconsistentState, InconsistentProperties
description: InconsistentState, InconsistentProperties
ms.assetid: 82A2ECA8-0155-402A-A745-B97D3F633643
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5522025eff8aecbdf0f4313c0052afebd4a17958
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708728"
---
# <a name="inconsistentstate-inconsistentproperties"></a><span data-ttu-id="986c9-103">InconsistentState, InconsistentProperties</span><span class="sxs-lookup"><span data-stu-id="986c9-103">InconsistentState, InconsistentProperties</span></span>

## <a name="text"></a><span data-ttu-id="986c9-104">Testo</span><span class="sxs-lookup"><span data-stu-id="986c9-104">Text</span></span>

<span data-ttu-id="986c9-105">Un controllo ha stati/proprietà che sono incoerenti {0} e {1}</span><span class="sxs-lookup"><span data-stu-id="986c9-105">A control has states/properties that are inconsistent {0} and {1}</span></span>

## <a name="type"></a><span data-ttu-id="986c9-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="986c9-106">Type</span></span>

<span data-ttu-id="986c9-107">Errore</span><span class="sxs-lookup"><span data-stu-id="986c9-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="986c9-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="986c9-108">Description</span></span>

<span data-ttu-id="986c9-109">Un elemento segnala stati MSAA incoerenti o in conflitto o proprietà di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="986c9-109">An element is reporting inconsistent or conflicting MSAA states or UI Automation properties.</span></span> <span data-ttu-id="986c9-110">Ad esempio, quando il metodo [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate) restituisce una delle combinazioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="986c9-110">For example, when the [**get\_accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate) method returns any of the following combinations.</span></span>

-   <span data-ttu-id="986c9-111">\_Sistema \_ di stato espanso e \_ sistema di stato \_ compresso</span><span class="sxs-lookup"><span data-stu-id="986c9-111">STATE\_SYSTEM\_EXPANDED and STATE\_SYSTEM\_COLLAPSED</span></span>
-   <span data-ttu-id="986c9-112">\_Sistema \_ di stato selezionato e non stato \_ sistema \_ selezionabile</span><span class="sxs-lookup"><span data-stu-id="986c9-112">STATE\_SYSTEM\_SELECTED and not STATE\_SYSTEM\_SELECTABLE</span></span>
-   <span data-ttu-id="986c9-113">\_Sistema \_ di stato con stato attivo e non \_ attivabile dal sistema di stato \_</span><span class="sxs-lookup"><span data-stu-id="986c9-113">STATE\_SYSTEM\_FOCUSED and not STATE\_SYSTEM\_FOCUSABLE</span></span>

<span data-ttu-id="986c9-114">Questo problema causa problemi per gli utenti che si affidano a un lettore di schermate e a una tastiera per la navigazione perché uno stato dell'elemento errato potrebbe essere segnalato all'utente.</span><span class="sxs-lookup"><span data-stu-id="986c9-114">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because an incorrect element state might be reported to the user.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="986c9-115">Possibili cause</span><span class="sxs-lookup"><span data-stu-id="986c9-115">Possible causes</span></span>

<span data-ttu-id="986c9-116">L'elemento o il relativo padre hanno uno stato MSAA impostato in modo non appropriato.</span><span class="sxs-lookup"><span data-stu-id="986c9-116">The element or its parent has an MSAA state set inappropriately.</span></span>

## <a name="related-topics"></a><span data-ttu-id="986c9-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="986c9-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="986c9-118">**IAccessible:: Get \_ accState**</span><span class="sxs-lookup"><span data-stu-id="986c9-118">**IAccessible::get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)
</dt> <dt>

[<span data-ttu-id="986c9-119">**Costanti di stato dell'oggetto**</span><span class="sxs-lookup"><span data-stu-id="986c9-119">**Object State Constants**</span></span>](object-state-constants.md)
</dt> <dt>

[<span data-ttu-id="986c9-120">Stati e proprietà</span><span class="sxs-lookup"><span data-stu-id="986c9-120">States and Properties</span></span>](uiauto-msaa.md)
</dt> </dl>

 

 




