---
title: Metodo bivio IVMVirtualMachine (VPCCOMInterfaces. h)
description: Spegnimento della macchina virtuale.
ms.assetid: 4ea00314-8f1e-47d9-bbb8-b5791af1fb86
keywords:
- Metodo bivio per PC virtuale
- Metodo deviazione Virtual PC, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC, metodo deviazione
topic_type:
- apiref
api_name:
- IVMVirtualMachine.TurnOff
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27a5b14955fcc8a060c49932e3fa4f238497a567
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048622"
---
# <a name="ivmvirtualmachineturnoff-method"></a><span data-ttu-id="32686-106">Metodo IVMVirtualMachine:: bivio</span><span class="sxs-lookup"><span data-stu-id="32686-106">IVMVirtualMachine::TurnOff method</span></span>

<span data-ttu-id="32686-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="32686-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="32686-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="32686-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="32686-109">Spegnimento della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="32686-109">Turns off the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="32686-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="32686-110">Syntax</span></span>


```C++
HRESULT TurnOff(
  [out, retval] IVMTask **turnOffTask
);
```



## <a name="parameters"></a><span data-ttu-id="32686-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="32686-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32686-112">*turnOffTask* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="32686-112">*turnOffTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="32686-113">Un oggetto [**IVMTask**](ivmtask.md) usato per tenere traccia dello stato di avanzamento della sequenza di deviazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="32686-113">An [**IVMTask**](ivmtask.md) object that is used to track the completion progress of the virtual machine's turnoff sequence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32686-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="32686-114">Return value</span></span>

<span data-ttu-id="32686-115">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="32686-115">This method can return one of these values.</span></span>



| <span data-ttu-id="32686-116">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="32686-116">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="32686-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="32686-117">Description</span></span>                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="32686-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="32686-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                | <span data-ttu-id="32686-119">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="32686-119">The operation was successful.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="32686-120"><dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="32686-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                  | <span data-ttu-id="32686-121">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="32686-121">The parameter is **NULL**.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="32686-122"><dt>**HRESULT \_ DA \_ Win32 ( \_ accesso errore \_ negato)**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="32686-122"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ACCESS\_DENIED)**</dt> <dt>0x80070005</dt></span></span> </dl> | <span data-ttu-id="32686-123">Il chiamante deve disporre delle autorizzazioni di accesso Execute per disattivare questa macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="32686-123">The caller must have execute access permissions to turn off this virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="32686-124"><dt>**Macchina virtuale \_ \_VM E \_ non \_ in esecuzione**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="32686-124"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                     | <span data-ttu-id="32686-125">La macchina virtuale non è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="32686-125">The virtual machine is not running.</span></span><br/>                                               |
| <dl> <span data-ttu-id="32686-126"><dt>**Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="32686-126"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                          | <span data-ttu-id="32686-127">La configurazione è sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="32686-127">The configuration is unknown.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="32686-128"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="32686-128"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                          | <span data-ttu-id="32686-129">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="32686-129">An unexpected error has occurred.</span></span><br/>                                                 |



 

## <a name="remarks"></a><span data-ttu-id="32686-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="32686-130">Remarks</span></span>

<span data-ttu-id="32686-131">Questo metodo disattiva la macchina virtuale in modo analogo alla disattivazione di un computer fisico.</span><span class="sxs-lookup"><span data-stu-id="32686-131">This method turns off the virtual machine in the same manner as turning the power off on a physical machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="32686-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="32686-132">Requirements</span></span>



| <span data-ttu-id="32686-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="32686-133">Requirement</span></span> | <span data-ttu-id="32686-134">Valore</span><span class="sxs-lookup"><span data-stu-id="32686-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="32686-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="32686-135">Minimum supported client</span></span><br/> | <span data-ttu-id="32686-136">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="32686-136">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="32686-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="32686-137">Minimum supported server</span></span><br/> | <span data-ttu-id="32686-138">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="32686-138">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="32686-139">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="32686-139">End of client support</span></span><br/>    | <span data-ttu-id="32686-140">Windows 7</span><span class="sxs-lookup"><span data-stu-id="32686-140">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="32686-141">Prodotto</span><span class="sxs-lookup"><span data-stu-id="32686-141">Product</span></span><br/>                  | <span data-ttu-id="32686-142">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="32686-142">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="32686-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="32686-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="32686-144"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="32686-144"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="32686-145">IID</span><span class="sxs-lookup"><span data-stu-id="32686-145">IID</span></span><br/>                      | <span data-ttu-id="32686-146">IID \_ IVMVirtualMachine è definito come f7092aa1-33ed-4F78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="32686-146">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="32686-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="32686-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32686-148">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="32686-148">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

