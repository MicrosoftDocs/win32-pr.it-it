---
title: Interfaccia IVMParallelPortCollection (VPCCOMInterfaces. h)
description: Definisce la raccolta di porte parallele all'interno della macchina virtuale. Per ottenere un oggetto IVMParallelPortCollection, usare la proprietà IVMVirtualMachine ParallelPorts.
ms.assetid: 038a5c08-cd92-426f-a059-9a4c2110548d
keywords:
- Interfaccia IVMParallelPortCollection Virtual PC
- Interfaccia IVMParallelPortCollection Virtual PC, descritta
topic_type:
- apiref
api_name:
- IVMParallelPortCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8284b3720e0272147c932cfbfd70448babf5606f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121351"
---
# <a name="ivmparallelportcollection-interface"></a><span data-ttu-id="0a9ba-106">Interfaccia IVMParallelPortCollection</span><span class="sxs-lookup"><span data-stu-id="0a9ba-106">IVMParallelPortCollection interface</span></span>

<span data-ttu-id="0a9ba-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="0a9ba-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="0a9ba-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="0a9ba-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="0a9ba-109">Definisce la raccolta di porte parallele all'interno della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0a9ba-109">Defines the collection of parallel ports within the virtual machine.</span></span> <span data-ttu-id="0a9ba-110">Per ottenere un oggetto **IVMParallelPortCollection** , usare la proprietà [**IVMVirtualMachine::P arallelports**](ivmvirtualmachine-parallelports.md) .</span><span class="sxs-lookup"><span data-stu-id="0a9ba-110">To obtain an **IVMParallelPortCollection** object, use the [**IVMVirtualMachine::ParallelPorts**](ivmvirtualmachine-parallelports.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="0a9ba-111">Membri</span><span class="sxs-lookup"><span data-stu-id="0a9ba-111">Members</span></span>

<span data-ttu-id="0a9ba-112">L'interfaccia **IVMParallelPortCollection** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="0a9ba-112">The **IVMParallelPortCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="0a9ba-113">**IVMParallelPortCollection** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="0a9ba-113">**IVMParallelPortCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="0a9ba-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0a9ba-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0a9ba-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0a9ba-115">Properties</span></span>

<span data-ttu-id="0a9ba-116">L'interfaccia **IVMParallelPortCollection** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="0a9ba-116">The **IVMParallelPortCollection** interface has these properties.</span></span>



| <span data-ttu-id="0a9ba-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0a9ba-117">Property</span></span>                                                           | <span data-ttu-id="0a9ba-118">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="0a9ba-118">Access type</span></span>          | <span data-ttu-id="0a9ba-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0a9ba-119">Description</span></span>                                                                  |
|:-------------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------|
| [<span data-ttu-id="0a9ba-120">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="0a9ba-120">**\_NewEnum**</span></span>](ivmparallelportcollection--newenum.md)<br/> | <span data-ttu-id="0a9ba-121">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="0a9ba-121">Read-only</span></span><br/> | <span data-ttu-id="0a9ba-122">Enumeratore per la raccolta.</span><span class="sxs-lookup"><span data-stu-id="0a9ba-122">An enumerator for the collection.</span></span><br/>                                 |
| [<span data-ttu-id="0a9ba-123">**Conteggio**</span><span class="sxs-lookup"><span data-stu-id="0a9ba-123">**Count**</span></span>](ivmparallelportcollection-count.md)<br/>        | <span data-ttu-id="0a9ba-124">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="0a9ba-124">Read-only</span></span><br/> | <span data-ttu-id="0a9ba-125">Numero di porte parallele in questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="0a9ba-125">The number of parallel ports in this collection.</span></span><br/>                  |
| [<span data-ttu-id="0a9ba-126">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="0a9ba-126">**Item**</span></span>](ivmparallelportcollection-item.md)<br/>          | <span data-ttu-id="0a9ba-127">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="0a9ba-127">Read-only</span></span><br/> | <span data-ttu-id="0a9ba-128">Oggetto porta parallela che corrisponde all'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="0a9ba-128">The parallel port object that corresponds to the specified index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0a9ba-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0a9ba-129">Requirements</span></span>



| <span data-ttu-id="0a9ba-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a9ba-130">Requirement</span></span> | <span data-ttu-id="0a9ba-131">Valore</span><span class="sxs-lookup"><span data-stu-id="0a9ba-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a9ba-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0a9ba-132">Minimum supported client</span></span><br/> | <span data-ttu-id="0a9ba-133">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="0a9ba-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0a9ba-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0a9ba-134">Minimum supported server</span></span><br/> | <span data-ttu-id="0a9ba-135">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="0a9ba-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="0a9ba-136">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="0a9ba-136">End of client support</span></span><br/>    | <span data-ttu-id="0a9ba-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0a9ba-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="0a9ba-138">Prodotto</span><span class="sxs-lookup"><span data-stu-id="0a9ba-138">Product</span></span><br/>                  | <span data-ttu-id="0a9ba-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="0a9ba-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="0a9ba-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0a9ba-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a9ba-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a9ba-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="0a9ba-142">IID</span><span class="sxs-lookup"><span data-stu-id="0a9ba-142">IID</span></span><br/>                      | <span data-ttu-id="0a9ba-143">IID \_ IVMParallelPortCollection è definito come 27c3e036-198f-430C-8735-6e652f7203fd</span><span class="sxs-lookup"><span data-stu-id="0a9ba-143">IID\_IVMParallelPortCollection is defined as 27c3e036-198f-430c-8735-6e652f7203fd</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="0a9ba-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0a9ba-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a9ba-145">**IVMParallelPort**</span><span class="sxs-lookup"><span data-stu-id="0a9ba-145">**IVMParallelPort**</span></span>](ivmparallelport.md)
</dt> <dt>

[<span data-ttu-id="0a9ba-146">**IVMVirtualMachine::P arallelPorts**</span><span class="sxs-lookup"><span data-stu-id="0a9ba-146">**IVMVirtualMachine::ParallelPorts**</span></span>](ivmvirtualmachine-parallelports.md)
</dt> </dl>

 

