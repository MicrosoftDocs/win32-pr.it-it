---
title: Usare OBJID \_ NATIVEOM per esporre un'interfaccia nativa per una finestra
description: Questa tecnica consente ai client di ottenere un oggetto personalizzato per una finestra. I server possono utilizzare questa operazione per esporre un puntatore a un oggetto documento personalizzato per una finestra.
ms.assetid: 91713fe5-f03f-464e-88ee-9d8d66d5b19d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c2c5c6ec194ca643475444feb5839c02d3fa890
ms.sourcegitcommit: 2e9db3c7d9a3dbea15196b03c883846fad6f32be
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/12/2019
ms.locfileid: "104398173"
---
# <a name="use-objid_nativeom-to-expose-a-native-interface-for-a-window"></a><span data-ttu-id="9df67-104">Usare OBJID \_ NATIVEOM per esporre un'interfaccia nativa per una finestra</span><span class="sxs-lookup"><span data-stu-id="9df67-104">Use OBJID\_NATIVEOM to expose a native interface for a window</span></span>

<span data-ttu-id="9df67-105">Questa tecnica consente ai client di ottenere un oggetto personalizzato per una finestra.</span><span class="sxs-lookup"><span data-stu-id="9df67-105">This technique allows clients to get a custom object for a window.</span></span> <span data-ttu-id="9df67-106">I server possono utilizzare questa operazione per esporre un puntatore a un oggetto documento personalizzato per una finestra.</span><span class="sxs-lookup"><span data-stu-id="9df67-106">Servers can use this to expose a pointer to a custom document object for a window.</span></span>

<span data-ttu-id="9df67-107">**Per esporre un'interfaccia del modello a oggetti nativo per una finestra (Server)**</span><span class="sxs-lookup"><span data-stu-id="9df67-107">**To expose a native object model interface for a window (servers)**</span></span>

1.  <span data-ttu-id="9df67-108">Gestire il messaggio [**WM \_ GetObject**](wm-getobject.md) nella routine della finestra.</span><span class="sxs-lookup"><span data-stu-id="9df67-108">Handle the [**WM\_GETOBJECT**](wm-getobject.md) message in the window procedure.</span></span> <span data-ttu-id="9df67-109">Quando il valore *lParam* è [**objid \_ NATIVEOM**](object-identifiers.md), restituisce un puntatore di interfaccia all'oggetto personalizzato utilizzando [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject).</span><span class="sxs-lookup"><span data-stu-id="9df67-109">When the *lParam* value is [**OBJID\_NATIVEOM**](object-identifiers.md), return an interface pointer to the custom object using [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject).</span></span>
2.  <span data-ttu-id="9df67-110">Rilasciare il puntatore di interfaccia dopo aver chiamato [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject), se appropriato.</span><span class="sxs-lookup"><span data-stu-id="9df67-110">Release your interface pointer after calling [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject), if appropriate.</span></span> <span data-ttu-id="9df67-111">Per ulteriori informazioni, vedere **LresultFromObject**.</span><span class="sxs-lookup"><span data-stu-id="9df67-111">For more information, see **LresultFromObject**.</span></span>

<span data-ttu-id="9df67-112">I client possono ottenere un puntatore a questo oggetto personalizzato.</span><span class="sxs-lookup"><span data-stu-id="9df67-112">Clients can obtain a pointer to this custom object.</span></span>

<span data-ttu-id="9df67-113">**Per ottenere un puntatore per un oggetto personalizzato per una finestra (client)**</span><span class="sxs-lookup"><span data-stu-id="9df67-113">**To obtain a pointer for a custom object for a window (clients)**</span></span>

-   <span data-ttu-id="9df67-114">Chiamare [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) e passare [**objid \_ NATIVEOM**](object-identifiers.md) come secondo parametro.</span><span class="sxs-lookup"><span data-stu-id="9df67-114">Call [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) and pass [**OBJID\_NATIVEOM**](object-identifiers.md) as the second parameter.</span></span>

<span data-ttu-id="9df67-115">Per questa tecnica si notino i problemi seguenti:</span><span class="sxs-lookup"><span data-stu-id="9df67-115">Note the following issues for this technique:</span></span>

-   <span data-ttu-id="9df67-116">Questa tecnica è simile alla restituzione di un puntatore a interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , fatta eccezione per l'ID oggetto utilizzato e il fatto che [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) restituisce un oggetto personalizzato anziché **IAccessible**.</span><span class="sxs-lookup"><span data-stu-id="9df67-116">This technique is similar to returning an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer except for the object ID used and the fact that [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) returns a custom object instead of **IAccessible**.</span></span>
-   <span data-ttu-id="9df67-117">Gli sviluppatori di server possono dover pubblicare informazioni che consentono ai client di identificare in modo univoco il **HWND** in modo che possano trovarlo prima di chiamare [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) sul relativo handle di finestra.</span><span class="sxs-lookup"><span data-stu-id="9df67-117">Server developers may need to publish information that allows clients to uniquely identify the **HWND** so that they can find it before calling [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) on its window handle.</span></span>
-   <span data-ttu-id="9df67-118">Non implementare l'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) nell'oggetto personalizzato restituito.</span><span class="sxs-lookup"><span data-stu-id="9df67-118">Do not implement the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface on the custom object that is returned.</span></span> <span data-ttu-id="9df67-119">In caso contrario, OLEACC lo considererà come un **IAccessible** standard e potrebbe impedire l'uso delle interfacce personalizzate.</span><span class="sxs-lookup"><span data-stu-id="9df67-119">If you do, OLEACC will treat it is as a standard **IAccessible** and may prevent the custom interfaces from being used.</span></span>
-   <span data-ttu-id="9df67-120">Per poter essere utilizzati tra i processi, potrebbe essere necessario registrare le interfacce sull'oggetto restituito con Component Object Model (COM).</span><span class="sxs-lookup"><span data-stu-id="9df67-120">In order to be used across processes, the interfaces on the returned object may need to be registered with Component Object Model (COM).</span></span>

<span data-ttu-id="9df67-121">Questa tecnica è supportata da diversi componenti Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="9df67-121">This technique is supported by several Microsoft Office components.</span></span> <span data-ttu-id="9df67-122">Per ulteriori informazioni, vedere [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow).</span><span class="sxs-lookup"><span data-stu-id="9df67-122">For more information, see [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow).</span></span>

 

 




