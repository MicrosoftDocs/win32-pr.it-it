---
title: Interfacce duali IAccessible e IDispatch
description: Gli sviluppatori di server devono fornire il IDispatch dell'interfaccia standard Component Object Model (COM) per i relativi oggetti accessibili.
ms.assetid: 043d6777-6f9a-4e93-aadc-9cbe9a9119c4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72bbe19e35a04414253dc8f22c4edbc19a041b27
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299840"
---
# <a name="dual-interfaces-iaccessible-and-idispatch"></a><span data-ttu-id="7fcc7-103">Interfacce doppie: IAccessible e IDispatch</span><span class="sxs-lookup"><span data-stu-id="7fcc7-103">Dual Interfaces: IAccessible and IDispatch</span></span>

<span data-ttu-id="7fcc7-104">Gli sviluppatori di server devono fornire il [**IDispatch**](idispatch-interface.md) dell'interfaccia standard Component Object Model (com) per i relativi oggetti accessibili.</span><span class="sxs-lookup"><span data-stu-id="7fcc7-104">Server developers must provide the standard Component Object Model (COM) interface [**IDispatch**](idispatch-interface.md) for their accessible objects.</span></span> <span data-ttu-id="7fcc7-105">L'interfaccia IDispatch consente alle applicazioni client scritte in Microsoft Visual Basic e a diversi linguaggi di scripting di utilizzare i metodi e le proprietà esposti da [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span><span class="sxs-lookup"><span data-stu-id="7fcc7-105">The IDispatch interface allows client applications written in Microsoft Visual Basic and various scripting languages to use the methods and properties exposed by [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span></span> <span data-ttu-id="7fcc7-106">Poiché un oggetto accessibile fornisce l'accesso a un oggetto indirettamente tramite [IDispatch:: Invoke]( /windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) o direttamente con **IAccessible**, si dice che dispone di un'interfaccia duale.</span><span class="sxs-lookup"><span data-stu-id="7fcc7-106">Because an accessible object provides access to an object either indirectly through [IDispatch::Invoke]( /windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) or directly with **IAccessible**, it is said to have a dual interface.</span></span>

<span data-ttu-id="7fcc7-107">Quando i client C/C++ ottengono un puntatore di interfaccia IDispatch, i client possono chiamare [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) per provare a convertire il puntatore dell'interfaccia IDispatch in un puntatore a interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .</span><span class="sxs-lookup"><span data-stu-id="7fcc7-107">When C/C++ clients get back an IDispatch interface pointer, clients can call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to try converting the IDispatch interface pointer to an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer.</span></span> <span data-ttu-id="7fcc7-108">Per chiamare indirettamente i metodi **IAccessible** , i client C/C++ chiamano IDispatch:: Invoke.</span><span class="sxs-lookup"><span data-stu-id="7fcc7-108">To call the **IAccessible** methods indirectly, C/C++ clients call IDispatch::Invoke.</span></span> <span data-ttu-id="7fcc7-109">Per migliorare le prestazioni, chiamare i metodi **IAccessible** per utilizzare l'oggetto direttamente.</span><span class="sxs-lookup"><span data-stu-id="7fcc7-109">For improved performance, call the **IAccessible** methods to use the object directly.</span></span>

<span data-ttu-id="7fcc7-110">Per un elenco degli ID di invio (DISPID) usati da **IDispatch** per identificare i metodi e le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , vedere [Appendice C: IAccessible DISPID](appendix-c--iaccessible-dispids.md).</span><span class="sxs-lookup"><span data-stu-id="7fcc7-110">For a list of the dispatch IDs (DISPIDs) that **IDispatch** uses to identify the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods and properties, see [Appendix C: IAccessible DISPIDs](appendix-c--iaccessible-dispids.md).</span></span>

> [!Note]  
> <span data-ttu-id="7fcc7-111">Nella versione 2,0 e successive di Microsoft Active Accessibility, i server non devono implementare completamente i metodi di [**IDispatch**](idispatch-interface.md) ma possono semplicemente restituire E \_ NOTIMPL dopo l'inizializzazione di tutti i parametri out, come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="7fcc7-111">Under version 2.0 and later of Microsoft Active Accessibility, servers do not have to fully implement the methods of [**IDispatch**](idispatch-interface.md) but can simply return E\_NOTIMPL after initializing any out parameters, as shown in the following example.</span></span>

 


```C++
HRESULT STDMETHODCALLTYPE AccServer::GetTypeInfoCount(UINT* pctinfo)
{
    *pctinfo = 0;
    return E_NOTIMPL;
};
```



 

 