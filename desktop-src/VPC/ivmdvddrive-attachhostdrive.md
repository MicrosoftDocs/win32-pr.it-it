---
title: Metodo IVMDVDDrive AttachHostDrive (VPCCOMInterfaces. h)
description: Connette un'unità host all'unità DVD all'interno della macchina virtuale.
ms.assetid: 68e658ba-470c-452c-8124-5bb2ec81911b
keywords:
- Metodo AttachHostDrive Virtual PC
- Metodo AttachHostDrive Virtual PC, interfaccia IVMDVDDrive
- Interfaccia IVMDVDDrive Virtual PC, metodo AttachHostDrive
topic_type:
- apiref
api_name:
- IVMDVDDrive.AttachHostDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 012afcdc0b88aa5b77f1d85cc5becff1e70853f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302420"
---
# <a name="ivmdvddriveattachhostdrive-method"></a><span data-ttu-id="96de1-106">Metodo IVMDVDDrive:: AttachHostDrive</span><span class="sxs-lookup"><span data-stu-id="96de1-106">IVMDVDDrive::AttachHostDrive method</span></span>

<span data-ttu-id="96de1-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="96de1-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="96de1-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="96de1-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="96de1-109">Connette un'unità host all'unità DVD all'interno della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="96de1-109">Attaches a host drive to the DVD drive within the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="96de1-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="96de1-110">Syntax</span></span>


```C++
HRESULT AttachHostDrive(
  [in] BSTR driveLetter
);
```



## <a name="parameters"></a><span data-ttu-id="96de1-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="96de1-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96de1-112">*LetteraUnità* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="96de1-112">*driveLetter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96de1-113">Lettera dell'unità host da collegare.</span><span class="sxs-lookup"><span data-stu-id="96de1-113">The letter of the host drive that is to be attached.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96de1-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="96de1-114">Return value</span></span>

<span data-ttu-id="96de1-115">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="96de1-115">This method can return one of these values.</span></span>



| <span data-ttu-id="96de1-116">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="96de1-116">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="96de1-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="96de1-117">Description</span></span>                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="96de1-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="96de1-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                          | <span data-ttu-id="96de1-119">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="96de1-119">The operation was successful.</span></span><br/>                                                                                                                                             |
| <dl> <span data-ttu-id="96de1-120"><dt>**E \_**</dt> <dt>0x80000003</dt> INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="96de1-120"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>         | <span data-ttu-id="96de1-121">Non è stata specificata alcuna lettera di unità o la lettera di unità specificata non è valida.</span><span class="sxs-lookup"><span data-stu-id="96de1-121">No drive letter was specified, or the specified drive letter is invalid.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="96de1-122"><dt>**E \_ ERRORE**</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="96de1-122"><dt>**E\_FAIL**</dt> <dt>0x80004005</dt></span></span> </dl>               | <span data-ttu-id="96de1-123">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="96de1-123">An unexpected error has occurred.</span></span><br/>                                                                                                                                         |
| <dl> <span data-ttu-id="96de1-124"><dt>**Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="96de1-124"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>    | <span data-ttu-id="96de1-125">Impossibile trovare la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="96de1-125">The virtual machine could not be found.</span></span><br/>                                                                                                                                   |
| <dl> <span data-ttu-id="96de1-126"><dt>**Macchina virtuale \_ \_Unità E \_ in \_ use**</dt> <dt>0xA0040727</dt></span><span class="sxs-lookup"><span data-stu-id="96de1-126"><dt>**VM\_E\_DRIVE\_IN\_USE**</dt> <dt>0xA0040727</dt></span></span> </dl> | <span data-ttu-id="96de1-127">Un'unità DVD o un'immagine ISO host è già collegata a questa unità all'interno della macchina virtuale oppure l'unità host specificata è già in uso in un'altra macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="96de1-127">A host DVD drive or ISO image is already attached to this drive within the virtual machine, or the specified host drive is already in use within another virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="96de1-128"><dt>**Macchina virtuale \_ Unità E 0xA0040502 \_ \_ non valide**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="96de1-128"><dt>**VM\_E\_DRIVE\_INVALID**</dt> <dt>0xA0040502</dt></span></span> </dl> | <span data-ttu-id="96de1-129">Il percorso del bus per questa unità non è valido o l'unità non sembra essere un'unità DVD valida.</span><span class="sxs-lookup"><span data-stu-id="96de1-129">The bus location for this drive is invalid, or the drive does not appear to be a valid DVD drive.</span></span><br/>                                                                         |
| <dl> <span data-ttu-id="96de1-130"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="96de1-130"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>    | <span data-ttu-id="96de1-131">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="96de1-131">An unexpected error has occurred.</span></span><br/>                                                                                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="96de1-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="96de1-132">Requirements</span></span>



| <span data-ttu-id="96de1-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="96de1-133">Requirement</span></span> | <span data-ttu-id="96de1-134">Valore</span><span class="sxs-lookup"><span data-stu-id="96de1-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="96de1-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="96de1-135">Minimum supported client</span></span><br/> | <span data-ttu-id="96de1-136">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="96de1-136">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="96de1-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="96de1-137">Minimum supported server</span></span><br/> | <span data-ttu-id="96de1-138">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="96de1-138">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="96de1-139">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="96de1-139">End of client support</span></span><br/>    | <span data-ttu-id="96de1-140">Windows 7</span><span class="sxs-lookup"><span data-stu-id="96de1-140">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="96de1-141">Prodotto</span><span class="sxs-lookup"><span data-stu-id="96de1-141">Product</span></span><br/>                  | <span data-ttu-id="96de1-142">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="96de1-142">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="96de1-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="96de1-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="96de1-144"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="96de1-144"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="96de1-145">IID</span><span class="sxs-lookup"><span data-stu-id="96de1-145">IID</span></span><br/>                      | <span data-ttu-id="96de1-146">IID \_ IVMDVDDrive è definito come b96328f6-6732-437D-a00d-ffa47e43971c</span><span class="sxs-lookup"><span data-stu-id="96de1-146">IID\_IVMDVDDrive is defined as b96328f6-6732-437d-a00d-ffa47e43971c</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="96de1-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="96de1-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96de1-148">**IVMDVDDrive**</span><span class="sxs-lookup"><span data-stu-id="96de1-148">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> </dl>

 

