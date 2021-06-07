---
title: Metodo GetParameter IVMGuestOS (VPCCOMInterfaces.h)
description: Recupera un parametro denominato all'interno del sistema operativo guest.
ms.assetid: d4d5acbd-fa19-4eb2-af75-2c94e5f6f7f0
keywords:
- Metodo GetParameter Virtual PC
- Metodo GetParameter Virtual PC, interfaccia IVMGuestOS
- Interfaccia IVMGuestOS Virtual PC, metodo GetParameter
topic_type:
- apiref
api_name:
- IVMGuestOS.GetParameter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d12bddec3fac5dc918f06d926fe5e5656b70d84d
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387647"
---
# <a name="ivmguestosgetparameter-method"></a><span data-ttu-id="31b54-106">Metodo IVMGuestOS::GetParameter</span><span class="sxs-lookup"><span data-stu-id="31b54-106">IVMGuestOS::GetParameter method</span></span>

<span data-ttu-id="31b54-107">\[Virtual PC Windows non è più disponibile per l'uso a Windows 8.</span><span class="sxs-lookup"><span data-stu-id="31b54-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="31b54-108">Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]</span><span class="sxs-lookup"><span data-stu-id="31b54-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="31b54-109">Recupera un parametro denominato all'interno del sistema operativo guest.</span><span class="sxs-lookup"><span data-stu-id="31b54-109">Retrieves a named parameter within the guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="31b54-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="31b54-110">Syntax</span></span>


```C++
HRESULT GetParameter(
  [in]          BSTR inParameterName,
  [out, retval] BSTR *outParameterValue
);
```



## <a name="parameters"></a><span data-ttu-id="31b54-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="31b54-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31b54-112">*inParameterName* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="31b54-112">*inParameterName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31b54-113">Nome del parametro.</span><span class="sxs-lookup"><span data-stu-id="31b54-113">The parameter name.</span></span> <span data-ttu-id="31b54-114">Deve avere una lunghezza compresa tra 1 e 255 caratteri e non può contenere una barra rovesciata ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="31b54-114">It must be between 1 and 255 characters in length and cannot contain a backslash (\\) character.</span></span>

</dd> <dt>

<span data-ttu-id="31b54-115">*outParameterValue* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="31b54-115">*outParameterValue* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="31b54-116">Valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="31b54-116">The parameter value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31b54-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="31b54-117">Return value</span></span>

<span data-ttu-id="31b54-118">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="31b54-118">This method can return one of these values.</span></span>



| <span data-ttu-id="31b54-119">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="31b54-119">Return code/value</span></span>                                                                                                                                                                    | <span data-ttu-id="31b54-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="31b54-120">Description</span></span>                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="31b54-121"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="31b54-121"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="31b54-122">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="31b54-122">The operation was successful.</span></span><br/>                                     |
| <dl> <span data-ttu-id="31b54-123"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="31b54-123"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                         | <span data-ttu-id="31b54-124">Parametro non valido o non specificato.</span><span class="sxs-lookup"><span data-stu-id="31b54-124">A parameter is not valid or not specified.</span></span><br/>                        |
| <dl> <span data-ttu-id="31b54-125"><dt>**E \_ Puntatore**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="31b54-125"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="31b54-126">Il parametro è **NULL.**</span><span class="sxs-lookup"><span data-stu-id="31b54-126">The parameter is **NULL**.</span></span><br/>                                        |
| <dl> <span data-ttu-id="31b54-127"><dt>**Macchina virtuale \_ E \_ TIMEOUT \_ 0xA0040202**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="31b54-127"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                     | <span data-ttu-id="31b54-128">L'operazione non è stata completata in modo corretto.</span><span class="sxs-lookup"><span data-stu-id="31b54-128">The operation did not complete in a timely manner.</span></span><br/>                |
| <dl> <span data-ttu-id="31b54-129"><dt>**Macchina virtuale \_ E \_ VM \_ NOT \_ RUNNING**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="31b54-129"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="31b54-130">La macchina virtuale non è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="31b54-130">The virtual machine is not running.</span></span><br/>                               |
| <dl> <span data-ttu-id="31b54-131"><dt>**Macchina virtuale \_ E \_ MACCHINA \_ VIRTUALE SOSPESA**</dt> <dt>0XA00400507</dt></span><span class="sxs-lookup"><span data-stu-id="31b54-131"><dt>**VM\_E\_VM\_PAUSED**</dt> <dt>0xA00400507</dt></span></span> </dl>                    | <span data-ttu-id="31b54-132">La macchina virtuale è sospesa.</span><span class="sxs-lookup"><span data-stu-id="31b54-132">The virtual machine is paused.</span></span><br/>                                    |
| <dl> <span data-ttu-id="31b54-133"><dt>**Macchina virtuale \_ E \_ ADDITIONS \_ FEATURE NOT \_ \_ AVAIL**</dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="31b54-133"><dt>**VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL**</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="31b54-134">I componenti di integrazione non vengono installati in questa macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="31b54-134">Integration components are not installed in this virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="31b54-135"><dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="31b54-135"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="31b54-136">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="31b54-136">An unexpected error has occurred.</span></span><br/>                                 |



 

## <a name="remarks"></a><span data-ttu-id="31b54-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="31b54-137">Remarks</span></span>

<span data-ttu-id="31b54-138">La macchina virtuale deve essere in esecuzione e i componenti di integrazione devono essere installati quando viene richiamato questo metodo.</span><span class="sxs-lookup"><span data-stu-id="31b54-138">The virtual machine must be running and integration components must be installed when this method is invoked.</span></span> <span data-ttu-id="31b54-139">Questo metodo è supportato solo per i sistemi operativi guest basati su Windows.</span><span class="sxs-lookup"><span data-stu-id="31b54-139">This method is only supported for Windows-based guest operating systems.</span></span>

<span data-ttu-id="31b54-140">Con i componenti di integrazione installati, la chiave seguente viene aggiunta automaticamente al Registro di sistema del sistema operativo guest:</span><span class="sxs-lookup"><span data-stu-id="31b54-140">With integration components installed, the following key is automatically added to the guest operating system's registry:</span></span>

<span data-ttu-id="31b54-141">**HKEY \_ LOCAL MACHINE SOFTWARE Parametri guest macchina virtuale \_ \\ \\ \\ \\ \\ Microsoft**</span><span class="sxs-lookup"><span data-stu-id="31b54-141">**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Virtual Machine\\Guest\\Parameters**</span></span>

<span data-ttu-id="31b54-142">All'avvio del sistema operativo guest, i valori di stringa del Registro di sistema seguenti vengono popolati nella **chiave Parameters:**</span><span class="sxs-lookup"><span data-stu-id="31b54-142">When the guest operating system starts, the following registry string values are populated in the **Parameters** key:</span></span>

-   <span data-ttu-id="31b54-143">**HostName**</span><span class="sxs-lookup"><span data-stu-id="31b54-143">**HostName**</span></span>
-   <span data-ttu-id="31b54-144">**PhysicalHostName**</span><span class="sxs-lookup"><span data-stu-id="31b54-144">**PhysicalHostName**</span></span>
-   <span data-ttu-id="31b54-145">**PhysicalHostNameFullyQualified**</span><span class="sxs-lookup"><span data-stu-id="31b54-145">**PhysicalHostNameFullyQualified**</span></span>
-   <span data-ttu-id="31b54-146">**VirtualMachineName**</span><span class="sxs-lookup"><span data-stu-id="31b54-146">**VirtualMachineName**</span></span>

## <a name="requirements"></a><span data-ttu-id="31b54-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="31b54-147">Requirements</span></span>



| <span data-ttu-id="31b54-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="31b54-148">Requirement</span></span> | <span data-ttu-id="31b54-149">Valore</span><span class="sxs-lookup"><span data-stu-id="31b54-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="31b54-150">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="31b54-150">Minimum supported client</span></span><br/> | <span data-ttu-id="31b54-151">Solo app desktop di Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="31b54-151">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="31b54-152">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="31b54-152">Minimum supported server</span></span><br/> | <span data-ttu-id="31b54-153">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="31b54-153">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="31b54-154">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="31b54-154">End of client support</span></span><br/>    | <span data-ttu-id="31b54-155">Windows 7</span><span class="sxs-lookup"><span data-stu-id="31b54-155">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="31b54-156">Prodotto</span><span class="sxs-lookup"><span data-stu-id="31b54-156">Product</span></span><br/>                  | <span data-ttu-id="31b54-157">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="31b54-157">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="31b54-158">Intestazione</span><span class="sxs-lookup"><span data-stu-id="31b54-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="31b54-159"><dt>VPCCOMInterfaces.h</dt></span><span class="sxs-lookup"><span data-stu-id="31b54-159"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="31b54-160">IID</span><span class="sxs-lookup"><span data-stu-id="31b54-160">IID</span></span><br/>                      | <span data-ttu-id="31b54-161">IID IVMGuestOS è definito come \_ 99fea0db-4880-499a-b6d8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="31b54-161">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="31b54-162">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="31b54-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31b54-163">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="31b54-163">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

