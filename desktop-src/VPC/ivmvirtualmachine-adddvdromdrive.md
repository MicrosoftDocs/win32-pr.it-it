---
title: Metodo IVMVirtualMachine AddDVDROMDrive (VPCCOMInterfaces. h)
description: Aggiunge una nuova unità CD o DVD alla macchina virtuale.
ms.assetid: d39f2728-6146-42ed-b67f-6586566a7209
keywords:
- Metodo AddDVDROMDrive Virtual PC
- Metodo AddDVDROMDrive Virtual PC, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC, metodo AddDVDROMDrive
topic_type:
- apiref
api_name:
- IVMVirtualMachine.AddDVDROMDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7acbe70f6b338b3490c12ab67bcdfdc997d90a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301777"
---
# <a name="ivmvirtualmachineadddvdromdrive-method"></a><span data-ttu-id="13a0a-106">Metodo IVMVirtualMachine:: AddDVDROMDrive</span><span class="sxs-lookup"><span data-stu-id="13a0a-106">IVMVirtualMachine::AddDVDROMDrive method</span></span>

<span data-ttu-id="13a0a-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="13a0a-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="13a0a-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="13a0a-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="13a0a-109">Aggiunge una nuova unità CD o DVD alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="13a0a-109">Adds a new CD or DVD drive to the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="13a0a-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="13a0a-110">Syntax</span></span>


```C++
HRESULT AddDVDROMDrive(
  [in]          long        busNumber,
  [in]          long        deviceNumber,
  [out, retval] IVMDVDDrive **dvdDrive
);
```



## <a name="parameters"></a><span data-ttu-id="13a0a-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="13a0a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13a0a-112">*busNumber* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="13a0a-112">*busNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13a0a-113">Il bus al quale verrà collegata l'unità.</span><span class="sxs-lookup"><span data-stu-id="13a0a-113">The bus to which the drive will be attached.</span></span>



| <span data-ttu-id="13a0a-114">Valore</span><span class="sxs-lookup"><span data-stu-id="13a0a-114">Value</span></span>                                                                        | <span data-ttu-id="13a0a-115">Significato</span><span class="sxs-lookup"><span data-stu-id="13a0a-115">Meaning</span></span>                                                  |
|------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="13a0a-116"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="13a0a-116"><dt>0</dt></span></span> </dl> | <span data-ttu-id="13a0a-117">L'unità verrà collegata al primo bus.</span><span class="sxs-lookup"><span data-stu-id="13a0a-117">The drive will be attached to the first bus.</span></span><br/>  |
| <dl> <span data-ttu-id="13a0a-118"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="13a0a-118"><dt>1</dt></span></span> </dl> | <span data-ttu-id="13a0a-119">L'unità verrà collegata al secondo bus.</span><span class="sxs-lookup"><span data-stu-id="13a0a-119">The drive will be attached to the second bus.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="13a0a-120">*deviceNumber* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="13a0a-120">*deviceNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13a0a-121">Dispositivo a cui verrà collegata l'unità.</span><span class="sxs-lookup"><span data-stu-id="13a0a-121">The device to which the drive will be attached.</span></span>



| <span data-ttu-id="13a0a-122">Valore</span><span class="sxs-lookup"><span data-stu-id="13a0a-122">Value</span></span>                                                                        | <span data-ttu-id="13a0a-123">Significato</span><span class="sxs-lookup"><span data-stu-id="13a0a-123">Meaning</span></span>                                                                |
|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="13a0a-124"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="13a0a-124"><dt>0</dt></span></span> </dl> | <span data-ttu-id="13a0a-125">L'unità verrà collegata al primo dispositivo del bus.</span><span class="sxs-lookup"><span data-stu-id="13a0a-125">The drive will be attached to the first device on the bus.</span></span><br/>  |
| <dl> <span data-ttu-id="13a0a-126"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="13a0a-126"><dt>1</dt></span></span> </dl> | <span data-ttu-id="13a0a-127">L'unità verrà collegata al secondo dispositivo del bus.</span><span class="sxs-lookup"><span data-stu-id="13a0a-127">The drive will be attached to the second device on the bus.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="13a0a-128">*dvdDrive* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="13a0a-128">*dvdDrive* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="13a0a-129">Oggetto [**IVMDVDDrive**](ivmdvddrive.md) .</span><span class="sxs-lookup"><span data-stu-id="13a0a-129">An [**IVMDVDDrive**](ivmdvddrive.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13a0a-130">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="13a0a-130">Return value</span></span>

<span data-ttu-id="13a0a-131">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="13a0a-131">This method can return one of these values.</span></span>



| <span data-ttu-id="13a0a-132">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="13a0a-132">Return code/value</span></span>                                                                                                                                                               | <span data-ttu-id="13a0a-133">Descrizione</span><span class="sxs-lookup"><span data-stu-id="13a0a-133">Description</span></span>                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="13a0a-134"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="13a0a-134"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                     | <span data-ttu-id="13a0a-135">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="13a0a-135">The operation was successful.</span></span><br/>                       |
| <dl> <span data-ttu-id="13a0a-136"><dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="13a0a-136"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                       | <span data-ttu-id="13a0a-137">Il parametro *dvdDrive* è **null**.</span><span class="sxs-lookup"><span data-stu-id="13a0a-137">The *dvdDrive* parameter is **NULL**.</span></span><br/>               |
| <dl> <span data-ttu-id="13a0a-138"><dt>**E \_**</dt> <dt>0x80000003</dt> INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="13a0a-138"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                    | <span data-ttu-id="13a0a-139">Un parametro non è valido.</span><span class="sxs-lookup"><span data-stu-id="13a0a-139">A parameter is not valid.</span></span><br/>                           |
| <dl> <span data-ttu-id="13a0a-140"><dt>**Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="13a0a-140"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>               | <span data-ttu-id="13a0a-141">La configurazione è sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="13a0a-141">The configuration is unknown.</span></span><br/>                       |
| <dl> <span data-ttu-id="13a0a-142"><dt>**Macchina virtuale \_ \_Macchina virtuale di e \_ in esecuzione \_ o \_ salvata**</dt> <dt>0xA004020B</dt></span><span class="sxs-lookup"><span data-stu-id="13a0a-142"><dt>**VM\_E\_VM\_RUNNING\_OR\_SAVED**</dt> <dt>0xA004020B</dt></span></span> </dl>    | <span data-ttu-id="13a0a-143">Lo stato della macchina virtuale è in esecuzione o salvato.</span><span class="sxs-lookup"><span data-stu-id="13a0a-143">The virtual machine is in a running or saved state.</span></span><br/> |
| <dl> <span data-ttu-id="13a0a-144"><dt>**Macchina virtuale \_ E \_ la \_ \_ loc \_ del bus di unità in \_ use**</dt> <dt>0xA00400503</dt></span><span class="sxs-lookup"><span data-stu-id="13a0a-144"><dt>**VM\_E\_DRIVE\_BUS\_LOC\_IN\_USE**</dt> <dt>0xA00400503</dt></span></span> </dl> | <span data-ttu-id="13a0a-145">Il percorso del bus specificato è in uso.</span><span class="sxs-lookup"><span data-stu-id="13a0a-145">The specified bus location is in use.</span></span><br/>               |
| <dl> <span data-ttu-id="13a0a-146"><dt>**Macchina virtuale \_ Unità E 0xA0040502 \_ \_ non valide**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="13a0a-146"><dt>**VM\_E\_DRIVE\_INVALID**</dt> <dt>0xA0040502</dt></span></span> </dl>            | <span data-ttu-id="13a0a-147">L'unità specificata non è valida.</span><span class="sxs-lookup"><span data-stu-id="13a0a-147">The drive specified is not valid.</span></span><br/>                   |
| <dl> <span data-ttu-id="13a0a-148"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="13a0a-148"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>               | <span data-ttu-id="13a0a-149">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="13a0a-149">An unexpected error has occurred.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="13a0a-150">Commenti</span><span class="sxs-lookup"><span data-stu-id="13a0a-150">Remarks</span></span>

<span data-ttu-id="13a0a-151">È possibile aggiungere solo una nuova unità CD o DVD a una macchina virtuale arrestata.</span><span class="sxs-lookup"><span data-stu-id="13a0a-151">You can only add a new CD or DVD drive to a stopped virtual machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="13a0a-152">Requisiti</span><span class="sxs-lookup"><span data-stu-id="13a0a-152">Requirements</span></span>



| <span data-ttu-id="13a0a-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="13a0a-153">Requirement</span></span> | <span data-ttu-id="13a0a-154">Valore</span><span class="sxs-lookup"><span data-stu-id="13a0a-154">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="13a0a-155">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="13a0a-155">Minimum supported client</span></span><br/> | <span data-ttu-id="13a0a-156">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="13a0a-156">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="13a0a-157">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="13a0a-157">Minimum supported server</span></span><br/> | <span data-ttu-id="13a0a-158">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="13a0a-158">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="13a0a-159">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="13a0a-159">End of client support</span></span><br/>    | <span data-ttu-id="13a0a-160">Windows 7</span><span class="sxs-lookup"><span data-stu-id="13a0a-160">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="13a0a-161">Prodotto</span><span class="sxs-lookup"><span data-stu-id="13a0a-161">Product</span></span><br/>                  | <span data-ttu-id="13a0a-162">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="13a0a-162">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="13a0a-163">Intestazione</span><span class="sxs-lookup"><span data-stu-id="13a0a-163">Header</span></span><br/>                   | <dl> <span data-ttu-id="13a0a-164"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="13a0a-164"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="13a0a-165">IID</span><span class="sxs-lookup"><span data-stu-id="13a0a-165">IID</span></span><br/>                      | <span data-ttu-id="13a0a-166">IID \_ IVMVirtualMachine è definito come f7092aa1-33ed-4F78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="13a0a-166">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="13a0a-167">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="13a0a-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13a0a-168">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="13a0a-168">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

