---
title: Recupero di un oggetto IAccessible
description: Microsoft Active Accessibility fornisce funzioni quali AccessibleObjectFromWindow e AccessibleObjectFromPoint che consentono ai client di recuperare gli oggetti accessibili.
ms.assetid: 971cbead-128b-465a-8e77-2a20217f8d0f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89237916597f27c7179fce9516df1e0ecf43a6db
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328791"
---
# <a name="retrieving-an-iaccessible-object"></a><span data-ttu-id="85a05-103">Recupero di un oggetto IAccessible</span><span class="sxs-lookup"><span data-stu-id="85a05-103">Retrieving an IAccessible Object</span></span>

<span data-ttu-id="85a05-104">Microsoft Active Accessibility fornisce funzioni quali [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) e [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint) che consentono ai client di recuperare gli oggetti accessibili.</span><span class="sxs-lookup"><span data-stu-id="85a05-104">Microsoft Active Accessibility provides functions such as [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) and [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint) that allow clients to retrieve accessible objects.</span></span> <span data-ttu-id="85a05-105">Queste funzioni restituiscono un puntatore all'interfaccia [**IDispatch**](idispatch-interface.md) o [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) tramite il quale i client ottengono informazioni sull'oggetto accessibile.</span><span class="sxs-lookup"><span data-stu-id="85a05-105">These functions return either an [**IDispatch**](idispatch-interface.md) or [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer through which clients get information about the accessible object.</span></span>

<span data-ttu-id="85a05-106">Quando un client chiama [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) o qualsiasi altra funzione \**AccessibleObjectFrom \* \* \* X* che recupera un'interfaccia a un oggetto, Microsoft Active Accessibility invia il messaggio della finestra [**WM \_ GetObject**](wm-getobject.md) alla routine della finestra applicabile all'interno dell'applicazione appropriata.</span><span class="sxs-lookup"><span data-stu-id="85a05-106">When a client calls [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) or any of the other \**AccessibleObjectFrom\*\*\*X* functions that retrieve an interface to an object, Microsoft Active Accessibility sends the [**WM\_GETOBJECT**](wm-getobject.md) window message to the applicable window procedure within the appropriate application.</span></span> <span data-ttu-id="85a05-107">Per fornire informazioni ai client, i server devono rispondere al messaggio **WM \_ GetObject** .</span><span class="sxs-lookup"><span data-stu-id="85a05-107">To provide information to clients, servers must respond to the **WM\_GETOBJECT** message.</span></span>

<span data-ttu-id="85a05-108">Per raccogliere informazioni specifiche su un elemento dell'interfaccia utente, i client devono prima recuperare un'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="85a05-108">To collect specific information about a UI element, clients must first retrieve an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface for the element.</span></span> <span data-ttu-id="85a05-109">Per recuperare l'oggetto **IAccessible** di un elemento, i client possono usare una delle funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="85a05-109">To retrieve an element's **IAccessible** object, clients can use one of the following functions:</span></span>

-   [<span data-ttu-id="85a05-110">**AccessibleObjectFromPoint**</span><span class="sxs-lookup"><span data-stu-id="85a05-110">**AccessibleObjectFromPoint**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
-   [<span data-ttu-id="85a05-111">**AccessibleObjectFromWindow**</span><span class="sxs-lookup"><span data-stu-id="85a05-111">**AccessibleObjectFromWindow**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)
-   [<span data-ttu-id="85a05-112">**AccessibleObjectFromEvent**</span><span class="sxs-lookup"><span data-stu-id="85a05-112">**AccessibleObjectFromEvent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)

<span data-ttu-id="85a05-113">**Per recuperare un puntatore di interfaccia IAccessible**</span><span class="sxs-lookup"><span data-stu-id="85a05-113">**To retrieve an IAccessible Interface Pointer**</span></span>

1.  <span data-ttu-id="85a05-114">Il client chiama una delle funzioni \**AccessibleObjectFrom \* \* \* X* .</span><span class="sxs-lookup"><span data-stu-id="85a05-114">Client calls one of the \**AccessibleObjectFrom\*\*\*X* functions.</span></span>
2.  <span data-ttu-id="85a05-115">Oleacc.dll Invia un messaggio [**WM \_ GetObject**](wm-getobject.md) al server.</span><span class="sxs-lookup"><span data-stu-id="85a05-115">Oleacc.dll sends a [**WM\_GETOBJECT**](wm-getobject.md) message to server.</span></span>
3.  <span data-ttu-id="85a05-116">Il server determina quale elemento dell'interfaccia utente corrisponde alla richiesta.</span><span class="sxs-lookup"><span data-stu-id="85a05-116">The server determines which UI element corresponds to the request.</span></span>
4.  <span data-ttu-id="85a05-117">Il server restituisce zero per richiedere un proxy di Oleacc.dll,</span><span class="sxs-lookup"><span data-stu-id="85a05-117">The server either returns zero to request an Oleacc.dll proxy,</span></span>

    <span data-ttu-id="85a05-118">Oppure</span><span class="sxs-lookup"><span data-stu-id="85a05-118">Or</span></span>

    <span data-ttu-id="85a05-119">Restituisce un oggetto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) (implementazione nativa).</span><span class="sxs-lookup"><span data-stu-id="85a05-119">Returns an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object (native implementation).</span></span> <span data-ttu-id="85a05-120">A tale scopo, è necessario:</span><span class="sxs-lookup"><span data-stu-id="85a05-120">To do this, it:</span></span>

    -   <span data-ttu-id="85a05-121">Costruisce un oggetto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="85a05-121">Constructs an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object for the element.</span></span>
    -   <span data-ttu-id="85a05-122">Chiama [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) per effettuare il marshalling del puntatore dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="85a05-122">Calls [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) to marshal the object's pointer.</span></span>
    -   <span data-ttu-id="85a05-123">Restituisce LRESULT per Oleacc.dll.</span><span class="sxs-lookup"><span data-stu-id="85a05-123">Returns the LRESULT to Oleacc.dll.</span></span>

5.  <span data-ttu-id="85a05-124">Oleacc.dll esamina il valore restituito da [**WM \_ GetObject**](wm-getobject.md).</span><span class="sxs-lookup"><span data-stu-id="85a05-124">Oleacc.dll examines the return value from [**WM\_GETOBJECT**](wm-getobject.md).</span></span>

    <span data-ttu-id="85a05-125">Se è zero, Oleacc.dll costruisce un oggetto proxy e lo restituisce al client.</span><span class="sxs-lookup"><span data-stu-id="85a05-125">If it is zero, Oleacc.dll constructs a proxy object and returns it to the client.</span></span>

    <span data-ttu-id="85a05-126">Oppure</span><span class="sxs-lookup"><span data-stu-id="85a05-126">Or</span></span>

    <span data-ttu-id="85a05-127">Se è diverso da zero, Oleacc.dll chiama [**ObjectFromLresult**](/windows/desktop/api/Oleacc/nf-oleacc-objectfromlresult) per annullare il marshalling del puntatore all'oggetto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) nativo e restituirlo al client.</span><span class="sxs-lookup"><span data-stu-id="85a05-127">If it is nonzero, Oleacc.dll calls [**ObjectFromLresult**](/windows/desktop/api/Oleacc/nf-oleacc-objectfromlresult) to unmarshal the native [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object pointer and returns it to the client.</span></span>

 

 




