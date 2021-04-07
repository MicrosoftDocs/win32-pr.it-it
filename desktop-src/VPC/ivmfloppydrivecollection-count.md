---
title: Proprietà Count IVMFloppyDriveCollection (VPCCOMInterfaces. h)
description: Numero di unità floppy in questa raccolta.
ms.assetid: d430e5ae-9782-4f88-a5a4-744e79545c7a
keywords:
- Conteggio proprietà PC virtuale
- Proprietà Count Virtual PC, interfaccia IVMFloppyDriveCollection
- Interfaccia IVMFloppyDriveCollection Virtual PC, proprietà Count
topic_type:
- apiref
api_name:
- IVMFloppyDriveCollection.Count
- IVMFloppyDriveCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21b00c13795a633c664cea2c4476d58b346f9108
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048725"
---
# <a name="ivmfloppydrivecollectioncount-property"></a><span data-ttu-id="d88aa-106">Proprietà IVMFloppyDriveCollection:: count</span><span class="sxs-lookup"><span data-stu-id="d88aa-106">IVMFloppyDriveCollection::Count property</span></span>

<span data-ttu-id="d88aa-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d88aa-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d88aa-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d88aa-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d88aa-109">Recupera il numero di unità floppy in questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="d88aa-109">Retrieves the number of floppy drives in this collection.</span></span>

<span data-ttu-id="d88aa-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="d88aa-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d88aa-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d88aa-111">Syntax</span></span>


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="d88aa-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="d88aa-112">Property value</span></span>

<span data-ttu-id="d88aa-113">Numero di unità floppy multimediali.</span><span class="sxs-lookup"><span data-stu-id="d88aa-113">The number of floppy media drives.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d88aa-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="d88aa-114">Error codes</span></span>



| <span data-ttu-id="d88aa-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="d88aa-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="d88aa-116">Significato</span><span class="sxs-lookup"><span data-stu-id="d88aa-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="d88aa-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d88aa-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="d88aa-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="d88aa-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="d88aa-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="d88aa-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="d88aa-120">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="d88aa-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="d88aa-121"><dt>Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="d88aa-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="d88aa-122">La configurazione è sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="d88aa-122">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="d88aa-123"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="d88aa-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="d88aa-124">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="d88aa-124">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="d88aa-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d88aa-125">Requirements</span></span>



| <span data-ttu-id="d88aa-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="d88aa-126">Requirement</span></span> | <span data-ttu-id="d88aa-127">Valore</span><span class="sxs-lookup"><span data-stu-id="d88aa-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d88aa-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d88aa-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d88aa-129">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="d88aa-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d88aa-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d88aa-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d88aa-131">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="d88aa-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d88aa-132">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="d88aa-132">End of client support</span></span><br/>    | <span data-ttu-id="d88aa-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d88aa-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d88aa-134">Prodotto</span><span class="sxs-lookup"><span data-stu-id="d88aa-134">Product</span></span><br/>                  | <span data-ttu-id="d88aa-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d88aa-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d88aa-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d88aa-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="d88aa-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="d88aa-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d88aa-138">IID</span><span class="sxs-lookup"><span data-stu-id="d88aa-138">IID</span></span><br/>                      | <span data-ttu-id="d88aa-139">IID \_ IVMFloppyDriveCollection è definito come 8ba70a25-f698-4ee5-85ce-3cc93a925516</span><span class="sxs-lookup"><span data-stu-id="d88aa-139">IID\_IVMFloppyDriveCollection is defined as 8ba70a25-f698-4ee5-85ce-3cc93a925516</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="d88aa-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d88aa-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d88aa-141">**IVMFloppyDriveCollection**</span><span class="sxs-lookup"><span data-stu-id="d88aa-141">**IVMFloppyDriveCollection**</span></span>](ivmfloppydrivecollection.md)
</dt> </dl>

 

