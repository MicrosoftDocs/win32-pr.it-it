---
title: Metodo Resume IVMVirtualMachine (VPCCOMInterfaces. h)
description: Riprende la macchina virtuale.
ms.assetid: 4a2d6b64-8dcf-484e-940d-b0180aba9f01
keywords:
- Riprendere il metodo Virtual PC
- Resume Method Virtual PC, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC, metodo Resume
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Resume
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c24af1e1a00aa0fa29acc077faf48287c0307414
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874285"
---
# <a name="ivmvirtualmachineresume-method"></a><span data-ttu-id="d8648-106">Metodo IVMVirtualMachine:: Resume</span><span class="sxs-lookup"><span data-stu-id="d8648-106">IVMVirtualMachine::Resume method</span></span>

<span data-ttu-id="d8648-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d8648-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d8648-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d8648-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d8648-109">Riprende la macchina virtuale (VM).</span><span class="sxs-lookup"><span data-stu-id="d8648-109">Resumes the virtual machine (VM).</span></span>

## <a name="syntax"></a><span data-ttu-id="d8648-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d8648-110">Syntax</span></span>


```C++
HRESULT Resume();
```



## <a name="parameters"></a><span data-ttu-id="d8648-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="d8648-111">Parameters</span></span>

<span data-ttu-id="d8648-112">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="d8648-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d8648-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d8648-113">Return value</span></span>

<span data-ttu-id="d8648-114">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="d8648-114">This method can return one of these values.</span></span>



| <span data-ttu-id="d8648-115">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="d8648-115">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="d8648-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d8648-116">Description</span></span>                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d8648-117"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d8648-117"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                | <span data-ttu-id="d8648-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="d8648-118">The operation was successful.</span></span><br/>                                      |
| <dl> <span data-ttu-id="d8648-119"><dt>**E \_ ERRORE**</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="d8648-119"><dt>**E\_FAIL**</dt> <dt>0x80004005</dt></span></span> </dl>                                     | <span data-ttu-id="d8648-120">La macchina virtuale non è sospesa.</span><span class="sxs-lookup"><span data-stu-id="d8648-120">The VM is not paused.</span></span><br/>                                              |
| <dl> <span data-ttu-id="d8648-121"><dt>**HRESULT \_ DA \_ Win32 ( \_ accesso errore \_ negato)**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="d8648-121"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ACCESS\_DENIED)**</dt> <dt>0x80070005</dt></span></span> </dl> | <span data-ttu-id="d8648-122">Il chiamante deve avere le autorizzazioni di accesso Execute per riprendere questa macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d8648-122">The caller must have execute access permissions to resume this VM.</span></span><br/> |
| <dl> <span data-ttu-id="d8648-123"><dt>**Macchina virtuale \_ E \_ timeout \_**</dt> <dt>0xA0040202</dt></span><span class="sxs-lookup"><span data-stu-id="d8648-123"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                           | <span data-ttu-id="d8648-124">L'operazione non è stata completata in modo tempestivo.</span><span class="sxs-lookup"><span data-stu-id="d8648-124">The operation did not complete in a timely manner.</span></span><br/>                 |
| <dl> <span data-ttu-id="d8648-125"><dt>**Macchina virtuale \_ \_VM E \_ non \_ in esecuzione**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="d8648-125"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                     | <span data-ttu-id="d8648-126">La macchina virtuale non è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="d8648-126">The VM is not running.</span></span><br/>                                             |
| <dl> <span data-ttu-id="d8648-127"><dt>**Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="d8648-127"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                          | <span data-ttu-id="d8648-128">La configurazione è sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="d8648-128">The configuration is unknown.</span></span><br/>                                      |
| <dl> <span data-ttu-id="d8648-129"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="d8648-129"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                          | <span data-ttu-id="d8648-130">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="d8648-130">An unexpected error has occurred.</span></span><br/>                                  |



 

## <a name="requirements"></a><span data-ttu-id="d8648-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d8648-131">Requirements</span></span>



| <span data-ttu-id="d8648-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8648-132">Requirement</span></span> | <span data-ttu-id="d8648-133">Valore</span><span class="sxs-lookup"><span data-stu-id="d8648-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8648-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d8648-134">Minimum supported client</span></span><br/> | <span data-ttu-id="d8648-135">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="d8648-135">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d8648-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d8648-136">Minimum supported server</span></span><br/> | <span data-ttu-id="d8648-137">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="d8648-137">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d8648-138">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="d8648-138">End of client support</span></span><br/>    | <span data-ttu-id="d8648-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d8648-139">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d8648-140">Prodotto</span><span class="sxs-lookup"><span data-stu-id="d8648-140">Product</span></span><br/>                  | <span data-ttu-id="d8648-141">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d8648-141">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d8648-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d8648-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8648-143"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8648-143"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d8648-144">IID</span><span class="sxs-lookup"><span data-stu-id="d8648-144">IID</span></span><br/>                      | <span data-ttu-id="d8648-145">IID \_ IVMVirtualMachine è definito come f7092aa1-33ed-4F78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="d8648-145">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="d8648-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d8648-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8648-147">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="d8648-147">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

