---
title: Interfaccia IVMParallelPort (VPCCOMInterfaces. h)
description: Definisce una porta parallela all'interno di una macchina virtuale.
ms.assetid: da8daf16-5d22-49be-8fe9-72d5018c0622
keywords:
- Interfaccia IVMParallelPort Virtual PC
- Interfaccia IVMParallelPort Virtual PC, descritta
topic_type:
- apiref
api_name:
- IVMParallelPort
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71b76b23f48e728104a3826afa80a8f272cd7e66
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302557"
---
# <a name="ivmparallelport-interface"></a><span data-ttu-id="bebee-105">Interfaccia IVMParallelPort</span><span class="sxs-lookup"><span data-stu-id="bebee-105">IVMParallelPort interface</span></span>

<span data-ttu-id="bebee-106">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="bebee-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="bebee-107">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="bebee-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="bebee-108">Definisce una porta parallela all'interno di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="bebee-108">Defines a parallel port inside a virtual machine.</span></span> <span data-ttu-id="bebee-109">Questa interfaccia consente di configurare le porte parallele all'interno di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="bebee-109">This interface allows you to configure parallel ports inside a virtual machine.</span></span> <span data-ttu-id="bebee-110">È possibile recuperare un oggetto **IVMParallelPort** dall'oggetto [**IVMParallelPortCollection**](ivmparallelportcollection.md) restituito dalla proprietà [**IVMVirtualMachine::P arallelports**](ivmvirtualmachine-parallelports.md) .</span><span class="sxs-lookup"><span data-stu-id="bebee-110">You can retrieve an **IVMParallelPort** object from the [**IVMParallelPortCollection**](ivmparallelportcollection.md) object returned from the [**IVMVirtualMachine::ParallelPorts**](ivmvirtualmachine-parallelports.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="bebee-111">Membri</span><span class="sxs-lookup"><span data-stu-id="bebee-111">Members</span></span>

<span data-ttu-id="bebee-112">L'interfaccia **IVMParallelPort** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="bebee-112">The **IVMParallelPort** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="bebee-113">**IVMParallelPort** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="bebee-113">**IVMParallelPort** also has these types of members:</span></span>

-   [<span data-ttu-id="bebee-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="bebee-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="bebee-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bebee-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="bebee-116">Metodi</span><span class="sxs-lookup"><span data-stu-id="bebee-116">Methods</span></span>

<span data-ttu-id="bebee-117">L'interfaccia **IVMParallelPort** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="bebee-117">The **IVMParallelPort** interface has these methods.</span></span>



| <span data-ttu-id="bebee-118">Metodo</span><span class="sxs-lookup"><span data-stu-id="bebee-118">Method</span></span>                              | <span data-ttu-id="bebee-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bebee-119">Description</span></span>                                                        |
|:------------------------------------|:-------------------------------------------------------------------|
| [<span data-ttu-id="bebee-120">**\_ID**</span><span class="sxs-lookup"><span data-stu-id="bebee-120">**\_ID**</span></span>](ivmparallelport--id.md) | <span data-ttu-id="bebee-121">Recupera l'identificatore interno della porta parallela.</span><span class="sxs-lookup"><span data-stu-id="bebee-121">Retrieves the internal identifier of the parallel port.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="bebee-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bebee-122">Properties</span></span>

<span data-ttu-id="bebee-123">L'interfaccia **IVMParallelPort** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="bebee-123">The **IVMParallelPort** interface has these properties.</span></span>



| <span data-ttu-id="bebee-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bebee-124">Property</span></span>                                        | <span data-ttu-id="bebee-125">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="bebee-125">Access type</span></span>           | <span data-ttu-id="bebee-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bebee-126">Description</span></span>                               |
|:------------------------------------------------|:----------------------|:------------------------------------------|
| [<span data-ttu-id="bebee-127">**Nome**</span><span class="sxs-lookup"><span data-stu-id="bebee-127">**Name**</span></span>](ivmparallelport-name.md)<br/> | <span data-ttu-id="bebee-128">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="bebee-128">Read/write</span></span><br/> | <span data-ttu-id="bebee-129">Nome della porta parallela.</span><span class="sxs-lookup"><span data-stu-id="bebee-129">The name of the parallel port.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="bebee-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bebee-130">Requirements</span></span>



| <span data-ttu-id="bebee-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="bebee-131">Requirement</span></span> | <span data-ttu-id="bebee-132">Valore</span><span class="sxs-lookup"><span data-stu-id="bebee-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="bebee-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bebee-133">Minimum supported client</span></span><br/> | <span data-ttu-id="bebee-134">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="bebee-134">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bebee-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bebee-135">Minimum supported server</span></span><br/> | <span data-ttu-id="bebee-136">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="bebee-136">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="bebee-137">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="bebee-137">End of client support</span></span><br/>    | <span data-ttu-id="bebee-138">Windows 7</span><span class="sxs-lookup"><span data-stu-id="bebee-138">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="bebee-139">Prodotto</span><span class="sxs-lookup"><span data-stu-id="bebee-139">Product</span></span><br/>                  | <span data-ttu-id="bebee-140">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="bebee-140">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="bebee-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bebee-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="bebee-142"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="bebee-142"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="bebee-143">IID</span><span class="sxs-lookup"><span data-stu-id="bebee-143">IID</span></span><br/>                      | <span data-ttu-id="bebee-144">IID \_ IVMParallelPort è definito come 097beecb-0A02-474F-abd6-298b22293fc6</span><span class="sxs-lookup"><span data-stu-id="bebee-144">IID\_IVMParallelPort is defined as 097beecb-0a02-474f-abd6-298b22293fc6</span></span><br/>            |



 

