---
title: Metodo pause IVMVirtualMachine (VPCCOMInterfaces. h)
description: Sospende la macchina virtuale.
ms.assetid: 29ac40c4-7713-4782-8a31-42f2c32b8f7d
keywords:
- Sospendere il metodo Virtual PC
- Sospendere il metodo Virtual PC, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC, metodo pause
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Pause
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c953da05d34c999066a6bc87cb1f51983defbd5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874173"
---
# <a name="ivmvirtualmachinepause-method"></a><span data-ttu-id="5bbf2-106">IVMVirtualMachine::P metodo ause</span><span class="sxs-lookup"><span data-stu-id="5bbf2-106">IVMVirtualMachine::Pause method</span></span>

<span data-ttu-id="5bbf2-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="5bbf2-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="5bbf2-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="5bbf2-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="5bbf2-109">Sospende la macchina virtuale (VM).</span><span class="sxs-lookup"><span data-stu-id="5bbf2-109">Pauses the virtual machine (VM).</span></span>

## <a name="syntax"></a><span data-ttu-id="5bbf2-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5bbf2-110">Syntax</span></span>


```C++
HRESULT Pause();
```



## <a name="parameters"></a><span data-ttu-id="5bbf2-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="5bbf2-111">Parameters</span></span>

<span data-ttu-id="5bbf2-112">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="5bbf2-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5bbf2-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5bbf2-113">Return value</span></span>

<span data-ttu-id="5bbf2-114">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="5bbf2-114">This method can return one of these values.</span></span>



| <span data-ttu-id="5bbf2-115">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="5bbf2-115">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="5bbf2-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5bbf2-116">Description</span></span>                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5bbf2-117"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="5bbf2-117"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                | <span data-ttu-id="5bbf2-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="5bbf2-118">The operation was successful.</span></span><br/>                                     |
| <dl> <span data-ttu-id="5bbf2-119"><dt>**E \_ ERRORE**</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="5bbf2-119"><dt>**E\_FAIL**</dt> <dt>0x80004005</dt></span></span> </dl>                                     | <span data-ttu-id="5bbf2-120">La macchina virtuale è già sospesa.</span><span class="sxs-lookup"><span data-stu-id="5bbf2-120">The VM is already paused.</span></span><br/>                                         |
| <dl> <span data-ttu-id="5bbf2-121"><dt>**HRESULT \_ DA \_ Win32 ( \_ accesso errore \_ negato)**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="5bbf2-121"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ACCESS\_DENIED)**</dt> <dt>0x80070005</dt></span></span> </dl> | <span data-ttu-id="5bbf2-122">Il chiamante deve disporre delle autorizzazioni di accesso Execute per sospendere la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="5bbf2-122">The caller must have execute access permissions to pause this VM.</span></span><br/> |
| <dl> <span data-ttu-id="5bbf2-123"><dt>**Macchina virtuale \_ E \_ timeout \_**</dt> <dt>0xA0040202</dt></span><span class="sxs-lookup"><span data-stu-id="5bbf2-123"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                           | <span data-ttu-id="5bbf2-124">L'operazione non è stata completata in modo tempestivo.</span><span class="sxs-lookup"><span data-stu-id="5bbf2-124">The operation did not complete in a timely manner.</span></span><br/>                |
| <dl> <span data-ttu-id="5bbf2-125"><dt>**Macchina virtuale \_ \_VM E \_ non \_ in esecuzione**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="5bbf2-125"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                     | <span data-ttu-id="5bbf2-126">La macchina virtuale non è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="5bbf2-126">The virtual machine is not running.</span></span><br/>                               |
| <dl> <span data-ttu-id="5bbf2-127"><dt>**Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="5bbf2-127"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                          | <span data-ttu-id="5bbf2-128">La configurazione è sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="5bbf2-128">The configuration is unknown.</span></span><br/>                                     |
| <dl> <span data-ttu-id="5bbf2-129"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="5bbf2-129"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                          | <span data-ttu-id="5bbf2-130">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="5bbf2-130">An unexpected error has occurred.</span></span><br/>                                 |



 

## <a name="remarks"></a><span data-ttu-id="5bbf2-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="5bbf2-131">Remarks</span></span>

<span data-ttu-id="5bbf2-132">**Sospende** non salva lo stato corrente della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="5bbf2-132">**Pause** does not save the current state of the VM.</span></span>

## <a name="requirements"></a><span data-ttu-id="5bbf2-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5bbf2-133">Requirements</span></span>



| <span data-ttu-id="5bbf2-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="5bbf2-134">Requirement</span></span> | <span data-ttu-id="5bbf2-135">Valore</span><span class="sxs-lookup"><span data-stu-id="5bbf2-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="5bbf2-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5bbf2-136">Minimum supported client</span></span><br/> | <span data-ttu-id="5bbf2-137">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="5bbf2-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5bbf2-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5bbf2-138">Minimum supported server</span></span><br/> | <span data-ttu-id="5bbf2-139">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="5bbf2-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="5bbf2-140">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="5bbf2-140">End of client support</span></span><br/>    | <span data-ttu-id="5bbf2-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="5bbf2-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="5bbf2-142">Prodotto</span><span class="sxs-lookup"><span data-stu-id="5bbf2-142">Product</span></span><br/>                  | <span data-ttu-id="5bbf2-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="5bbf2-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="5bbf2-144">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5bbf2-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="5bbf2-145"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="5bbf2-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="5bbf2-146">IID</span><span class="sxs-lookup"><span data-stu-id="5bbf2-146">IID</span></span><br/>                      | <span data-ttu-id="5bbf2-147">IID \_ IVMVirtualMachine è definito come f7092aa1-33ed-4F78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="5bbf2-147">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="5bbf2-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5bbf2-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bbf2-149">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="5bbf2-149">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

