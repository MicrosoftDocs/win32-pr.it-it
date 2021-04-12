---
title: Metodo IVMVirtualMachine GetActivationValue (VPCCOMInterfaces. h)
description: Recupera il valore dell'impostazione di attivazione specificata per questa macchina virtuale.
ms.assetid: 9a6f138f-6a8a-4cdf-8fb3-83d541d88fba
keywords:
- Metodo GetActivationValue Virtual PC
- Metodo GetActivationValue Virtual PC, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC, metodo GetActivationValue
topic_type:
- apiref
api_name:
- IVMVirtualMachine.GetActivationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e87b51e34feb654fa9c5ab00ed7906268cdc9ec3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340313"
---
# <a name="ivmvirtualmachinegetactivationvalue-method"></a><span data-ttu-id="245fe-106">Metodo IVMVirtualMachine:: GetActivationValue</span><span class="sxs-lookup"><span data-stu-id="245fe-106">IVMVirtualMachine::GetActivationValue method</span></span>

<span data-ttu-id="245fe-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="245fe-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="245fe-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="245fe-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="245fe-109">Recupera il valore dell'impostazione di attivazione specificata per questa macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="245fe-109">Retrieves the value of the specified activation setting for this virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="245fe-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="245fe-110">Syntax</span></span>


```C++
HRESULT GetActivationValue(
  [in]          BSTR    activationKey,
  [out, retval] VARIANT *activationValue
);
```



## <a name="parameters"></a><span data-ttu-id="245fe-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="245fe-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="245fe-112">*attivazione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="245fe-112">*activationKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="245fe-113">Chiave utilizzata per identificare il valore di attivazione archiviato nel \* file ". vmc".</span><span class="sxs-lookup"><span data-stu-id="245fe-113">The key used to identify the activation value as stored in the "\*.vmc" file.</span></span>

</dd> <dt>

<span data-ttu-id="245fe-114">*activationValue* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="245fe-114">*activationValue* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="245fe-115">Valore di attivazione.</span><span class="sxs-lookup"><span data-stu-id="245fe-115">The activation value.</span></span> <span data-ttu-id="245fe-116">Questo valore può essere uno dei tipi **Variant** seguenti: VT **\_ Array** VT \| **\_ Ui1** (byte non elaborati), **VT \_ BSTR** (String) **, VT \_ I4** (Integer) o **VT \_ bool** (Boolean).</span><span class="sxs-lookup"><span data-stu-id="245fe-116">This value can be one of the following **VARIANT** types: **VT\_ARRAY** \| **VT\_UI1** (raw bytes), **VT\_BSTR** (string), **VT\_I4** (integer), or **VT\_BOOL** (Boolean).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="245fe-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="245fe-117">Return value</span></span>

<span data-ttu-id="245fe-118">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="245fe-118">This method can return one of these values.</span></span>



| <span data-ttu-id="245fe-119">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="245fe-119">Return code/value</span></span>                                                                                                                                                      | <span data-ttu-id="245fe-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="245fe-120">Description</span></span>                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="245fe-121"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="245fe-121"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="245fe-122">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="245fe-122">The operation was successful.</span></span><br/>                                                |
| <dl> <span data-ttu-id="245fe-123"><dt>**E \_**</dt> <dt>0x80000003</dt> INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="245fe-123"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>           | <span data-ttu-id="245fe-124">Il parametro *attivazione* è **null** o vuoto.</span><span class="sxs-lookup"><span data-stu-id="245fe-124">The *activationKey* parameter is **NULL** or empty.</span></span><br/>                          |
| <dl> <span data-ttu-id="245fe-125"><dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="245fe-125"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>              | <span data-ttu-id="245fe-126">Il parametro *activationValue* è **null**.</span><span class="sxs-lookup"><span data-stu-id="245fe-126">The *activationValue* parameter is **NULL**.</span></span><br/>                                 |
| <dl> <span data-ttu-id="245fe-127"><dt>**Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="245fe-127"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>      | <span data-ttu-id="245fe-128">La configurazione è sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="245fe-128">The configuration is unknown.</span></span><br/>                                                |
| <dl> <span data-ttu-id="245fe-129"><dt>**Macchina virtuale \_ E \_ pref \_ non \_ trovato**</dt> <dt>0xA0040300</dt></span><span class="sxs-lookup"><span data-stu-id="245fe-129"><dt>**VM\_E\_PREF\_NOT\_FOUND**</dt> <dt>0xA0040300</dt></span></span> </dl> | <span data-ttu-id="245fe-130">La preferenza non è stata trovata o questa configurazione non ha un'attivazione valida.</span><span class="sxs-lookup"><span data-stu-id="245fe-130">The preference was not found, or this configuration has no valid activation.</span></span><br/> |
| <dl> <span data-ttu-id="245fe-131"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="245fe-131"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="245fe-132">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="245fe-132">An unexpected error has occurred.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="245fe-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="245fe-133">Remarks</span></span>

<span data-ttu-id="245fe-134">Questo metodo fornisce l'accesso di basso livello a qualsiasi valore di attivazione.</span><span class="sxs-lookup"><span data-stu-id="245fe-134">This method provides low-level access to any activation value.</span></span> <span data-ttu-id="245fe-135">Può essere usato per impostare i valori di attivazione per le chiavi definite dal cliente.</span><span class="sxs-lookup"><span data-stu-id="245fe-135">It can be used to set activation values for customer-defined keys.</span></span> <span data-ttu-id="245fe-136">Quando viene avviata una macchina virtuale, viene creata una copia dei valori di configurazione, che diventa il set di valori di attivazione.</span><span class="sxs-lookup"><span data-stu-id="245fe-136">When a virtual machine is started, a copy is made of its configuration values, which becomes its set of activation values.</span></span> <span data-ttu-id="245fe-137">I valori di attivazione vengono mantenuti fino a quando la macchina virtuale non viene arrestata o riavviata.</span><span class="sxs-lookup"><span data-stu-id="245fe-137">Activation values are maintained until the virtual machine is shut down or restarted.</span></span> <span data-ttu-id="245fe-138">Si noti che Windows Virtual PC può utilizzare la configurazione solo per archiviare i valori per determinate chiavi, ovvero il valore di attivazione non può mai essere utilizzato.</span><span class="sxs-lookup"><span data-stu-id="245fe-138">Note that Windows Virtual PC may only use the configuration to store values for certain keys, that is, the activation value may never be used.</span></span>

<span data-ttu-id="245fe-139">Le chiavi di attivazione sono archiviate internamente in modo gerarchico Analogamente alle chiavi del registro di sistema di Windows.</span><span class="sxs-lookup"><span data-stu-id="245fe-139">Activation keys are stored internally in a hierarchical manner similar to the registry keys in Windows.</span></span> <span data-ttu-id="245fe-140">Per specificare una sottochiave specifica, viene creato un "percorso della chiave" che specifica le varie chiavi in un formato delimitato da barre.</span><span class="sxs-lookup"><span data-stu-id="245fe-140">To specify a specific subkey, a "key path" is constructed which specifies the various keys in a slash mark delimited format.</span></span>

<span data-ttu-id="245fe-141">Ad esempio, per leggere il valore della \_ chiave "azione predefinita" situata nell'albero delle chiavi seguente:</span><span class="sxs-lookup"><span data-stu-id="245fe-141">For example, to read the value of the "default\_action" key located in the following key tree:</span></span>

``` syntax
<settings>
    <undo_drives>
        <default_action type="integer">1</default_action>
```

<span data-ttu-id="245fe-142">La stringa di percorso *attivazione* viene specificata come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="245fe-142">The *activationKey* path string would be specified as follows:</span></span>

``` syntax
"settings/undo_drives/default_action"
```

## <a name="requirements"></a><span data-ttu-id="245fe-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="245fe-143">Requirements</span></span>



| <span data-ttu-id="245fe-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="245fe-144">Requirement</span></span> | <span data-ttu-id="245fe-145">Valore</span><span class="sxs-lookup"><span data-stu-id="245fe-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="245fe-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="245fe-146">Minimum supported client</span></span><br/> | <span data-ttu-id="245fe-147">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="245fe-147">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="245fe-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="245fe-148">Minimum supported server</span></span><br/> | <span data-ttu-id="245fe-149">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="245fe-149">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="245fe-150">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="245fe-150">End of client support</span></span><br/>    | <span data-ttu-id="245fe-151">Windows 7</span><span class="sxs-lookup"><span data-stu-id="245fe-151">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="245fe-152">Prodotto</span><span class="sxs-lookup"><span data-stu-id="245fe-152">Product</span></span><br/>                  | <span data-ttu-id="245fe-153">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="245fe-153">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="245fe-154">Intestazione</span><span class="sxs-lookup"><span data-stu-id="245fe-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="245fe-155"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="245fe-155"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="245fe-156">IID</span><span class="sxs-lookup"><span data-stu-id="245fe-156">IID</span></span><br/>                      | <span data-ttu-id="245fe-157">IID \_ IVMVirtualMachine è definito come f7092aa1-33ed-4F78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="245fe-157">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="245fe-158">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="245fe-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="245fe-159">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="245fe-159">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

