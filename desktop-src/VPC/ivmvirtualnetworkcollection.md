---
title: Interfaccia IVMVirtualNetworkCollection (VPCCOMInterfaces. h)
description: Definisce una raccolta di oggetti IVMVirtualNetwork. Per ottenere un oggetto IVMVirtualNetworkCollection, usare la proprietà IVMVirtualPC VirtualNetworks.
ms.assetid: 3d595bc3-1a8d-4e09-a809-944d4dcdc675
keywords:
- Interfaccia IVMVirtualNetworkCollection Virtual PC
- Interfaccia IVMVirtualNetworkCollection Virtual PC, descritta
topic_type:
- apiref
api_name:
- IVMVirtualNetworkCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76935fd4a67983847e211d8aa53f4a616bed9d4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743082"
---
# <a name="ivmvirtualnetworkcollection-interface"></a><span data-ttu-id="58ff1-106">Interfaccia IVMVirtualNetworkCollection</span><span class="sxs-lookup"><span data-stu-id="58ff1-106">IVMVirtualNetworkCollection interface</span></span>

<span data-ttu-id="58ff1-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="58ff1-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="58ff1-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="58ff1-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="58ff1-109">Definisce una raccolta di oggetti [**IVMVirtualNetwork**](ivmvirtualnetwork.md) .</span><span class="sxs-lookup"><span data-stu-id="58ff1-109">Defines a collection of [**IVMVirtualNetwork**](ivmvirtualnetwork.md) objects.</span></span> <span data-ttu-id="58ff1-110">Per ottenere un oggetto **IVMVirtualNetworkCollection** , usare la proprietà [**IVMVirtualPC:: VirtualNetworks**](ivmvirtualpc-virtualnetworks.md) .</span><span class="sxs-lookup"><span data-stu-id="58ff1-110">To obtain an **IVMVirtualNetworkCollection** object, use the [**IVMVirtualPC::VirtualNetworks**](ivmvirtualpc-virtualnetworks.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="58ff1-111">Membri</span><span class="sxs-lookup"><span data-stu-id="58ff1-111">Members</span></span>

<span data-ttu-id="58ff1-112">L'interfaccia **IVMVirtualNetworkCollection** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="58ff1-112">The **IVMVirtualNetworkCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="58ff1-113">**IVMVirtualNetworkCollection** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="58ff1-113">**IVMVirtualNetworkCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="58ff1-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="58ff1-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="58ff1-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="58ff1-115">Properties</span></span>

<span data-ttu-id="58ff1-116">L'interfaccia **IVMVirtualNetworkCollection** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="58ff1-116">The **IVMVirtualNetworkCollection** interface has these properties.</span></span>



| <span data-ttu-id="58ff1-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="58ff1-117">Property</span></span>                                                             | <span data-ttu-id="58ff1-118">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="58ff1-118">Access type</span></span>          | <span data-ttu-id="58ff1-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="58ff1-119">Description</span></span>                                                                                                   |
|:---------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="58ff1-120">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="58ff1-120">**\_NewEnum**</span></span>](ivmvirtualnetworkcollection--newenum.md)<br/> | <span data-ttu-id="58ff1-121">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="58ff1-121">Read-only</span></span><br/> | <span data-ttu-id="58ff1-122">Enumeratore per la raccolta.</span><span class="sxs-lookup"><span data-stu-id="58ff1-122">An enumerator for the collection.</span></span><br/>                                                                  |
| [<span data-ttu-id="58ff1-123">**Conteggio**</span><span class="sxs-lookup"><span data-stu-id="58ff1-123">**Count**</span></span>](ivmvirtualnetworkcollection-count.md)<br/>        | <span data-ttu-id="58ff1-124">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="58ff1-124">Read-only</span></span><br/> | <span data-ttu-id="58ff1-125">Numero di reti virtuali in questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="58ff1-125">The number of virtual networks in this collection.</span></span><br/>                                                 |
| [<span data-ttu-id="58ff1-126">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="58ff1-126">**Item**</span></span>](ivmvirtualnetworkcollection-item.md)<br/>          | <span data-ttu-id="58ff1-127">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="58ff1-127">Read-only</span></span><br/> | <span data-ttu-id="58ff1-128">Oggetto [**IVMVirtualNetwork**](ivmvirtualnetwork.md) che corrisponde all'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="58ff1-128">The [**IVMVirtualNetwork**](ivmvirtualnetwork.md) object that corresponds to the specified index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="58ff1-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="58ff1-129">Requirements</span></span>



| <span data-ttu-id="58ff1-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="58ff1-130">Requirement</span></span> | <span data-ttu-id="58ff1-131">Valore</span><span class="sxs-lookup"><span data-stu-id="58ff1-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58ff1-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="58ff1-132">Minimum supported client</span></span><br/> | <span data-ttu-id="58ff1-133">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="58ff1-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="58ff1-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="58ff1-134">Minimum supported server</span></span><br/> | <span data-ttu-id="58ff1-135">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="58ff1-135">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="58ff1-136">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="58ff1-136">End of client support</span></span><br/>    | <span data-ttu-id="58ff1-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="58ff1-137">Windows 7</span></span><br/>                                                                           |
| <span data-ttu-id="58ff1-138">Prodotto</span><span class="sxs-lookup"><span data-stu-id="58ff1-138">Product</span></span><br/>                  | <span data-ttu-id="58ff1-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="58ff1-139">Windows Virtual PC</span></span><br/>                                                                  |
| <span data-ttu-id="58ff1-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="58ff1-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="58ff1-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="58ff1-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>  |
| <span data-ttu-id="58ff1-142">IID</span><span class="sxs-lookup"><span data-stu-id="58ff1-142">IID</span></span><br/>                      | <span data-ttu-id="58ff1-143">IID \_ IVMVirtualNetworkCollection è definito come 8ed680be-4242-4B2A-A21C-1982d8b0f675</span><span class="sxs-lookup"><span data-stu-id="58ff1-143">IID\_IVMVirtualNetworkCollection is defined as 8ed680be-4242-4b2a-a21c-1982d8b0f675</span></span><br/> |



 

