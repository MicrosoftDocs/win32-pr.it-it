---
title: Proprietà Count IVMTaskCollection (VPCCOMInterfaces. h)
description: Recupera il numero di attività in questa raccolta.
ms.assetid: 5ff33bea-3f27-47ad-bcbc-6c40f2a8d78d
keywords:
- Conteggio proprietà PC virtuale
- Proprietà Count Virtual PC, interfaccia IVMTaskCollection
- Interfaccia IVMTaskCollection Virtual PC, proprietà Count
topic_type:
- apiref
api_name:
- IVMTaskCollection.Count
- IVMTaskCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5e868296437a8939b29947e785aabaff08fdcb3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874177"
---
# <a name="ivmtaskcollectioncount-property"></a><span data-ttu-id="df728-106">Proprietà IVMTaskCollection:: count</span><span class="sxs-lookup"><span data-stu-id="df728-106">IVMTaskCollection::Count property</span></span>

<span data-ttu-id="df728-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="df728-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="df728-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="df728-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="df728-109">Recupera il numero di attività in questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="df728-109">Retrieves the number of tasks in this collection.</span></span>

<span data-ttu-id="df728-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="df728-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="df728-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="df728-111">Syntax</span></span>


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="df728-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="df728-112">Property value</span></span>

<span data-ttu-id="df728-113">Numero di attività.</span><span class="sxs-lookup"><span data-stu-id="df728-113">The number of tasks.</span></span>

## <a name="error-codes"></a><span data-ttu-id="df728-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="df728-114">Error codes</span></span>



| <span data-ttu-id="df728-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="df728-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="df728-116">Significato</span><span class="sxs-lookup"><span data-stu-id="df728-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="df728-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="df728-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="df728-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="df728-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="df728-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="df728-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="df728-120">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="df728-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="df728-121"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="df728-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="df728-122">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="df728-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="df728-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="df728-123">Requirements</span></span>



| <span data-ttu-id="df728-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="df728-124">Requirement</span></span> | <span data-ttu-id="df728-125">Valore</span><span class="sxs-lookup"><span data-stu-id="df728-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="df728-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="df728-126">Minimum supported client</span></span><br/> | <span data-ttu-id="df728-127">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="df728-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="df728-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="df728-128">Minimum supported server</span></span><br/> | <span data-ttu-id="df728-129">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="df728-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="df728-130">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="df728-130">End of client support</span></span><br/>    | <span data-ttu-id="df728-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="df728-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="df728-132">Prodotto</span><span class="sxs-lookup"><span data-stu-id="df728-132">Product</span></span><br/>                  | <span data-ttu-id="df728-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="df728-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="df728-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="df728-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="df728-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="df728-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="df728-136">IID</span><span class="sxs-lookup"><span data-stu-id="df728-136">IID</span></span><br/>                      | <span data-ttu-id="df728-137">IID \_ IVMTaskCollection è definito come 5c4387c8-0e8b-4b97-8058-84679adf4c40</span><span class="sxs-lookup"><span data-stu-id="df728-137">IID\_IVMTaskCollection is defined as 5c4387c8-0e8b-4b97-8058-84679adf4c40</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="df728-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="df728-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df728-139">**IVMTaskCollection**</span><span class="sxs-lookup"><span data-stu-id="df728-139">**IVMTaskCollection**</span></span>](ivmtaskcollection.md)
</dt> </dl>

 

