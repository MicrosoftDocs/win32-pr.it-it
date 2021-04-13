---
title: Metodo IVMDVDDrive ReleaseHostDrive (VPCCOMInterfaces. h)
description: Rilascia un'unità host acquisita dall'unità DVD.
ms.assetid: 88bbe364-0c39-40c2-89e7-22ffd66259a2
keywords:
- Metodo ReleaseHostDrive Virtual PC
- Metodo ReleaseHostDrive Virtual PC, interfaccia IVMDVDDrive
- Interfaccia IVMDVDDrive Virtual PC, metodo ReleaseHostDrive
topic_type:
- apiref
api_name:
- IVMDVDDrive.ReleaseHostDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2ed2c551ba619855743266b9b506a0c579f92a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400514"
---
# <a name="ivmdvddrivereleasehostdrive-method"></a><span data-ttu-id="1e87e-106">Metodo IVMDVDDrive:: ReleaseHostDrive</span><span class="sxs-lookup"><span data-stu-id="1e87e-106">IVMDVDDrive::ReleaseHostDrive method</span></span>

<span data-ttu-id="1e87e-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="1e87e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="1e87e-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="1e87e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="1e87e-109">Rilascia un'unità host acquisita dall'unità DVD.</span><span class="sxs-lookup"><span data-stu-id="1e87e-109">Releases a captured host drive from the DVD drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e87e-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1e87e-110">Syntax</span></span>


```C++
HRESULT ReleaseHostDrive();
```



## <a name="parameters"></a><span data-ttu-id="1e87e-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="1e87e-111">Parameters</span></span>

<span data-ttu-id="1e87e-112">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="1e87e-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1e87e-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1e87e-113">Return value</span></span>

<span data-ttu-id="1e87e-114">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="1e87e-114">This method can return one of these values.</span></span>



| <span data-ttu-id="1e87e-115">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="1e87e-115">Return code/value</span></span>                                                                                                                                                         | <span data-ttu-id="1e87e-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1e87e-116">Description</span></span>                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1e87e-117"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="1e87e-117"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                               | <span data-ttu-id="1e87e-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="1e87e-118">The operation was successful.</span></span><br/>                                      |
| <dl> <span data-ttu-id="1e87e-119"><dt>**E \_ ERRORE**</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="1e87e-119"><dt>**E\_FAIL**</dt> <dt>0x80004005</dt></span></span> </dl>                    | <span data-ttu-id="1e87e-120">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="1e87e-120">An unexpected error has occurred.</span></span><br/>                                  |
| <dl> <span data-ttu-id="1e87e-121"><dt>**Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="1e87e-121"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>         | <span data-ttu-id="1e87e-122">Impossibile trovare la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="1e87e-122">The virtual machine could not be found.</span></span><br/>                            |
| <dl> <span data-ttu-id="1e87e-123"><dt>**Macchina virtuale \_ E \_ media \_ di \_ tipo errato**</dt> <dt>0xA00400728</dt></span><span class="sxs-lookup"><span data-stu-id="1e87e-123"><dt>**VM\_E\_MEDIA\_WRONG\_TYPE**</dt> <dt>0xA00400728</dt></span></span> </dl> | <span data-ttu-id="1e87e-124">Il supporto attualmente acquisito non è un'unità disco host.</span><span class="sxs-lookup"><span data-stu-id="1e87e-124">The currently captured media is not a host disk drive.</span></span><br/>             |
| <dl> <span data-ttu-id="1e87e-125"><dt>**Macchina virtuale \_ Unità E 0xA0040502 \_ \_ non valide**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="1e87e-125"><dt>**VM\_E\_DRIVE\_INVALID**</dt> <dt>0xA0040502</dt></span></span> </dl>      | <span data-ttu-id="1e87e-126">Non è stato possibile inizializzare l'unità a causa di una posizione del bus non valida.</span><span class="sxs-lookup"><span data-stu-id="1e87e-126">The drive could not be initialized due to an invalid bus location.</span></span><br/> |
| <dl> <span data-ttu-id="1e87e-127"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="1e87e-127"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>         | <span data-ttu-id="1e87e-128">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="1e87e-128">An unexpected error has occurred.</span></span><br/>                                  |



 

## <a name="requirements"></a><span data-ttu-id="1e87e-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1e87e-129">Requirements</span></span>



| <span data-ttu-id="1e87e-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e87e-130">Requirement</span></span> | <span data-ttu-id="1e87e-131">Valore</span><span class="sxs-lookup"><span data-stu-id="1e87e-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e87e-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1e87e-132">Minimum supported client</span></span><br/> | <span data-ttu-id="1e87e-133">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="1e87e-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1e87e-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1e87e-134">Minimum supported server</span></span><br/> | <span data-ttu-id="1e87e-135">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="1e87e-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="1e87e-136">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="1e87e-136">End of client support</span></span><br/>    | <span data-ttu-id="1e87e-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1e87e-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="1e87e-138">Prodotto</span><span class="sxs-lookup"><span data-stu-id="1e87e-138">Product</span></span><br/>                  | <span data-ttu-id="1e87e-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="1e87e-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="1e87e-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1e87e-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e87e-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e87e-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="1e87e-142">IID</span><span class="sxs-lookup"><span data-stu-id="1e87e-142">IID</span></span><br/>                      | <span data-ttu-id="1e87e-143">IID \_ IVMDVDDrive è definito come b96328f6-6732-437D-a00d-ffa47e43971c</span><span class="sxs-lookup"><span data-stu-id="1e87e-143">IID\_IVMDVDDrive is defined as b96328f6-6732-437d-a00d-ffa47e43971c</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="1e87e-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1e87e-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e87e-145">**IVMDVDDrive**</span><span class="sxs-lookup"><span data-stu-id="1e87e-145">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> </dl>

 

