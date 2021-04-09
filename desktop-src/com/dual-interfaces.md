---
title: Interfacce duali (COM)
description: Interfacce doppie
ms.assetid: 6e4dc529-8a25-4ae5-b868-28cb17e0db52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da95c77a307c40721b909eceb1e6d29bab23bc14
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104047472"
---
# <a name="dual-interfaces"></a><span data-ttu-id="ba18f-103">Interfacce doppie</span><span class="sxs-lookup"><span data-stu-id="ba18f-103">Dual Interfaces</span></span>

<span data-ttu-id="ba18f-104">L'automazione OLE consente a un oggetto di esporre un set di metodi in due modi: tramite l'interfaccia **IDispatch** e tramite l'associazione OLE vtable diretta.</span><span class="sxs-lookup"><span data-stu-id="ba18f-104">OLE Automation enables an object to expose a set of methods in two ways: via the **IDispatch** interface, and through direct OLE VTable binding.</span></span> <span data-ttu-id="ba18f-105">**IDispatch** è usato dalla maggior parte degli strumenti attualmente disponibili e offre supporto per l'associazione tardiva a proprietà e metodi.</span><span class="sxs-lookup"><span data-stu-id="ba18f-105">**IDispatch** is used by most tools available today, and offers support for late binding to properties and methods.</span></span>

<span data-ttu-id="ba18f-106">L'associazione VTable offre prestazioni molto più elevate poiché questo metodo viene chiamato direttamente anziché tramite **IDispatch:: Invoke**.</span><span class="sxs-lookup"><span data-stu-id="ba18f-106">VTable binding offers much higher performance because this method is called directly instead of through **IDispatch::Invoke**.</span></span> <span data-ttu-id="ba18f-107">**IDispatch** offre supporto con associazione tardiva, in cui l'associazione vtable diretta offre un miglioramento significativo delle prestazioni. entrambe le tecniche sono utili e importanti in scenari diversi.</span><span class="sxs-lookup"><span data-stu-id="ba18f-107">**IDispatch** offers late bound support, where direct VTable binding offers a significant performance gain; both techniques are valuable and important in different scenarios.</span></span> <span data-ttu-id="ba18f-108">Etichettando un'interfaccia come \[ [**duale**](/windows/desktop/Midl/dual) \] nella libreria dei tipi, un'interfaccia di automazione OLE può essere usata tramite **IDispatch** oppure può essere associata direttamente a.</span><span class="sxs-lookup"><span data-stu-id="ba18f-108">By labeling an interface as \[[**dual**](/windows/desktop/Midl/dual)\] in the type library, an OLE Automation interface can be used either via **IDispatch**, or it can be bound to directly.</span></span> <span data-ttu-id="ba18f-109">I contenitori possono quindi scegliere la tecnica più appropriata.</span><span class="sxs-lookup"><span data-stu-id="ba18f-109">Containers can thus choose the most appropriate technique.</span></span> <span data-ttu-id="ba18f-110">Il supporto per le interfacce duali è fortemente consigliato sia per i controlli che per i contenitori.</span><span class="sxs-lookup"><span data-stu-id="ba18f-110">Support for dual interfaces is strongly recommended for both controls and containers.</span></span>

 

 