---
title: Interfaccia IVMVirtualNetwork (VPCCOMInterfaces. h)
description: Definisce una rete virtuale.
ms.assetid: 1ddafc33-05d4-45fb-924d-9830288aa240
keywords:
- Interfaccia IVMVirtualNetwork Virtual PC
- Interfaccia IVMVirtualNetwork Virtual PC, descritta
topic_type:
- apiref
api_name:
- IVMVirtualNetwork
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06fb7c759059034874890f1dba7f7e2d1280ea8a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302550"
---
# <a name="ivmvirtualnetwork-interface"></a><span data-ttu-id="d67b2-105">Interfaccia IVMVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d67b2-105">IVMVirtualNetwork interface</span></span>

<span data-ttu-id="d67b2-106">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d67b2-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d67b2-107">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d67b2-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d67b2-108">Definisce una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="d67b2-108">Defines a virtual network.</span></span> <span data-ttu-id="d67b2-109">Gli oggetti **IVMVirtualNetwork** vengono restituiti dal metodo [**IVMVirtualPC**](ivmvirtualpc.md) [**FindVirtualNetwork**](ivmvirtualpc-findvirtualnetwork.md).</span><span class="sxs-lookup"><span data-stu-id="d67b2-109">**IVMVirtualNetwork** objects are returned from [**IVMVirtualPC**](ivmvirtualpc.md) method [**FindVirtualNetwork**](ivmvirtualpc-findvirtualnetwork.md).</span></span> <span data-ttu-id="d67b2-110">È anche possibile recuperare un oggetto **IVMVirtualNetwork** dall'oggetto [**IVMVirtualNetworkCollection**](ivmvirtualnetworkcollection.md) restituito dalla proprietà [**IVMVirtualPC:: VirtualNetworks**](ivmvirtualpc-virtualnetworks.md) .</span><span class="sxs-lookup"><span data-stu-id="d67b2-110">You can also retrieve an **IVMVirtualNetwork** object from the [**IVMVirtualNetworkCollection**](ivmvirtualnetworkcollection.md) object returned from the [**IVMVirtualPC::VirtualNetworks**](ivmvirtualpc-virtualnetworks.md) property.</span></span>

<span data-ttu-id="d67b2-111">Una rete virtuale è costituita da un commutire virtuale, che esegue tutti i routing interni e diverse connessioni "collegate" al commutere virtuale.</span><span class="sxs-lookup"><span data-stu-id="d67b2-111">A virtual network consists of a virtual switch, which performs all internal routing, and several connections that are "plugged in" to the virtual switch.</span></span> <span data-ttu-id="d67b2-112">Queste connessioni possono essere una connessione host esterna reale, una rete interna o una rete condivisa (NAT).</span><span class="sxs-lookup"><span data-stu-id="d67b2-112">These connections can be a real external host connection, an "internal network" or shared networking (NAT).</span></span>

## <a name="members"></a><span data-ttu-id="d67b2-113">Membri</span><span class="sxs-lookup"><span data-stu-id="d67b2-113">Members</span></span>

<span data-ttu-id="d67b2-114">L'interfaccia **IVMVirtualNetwork** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="d67b2-114">The **IVMVirtualNetwork** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="d67b2-115">**IVMVirtualNetwork** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="d67b2-115">**IVMVirtualNetwork** also has these types of members:</span></span>

-   [<span data-ttu-id="d67b2-116">Metodi</span><span class="sxs-lookup"><span data-stu-id="d67b2-116">Methods</span></span>](#methods)
-   [<span data-ttu-id="d67b2-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d67b2-117">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d67b2-118">Metodi</span><span class="sxs-lookup"><span data-stu-id="d67b2-118">Methods</span></span>

<span data-ttu-id="d67b2-119">L'interfaccia **IVMVirtualNetwork** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="d67b2-119">The **IVMVirtualNetwork** interface has these methods.</span></span>



| <span data-ttu-id="d67b2-120">Metodo</span><span class="sxs-lookup"><span data-stu-id="d67b2-120">Method</span></span>                                | <span data-ttu-id="d67b2-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d67b2-121">Description</span></span>                                                          |
|:--------------------------------------|:---------------------------------------------------------------------|
| [<span data-ttu-id="d67b2-122">**\_ID**</span><span class="sxs-lookup"><span data-stu-id="d67b2-122">**\_ID**</span></span>](ivmvirtualnetwork--id.md) | <span data-ttu-id="d67b2-123">Recupera l'identificatore interno della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="d67b2-123">Retrieves the internal identifier of the virtual network.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="d67b2-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d67b2-124">Properties</span></span>

<span data-ttu-id="d67b2-125">L'interfaccia **IVMVirtualNetwork** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="d67b2-125">The **IVMVirtualNetwork** interface has these properties.</span></span>



| <span data-ttu-id="d67b2-126">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d67b2-126">Property</span></span>                                                                | <span data-ttu-id="d67b2-127">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="d67b2-127">Access type</span></span>          | <span data-ttu-id="d67b2-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d67b2-128">Description</span></span>                                                                    |
|:------------------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------|
| [<span data-ttu-id="d67b2-129">**HostAdapter**</span><span class="sxs-lookup"><span data-stu-id="d67b2-129">**HostAdapter**</span></span>](ivmvirtualnetwork-hostadapter.md)<br/>         | <span data-ttu-id="d67b2-130">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="d67b2-130">Read-only</span></span><br/> | <span data-ttu-id="d67b2-131">Nome dell'adapter a cui è connessa la rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="d67b2-131">The name of the adapter to which the virtual network is connected.</span></span><br/>  |
| <span data-ttu-id="d67b2-132">[**MediaType**](/previous-versions/windows/desktop/legacy/dd796707(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d67b2-132">[**MediaType**](/previous-versions/windows/desktop/legacy/dd796707(v=vs.85))</span></span><br/>             | <span data-ttu-id="d67b2-133">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="d67b2-133">Read-only</span></span><br/> | <span data-ttu-id="d67b2-134">Determina se l'istanza della rete virtuale è wireless o meno.</span><span class="sxs-lookup"><span data-stu-id="d67b2-134">Determines whether the virtual network instance is wireless or not.</span></span><br/> |
| [<span data-ttu-id="d67b2-135">**Nome**</span><span class="sxs-lookup"><span data-stu-id="d67b2-135">**Name**</span></span>](ivmvirtualnetwork-name.md)<br/>                       | <span data-ttu-id="d67b2-136">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="d67b2-136">Read-only</span></span><br/> | <span data-ttu-id="d67b2-137">Nome univoco dell'istanza di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="d67b2-137">The unique name of the virtual network instance.</span></span><br/>                    |
| [<span data-ttu-id="d67b2-138">**I NetworkAdapter**</span><span class="sxs-lookup"><span data-stu-id="d67b2-138">**NetworkAdapters**</span></span>](ivmvirtualnetwork-networkadapters.md)<br/> | <span data-ttu-id="d67b2-139">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="d67b2-139">Read-only</span></span><br/> | <span data-ttu-id="d67b2-140">Raccolta enumerabile di schede di rete collegate alla rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="d67b2-140">An enumerable collection of NICs attached to the virtual network.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="d67b2-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d67b2-141">Requirements</span></span>



| <span data-ttu-id="d67b2-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="d67b2-142">Requirement</span></span> | <span data-ttu-id="d67b2-143">Valore</span><span class="sxs-lookup"><span data-stu-id="d67b2-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d67b2-144">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d67b2-144">Minimum supported client</span></span><br/> | <span data-ttu-id="d67b2-145">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="d67b2-145">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d67b2-146">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d67b2-146">Minimum supported server</span></span><br/> | <span data-ttu-id="d67b2-147">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="d67b2-147">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d67b2-148">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="d67b2-148">End of client support</span></span><br/>    | <span data-ttu-id="d67b2-149">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d67b2-149">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d67b2-150">Prodotto</span><span class="sxs-lookup"><span data-stu-id="d67b2-150">Product</span></span><br/>                  | <span data-ttu-id="d67b2-151">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d67b2-151">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d67b2-152">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d67b2-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="d67b2-153"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="d67b2-153"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d67b2-154">IID</span><span class="sxs-lookup"><span data-stu-id="d67b2-154">IID</span></span><br/>                      | <span data-ttu-id="d67b2-155">IID \_ IVMVirtualNetwork è definito come 431cb7a1-2469-4563-b94e-38b987adca63</span><span class="sxs-lookup"><span data-stu-id="d67b2-155">IID\_IVMVirtualNetwork is defined as 431cb7a1-2469-4563-b94e-38b987adca63</span></span><br/>          |



 

