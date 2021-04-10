---
title: Metodo IVMVirtualMachine RemoveDVDROMDrive (VPCCOMInterfaces. h)
description: Rimuove l'unità CD o DVD specificata dalla macchina virtuale.
ms.assetid: 1c45c271-bead-41f6-8371-448d385a1288
keywords:
- Metodo RemoveDVDROMDrive Virtual PC
- Metodo RemoveDVDROMDrive Virtual PC, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC, metodo RemoveDVDROMDrive
topic_type:
- apiref
api_name:
- IVMVirtualMachine.RemoveDVDROMDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf0962b388c318d5abebdbd7a021a4466e644a28
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120050"
---
# <a name="ivmvirtualmachineremovedvdromdrive-method"></a><span data-ttu-id="4efb1-106">Metodo IVMVirtualMachine:: RemoveDVDROMDrive</span><span class="sxs-lookup"><span data-stu-id="4efb1-106">IVMVirtualMachine::RemoveDVDROMDrive method</span></span>

<span data-ttu-id="4efb1-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="4efb1-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="4efb1-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="4efb1-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="4efb1-109">Rimuove l'unità CD o DVD specificata dalla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="4efb1-109">Removes the specified CD or DVD drive from the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="4efb1-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4efb1-110">Syntax</span></span>


```C++
HRESULT RemoveDVDROMDrive(
  [in] IVMDVDDrive *dvdDrive
);
```



## <a name="parameters"></a><span data-ttu-id="4efb1-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="4efb1-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4efb1-112">*dvdDrive* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4efb1-112">*dvdDrive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4efb1-113">Unità da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="4efb1-113">The drive to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4efb1-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4efb1-114">Return value</span></span>

<span data-ttu-id="4efb1-115">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="4efb1-115">This method can return one of these values.</span></span>



| <span data-ttu-id="4efb1-116">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="4efb1-116">Return code/value</span></span>                                                                                                                                                            | <span data-ttu-id="4efb1-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4efb1-117">Description</span></span>                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="4efb1-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4efb1-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                  | <span data-ttu-id="4efb1-119">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="4efb1-119">The operation was successful.</span></span><br/>                              |
| <dl> <span data-ttu-id="4efb1-120"><dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="4efb1-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                    | <span data-ttu-id="4efb1-121">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="4efb1-121">The parameter is **NULL**.</span></span><br/>                                 |
| <dl> <span data-ttu-id="4efb1-122"><dt>**Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="4efb1-122"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>            | <span data-ttu-id="4efb1-123">La configurazione è sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="4efb1-123">The configuration is unknown.</span></span><br/>                              |
| <dl> <span data-ttu-id="4efb1-124"><dt>**Macchina virtuale \_ \_Macchina virtuale di e \_ in esecuzione \_ o \_ salvata**</dt> <dt>0xA004020B</dt></span><span class="sxs-lookup"><span data-stu-id="4efb1-124"><dt>**VM\_E\_VM\_RUNNING\_OR\_SAVED**</dt> <dt>0xA004020B</dt></span></span> </dl> | <span data-ttu-id="4efb1-125">Lo stato della macchina virtuale è in esecuzione o salvato.</span><span class="sxs-lookup"><span data-stu-id="4efb1-125">The virtual machine is in a running or saved state.</span></span><br/>        |
| <dl> <span data-ttu-id="4efb1-126"><dt>**Macchina virtuale \_ Unità E 0xA0040502 \_ \_ non valide**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="4efb1-126"><dt>**VM\_E\_DRIVE\_INVALID**</dt> <dt>0xA0040502</dt></span></span> </dl>         | <span data-ttu-id="4efb1-127">L'unità specificata non è connessa a questo percorso del bus.</span><span class="sxs-lookup"><span data-stu-id="4efb1-127">The drive specified is not connected to this bus location.</span></span><br/> |
| <dl> <span data-ttu-id="4efb1-128"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="4efb1-128"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>            | <span data-ttu-id="4efb1-129">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="4efb1-129">An unexpected error has occurred.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="4efb1-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="4efb1-130">Remarks</span></span>

<span data-ttu-id="4efb1-131">È possibile rimuovere solo un'unità CD o DVD esistente da una macchina virtuale arrestata.</span><span class="sxs-lookup"><span data-stu-id="4efb1-131">You can only remove an existing CD or DVD drive from a stopped virtual machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="4efb1-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4efb1-132">Requirements</span></span>



| <span data-ttu-id="4efb1-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="4efb1-133">Requirement</span></span> | <span data-ttu-id="4efb1-134">Valore</span><span class="sxs-lookup"><span data-stu-id="4efb1-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4efb1-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4efb1-135">Minimum supported client</span></span><br/> | <span data-ttu-id="4efb1-136">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="4efb1-136">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4efb1-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4efb1-137">Minimum supported server</span></span><br/> | <span data-ttu-id="4efb1-138">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="4efb1-138">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="4efb1-139">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="4efb1-139">End of client support</span></span><br/>    | <span data-ttu-id="4efb1-140">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4efb1-140">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="4efb1-141">Prodotto</span><span class="sxs-lookup"><span data-stu-id="4efb1-141">Product</span></span><br/>                  | <span data-ttu-id="4efb1-142">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="4efb1-142">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="4efb1-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4efb1-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="4efb1-144"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="4efb1-144"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="4efb1-145">IID</span><span class="sxs-lookup"><span data-stu-id="4efb1-145">IID</span></span><br/>                      | <span data-ttu-id="4efb1-146">IID \_ IVMVirtualMachine è definito come f7092aa1-33ed-4F78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="4efb1-146">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="4efb1-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4efb1-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4efb1-148">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="4efb1-148">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

