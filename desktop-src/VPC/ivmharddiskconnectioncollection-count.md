---
title: Proprietà Count IVMHardDiskConnectionCollection (VPCCOMInterfaces. h)
description: Recupera il numero di connessioni del disco rigido in questa raccolta.
ms.assetid: 913c1bb7-0237-4f11-9873-7b42a94004f8
keywords:
- Conteggio proprietà PC virtuale
- Proprietà Count Virtual PC, interfaccia IVMHardDiskConnectionCollection
- Interfaccia IVMHardDiskConnectionCollection Virtual PC, proprietà Count
topic_type:
- apiref
api_name:
- IVMHardDiskConnectionCollection.Count
- IVMHardDiskConnectionCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f34bbf4d07d7c5967ccfc38e16a743105de8e69
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741754"
---
# <a name="ivmharddiskconnectioncollectioncount-property"></a><span data-ttu-id="0653f-106">Proprietà IVMHardDiskConnectionCollection:: count</span><span class="sxs-lookup"><span data-stu-id="0653f-106">IVMHardDiskConnectionCollection::Count property</span></span>

<span data-ttu-id="0653f-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="0653f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="0653f-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="0653f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="0653f-109">Recupera il numero di connessioni del disco rigido in questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="0653f-109">Retrieves the number of hard disk connections in this collection.</span></span>

<span data-ttu-id="0653f-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="0653f-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0653f-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0653f-111">Syntax</span></span>


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="0653f-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="0653f-112">Property value</span></span>

<span data-ttu-id="0653f-113">Numero di connessioni al disco rigido.</span><span class="sxs-lookup"><span data-stu-id="0653f-113">The number of hard disk connections.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0653f-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="0653f-114">Error codes</span></span>



| <span data-ttu-id="0653f-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="0653f-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="0653f-116">Significato</span><span class="sxs-lookup"><span data-stu-id="0653f-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="0653f-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="0653f-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="0653f-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="0653f-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="0653f-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="0653f-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="0653f-120">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="0653f-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="0653f-121"><dt>Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="0653f-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="0653f-122">La configurazione è sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="0653f-122">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="0653f-123"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="0653f-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="0653f-124">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="0653f-124">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="0653f-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0653f-125">Requirements</span></span>



| <span data-ttu-id="0653f-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="0653f-126">Requirement</span></span> | <span data-ttu-id="0653f-127">Valore</span><span class="sxs-lookup"><span data-stu-id="0653f-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0653f-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0653f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="0653f-129">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="0653f-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                         |
| <span data-ttu-id="0653f-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0653f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="0653f-131">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="0653f-131">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="0653f-132">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="0653f-132">End of client support</span></span><br/>    | <span data-ttu-id="0653f-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0653f-133">Windows 7</span></span><br/>                                                                               |
| <span data-ttu-id="0653f-134">Prodotto</span><span class="sxs-lookup"><span data-stu-id="0653f-134">Product</span></span><br/>                  | <span data-ttu-id="0653f-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="0653f-135">Windows Virtual PC</span></span><br/>                                                                      |
| <span data-ttu-id="0653f-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0653f-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="0653f-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="0653f-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>      |
| <span data-ttu-id="0653f-138">IID</span><span class="sxs-lookup"><span data-stu-id="0653f-138">IID</span></span><br/>                      | <span data-ttu-id="0653f-139">IID \_ IVMHardDiskconnectionCollection è definito come b9f2caf4-0aeb-4085-B105-ceddb90dbf62</span><span class="sxs-lookup"><span data-stu-id="0653f-139">IID\_IVMHardDiskconnectionCollection is defined as b9f2caf4-0aeb-4085-b105-ceddb90dbf62</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0653f-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0653f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0653f-141">**IVMHardDiskConnectionCollection**</span><span class="sxs-lookup"><span data-stu-id="0653f-141">**IVMHardDiskConnectionCollection**</span></span>](ivmharddiskconnectioncollection.md)
</dt> </dl>

 

