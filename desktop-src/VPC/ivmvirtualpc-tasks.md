---
title: Proprietà attività IVMVirtualPC (VPCCOMInterfaces. h)
description: Recupera una raccolta di attività.
ms.assetid: bba9c4b4-c933-43c8-9fbc-f2beb59867cf
keywords:
- Proprietà attività PC virtuale
- Proprietà delle attività Virtual PC, interfaccia IVMVirtualPC
- Interfaccia IVMVirtualPC Virtual PC, proprietà Tasks
topic_type:
- apiref
api_name:
- IVMVirtualPC.Tasks
- IVMVirtualPC.get_Tasks
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83eb27a48654a52a5724768da4ecf38584ea1231
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874249"
---
# <a name="ivmvirtualpctasks-property"></a><span data-ttu-id="ab499-106">Proprietà IVMVirtualPC:: Tasks</span><span class="sxs-lookup"><span data-stu-id="ab499-106">IVMVirtualPC::Tasks property</span></span>

<span data-ttu-id="ab499-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="ab499-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="ab499-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="ab499-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="ab499-109">Recupera una raccolta di attività.</span><span class="sxs-lookup"><span data-stu-id="ab499-109">Retrieves a collection of tasks.</span></span>

<span data-ttu-id="ab499-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="ab499-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab499-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ab499-111">Syntax</span></span>


```C++
HRESULT get_Tasks(
  [out, retval] IVMTaskCollection **taskCollection
);
```



## <a name="property-value"></a><span data-ttu-id="ab499-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="ab499-112">Property value</span></span>

<span data-ttu-id="ab499-113">Raccolta di oggetti [**IVMTask**](ivmtask.md) .</span><span class="sxs-lookup"><span data-stu-id="ab499-113">A collection of [**IVMTask**](ivmtask.md) objects.</span></span> <span data-ttu-id="ab499-114">Vedere [**IVMTaskCollection**](ivmtaskcollection.md).</span><span class="sxs-lookup"><span data-stu-id="ab499-114">See [**IVMTaskCollection**](ivmtaskcollection.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="ab499-115">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="ab499-115">Error codes</span></span>



| <span data-ttu-id="ab499-116">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="ab499-116">Name/value</span></span>                                                                                                                                                                           | <span data-ttu-id="ab499-117">Significato</span><span class="sxs-lookup"><span data-stu-id="ab499-117">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ab499-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ab499-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="ab499-119">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="ab499-119">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="ab499-120"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="ab499-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="ab499-121">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="ab499-121">The parameter is **NULL**.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="ab499-122"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="ab499-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="ab499-123">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="ab499-123">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="ab499-124"><dt>Macchina virtuale \_ E \_ \_ virtualizzazione hardware \_ disabilitato</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="ab499-124"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="ab499-125">Il processore non supporta le estensioni di virtualizzazione accelerata hardware (HAV).</span><span class="sxs-lookup"><span data-stu-id="ab499-125">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="ab499-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ab499-126">Requirements</span></span>



| <span data-ttu-id="ab499-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab499-127">Requirement</span></span> | <span data-ttu-id="ab499-128">Valore</span><span class="sxs-lookup"><span data-stu-id="ab499-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab499-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ab499-129">Minimum supported client</span></span><br/> | <span data-ttu-id="ab499-130">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="ab499-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ab499-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ab499-131">Minimum supported server</span></span><br/> | <span data-ttu-id="ab499-132">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="ab499-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="ab499-133">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="ab499-133">End of client support</span></span><br/>    | <span data-ttu-id="ab499-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ab499-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="ab499-135">Prodotto</span><span class="sxs-lookup"><span data-stu-id="ab499-135">Product</span></span><br/>                  | <span data-ttu-id="ab499-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="ab499-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="ab499-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ab499-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab499-138"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab499-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="ab499-139">IID</span><span class="sxs-lookup"><span data-stu-id="ab499-139">IID</span></span><br/>                      | <span data-ttu-id="ab499-140">IID \_ IVMVirtualPC è definito come 236ba0d9-A24A-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="ab499-140">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="ab499-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ab499-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab499-142">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="ab499-142">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

