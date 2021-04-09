---
title: Considerazioni di progettazione per gli oggetti proxy
description: Il proxy e la progettazione degli oggetti accessibili dipendono dalla progettazione degli elementi dell'interfaccia utente del server. Indipendentemente dalla progettazione, un elemento dell'interfaccia utente deve notificare all'oggetto proxy immediatamente prima che venga eliminato definitivamente, in modo che l'oggetto proxy gestisca le chiamate dai client in modo appropriato.
ms.assetid: 83a9ff66-2fe6-4589-a187-cdaf207b02b8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9578c79f93f91834dec14808a1a1867f40b215a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044302"
---
# <a name="design-considerations-for-proxy-objects"></a><span data-ttu-id="a10fd-104">Considerazioni di progettazione per gli oggetti proxy</span><span class="sxs-lookup"><span data-stu-id="a10fd-104">Design Considerations for Proxy Objects</span></span>

<span data-ttu-id="a10fd-105">Il proxy e la progettazione degli oggetti accessibili dipendono dalla progettazione degli elementi dell'interfaccia utente del server.</span><span class="sxs-lookup"><span data-stu-id="a10fd-105">Proxy and accessible object design depends on the design of the server UI elements.</span></span> <span data-ttu-id="a10fd-106">Indipendentemente dalla progettazione, un elemento dell'interfaccia utente deve notificare all'oggetto proxy immediatamente prima che venga eliminato definitivamente, in modo che l'oggetto proxy gestisca le chiamate dai client in modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="a10fd-106">Regardless of the design, a UI element must notify its proxy object right before it is destroyed so that the proxy object handles calls from clients appropriately.</span></span>

<span data-ttu-id="a10fd-107">Nell'elenco seguente vengono descritte due possibilità di progettazione:</span><span class="sxs-lookup"><span data-stu-id="a10fd-107">The following list describes two design possibilities:</span></span>

-   <span data-ttu-id="a10fd-108">Inserire il codice che implementa l'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) nello stesso modulo del codice che implementa l'elemento dell'interfaccia utente se il codice dell'interfaccia utente è facilmente estendibile.</span><span class="sxs-lookup"><span data-stu-id="a10fd-108">Place the code that implements the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface in the same module as the code that implements the user interface element if the user interface code is easily extensible.</span></span> <span data-ttu-id="a10fd-109">In questo caso, il proxy è "leggero" nel senso che tutto ciò che esegue è il monitoraggio della durata dell'oggetto accessibile, l'inoltro delle chiamate all'oggetto accessibile e la restituzione dei risultati.</span><span class="sxs-lookup"><span data-stu-id="a10fd-109">In this case, the proxy is "lightweight" in the sense that all it does is monitor the life span of the accessible object, forward calls to the accessible object, and return the results.</span></span>
-   <span data-ttu-id="a10fd-110">Inserire il codice che implementa [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) nello stesso modulo del codice che implementa l'oggetto proxy.</span><span class="sxs-lookup"><span data-stu-id="a10fd-110">Place the code that implements [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) in the same module as the code that implements the proxy object.</span></span> <span data-ttu-id="a10fd-111">In questo caso, l'oggetto accessibile utilizza funzioni interne per ottenere informazioni sull'elemento dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="a10fd-111">In this case, the accessible object uses internal functions to obtain information about the UI element.</span></span>

## <a name="trackbar-controls"></a><span data-ttu-id="a10fd-112">Controlli TrackBar</span><span class="sxs-lookup"><span data-stu-id="a10fd-112">Trackbar Controls</span></span>

<span data-ttu-id="a10fd-113">Quando si implementano i controlli TrackBar, utilizzare il tipo di oggetto TrackBar **\_ invertito** per fornire informazioni più significative.</span><span class="sxs-lookup"><span data-stu-id="a10fd-113">When implementing trackbar controls, use the trackbar style **TBS\_REVERSED** to provide more meaningful information.</span></span> <span data-ttu-id="a10fd-114">Questo stile inverte la scala utilizzata da [**IAccessible:: Get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue).</span><span class="sxs-lookup"><span data-stu-id="a10fd-114">This style reverses the scale used by [**IAccessible::get\_accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue).</span></span>

<span data-ttu-id="a10fd-115">Per gli TrackBar verticali senza questo stile, [**IAccessible:: Get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) restituisce zero (0) quando il cursore TrackBar si trova nella parte superiore del controllo; i valori aumentano quando si scorre il cursore verso il basso.</span><span class="sxs-lookup"><span data-stu-id="a10fd-115">For vertical trackbars without this style, [**IAccessible::get\_accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) returns zero (0) when the trackbar thumb is at the top of the control; the values increase as you slide the thumb toward the bottom.</span></span> <span data-ttu-id="a10fd-116">Con lo stile **TBS \_ invertito** , **IAccessible:: Get \_ accValue** restituisce 100 (100) quando il cursore TrackBar si trova nella parte superiore; i numeri diminuiscono quando si sposta il cursore del controllo TrackBar verso il basso.</span><span class="sxs-lookup"><span data-stu-id="a10fd-116">With the **TBS\_REVERSED** style, **IAccessible::get\_accValue** returns one hundred (100) when the trackbar thumb is at the top; the numbers decrease as you move the trackbar thumb toward the bottom.</span></span>

<span data-ttu-id="a10fd-117">Per gli TrackBar orizzontali senza questo stile, viene restituito zero (0) quando il cursore TrackBar si trova all'estremità sinistra del controllo; i valori aumentano quando si sposta il cursore del controllo TrackBar a destra.</span><span class="sxs-lookup"><span data-stu-id="a10fd-117">For horizontal trackbars without this style, zero (0) is returned when the trackbar thumb is at the left end of the control; the values increase as you move the trackbar thumb to the right.</span></span> <span data-ttu-id="a10fd-118">Con lo stile **TBS \_ invertito** , [**IAccessible:: Get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) restituisce 100 (100) quando il cursore TrackBar si trova a sinistra; i valori diminuiscono quando si sposta il cursore del controllo TrackBar a destra.</span><span class="sxs-lookup"><span data-stu-id="a10fd-118">With the **TBS\_REVERSED** style, [**IAccessible::get\_accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) returns one hundred (100) when the trackbar thumb is at the left; the values decrease as you move the trackbar thumb to the right.</span></span>

 

 




