---
title: Interfacce duali (ADSI)
description: Utilizzare le interfacce COM per accedere alle proprietà e ai metodi di qualsiasi oggetto ADSI del provider.
ms.assetid: 6f3fd725-d660-4cc3-8de2-8ed7800b1141
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a34c858275098dd82362d229bc9e1cc35b544c55
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730186"
---
# <a name="dual-interfaces-adsi"></a><span data-ttu-id="9511b-103">Interfacce duali (ADSI)</span><span class="sxs-lookup"><span data-stu-id="9511b-103">Dual Interfaces (ADSI)</span></span>

<span data-ttu-id="9511b-104">Utilizzare le interfacce COM per accedere alle proprietà e ai metodi di qualsiasi oggetto ADSI del provider.</span><span class="sxs-lookup"><span data-stu-id="9511b-104">Use COM interfaces to access the properties and methods on any provider ADSI objects.</span></span> <span data-ttu-id="9511b-105">Una proprietà di sola lettura viene mappata a una voce di interfaccia del form **get \_ <PropertyName>**.</span><span class="sxs-lookup"><span data-stu-id="9511b-105">A read-only property maps to an interface entry of the form **get\_<PropertyName>**.</span></span> <span data-ttu-id="9511b-106">Una proprietà di lettura/scrittura esegue il mapping a due voci di interfaccia del form **get \_ <PropertyName>** e **put \_ <PropertyName>**.</span><span class="sxs-lookup"><span data-stu-id="9511b-106">A read/write property maps to two interface entries of the form **get\_<PropertyName>** and **put\_<PropertyName>**.</span></span>

<span data-ttu-id="9511b-107">Tutti i metodi in un'interfaccia COM devono:</span><span class="sxs-lookup"><span data-stu-id="9511b-107">All methods on a COM interface must:</span></span>

-   <span data-ttu-id="9511b-108">Restituisce un valore HRESULT per indicare l'esito positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="9511b-108">Return an HRESULT value to indicate success or failure.</span></span> <span data-ttu-id="9511b-109">Il tipo **HRESULT** viene descritto nella specifica com.</span><span class="sxs-lookup"><span data-stu-id="9511b-109">The **HRESULT** type is discussed in the COM specification.</span></span>
-   <span data-ttu-id="9511b-110">Nelle chiamate a **QueryInterface**, restituire **E \_ nointerface** per le interfacce non implementate.</span><span class="sxs-lookup"><span data-stu-id="9511b-110">On calls to **QueryInterface**, return **E\_NOINTERFACE** for unimplemented interfaces.</span></span>
-   <span data-ttu-id="9511b-111">Restituisce **E \_ NOTIMPL** per i metodi non implementati sulle interfacce altrimenti implementate.</span><span class="sxs-lookup"><span data-stu-id="9511b-111">Return **E\_NOTIMPL** for unimplemented methods on interfaces that are otherwise implemented.</span></span>
-   <span data-ttu-id="9511b-112">La **Proprietà return E \_ Ads \_ non è \_ \_ supportata** per le proprietà dell'interfaccia che non sono supportate.</span><span class="sxs-lookup"><span data-stu-id="9511b-112">Return **E\_ADS\_PROPERTY\_NOT\_SUPPORTED** for interface properties that are not supported.</span></span>

<span data-ttu-id="9511b-113">Per mantenere la compatibilità con i controller di automazione, tutti i parametri e i tipi restituiti devono essere inclusi nel subset definito dal tipo di dati VARIANT di automazione.</span><span class="sxs-lookup"><span data-stu-id="9511b-113">To retain compatibility with Automation controllers, all parameters and return types should be within the subset defined by the Automation VARIANT data type.</span></span> <span data-ttu-id="9511b-114">Per ulteriori informazioni, vedere **Variant** e **VARIANTARG** in Platform Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="9511b-114">For more information, see **VARIANT** and **VARIANTARG** in the Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="9511b-115">Un provider Active Directory oggetto può esporre interfacce che usano tipi di dati diversi da quelli nel subset di **varianti** .</span><span class="sxs-lookup"><span data-stu-id="9511b-115">A provider Active Directory object can expose interfaces that use data types other than those in the **VARIANT** subset.</span></span> <span data-ttu-id="9511b-116">Tuttavia, i controller di automazione come Visual Basic non sono in grado di chiamare tali interfacce.</span><span class="sxs-lookup"><span data-stu-id="9511b-116">However, Automation controllers such as Visual Basic are not able to call those interfaces.</span></span> <span data-ttu-id="9511b-117">La maggior parte delle interfacce del provider ADSI sono derivate da [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) e possono essere usate come puntatori dell'interfaccia **IDispatch** .</span><span class="sxs-lookup"><span data-stu-id="9511b-117">Most ADSI provider interfaces are derived from [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) and can be used as **IDispatch** interface pointers.</span></span> <span data-ttu-id="9511b-118">Tuttavia, le interfacce ADSI [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject), [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)e [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) non sono derivate da **IDispatch**.</span><span class="sxs-lookup"><span data-stu-id="9511b-118">However, the [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject), [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch), and [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) ADSI interfaces are not derived from **IDispatch**.</span></span>

 

 