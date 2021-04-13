---
title: Proprietà Item di IVMTaskCollection (VPCCOMInterfaces. h)
description: Recupera l'oggetto attività che corrisponde all'indice specificato.
ms.assetid: e4738b7a-12d6-4aed-992d-2f70c5cdd4d0
keywords:
- Proprietà elemento Virtual PC
- Proprietà elemento Virtual PC, interfaccia IVMTaskCollection
- Interfaccia IVMTaskCollection Virtual PC, proprietà Item
topic_type:
- apiref
api_name:
- IVMTaskCollection.Item
- IVMTaskCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f445280834383ee594fbb53a3390c91b1928f4ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518387"
---
# <a name="ivmtaskcollectionitem-property"></a><span data-ttu-id="92873-106">Proprietà IVMTaskCollection:: Item</span><span class="sxs-lookup"><span data-stu-id="92873-106">IVMTaskCollection::Item property</span></span>

<span data-ttu-id="92873-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="92873-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="92873-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="92873-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="92873-109">Recupera l'oggetto attività che corrisponde all'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="92873-109">Retrieves the task object that corresponds to the specified index.</span></span>

<span data-ttu-id="92873-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="92873-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="92873-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="92873-111">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]          long    index,
  [out, retval] IVMTask **task
);
```



## <a name="property-value"></a><span data-ttu-id="92873-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="92873-112">Property value</span></span>

<span data-ttu-id="92873-113">Oggetto [**IVMTask**](ivmtask.md) .</span><span class="sxs-lookup"><span data-stu-id="92873-113">The [**IVMTask**](ivmtask.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="92873-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="92873-114">Error codes</span></span>



| <span data-ttu-id="92873-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="92873-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="92873-116">Significato</span><span class="sxs-lookup"><span data-stu-id="92873-116">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="92873-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="92873-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="92873-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="92873-118">The operation was successful.</span></span> <br/>                                                      |
| <dl> <span data-ttu-id="92873-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="92873-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="92873-120">Il parametro dell' *attività* è **null**.</span><span class="sxs-lookup"><span data-stu-id="92873-120">The *task* parameter is **NULL**.</span></span> <br/>                                                  |
| <dl> <span data-ttu-id="92873-121"><dt>Disp \_ E \_ BADINDEX</dt> <dt>0x8002000B</dt></span><span class="sxs-lookup"><span data-stu-id="92873-121"><dt>DISP\_E\_BADINDEX</dt> <dt>0x8002000B</dt></span></span> </dl>  | <span data-ttu-id="92873-122">L'indice dell'elemento richiesto non corrisponde a un elemento in questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="92873-122">The index of the requested item does not correspond to an item in this collection.</span></span> <br/> |
| <dl> <span data-ttu-id="92873-123"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="92873-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="92873-124">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="92873-124">An unexpected error has occurred.</span></span><br/>                                                   |



## <a name="requirements"></a><span data-ttu-id="92873-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="92873-125">Requirements</span></span>



| <span data-ttu-id="92873-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="92873-126">Requirement</span></span> | <span data-ttu-id="92873-127">Valore</span><span class="sxs-lookup"><span data-stu-id="92873-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="92873-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="92873-128">Minimum supported client</span></span><br/> | <span data-ttu-id="92873-129">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="92873-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="92873-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="92873-130">Minimum supported server</span></span><br/> | <span data-ttu-id="92873-131">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="92873-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="92873-132">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="92873-132">End of client support</span></span><br/>    | <span data-ttu-id="92873-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="92873-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="92873-134">Prodotto</span><span class="sxs-lookup"><span data-stu-id="92873-134">Product</span></span><br/>                  | <span data-ttu-id="92873-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="92873-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="92873-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="92873-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="92873-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="92873-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="92873-138">IID</span><span class="sxs-lookup"><span data-stu-id="92873-138">IID</span></span><br/>                      | <span data-ttu-id="92873-139">IID \_ IVMTaskCollection è definito come 5c4387c8-0e8b-4b97-8058-84679adf4c40</span><span class="sxs-lookup"><span data-stu-id="92873-139">IID\_IVMTaskCollection is defined as 5c4387c8-0e8b-4b97-8058-84679adf4c40</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="92873-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="92873-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92873-141">**IVMTask**</span><span class="sxs-lookup"><span data-stu-id="92873-141">**IVMTask**</span></span>](ivmtask.md)
</dt> <dt>

[<span data-ttu-id="92873-142">**IVMTaskCollection**</span><span class="sxs-lookup"><span data-stu-id="92873-142">**IVMTaskCollection**</span></span>](ivmtaskcollection.md)
</dt> </dl>

 

