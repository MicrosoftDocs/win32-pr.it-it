---
title: Metodo IVMGuestOS IsUserLoggedOn (VPCCOMInterfaces. h)
description: Determina se la sessione richiesta è presente.
ms.assetid: 28035e30-023a-4ec2-88ef-43fe22f6d14e
keywords:
- Metodo IsUserLoggedOn Virtual PC
- Metodo IsUserLoggedOn Virtual PC, interfaccia IVMGuestOS
- Interfaccia IVMGuestOS Virtual PC, metodo IsUserLoggedOn
topic_type:
- apiref
api_name:
- IVMGuestOS.IsUserLoggedOn
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4eeb0482d7d3ac45b67a863948526b57d6c6e412
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301048"
---
# <a name="ivmguestosisuserloggedon-method"></a><span data-ttu-id="a73ab-106">Metodo IVMGuestOS:: IsUserLoggedOn</span><span class="sxs-lookup"><span data-stu-id="a73ab-106">IVMGuestOS::IsUserLoggedOn method</span></span>

<span data-ttu-id="a73ab-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a73ab-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a73ab-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a73ab-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a73ab-109">Determina se la sessione richiesta è presente.</span><span class="sxs-lookup"><span data-stu-id="a73ab-109">Determines whether the requested session is present.</span></span>

## <a name="syntax"></a><span data-ttu-id="a73ab-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a73ab-110">Syntax</span></span>


```C++
HRESULT IsUserLoggedOn(
  [in]          long         inRailSession,
  [out, retval] VARIANT_BOOL *outSessionPresent
);
```



## <a name="parameters"></a><span data-ttu-id="a73ab-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="a73ab-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a73ab-112">*inRailSession* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a73ab-112">*inRailSession* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a73ab-113">Impostare su 0 per una sessione binaria o 1 per una sessione RDP.</span><span class="sxs-lookup"><span data-stu-id="a73ab-113">Set to 0 for a Rail session or 1 for an RDP session.</span></span>

</dd> <dt>

<span data-ttu-id="a73ab-114">*outSessionPresent* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="a73ab-114">*outSessionPresent* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="a73ab-115">Impostare su **Variant \_ true** se la sessione è presente e **Variant \_ false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="a73ab-115">Set to **VARIANT\_TRUE** if the session is present and **VARIANT\_FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a73ab-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a73ab-116">Return value</span></span>

<span data-ttu-id="a73ab-117">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="a73ab-117">This method can return one of these values.</span></span>



| <span data-ttu-id="a73ab-118">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="a73ab-118">Return code/value</span></span>                                                                                                                                                                       | <span data-ttu-id="a73ab-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a73ab-119">Description</span></span>                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a73ab-120"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a73ab-120"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                             | <span data-ttu-id="a73ab-121">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="a73ab-121">The operation was successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="a73ab-122"><dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="a73ab-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                               | <span data-ttu-id="a73ab-123">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="a73ab-123">The parameter is **NULL**.</span></span><br/>                                      |
| <dl> <span data-ttu-id="a73ab-124"><dt>**E \_**</dt> <dt>0x80000003</dt> INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="a73ab-124"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                            | <span data-ttu-id="a73ab-125">Il parametro *outSessionPresent* non è valido o è **null**.</span><span class="sxs-lookup"><span data-stu-id="a73ab-125">The *outSessionPresent* parameter is not valid or is **NULL**.</span></span><br/>  |
| <dl> <span data-ttu-id="a73ab-126"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="a73ab-126"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                       | <span data-ttu-id="a73ab-127">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="a73ab-127">An unexpected error has occurred.</span></span><br/>                               |
| <dl> <span data-ttu-id="a73ab-128"><dt>**HRESULT \_ DA \_ Win32 (Error \_ OutOfMemory)**</dt> <dt>0x8007000e</dt></span><span class="sxs-lookup"><span data-stu-id="a73ab-128"><dt>**HRESULT\_FROM\_WIN32(ERROR\_OUTOFMEMORY)**</dt> <dt>0x8007000e</dt></span></span> </dl> | <span data-ttu-id="a73ab-129">La memoria disponibile non è sufficiente per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="a73ab-129">There is not enough memory available to complete this request.</span></span><br/>  |
| <dl> <span data-ttu-id="a73ab-130"><dt>**Macchina virtuale \_ E \_ timeout \_**</dt> <dt>0xA0040202</dt></span><span class="sxs-lookup"><span data-stu-id="a73ab-130"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                        | <span data-ttu-id="a73ab-131">L'operazione non è stata completata in modo tempestivo.</span><span class="sxs-lookup"><span data-stu-id="a73ab-131">The operation did not complete in a timely manner.</span></span><br/>              |
| <dl> <span data-ttu-id="a73ab-132"><dt>**Macchina virtuale \_ \_VM E \_ non \_ in esecuzione**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="a73ab-132"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                  | <span data-ttu-id="a73ab-133">Per questa operazione è necessario che la macchina virtuale (VM) sia in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="a73ab-133">The virtual machine (VM) must be running for this operation.</span></span><br/>    |
| <dl> <span data-ttu-id="a73ab-134"><dt>**Macchina virtuale \_ E \_ funzionalità aggiuntive \_ \_ non \_ disponibili**</dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="a73ab-134"><dt>**VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL**</dt> <dt>0xA0040505</dt></span></span> </dl>    | <span data-ttu-id="a73ab-135">La funzionalità componenti di integrazione non è installata in questa macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a73ab-135">The integration components feature is not installed in this VM.</span></span><br/> |
| <dl> <span data-ttu-id="a73ab-136"><dt>**Macchina virtuale \_ 0xA00400507 \_ macchina virtuale E \_ sospesa**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="a73ab-136"><dt>**VM\_E\_VM\_PAUSED**</dt> <dt>0xA00400507</dt></span></span> </dl>                       | <span data-ttu-id="a73ab-137">La macchina virtuale è sospesa.</span><span class="sxs-lookup"><span data-stu-id="a73ab-137">The VM is paused.</span></span><br/>                                               |



 

## <a name="requirements"></a><span data-ttu-id="a73ab-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a73ab-138">Requirements</span></span>



| <span data-ttu-id="a73ab-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="a73ab-139">Requirement</span></span> | <span data-ttu-id="a73ab-140">Valore</span><span class="sxs-lookup"><span data-stu-id="a73ab-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a73ab-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a73ab-141">Minimum supported client</span></span><br/> | <span data-ttu-id="a73ab-142">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="a73ab-142">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a73ab-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a73ab-143">Minimum supported server</span></span><br/> | <span data-ttu-id="a73ab-144">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a73ab-144">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="a73ab-145">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="a73ab-145">End of client support</span></span><br/>    | <span data-ttu-id="a73ab-146">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a73ab-146">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a73ab-147">Prodotto</span><span class="sxs-lookup"><span data-stu-id="a73ab-147">Product</span></span><br/>                  | <span data-ttu-id="a73ab-148">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a73ab-148">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="a73ab-149">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a73ab-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="a73ab-150"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="a73ab-150"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="a73ab-151">IID</span><span class="sxs-lookup"><span data-stu-id="a73ab-151">IID</span></span><br/>                      | <span data-ttu-id="a73ab-152">IID \_ IVMGuestOS è definito come 99fea0db-4880-499a-B6D8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="a73ab-152">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="a73ab-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a73ab-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a73ab-154">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="a73ab-154">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

