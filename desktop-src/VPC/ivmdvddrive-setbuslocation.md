---
title: Metodo IVMDVDDrive SetBusLocation (VPCCOMInterfaces. h)
description: Connette l'unità DVD al percorso del bus specificato nella macchina virtuale.
ms.assetid: 765274b8-91bc-475a-ac4d-994b2425a421
keywords:
- Metodo SetBusLocation Virtual PC
- Metodo SetBusLocation Virtual PC, interfaccia IVMDVDDrive
- Interfaccia IVMDVDDrive Virtual PC, metodo SetBusLocation
topic_type:
- apiref
api_name:
- IVMDVDDrive.SetBusLocation
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db6091493a56c020f57300e65328fee0eb65a69e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301736"
---
# <a name="ivmdvddrivesetbuslocation-method"></a><span data-ttu-id="667e7-106">Metodo IVMDVDDrive:: SetBusLocation</span><span class="sxs-lookup"><span data-stu-id="667e7-106">IVMDVDDrive::SetBusLocation method</span></span>

<span data-ttu-id="667e7-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="667e7-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="667e7-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="667e7-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="667e7-109">Connette l'unità DVD al percorso del bus specificato nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="667e7-109">Attaches the DVD drive to the specified bus location in the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="667e7-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="667e7-110">Syntax</span></span>


```C++
HRESULT SetBusLocation(
  [in] long busNumber,
  [in] long deviceNumber
);
```



## <a name="parameters"></a><span data-ttu-id="667e7-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="667e7-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="667e7-112">*busNumber* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="667e7-112">*busNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="667e7-113">Numero del bus a cui deve essere collegata l'unità.</span><span class="sxs-lookup"><span data-stu-id="667e7-113">The bus number to which this drive is to be attached.</span></span> <span data-ttu-id="667e7-114">Ad esempio, in un bus IDE, questo numero indicherà se usare il numero di bus primario o secondario.</span><span class="sxs-lookup"><span data-stu-id="667e7-114">For example, on an IDE bus, this number would represent whether to use the primary or secondary bus number.</span></span>

</dd> <dt>

<span data-ttu-id="667e7-115">*deviceNumber* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="667e7-115">*deviceNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="667e7-116">Numero del dispositivo a cui deve essere collegata l'unità.</span><span class="sxs-lookup"><span data-stu-id="667e7-116">The device number to which this drive is to be attached.</span></span> <span data-ttu-id="667e7-117">Ad esempio, in un bus IDE, questo numero indicherà se usare il percorso del dispositivo primario o secondario.</span><span class="sxs-lookup"><span data-stu-id="667e7-117">For example, on an IDE bus, this number would represent whether to use the primary or secondary device location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="667e7-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="667e7-118">Return value</span></span>

<span data-ttu-id="667e7-119">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="667e7-119">This method can return one of these values.</span></span>



| <span data-ttu-id="667e7-120">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="667e7-120">Return code/value</span></span>                                                                                                                                                            | <span data-ttu-id="667e7-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="667e7-121">Description</span></span>                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="667e7-122"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="667e7-122"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                  | <span data-ttu-id="667e7-123">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="667e7-123">The operation was successful.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="667e7-124"><dt>**E \_**</dt> <dt>0x80000003</dt> INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="667e7-124"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                 | <span data-ttu-id="667e7-125">Il percorso del bus specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="667e7-125">The bus location specified is not valid.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="667e7-126"><dt>**E \_ ERRORE**</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="667e7-126"><dt>**E\_FAIL**</dt> <dt>0x80004005</dt></span></span> </dl>                       | <span data-ttu-id="667e7-127">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="667e7-127">An unexpected error has occurred.</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="667e7-128"><dt>**Macchina virtuale \_ \_Macchina virtuale di e \_ in esecuzione \_ o \_ salvata**</dt> <dt>0xA004020B</dt></span><span class="sxs-lookup"><span data-stu-id="667e7-128"><dt>**VM\_E\_VM\_RUNNING\_OR\_SAVED**</dt> <dt>0xA004020B</dt></span></span> </dl> | <span data-ttu-id="667e7-129">Non è possibile impostare il percorso del bus mentre la macchina virtuale è in esecuzione o è in uno stato salvato.</span><span class="sxs-lookup"><span data-stu-id="667e7-129">The bus location cannot be set while the virtual machine is running or in a saved state.</span></span><br/>                                     |
| <dl> <span data-ttu-id="667e7-130"><dt>**\_loc VM \_ E \_ bus \_ in \_ uso**</dt></span><span class="sxs-lookup"><span data-stu-id="667e7-130"><dt>**VM\_E\_BUS\_LOC\_IN\_USE**</dt></span></span> </dl>                                                                      | <span data-ttu-id="667e7-131">Un altro dispositivo è già collegato al percorso del bus specificato.</span><span class="sxs-lookup"><span data-stu-id="667e7-131">Another device is already attached to the specified bus location.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="667e7-132"><dt>**Macchina virtuale \_ Unità E 0xA0040502 \_ \_ non valide**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="667e7-132"><dt>**VM\_E\_DRIVE\_INVALID**</dt> <dt>0xA0040502</dt></span></span> </dl>         | <span data-ttu-id="667e7-133">Non è stato possibile inizializzare l'unità corrente.</span><span class="sxs-lookup"><span data-stu-id="667e7-133">The current drive could not be initialized.</span></span><br/>                                                                                  |
| <dl> <span data-ttu-id="667e7-134"><dt>**Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="667e7-134"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>            | <span data-ttu-id="667e7-135">Non è stato possibile scrivere le modifiche nel file delle preferenze perché non è stato possibile determinare la macchina virtuale per questa unità.</span><span class="sxs-lookup"><span data-stu-id="667e7-135">The changes could not be written to the preferences file because the virtual machine for this drive could not be determined.</span></span><br/> |
| <dl> <span data-ttu-id="667e7-136"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="667e7-136"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>            | <span data-ttu-id="667e7-137">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="667e7-137">An unexpected error has occurred.</span></span><br/>                                                                                            |



 

## <a name="requirements"></a><span data-ttu-id="667e7-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="667e7-138">Requirements</span></span>



| <span data-ttu-id="667e7-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="667e7-139">Requirement</span></span> | <span data-ttu-id="667e7-140">Valore</span><span class="sxs-lookup"><span data-stu-id="667e7-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="667e7-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="667e7-141">Minimum supported client</span></span><br/> | <span data-ttu-id="667e7-142">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="667e7-142">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="667e7-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="667e7-143">Minimum supported server</span></span><br/> | <span data-ttu-id="667e7-144">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="667e7-144">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="667e7-145">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="667e7-145">End of client support</span></span><br/>    | <span data-ttu-id="667e7-146">Windows 7</span><span class="sxs-lookup"><span data-stu-id="667e7-146">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="667e7-147">Prodotto</span><span class="sxs-lookup"><span data-stu-id="667e7-147">Product</span></span><br/>                  | <span data-ttu-id="667e7-148">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="667e7-148">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="667e7-149">Intestazione</span><span class="sxs-lookup"><span data-stu-id="667e7-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="667e7-150"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="667e7-150"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="667e7-151">IID</span><span class="sxs-lookup"><span data-stu-id="667e7-151">IID</span></span><br/>                      | <span data-ttu-id="667e7-152">IID \_ IVMDVDDrive è definito come b96328f6-6732-437D-a00d-ffa47e43971c</span><span class="sxs-lookup"><span data-stu-id="667e7-152">IID\_IVMDVDDrive is defined as b96328f6-6732-437d-a00d-ffa47e43971c</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="667e7-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="667e7-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="667e7-154">**IVMDVDDrive**</span><span class="sxs-lookup"><span data-stu-id="667e7-154">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> </dl>

 

