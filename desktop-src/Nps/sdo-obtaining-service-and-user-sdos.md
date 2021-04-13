---
title: Recupero del servizio e dell'utente SDOs
description: Per ottenere SDOs per NPS (IAS) o un particolare utente, chiamare i metodi ISdoMachine GetServiceSDO o ISdoMachine GetUserSDO.
ms.assetid: 23e23fb3-0102-4c36-b30f-18604131ee32
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c7562c3b7c6aa1150ba3ce6581441064eb386f7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338246"
---
# <a name="obtaining-service-and-user-sdos"></a><span data-ttu-id="852ec-103">Recupero del servizio e dell'utente SDOs</span><span class="sxs-lookup"><span data-stu-id="852ec-103">Obtaining Service and User SDOs</span></span>

> [!Note]  
> <span data-ttu-id="852ec-104">Il servizio di autenticazione Internet (IAS) è stato rinominato server dei criteri di rete (NPS) a partire da Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="852ec-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span>

 

<span data-ttu-id="852ec-105">Per ottenere SDOs per NPS (IAS) o un utente specifico, chiamare i metodi [**ISdoMachine:: GetServiceSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo) o [**ISdoMachine:: GetUserSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo) .</span><span class="sxs-lookup"><span data-stu-id="852ec-105">To obtain SDOs for NPS (IAS) or a particular user, call the [**ISdoMachine::GetServiceSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo) or [**ISdoMachine::GetUserSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo) methods.</span></span> <span data-ttu-id="852ec-106">Questi metodi restituiscono puntatori alle interfacce [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) per questi oggetti.</span><span class="sxs-lookup"><span data-stu-id="852ec-106">These methods return pointers to [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interfaces for these objects.</span></span> <span data-ttu-id="852ec-107">Per l'utente SDO, usare il metodo [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) per ottenere un'interfaccia [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="852ec-107">For the user SDO, use the [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method to obtain an [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) interface for the object.</span></span> <span data-ttu-id="852ec-108">Per il servizio SDO, usare **IUnknown:: QueryInterface** per ottenere un'interfaccia [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) o un'interfaccia [**ISdoServiceControl**](/windows/desktop/api/sdoias/nn-sdoias-isdoservicecontrol) .</span><span class="sxs-lookup"><span data-stu-id="852ec-108">For the service SDO, use **IUnknown::QueryInterface** to obtain an [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) interface or [**ISdoServiceControl**](/windows/desktop/api/sdoias/nn-sdoias-isdoservicecontrol) interface.</span></span>

<span data-ttu-id="852ec-109">Prima di chiamare [**ISdoMachine:: GetServiceSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo) o [**ISdoMachine:: GetUserSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo), chiamare [**ISdoMachine:: Connetti**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-attach) per associare l'oggetto computer al computer locale.</span><span class="sxs-lookup"><span data-stu-id="852ec-109">Before calling either [**ISdoMachine::GetServiceSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo) or [**ISdoMachine::GetUserSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo), call [**ISdoMachine::Attach**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-attach) to associate the machine object with the local computer.</span></span>

<span data-ttu-id="852ec-110">Vedere [recupero di un servizio SDO](/windows/desktop/Nps/sdo-retrieving-a-service-sdo) e [recupero di un SDO utente per il](/windows/desktop/Nps/sdo-retrieving-a-user-sdo) codice di esempio che illustra come ottenere questi SDOs.</span><span class="sxs-lookup"><span data-stu-id="852ec-110">See [Retrieving a Service SDO](/windows/desktop/Nps/sdo-retrieving-a-service-sdo) and [Retrieving a User SDO](/windows/desktop/Nps/sdo-retrieving-a-user-sdo) for sample code that demonstrates how to obtain these SDOs.</span></span>

 

 