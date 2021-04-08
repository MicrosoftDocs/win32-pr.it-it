---
title: Ricezione di errori per i puntatori dell'interfaccia IAccessible
description: In questo argomento vengono descritte le situazioni in cui è possibile che venga visualizzato un errore per un puntatore di interfaccia IAccessible.
ms.assetid: 408bfa47-fda0-4a25-89c1-da41d967ad61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e54d3bd9e39dae9c5de9ad1644e5955bd5fb90d2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856546"
---
# <a name="receiving-errors-for-iaccessible-interface-pointers"></a><span data-ttu-id="2d634-103">Ricezione di errori per i puntatori dell'interfaccia IAccessible</span><span class="sxs-lookup"><span data-stu-id="2d634-103">Receiving Errors for IAccessible Interface Pointers</span></span>

<span data-ttu-id="2d634-104">In questo argomento vengono descritte le situazioni in cui è possibile che venga visualizzato un errore per un puntatore di interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .</span><span class="sxs-lookup"><span data-stu-id="2d634-104">This topic describes situations in which you might receive an error for an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer.</span></span> <span data-ttu-id="2d634-105">Le funzioni **IAccessible** possono restituire errori per i puntatori dell'interfaccia **IAccessible** quando un utente chiude un'applicazione a cui appartiene l'oggetto oppure se un utente chiude un controllo tramite l'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="2d634-105">**IAccessible** functions can return errors for **IAccessible** interface pointers when a user closes an application that the object belongs to, or if a user dismisses a control through the user interface.</span></span>

## <a name="user-closes-an-application"></a><span data-ttu-id="2d634-106">L'utente chiude un'applicazione</span><span class="sxs-lookup"><span data-stu-id="2d634-106">User Closes an Application</span></span>

<span data-ttu-id="2d634-107">Se un utente chiude l'applicazione che contiene un oggetto a cui punta il puntatore all'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , tutte le chiamate future a tale oggetto restituiranno un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="2d634-107">If a user closes the application that contains an object to which the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer was pointing, then all future calls to that object will return an error code.</span></span> <span data-ttu-id="2d634-108">L'errore, ad esempio **Co \_ E \_ OBJNOTCONNECTED**, indicherà che l'oggetto non esiste più.</span><span class="sxs-lookup"><span data-stu-id="2d634-108">The error, such as **CO\_E\_OBJNOTCONNECTED**, will indicate that the object does not exist anymore.</span></span> <span data-ttu-id="2d634-109">Si applica a tutti i puntatori dell'interfaccia **IAccessible** .</span><span class="sxs-lookup"><span data-stu-id="2d634-109">This applies to all **IAccessible** interface pointers.</span></span>

## <a name="user-dismisses-a-control"></a><span data-ttu-id="2d634-110">L'utente dimentica un controllo</span><span class="sxs-lookup"><span data-stu-id="2d634-110">User Dismisses a Control</span></span>

<span data-ttu-id="2d634-111">Se un utente omette un controllo (ad esempio, premendo un pulsante di push), i client possono comunque chiamare i metodi e le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per questo oggetto perché l'oggetto non è stato rilasciato.</span><span class="sxs-lookup"><span data-stu-id="2d634-111">If a user dismisses a control (for example, by pressing a push button), clients can still call [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods and properties on this object because the object has not been released.</span></span> <span data-ttu-id="2d634-112">Tuttavia, le chiamate future riceveranno messaggi di errore.</span><span class="sxs-lookup"><span data-stu-id="2d634-112">However, future calls will receive error messages.</span></span>

<span data-ttu-id="2d634-113">Questa situazione si applica alle funzioni e ai metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="2d634-113">This situation applies to the following functions and methods:</span></span>

-   [<span data-ttu-id="2d634-114">**AccessibleObjectFromEvent**</span><span class="sxs-lookup"><span data-stu-id="2d634-114">**AccessibleObjectFromEvent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)
-   [<span data-ttu-id="2d634-115">**AccessibleObjectFromPoint**</span><span class="sxs-lookup"><span data-stu-id="2d634-115">**AccessibleObjectFromPoint**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
-   [<span data-ttu-id="2d634-116">**AccessibleObjectFromWindow**</span><span class="sxs-lookup"><span data-stu-id="2d634-116">**AccessibleObjectFromWindow**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)
-   [<span data-ttu-id="2d634-117">**IAccessible:: accHitTest**</span><span class="sxs-lookup"><span data-stu-id="2d634-117">**IAccessible::accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="2d634-118">**IAccessible:: accNavigate**</span><span class="sxs-lookup"><span data-stu-id="2d634-118">**IAccessible::accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="2d634-119">**IAccessible:: Get \_ accFocus**</span><span class="sxs-lookup"><span data-stu-id="2d634-119">**IAccessible::get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)
-   [<span data-ttu-id="2d634-120">**IAccessible:: Get \_ accSelection**</span><span class="sxs-lookup"><span data-stu-id="2d634-120">**IAccessible::get\_accSelection**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection)

 

 




