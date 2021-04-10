---
title: Proprietà Count IVMParallelPortCollection (VPCCOMInterfaces. h)
description: Numero di porte parallele in questa raccolta.
ms.assetid: f2f4cac4-bb63-4ac2-ba6e-321a8a29c6d4
keywords:
- Conteggio proprietà PC virtuale
- Proprietà Count Virtual PC, interfaccia IVMParallelPortCollection
- Interfaccia IVMParallelPortCollection Virtual PC, proprietà Count
topic_type:
- apiref
api_name:
- IVMParallelPortCollection.Count
- IVMParallelPortCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0bb1af40f0e4d15b7eae65e18a8d9910deb769c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964312"
---
# <a name="ivmparallelportcollectioncount-property"></a><span data-ttu-id="a3bad-106">Proprietà IVMParallelPortCollection:: count</span><span class="sxs-lookup"><span data-stu-id="a3bad-106">IVMParallelPortCollection::Count property</span></span>

<span data-ttu-id="a3bad-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a3bad-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a3bad-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a3bad-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a3bad-109">Recupera il numero di porte parallele in questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="a3bad-109">Retrieves the number of parallel ports in this collection.</span></span>

<span data-ttu-id="a3bad-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="a3bad-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3bad-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a3bad-111">Syntax</span></span>


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="a3bad-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="a3bad-112">Property value</span></span>

<span data-ttu-id="a3bad-113">Numero di porte parallele.</span><span class="sxs-lookup"><span data-stu-id="a3bad-113">The number of parallel ports.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a3bad-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="a3bad-114">Error codes</span></span>



| <span data-ttu-id="a3bad-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="a3bad-115">Name/value</span></span>                                                                                                                                            | <span data-ttu-id="a3bad-116">Significato</span><span class="sxs-lookup"><span data-stu-id="a3bad-116">Meaning</span></span>                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <span data-ttu-id="a3bad-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a3bad-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>               | <span data-ttu-id="a3bad-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="a3bad-118">The operation was successful.</span></span><br/> |
| <dl> <span data-ttu-id="a3bad-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="a3bad-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl> | <span data-ttu-id="a3bad-120">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="a3bad-120">The parameter is **NULL**.</span></span><br/>    |



## <a name="requirements"></a><span data-ttu-id="a3bad-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a3bad-121">Requirements</span></span>



| <span data-ttu-id="a3bad-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3bad-122">Requirement</span></span> | <span data-ttu-id="a3bad-123">Valore</span><span class="sxs-lookup"><span data-stu-id="a3bad-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3bad-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a3bad-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a3bad-125">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="a3bad-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a3bad-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a3bad-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a3bad-127">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a3bad-127">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="a3bad-128">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="a3bad-128">End of client support</span></span><br/>    | <span data-ttu-id="a3bad-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a3bad-129">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a3bad-130">Prodotto</span><span class="sxs-lookup"><span data-stu-id="a3bad-130">Product</span></span><br/>                  | <span data-ttu-id="a3bad-131">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a3bad-131">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="a3bad-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a3bad-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3bad-133"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3bad-133"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="a3bad-134">IID</span><span class="sxs-lookup"><span data-stu-id="a3bad-134">IID</span></span><br/>                      | <span data-ttu-id="a3bad-135">IID \_ IVMParallelPortCollection è definito come 27c3e036-198f-430C-8735-6e652f7203fd</span><span class="sxs-lookup"><span data-stu-id="a3bad-135">IID\_IVMParallelPortCollection is defined as 27c3e036-198f-430c-8735-6e652f7203fd</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="a3bad-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a3bad-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3bad-137">**IVMParallelPortCollection**</span><span class="sxs-lookup"><span data-stu-id="a3bad-137">**IVMParallelPortCollection**</span></span>](ivmparallelportcollection.md)
</dt> </dl>

 

