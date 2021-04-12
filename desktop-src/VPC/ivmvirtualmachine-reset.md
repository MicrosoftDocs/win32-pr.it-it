---
title: Metodo Reset IVMVirtualMachine (VPCCOMInterfaces. h)
description: Reimposta la macchina virtuale.
ms.assetid: 44daf6be-66ce-4291-a535-c30369eed60f
keywords:
- Reimposta il metodo Virtual PC
- Metodo Reset Virtual PC, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC, metodo Reset
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Reset
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45314eef6d837ac00647d477f3652b63221d977c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478346"
---
# <a name="ivmvirtualmachinereset-method"></a><span data-ttu-id="07d9e-106">Metodo IVMVirtualMachine:: Reset</span><span class="sxs-lookup"><span data-stu-id="07d9e-106">IVMVirtualMachine::Reset method</span></span>

<span data-ttu-id="07d9e-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="07d9e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="07d9e-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="07d9e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="07d9e-109">Reimposta la macchina virtuale (VM).</span><span class="sxs-lookup"><span data-stu-id="07d9e-109">Resets the virtual machine (VM).</span></span>

## <a name="syntax"></a><span data-ttu-id="07d9e-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="07d9e-110">Syntax</span></span>


```C++
HRESULT Reset(
  [out, retval] IVMTask **resetTask
);
```



## <a name="parameters"></a><span data-ttu-id="07d9e-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="07d9e-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07d9e-112">*resetTask* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="07d9e-112">*resetTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="07d9e-113">Oggetto [**IVMTask**](ivmtask.md) utilizzato per tenere traccia dello stato di avanzamento della sequenza di reimpostazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="07d9e-113">An [**IVMTask**](ivmtask.md) object that is used to track the completion progress of the VM's reset sequence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07d9e-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="07d9e-114">Return value</span></span>

<span data-ttu-id="07d9e-115">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="07d9e-115">This method can return one of these values.</span></span>



| <span data-ttu-id="07d9e-116">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="07d9e-116">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="07d9e-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="07d9e-117">Description</span></span>                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="07d9e-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="07d9e-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                | <span data-ttu-id="07d9e-119">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="07d9e-119">The operation was successful.</span></span><br/>                                     |
| <dl> <span data-ttu-id="07d9e-120"><dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="07d9e-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                  | <span data-ttu-id="07d9e-121">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="07d9e-121">The parameter is **NULL**.</span></span><br/>                                        |
| <dl> <span data-ttu-id="07d9e-122"><dt>**HRESULT \_ DA \_ Win32 ( \_ accesso errore \_ negato)**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="07d9e-122"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ACCESS\_DENIED)**</dt> <dt>0x80070005</dt></span></span> </dl> | <span data-ttu-id="07d9e-123">Il chiamante deve disporre delle autorizzazioni di accesso Execute per reimpostare questa macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="07d9e-123">The caller must have execute access permissions to reset this VM.</span></span><br/> |
| <dl> <span data-ttu-id="07d9e-124"><dt>**Macchina virtuale \_ \_VM E \_ non \_ in esecuzione**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="07d9e-124"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                     | <span data-ttu-id="07d9e-125">La macchina virtuale non è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="07d9e-125">The VM is not running.</span></span><br/>                                            |
| <dl> <span data-ttu-id="07d9e-126"><dt>**Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="07d9e-126"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                          | <span data-ttu-id="07d9e-127">La configurazione è sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="07d9e-127">The configuration is unknown.</span></span><br/>                                     |
| <dl> <span data-ttu-id="07d9e-128"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="07d9e-128"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                          | <span data-ttu-id="07d9e-129">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="07d9e-129">An unexpected error has occurred.</span></span><br/>                                 |



 

## <a name="requirements"></a><span data-ttu-id="07d9e-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="07d9e-130">Requirements</span></span>



| <span data-ttu-id="07d9e-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="07d9e-131">Requirement</span></span> | <span data-ttu-id="07d9e-132">Valore</span><span class="sxs-lookup"><span data-stu-id="07d9e-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="07d9e-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="07d9e-133">Minimum supported client</span></span><br/> | <span data-ttu-id="07d9e-134">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="07d9e-134">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="07d9e-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="07d9e-135">Minimum supported server</span></span><br/> | <span data-ttu-id="07d9e-136">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="07d9e-136">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="07d9e-137">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="07d9e-137">End of client support</span></span><br/>    | <span data-ttu-id="07d9e-138">Windows 7</span><span class="sxs-lookup"><span data-stu-id="07d9e-138">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="07d9e-139">Prodotto</span><span class="sxs-lookup"><span data-stu-id="07d9e-139">Product</span></span><br/>                  | <span data-ttu-id="07d9e-140">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="07d9e-140">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="07d9e-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="07d9e-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="07d9e-142"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="07d9e-142"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="07d9e-143">IID</span><span class="sxs-lookup"><span data-stu-id="07d9e-143">IID</span></span><br/>                      | <span data-ttu-id="07d9e-144">IID \_ IVMVirtualMachine è definito come f7092aa1-33ed-4F78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="07d9e-144">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="07d9e-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="07d9e-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07d9e-146">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="07d9e-146">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

