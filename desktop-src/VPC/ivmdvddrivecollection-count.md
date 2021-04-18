---
title: Proprietà Count IVMDVDDriveCollection (VPCCOMInterfaces. h)
description: Recupera il numero di unità CD e DVD in questa raccolta.
ms.assetid: 22e39c42-1f98-4680-a97e-0d329dc608e2
keywords:
- Conteggio proprietà PC virtuale
- Proprietà Count Virtual PC, interfaccia IVMDVDDriveCollection
- Interfaccia IVMDVDDriveCollection Virtual PC, proprietà Count
topic_type:
- apiref
api_name:
- IVMDVDDriveCollection.Count
- IVMDVDDriveCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e9ea713810348c0bd78c7de307600fc6ac9adc0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301850"
---
# <a name="ivmdvddrivecollectioncount-property"></a><span data-ttu-id="f395b-106">Proprietà IVMDVDDriveCollection:: count</span><span class="sxs-lookup"><span data-stu-id="f395b-106">IVMDVDDriveCollection::Count property</span></span>

<span data-ttu-id="f395b-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f395b-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f395b-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f395b-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f395b-109">Recupera il numero di unità CD e DVD in questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="f395b-109">Retrieves the number of CD and DVD drives in this collection.</span></span>

<span data-ttu-id="f395b-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="f395b-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f395b-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f395b-111">Syntax</span></span>


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="f395b-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="f395b-112">Property value</span></span>

<span data-ttu-id="f395b-113">Il numero di unità CD e DVD.</span><span class="sxs-lookup"><span data-stu-id="f395b-113">The number of CD and DVD drives.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f395b-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="f395b-114">Error codes</span></span>



| <span data-ttu-id="f395b-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="f395b-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="f395b-116">Significato</span><span class="sxs-lookup"><span data-stu-id="f395b-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="f395b-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f395b-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="f395b-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="f395b-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="f395b-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="f395b-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="f395b-120">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="f395b-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="f395b-121"><dt>E \_ ERRORE</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="f395b-121"><dt>E\_FAIL</dt> <dt>0x80004005</dt></span></span> </dl>            | <span data-ttu-id="f395b-122">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="f395b-122">An unexpected error has occurred.</span></span><br/> |
| <dl> <span data-ttu-id="f395b-123"><dt>Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="f395b-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="f395b-124">La configurazione è sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="f395b-124">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="f395b-125"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="f395b-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="f395b-126">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="f395b-126">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="f395b-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f395b-127">Requirements</span></span>



| <span data-ttu-id="f395b-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="f395b-128">Requirement</span></span> | <span data-ttu-id="f395b-129">Valore</span><span class="sxs-lookup"><span data-stu-id="f395b-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f395b-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f395b-130">Minimum supported client</span></span><br/> | <span data-ttu-id="f395b-131">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f395b-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f395b-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f395b-132">Minimum supported server</span></span><br/> | <span data-ttu-id="f395b-133">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="f395b-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f395b-134">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="f395b-134">End of client support</span></span><br/>    | <span data-ttu-id="f395b-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f395b-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f395b-136">Prodotto</span><span class="sxs-lookup"><span data-stu-id="f395b-136">Product</span></span><br/>                  | <span data-ttu-id="f395b-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f395b-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f395b-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f395b-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="f395b-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="f395b-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="f395b-140">IID</span><span class="sxs-lookup"><span data-stu-id="f395b-140">IID</span></span><br/>                      | <span data-ttu-id="f395b-141">IID \_ IVMDVDDriveCollection è definito come bc86e297-e55f-4742-9614-ad11d3131f68</span><span class="sxs-lookup"><span data-stu-id="f395b-141">IID\_IVMDVDDriveCollection is defined as bc86e297-e55f-4742-9614-ad11d3131f68</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="f395b-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f395b-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f395b-143">**IVMDVDDriveCollection**</span><span class="sxs-lookup"><span data-stu-id="f395b-143">**IVMDVDDriveCollection**</span></span>](ivmdvddrivecollection.md)
</dt> </dl>

 

