---
title: Come gestire WM_GETOBJECT
description: Quando riceve un messaggio WM \_ GetObject che contiene il \_ client ObjID, il server deve restituire un puntatore all'oggetto che implementa IAccessible.
ms.assetid: 455398b7-f748-4ab0-8953-3f74439e44f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6223d75339f537ccf1939f9c9af46a42aa47bfdb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711716"
---
# <a name="how-to-handle-wm_getobject"></a><span data-ttu-id="a6685-103">Come gestire WM \_ GETobject</span><span class="sxs-lookup"><span data-stu-id="a6685-103">How to Handle WM\_GETOBJECT</span></span>

<span data-ttu-id="a6685-104">Quando riceve un messaggio [**WM \_ GetObject**](wm-getobject.md) che contiene il [**\_ client ObjID**](object-identifiers.md), il server deve restituire un puntatore all'oggetto che implementa [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span><span class="sxs-lookup"><span data-stu-id="a6685-104">When it receives a [**WM\_GETOBJECT**](wm-getobject.md) message that contains [**OBJID\_CLIENT**](object-identifiers.md), the server must return a pointer to the object that implements [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span></span> <span data-ttu-id="a6685-105">Questo puntatore è un LRESULT ottenuto chiamando [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject).</span><span class="sxs-lookup"><span data-stu-id="a6685-105">This pointer is an LRESULT that is obtained by calling [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject).</span></span> <span data-ttu-id="a6685-106">Microsoft Active Accessibility, insieme alla libreria di Component Object Model (COM), esegue il marshalling appropriato e passa il puntatore all'interfaccia **IAccessible** dal server al client.</span><span class="sxs-lookup"><span data-stu-id="a6685-106">Microsoft Active Accessibility, in conjunction with the Component Object Model (COM) library, performs the appropriate marshaling and passes the **IAccessible** interface pointer from the server to the client.</span></span>

<span data-ttu-id="a6685-107">I server devono gestire correttamente il conteggio dei riferimenti per l'oggetto accessibile.</span><span class="sxs-lookup"><span data-stu-id="a6685-107">Servers must correctly handle reference counting on the accessible object.</span></span> <span data-ttu-id="a6685-108">Tenere presente che quando si crea un oggetto COM, il conteggio dei riferimenti è 1.</span><span class="sxs-lookup"><span data-stu-id="a6685-108">Remember that when you create a COM object, the reference count is 1.</span></span> <span data-ttu-id="a6685-109">[**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) incrementa il conteggio dei riferimenti più volte.</span><span class="sxs-lookup"><span data-stu-id="a6685-109">[**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) then further increments the reference count several times.</span></span> <span data-ttu-id="a6685-110">Tutti i riferimenti creati da **LresultFromObject** vengono rilasciati automaticamente quando l'oggetto non è più necessario, ma il server è responsabile del rilascio del riferimento iniziale e, a meno che non lo faccia, l'oggetto non verrà mai eliminato definitivamente.</span><span class="sxs-lookup"><span data-stu-id="a6685-110">All the references created by **LresultFromObject** are automatically released when the object is no longer needed, but the server is responsible for releasing the initial reference, and unless it does so, the object will never be destroyed.</span></span> <span data-ttu-id="a6685-111">Negli esempi nelle sezioni seguenti viene illustrato come rilasciare i riferimenti agli oggetti accessibili.</span><span class="sxs-lookup"><span data-stu-id="a6685-111">The examples in the following sections show how to release references to accessible objects.</span></span>

<span data-ttu-id="a6685-112">I server in genere gestiscono [**WM \_ GetObject**](wm-getobject.md) in uno dei modi seguenti:</span><span class="sxs-lookup"><span data-stu-id="a6685-112">Servers typically handle [**WM\_GETOBJECT**](wm-getobject.md) in one of the following ways:</span></span>

-   [<span data-ttu-id="a6685-113">Creare nuovi oggetti accessibili</span><span class="sxs-lookup"><span data-stu-id="a6685-113">Create New Accessible Objects</span></span>](create-new-accessible-objects.md)
-   [<span data-ttu-id="a6685-114">Riutilizza puntatori esistenti a oggetti</span><span class="sxs-lookup"><span data-stu-id="a6685-114">Reuse Existing Pointers to Objects</span></span>](reuse-existing-pointers-to-objects.md)
-   [<span data-ttu-id="a6685-115">Crea nuove interfacce per lo stesso oggetto</span><span class="sxs-lookup"><span data-stu-id="a6685-115">Create New Interfaces to the Same Object</span></span>](create-new-interfaces-to-the-same-object.md)

> [!Note]  
> <span data-ttu-id="a6685-116">In questa sezione, come nel resto della documentazione, quando viene discusso un puntatore a un'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , questo puntatore può essere effettivamente un puntatore a un oggetto proxy che esegue il wrapping dell'interfaccia **IAccessible** .</span><span class="sxs-lookup"><span data-stu-id="a6685-116">In this section as in the rest of the documentation, when a pointer to an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface is discussed, this pointer may actually be a pointer to a proxy object that wraps the **IAccessible** interface.</span></span> <span data-ttu-id="a6685-117">Per ulteriori informazioni sugli oggetti proxy, vedere [creazione di oggetti proxy](creating-proxy-objects.md).</span><span class="sxs-lookup"><span data-stu-id="a6685-117">For more information about proxy objects, see [Creating Proxy Objects](creating-proxy-objects.md).</span></span>

 

<span data-ttu-id="a6685-118">Per una panoramica di [**WM \_ GetObject**](wm-getobject.md), vedere funzionamento di [WM \_ GetObject](how-wm-getobject-works.md).</span><span class="sxs-lookup"><span data-stu-id="a6685-118">For an overview of [**WM\_GETOBJECT**](wm-getobject.md), see [How WM\_GETOBJECT Works](how-wm-getobject-works.md).</span></span>

 

 




