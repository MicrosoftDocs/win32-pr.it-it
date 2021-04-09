---
title: Metodo IVMVirtualPC GetConfigurationValue (VPCCOMInterfaces. h)
description: Recupera il valore dell'impostazione di configurazione specificata.
ms.assetid: 4598b57c-9942-4b40-97b5-41ad9ec74bfa
keywords:
- Metodo GetConfigurationValue Virtual PC
- Metodo GetConfigurationValue Virtual PC, interfaccia IVMVirtualPC
- Interfaccia IVMVirtualPC Virtual PC, metodo GetConfigurationValue
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetConfigurationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11851e2dc2e51c0dc5eed876fc755655ed488554
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120783"
---
# <a name="ivmvirtualpcgetconfigurationvalue-method"></a><span data-ttu-id="81071-106">Metodo IVMVirtualPC:: GetConfigurationValue</span><span class="sxs-lookup"><span data-stu-id="81071-106">IVMVirtualPC::GetConfigurationValue method</span></span>

<span data-ttu-id="81071-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="81071-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="81071-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="81071-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="81071-109">Recupera il valore dell'impostazione di configurazione specificata.</span><span class="sxs-lookup"><span data-stu-id="81071-109">Retrieves the value of the specified configuration setting.</span></span>

## <a name="syntax"></a><span data-ttu-id="81071-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="81071-110">Syntax</span></span>


```C++
HRESULT GetConfigurationValue(
  [in]          BSTR    preferenceKey,
  [out, retval] VARIANT *preferenceValue
);
```



## <a name="parameters"></a><span data-ttu-id="81071-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="81071-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81071-112">*preferenceKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="81071-112">*preferenceKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81071-113">Chiave utilizzata per identificare la preferenza, archiviata nel file di configurazione.</span><span class="sxs-lookup"><span data-stu-id="81071-113">The key used to identify the preference, as stored in the configuration file.</span></span>

</dd> <dt>

<span data-ttu-id="81071-114">*preferenceValue* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="81071-114">*preferenceValue* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="81071-115">Valore di preferenza.</span><span class="sxs-lookup"><span data-stu-id="81071-115">The preference value.</span></span> <span data-ttu-id="81071-116">Questo parametro può essere uno dei tipi **Variant** seguenti: VT **\_ Array** VT \| **\_ Ui1** (byte non elaborati), **VT \_ BSTR** (String) **, VT \_ I4** (Integer) o **VT \_ bool** (Boolean).</span><span class="sxs-lookup"><span data-stu-id="81071-116">This parameter may be one of the following **VARIANT** types: **VT\_ARRAY**\|**VT\_UI1** (raw bytes), **VT\_BSTR** (string), **VT\_I4** (integer), or **VT\_BOOL** (Boolean).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81071-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="81071-117">Return value</span></span>

<span data-ttu-id="81071-118">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="81071-118">This method can return one of these values.</span></span>



| <span data-ttu-id="81071-119">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="81071-119">Return code/value</span></span>                                                                                                                                                                        | <span data-ttu-id="81071-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="81071-120">Description</span></span>                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="81071-121"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="81071-121"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="81071-122">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="81071-122">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="81071-123"><dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="81071-123"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="81071-124">Il parametro *preferenceKey* o *preferenceValue* è **null**.</span><span class="sxs-lookup"><span data-stu-id="81071-124">The *preferenceKey* or *preferenceValue* parameter is **NULL**.</span></span><br/>                      |
| <dl> <span data-ttu-id="81071-125"><dt>**Macchina virtuale \_ E \_ pref \_ non \_ trovato**</dt> <dt>0xa0040300</dt></span><span class="sxs-lookup"><span data-stu-id="81071-125"><dt>**VM\_E\_PREF\_NOT\_FOUND**</dt> <dt>0xa0040300</dt></span></span> </dl>                   | <span data-ttu-id="81071-126">La preferenza non è stata trovata.</span><span class="sxs-lookup"><span data-stu-id="81071-126">The preference was not found.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="81071-127"><dt>**Macchina virtuale \_ E \_ \_ virtualizzazione hardware \_ disabilitato**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="81071-127"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="81071-128">Il processore non supporta le estensioni di virtualizzazione accelerata hardware (HAV).</span><span class="sxs-lookup"><span data-stu-id="81071-128">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |
| <dl> <span data-ttu-id="81071-129"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="81071-129"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="81071-130">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="81071-130">An unexpected error has occurred.</span></span><br/>                                                    |



 

## <a name="remarks"></a><span data-ttu-id="81071-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="81071-131">Remarks</span></span>

<span data-ttu-id="81071-132">Questo metodo fornisce accesso di basso livello a qualsiasi valore di preferenza per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="81071-132">This method provides low-level access to any preference value for the current user.</span></span> <span data-ttu-id="81071-133">Può essere usato per recuperare i valori di preferenza per le chiavi definite dal cliente.</span><span class="sxs-lookup"><span data-stu-id="81071-133">It can be used to retrieve preference values for customer-defined keys.</span></span>

## <a name="requirements"></a><span data-ttu-id="81071-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="81071-134">Requirements</span></span>



| <span data-ttu-id="81071-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="81071-135">Requirement</span></span> | <span data-ttu-id="81071-136">Valore</span><span class="sxs-lookup"><span data-stu-id="81071-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="81071-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="81071-137">Minimum supported client</span></span><br/> | <span data-ttu-id="81071-138">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="81071-138">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="81071-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="81071-139">Minimum supported server</span></span><br/> | <span data-ttu-id="81071-140">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="81071-140">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="81071-141">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="81071-141">End of client support</span></span><br/>    | <span data-ttu-id="81071-142">Windows 7</span><span class="sxs-lookup"><span data-stu-id="81071-142">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="81071-143">Prodotto</span><span class="sxs-lookup"><span data-stu-id="81071-143">Product</span></span><br/>                  | <span data-ttu-id="81071-144">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="81071-144">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="81071-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="81071-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="81071-146"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="81071-146"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="81071-147">IID</span><span class="sxs-lookup"><span data-stu-id="81071-147">IID</span></span><br/>                      | <span data-ttu-id="81071-148">IID \_ IVMVirtualPC è definito come 236ba0d9-A24A-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="81071-148">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="81071-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="81071-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81071-150">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="81071-150">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

