---
title: Proprietà IVMDVDDrive HostDriveLetter (VPCCOMInterfaces. h)
description: Lettera dell'unità host impostata per questo dispositivo.
ms.assetid: e17f707f-e1cf-4302-a69e-caa5829df1af
keywords:
- Proprietà HostDriveLetter Virtual PC
- Proprietà HostDriveLetter Virtual PC, interfaccia IVMDVDDrive
- Interfaccia IVMDVDDrive Virtual PC, proprietà HostDriveLetter
topic_type:
- apiref
api_name:
- IVMDVDDrive.HostDriveLetter
- IVMDVDDrive.get_HostDriveLetter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d60d2599b8fb73e727100111dc37d29a9d13c5d3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741095"
---
# <a name="ivmdvddrivehostdriveletter-property"></a><span data-ttu-id="700bb-106">Proprietà IVMDVDDrive:: HostDriveLetter</span><span class="sxs-lookup"><span data-stu-id="700bb-106">IVMDVDDrive::HostDriveLetter property</span></span>

<span data-ttu-id="700bb-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="700bb-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="700bb-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="700bb-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="700bb-109">Recupera la lettera del set di unità host per questo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="700bb-109">Retrieves the letter of the host drive set for this device.</span></span>

<span data-ttu-id="700bb-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="700bb-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="700bb-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="700bb-111">Syntax</span></span>


```C++
HRESULT get_HostDriveLetter(
  [out, retval] BSTR *driveLetter
);
```



## <a name="property-value"></a><span data-ttu-id="700bb-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="700bb-112">Property value</span></span>

<span data-ttu-id="700bb-113">Lettera di unità.</span><span class="sxs-lookup"><span data-stu-id="700bb-113">The drive letter.</span></span>

## <a name="error-codes"></a><span data-ttu-id="700bb-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="700bb-114">Error codes</span></span>



| <span data-ttu-id="700bb-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="700bb-115">Name/value</span></span>                                                                                                                                                            | <span data-ttu-id="700bb-116">Significato</span><span class="sxs-lookup"><span data-stu-id="700bb-116">Meaning</span></span>                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="700bb-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="700bb-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                               | <span data-ttu-id="700bb-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="700bb-118">The operation was successful.</span></span><br/>                             |
| <dl> <span data-ttu-id="700bb-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="700bb-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                 | <span data-ttu-id="700bb-120">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="700bb-120">The parameter is **NULL**.</span></span><br/>                                |
| <dl> <span data-ttu-id="700bb-121"><dt>E \_ ERRORE</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="700bb-121"><dt>E\_FAIL</dt> <dt>0x80004005</dt></span></span> </dl>                    | <span data-ttu-id="700bb-122">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="700bb-122">An unexpected error has occurred.</span></span><br/>                         |
| <dl> <span data-ttu-id="700bb-123"><dt>Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="700bb-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>         | <span data-ttu-id="700bb-124">Impossibile trovare la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="700bb-124">The virtual machine could not be found.</span></span><br/>                   |
| <dl> <span data-ttu-id="700bb-125"><dt>Macchina virtuale \_ E \_ media \_ di \_ tipo errato</dt> <dt>0xA00400728</dt></span><span class="sxs-lookup"><span data-stu-id="700bb-125"><dt>VM\_E\_MEDIA\_WRONG\_TYPE</dt> <dt>0xA00400728</dt></span></span> </dl> | <span data-ttu-id="700bb-126">Il supporto acquisito da questa unità DVD non è un'unità host.</span><span class="sxs-lookup"><span data-stu-id="700bb-126">The media captured by this DVD drive is not a host drive.</span></span><br/> |
| <dl> <span data-ttu-id="700bb-127"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="700bb-127"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>         | <span data-ttu-id="700bb-128">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="700bb-128">An unexpected error has occurred.</span></span><br/>                         |



## <a name="requirements"></a><span data-ttu-id="700bb-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="700bb-129">Requirements</span></span>



| <span data-ttu-id="700bb-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="700bb-130">Requirement</span></span> | <span data-ttu-id="700bb-131">Valore</span><span class="sxs-lookup"><span data-stu-id="700bb-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="700bb-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="700bb-132">Minimum supported client</span></span><br/> | <span data-ttu-id="700bb-133">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="700bb-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="700bb-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="700bb-134">Minimum supported server</span></span><br/> | <span data-ttu-id="700bb-135">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="700bb-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="700bb-136">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="700bb-136">End of client support</span></span><br/>    | <span data-ttu-id="700bb-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="700bb-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="700bb-138">Prodotto</span><span class="sxs-lookup"><span data-stu-id="700bb-138">Product</span></span><br/>                  | <span data-ttu-id="700bb-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="700bb-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="700bb-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="700bb-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="700bb-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="700bb-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="700bb-142">IID</span><span class="sxs-lookup"><span data-stu-id="700bb-142">IID</span></span><br/>                      | <span data-ttu-id="700bb-143">IID \_ IVMDVDDrive è definito come b96328f6-6732-437D-a00d-ffa47e43971c</span><span class="sxs-lookup"><span data-stu-id="700bb-143">IID\_IVMDVDDrive is defined as b96328f6-6732-437d-a00d-ffa47e43971c</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="700bb-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="700bb-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="700bb-145">**IVMDVDDrive**</span><span class="sxs-lookup"><span data-stu-id="700bb-145">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> </dl>

 

