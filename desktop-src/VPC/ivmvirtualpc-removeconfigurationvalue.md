---
title: Metodo IVMVirtualPC RemoveConfigurationValue (VPCCOMInterfaces. h)
description: Rimuove il valore dell'impostazione di configurazione specificata.
ms.assetid: 07bafa5e-bf62-45bf-af4e-a66050f5afad
keywords:
- Metodo RemoveConfigurationValue Virtual PC
- Metodo RemoveConfigurationValue Virtual PC, interfaccia IVMVirtualPC
- Interfaccia IVMVirtualPC Virtual PC, metodo RemoveConfigurationValue
topic_type:
- apiref
api_name:
- IVMVirtualPC.RemoveConfigurationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73821657ed7983e2d92fc379c3222f343763b3ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874281"
---
# <a name="ivmvirtualpcremoveconfigurationvalue-method"></a><span data-ttu-id="9d6db-106">Metodo IVMVirtualPC:: RemoveConfigurationValue</span><span class="sxs-lookup"><span data-stu-id="9d6db-106">IVMVirtualPC::RemoveConfigurationValue method</span></span>

<span data-ttu-id="9d6db-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="9d6db-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="9d6db-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="9d6db-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="9d6db-109">Rimuove il valore dell'impostazione di configurazione specificata.</span><span class="sxs-lookup"><span data-stu-id="9d6db-109">Removes the value of the specified configuration setting.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d6db-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9d6db-110">Syntax</span></span>


```C++
HRESULT RemoveConfigurationValue(
  [in] BSTR preferenceKey
);
```



## <a name="parameters"></a><span data-ttu-id="9d6db-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="9d6db-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d6db-112">*preferenceKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9d6db-112">*preferenceKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d6db-113">Chiave utilizzata per identificare la preferenza, archiviata nel file di configurazione.</span><span class="sxs-lookup"><span data-stu-id="9d6db-113">The key used to identify the preference, as stored in the configuration file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d6db-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9d6db-114">Return value</span></span>

<span data-ttu-id="9d6db-115">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="9d6db-115">This method can return one of these values.</span></span>



| <span data-ttu-id="9d6db-116">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="9d6db-116">Return code/value</span></span>                                                                                                                                                                        | <span data-ttu-id="9d6db-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9d6db-117">Description</span></span>                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9d6db-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="9d6db-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="9d6db-119">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="9d6db-119">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="9d6db-120"><dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="9d6db-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="9d6db-121">Il parametro *preferenceKey* è **null**.</span><span class="sxs-lookup"><span data-stu-id="9d6db-121">The *preferenceKey* parameter is **NULL**.</span></span><br/>                                           |
| <dl> <span data-ttu-id="9d6db-122"><dt>**E \_**</dt> <dt>0x80000003</dt> INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="9d6db-122"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                             | <span data-ttu-id="9d6db-123">Il parametro *preferenceKey* non è valido o è una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="9d6db-123">The *preferenceKey* parameter is not valid or is an empty string.</span></span><br/>                    |
| <dl> <span data-ttu-id="9d6db-124"><dt>**Macchina virtuale \_ E \_ pref \_ non \_ trovato**</dt> <dt>0xA0040300</dt></span><span class="sxs-lookup"><span data-stu-id="9d6db-124"><dt>**VM\_E\_PREF\_NOT\_FOUND**</dt> <dt>0xA0040300</dt></span></span> </dl>                   | <span data-ttu-id="9d6db-125">La preferenza non è stata trovata.</span><span class="sxs-lookup"><span data-stu-id="9d6db-125">The preference was not found.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="9d6db-126"><dt>**Macchina virtuale \_ E \_ \_ virtualizzazione hardware \_ disabilitato**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="9d6db-126"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="9d6db-127">Il processore non supporta le estensioni di virtualizzazione accelerata hardware (HAV).</span><span class="sxs-lookup"><span data-stu-id="9d6db-127">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |
| <dl> <span data-ttu-id="9d6db-128"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="9d6db-128"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="9d6db-129">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="9d6db-129">An unexpected error has occurred.</span></span><br/>                                                    |



 

## <a name="remarks"></a><span data-ttu-id="9d6db-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="9d6db-130">Remarks</span></span>

<span data-ttu-id="9d6db-131">Questo metodo fornisce accesso di basso livello a qualsiasi valore di preferenza per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="9d6db-131">This method provides low-level access to any preference value for the current user.</span></span> <span data-ttu-id="9d6db-132">Può essere usato per rimuovere i valori di preferenza per le chiavi definite dal cliente.</span><span class="sxs-lookup"><span data-stu-id="9d6db-132">It can be used to remove preference values for customer-defined keys.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d6db-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9d6db-133">Requirements</span></span>



| <span data-ttu-id="9d6db-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d6db-134">Requirement</span></span> | <span data-ttu-id="9d6db-135">Valore</span><span class="sxs-lookup"><span data-stu-id="9d6db-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d6db-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9d6db-136">Minimum supported client</span></span><br/> | <span data-ttu-id="9d6db-137">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="9d6db-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9d6db-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9d6db-138">Minimum supported server</span></span><br/> | <span data-ttu-id="9d6db-139">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="9d6db-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="9d6db-140">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="9d6db-140">End of client support</span></span><br/>    | <span data-ttu-id="9d6db-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9d6db-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="9d6db-142">Prodotto</span><span class="sxs-lookup"><span data-stu-id="9d6db-142">Product</span></span><br/>                  | <span data-ttu-id="9d6db-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="9d6db-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="9d6db-144">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9d6db-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d6db-145"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d6db-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="9d6db-146">IID</span><span class="sxs-lookup"><span data-stu-id="9d6db-146">IID</span></span><br/>                      | <span data-ttu-id="9d6db-147">IID \_ IVMVirtualPC è definito come 236ba0d9-A24A-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="9d6db-147">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="9d6db-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9d6db-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d6db-149">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="9d6db-149">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

