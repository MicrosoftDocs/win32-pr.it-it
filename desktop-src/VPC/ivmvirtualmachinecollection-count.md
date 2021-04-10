---
title: Proprietà Count IVMVirtualMachineCollection (VPCCOMInterfaces. h)
description: Recupera il numero di macchine virtuali in questa raccolta.
ms.assetid: c1f38528-fd9b-4b86-aac6-de944379b92e
keywords:
- Conteggio proprietà PC virtuale
- Proprietà Count Virtual PC, interfaccia IVMVirtualMachineCollection
- Interfaccia IVMVirtualMachineCollection Virtual PC, proprietà Count
topic_type:
- apiref
api_name:
- IVMVirtualMachineCollection.Count
- IVMVirtualMachineCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f641fad504c6dd593737cf35014813f49609a4aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121083"
---
# <a name="ivmvirtualmachinecollectioncount-property"></a><span data-ttu-id="46472-106">Proprietà IVMVirtualMachineCollection:: count</span><span class="sxs-lookup"><span data-stu-id="46472-106">IVMVirtualMachineCollection::Count property</span></span>

<span data-ttu-id="46472-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="46472-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="46472-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="46472-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="46472-109">Recupera il numero di macchine virtuali in questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="46472-109">Retrieves the number of virtual machines in this collection.</span></span>

<span data-ttu-id="46472-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="46472-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="46472-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="46472-111">Syntax</span></span>


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="46472-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="46472-112">Property value</span></span>

<span data-ttu-id="46472-113">Numero di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="46472-113">The number of virtual machines.</span></span>

## <a name="error-codes"></a><span data-ttu-id="46472-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="46472-114">Error codes</span></span>



| <span data-ttu-id="46472-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="46472-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="46472-116">Significato</span><span class="sxs-lookup"><span data-stu-id="46472-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="46472-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="46472-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="46472-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="46472-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="46472-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="46472-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="46472-120">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="46472-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="46472-121"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="46472-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="46472-122">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="46472-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="46472-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="46472-123">Requirements</span></span>



| <span data-ttu-id="46472-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="46472-124">Requirement</span></span> | <span data-ttu-id="46472-125">Valore</span><span class="sxs-lookup"><span data-stu-id="46472-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46472-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="46472-126">Minimum supported client</span></span><br/> | <span data-ttu-id="46472-127">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="46472-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="46472-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="46472-128">Minimum supported server</span></span><br/> | <span data-ttu-id="46472-129">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="46472-129">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="46472-130">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="46472-130">End of client support</span></span><br/>    | <span data-ttu-id="46472-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="46472-131">Windows 7</span></span><br/>                                                                           |
| <span data-ttu-id="46472-132">Prodotto</span><span class="sxs-lookup"><span data-stu-id="46472-132">Product</span></span><br/>                  | <span data-ttu-id="46472-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="46472-133">Windows Virtual PC</span></span><br/>                                                                  |
| <span data-ttu-id="46472-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="46472-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="46472-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="46472-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>  |
| <span data-ttu-id="46472-136">IID</span><span class="sxs-lookup"><span data-stu-id="46472-136">IID</span></span><br/>                      | <span data-ttu-id="46472-137">IID \_ IVMVirtualMachineCollection è definito come 59f31786-2a3d-4FBF-9896-d85338ca0da1</span><span class="sxs-lookup"><span data-stu-id="46472-137">IID\_IVMVirtualMachineCollection is defined as 59f31786-2a3d-4fbf-9896-d85338ca0da1</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="46472-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="46472-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46472-139">**IVMVirtualMachineCollection**</span><span class="sxs-lookup"><span data-stu-id="46472-139">**IVMVirtualMachineCollection**</span></span>](ivmvirtualmachinecollection.md)
</dt> </dl>

 

