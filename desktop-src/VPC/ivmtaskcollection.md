---
title: Interfaccia IVMTaskCollection (VPCCOMInterfaces. h)
description: Definisce la raccolta di oggetti attività. Per ottenere un oggetto IVMTaskCollection, utilizzare la proprietà attività IVMVirtualPC.
ms.assetid: 5cfc543c-81a1-49d2-93a9-9b1db1cb5070
keywords:
- Interfaccia IVMTaskCollection Virtual PC
- Interfaccia IVMTaskCollection Virtual PC, descritta
topic_type:
- apiref
api_name:
- IVMTaskCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43ff7a4b12b936f2b5c72a73818eca0f927eef12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400816"
---
# <a name="ivmtaskcollection-interface"></a><span data-ttu-id="06c55-106">Interfaccia IVMTaskCollection</span><span class="sxs-lookup"><span data-stu-id="06c55-106">IVMTaskCollection interface</span></span>

<span data-ttu-id="06c55-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="06c55-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="06c55-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="06c55-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="06c55-109">Definisce la raccolta di oggetti attività.</span><span class="sxs-lookup"><span data-stu-id="06c55-109">Defines the collection of task objects.</span></span> <span data-ttu-id="06c55-110">Per ottenere un oggetto **IVMTaskCollection** , usare la proprietà [**IVMVirtualPC:: Tasks**](ivmvirtualpc-tasks.md) .</span><span class="sxs-lookup"><span data-stu-id="06c55-110">To obtain an **IVMTaskCollection** object, use the [**IVMVirtualPC::Tasks**](ivmvirtualpc-tasks.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="06c55-111">Membri</span><span class="sxs-lookup"><span data-stu-id="06c55-111">Members</span></span>

<span data-ttu-id="06c55-112">L'interfaccia **IVMTaskCollection** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="06c55-112">The **IVMTaskCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="06c55-113">**IVMTaskCollection** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="06c55-113">**IVMTaskCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="06c55-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="06c55-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="06c55-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="06c55-115">Properties</span></span>

<span data-ttu-id="06c55-116">L'interfaccia **IVMTaskCollection** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="06c55-116">The **IVMTaskCollection** interface has these properties.</span></span>



| <span data-ttu-id="06c55-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="06c55-117">Property</span></span>                                                   | <span data-ttu-id="06c55-118">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="06c55-118">Access type</span></span>          | <span data-ttu-id="06c55-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="06c55-119">Description</span></span>                                                         |
|:-----------------------------------------------------------|:---------------------|:--------------------------------------------------------------------|
| [<span data-ttu-id="06c55-120">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="06c55-120">**\_NewEnum**</span></span>](ivmtaskcollection--newenum.md)<br/> | <span data-ttu-id="06c55-121">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="06c55-121">Read-only</span></span><br/> | <span data-ttu-id="06c55-122">Enumeratore per la raccolta.</span><span class="sxs-lookup"><span data-stu-id="06c55-122">An enumerator for the collection.</span></span><br/>                        |
| [<span data-ttu-id="06c55-123">**Conteggio**</span><span class="sxs-lookup"><span data-stu-id="06c55-123">**Count**</span></span>](ivmtaskcollection-count.md)<br/>        | <span data-ttu-id="06c55-124">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="06c55-124">Read-only</span></span><br/> | <span data-ttu-id="06c55-125">Numero di attività in questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="06c55-125">The number of tasks in this collection.</span></span><br/>                  |
| [<span data-ttu-id="06c55-126">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="06c55-126">**Item**</span></span>](ivmtaskcollection-item.md)<br/>          | <span data-ttu-id="06c55-127">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="06c55-127">Read-only</span></span><br/> | <span data-ttu-id="06c55-128">Oggetto attività che corrisponde all'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="06c55-128">The task object that corresponds to the specified index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="06c55-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="06c55-129">Requirements</span></span>



| <span data-ttu-id="06c55-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="06c55-130">Requirement</span></span> | <span data-ttu-id="06c55-131">Valore</span><span class="sxs-lookup"><span data-stu-id="06c55-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="06c55-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="06c55-132">Minimum supported client</span></span><br/> | <span data-ttu-id="06c55-133">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="06c55-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="06c55-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="06c55-134">Minimum supported server</span></span><br/> | <span data-ttu-id="06c55-135">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="06c55-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="06c55-136">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="06c55-136">End of client support</span></span><br/>    | <span data-ttu-id="06c55-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="06c55-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="06c55-138">Prodotto</span><span class="sxs-lookup"><span data-stu-id="06c55-138">Product</span></span><br/>                  | <span data-ttu-id="06c55-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="06c55-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="06c55-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="06c55-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="06c55-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="06c55-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="06c55-142">IID</span><span class="sxs-lookup"><span data-stu-id="06c55-142">IID</span></span><br/>                      | <span data-ttu-id="06c55-143">IID \_ IVMTaskCollection è definito come 5c4387c8-0e8b-4b97-8058-84679adf4c40</span><span class="sxs-lookup"><span data-stu-id="06c55-143">IID\_IVMTaskCollection is defined as 5c4387c8-0e8b-4b97-8058-84679adf4c40</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="06c55-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="06c55-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06c55-145">**IVMTask**</span><span class="sxs-lookup"><span data-stu-id="06c55-145">**IVMTask**</span></span>](ivmtask.md)
</dt> <dt>

[<span data-ttu-id="06c55-146">**IVMVirtualPC:: Tasks**</span><span class="sxs-lookup"><span data-stu-id="06c55-146">**IVMVirtualPC::Tasks**</span></span>](ivmvirtualpc-tasks.md)
</dt> </dl>

 

