---
description: Implementazione di un dispenser di risorse COM+
ms.assetid: 083c5962-f55a-435a-964e-fdc868f9bd3d
title: Implementazione di un dispenser di risorse COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a81e189f3bfc5025bc949ef6e5bc82bf9408c339
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127550"
---
# <a name="implementing-a-com-resource-dispenser"></a><span data-ttu-id="1c1d4-103">Implementazione di un dispenser di risorse COM+</span><span class="sxs-lookup"><span data-stu-id="1c1d4-103">Implementing a COM+ Resource Dispenser</span></span>

<span data-ttu-id="1c1d4-104">Nei passaggi seguenti viene illustrata una procedura generale per l'implementazione di un dispenser di risorse COM+:</span><span class="sxs-lookup"><span data-stu-id="1c1d4-104">The following steps outline a general procedure for implementing a COM+ resource dispenser:</span></span>

1.  <span data-ttu-id="1c1d4-105">Decidere il formato **RESTYPID** che categorizza le differenze tra le risorse.</span><span class="sxs-lookup"><span data-stu-id="1c1d4-105">Decide on **RESTYPID** format that categorizes how your resources differ from each other.</span></span>

2.  <span data-ttu-id="1c1d4-106">Utilizzare rispettivamente il file di intestazione e la libreria Mtxdm. h e Mtxdm. lib.</span><span class="sxs-lookup"><span data-stu-id="1c1d4-106">Use the Mtxdm.h and Mtxdm.lib header file and library, respectively.</span></span>

3.  <span data-ttu-id="1c1d4-107">Compilare una DLL che implementi l'interfaccia [**IDispenserDriver**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispenserdriver) e l'API che si vuole esporre alle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="1c1d4-107">Build a DLL that implements the [**IDispenserDriver**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispenserdriver) interface and the API you want to expose to applications.</span></span>

4.  <span data-ttu-id="1c1d4-108">Nell'avvio ([*DllMain*](/windows/desktop/Dlls/dllmain) o prima chiamata all'API del dispenser), chiamare la funzione [**GetDispenserManager**](/windows/desktop/api/MtxDM/nf-mtxdm-getdispensermanager) .</span><span class="sxs-lookup"><span data-stu-id="1c1d4-108">In the startup ([*DllMain*](/windows/desktop/Dlls/dllmain) or first call to the dispenser API), call the [**GetDispenserManager**](/windows/desktop/api/MtxDM/nf-mtxdm-getdispensermanager) function.</span></span> <span data-ttu-id="1c1d4-109">Viene restituito un puntatore all'interfaccia [**IDispenserManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispensermanager) del gestore del dispenser.</span><span class="sxs-lookup"><span data-stu-id="1c1d4-109">This returns a pointer to the dispenser manager's [**IDispenserManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispensermanager) interface.</span></span>

5.  <span data-ttu-id="1c1d4-110">Chiamare [**IDispenserManager:: RegisterDispenser**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispensermanager-registerdispenser), passando un puntatore all'implementazione di [**IDispenserDriver**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispenserdriver).</span><span class="sxs-lookup"><span data-stu-id="1c1d4-110">Call [**IDispenserManager::RegisterDispenser**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispensermanager-registerdispenser), passing a pointer to your implementation of [**IDispenserDriver**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispenserdriver).</span></span> <span data-ttu-id="1c1d4-111">In questo modo, il responsabile del dispenser crea un contenitore (gestione pool) per il dispenser di risorse e quindi restituisce il puntatore all'interfaccia [**IHolder**](/windows/desktop/api/ComSvcs/nn-comsvcs-iholder) .</span><span class="sxs-lookup"><span data-stu-id="1c1d4-111">This causes the dispenser manager to create a holder (pooling manager) for your resource dispenser and then return the pointer to your [**IHolder**](/windows/desktop/api/ComSvcs/nn-comsvcs-iholder) interface.</span></span>

6.  <span data-ttu-id="1c1d4-112">Archiviare questo puntatore in modo che sia possibile chiamare [**IHolder:: AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) e [**IHolder:: FreeResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-freeresource).</span><span class="sxs-lookup"><span data-stu-id="1c1d4-112">Store this pointer so that you can call [**IHolder::AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) and [**IHolder::FreeResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-freeresource).</span></span>

7.  <span data-ttu-id="1c1d4-113">È ora possibile (in risposta alle chiamate all'API) effettuare chiamate a [**AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) e [**FreeResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-freeresource).</span><span class="sxs-lookup"><span data-stu-id="1c1d4-113">You can now (in response to calls to your API) make calls to [**AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) and [**FreeResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-freeresource).</span></span> <span data-ttu-id="1c1d4-114">**AllocResource** risponde inizialmente chiamando al metodo [**CreateResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-createresource) , ma le chiamate **AllocResource** successive vengono gestite dal pool di risorse in continua crescita.</span><span class="sxs-lookup"><span data-stu-id="1c1d4-114">**AllocResource** initially responds by calling back to your [**CreateResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-createresource) method, but later **AllocResource** calls are serviced from the growing pool of resources.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1c1d4-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1c1d4-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c1d4-116">Concetti relativi al dispenser di risorse COM+</span><span class="sxs-lookup"><span data-stu-id="1c1d4-116">COM+ Resource Dispenser Concepts</span></span>](com--resource-dispenser-concepts.md)
</dt> <dt>

[<span data-ttu-id="1c1d4-117">Interfacce del dispenser di risorse COM+</span><span class="sxs-lookup"><span data-stu-id="1c1d4-117">COM+ Resource Dispenser Interfaces</span></span>](com--resource-dispenser-interfaces.md)
</dt> </dl>

 

 
