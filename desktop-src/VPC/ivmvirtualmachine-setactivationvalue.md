---
title: Metodo IVMVirtualMachine SetActivationValue (VPCCOMInterfaces. h)
description: Imposta il valore dell'impostazione di attivazione specificata per questa macchina virtuale.
ms.assetid: 6d664a80-1777-42ca-8454-df84c64ab505
keywords:
- Metodo SetActivationValue Virtual PC
- Metodo SetActivationValue Virtual PC, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC, metodo SetActivationValue
topic_type:
- apiref
api_name:
- IVMVirtualMachine.SetActivationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c7cb48b5691a9ca99a0fca5b696d8b545a40e46
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478334"
---
# <a name="ivmvirtualmachinesetactivationvalue-method"></a><span data-ttu-id="b5b7d-106">Metodo IVMVirtualMachine:: SetActivationValue</span><span class="sxs-lookup"><span data-stu-id="b5b7d-106">IVMVirtualMachine::SetActivationValue method</span></span>

<span data-ttu-id="b5b7d-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b5b7d-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b5b7d-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b5b7d-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b5b7d-109">Imposta il valore dell'impostazione di attivazione specificata per questa macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b5b7d-109">Sets the value of the specified activation setting for this virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5b7d-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b5b7d-110">Syntax</span></span>


```C++
HRESULT SetActivationValue(
  [in] BSTR    activationKey,
  [in] VARIANT activationValue
);
```



## <a name="parameters"></a><span data-ttu-id="b5b7d-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="b5b7d-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5b7d-112">*attivazione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b5b7d-112">*activationKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5b7d-113">Chiave utilizzata per identificare il valore di attivazione archiviato nel \* file ". vmc".</span><span class="sxs-lookup"><span data-stu-id="b5b7d-113">The key used to identify the activation value as stored in the "\*.vmc" file.</span></span>

</dd> <dt>

<span data-ttu-id="b5b7d-114">*activationValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b5b7d-114">*activationValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5b7d-115">Valore di attivazione.</span><span class="sxs-lookup"><span data-stu-id="b5b7d-115">The activation value.</span></span> <span data-ttu-id="b5b7d-116">Questo valore può essere uno dei tipi **Variant** seguenti: VT **\_ Array** VT \| **\_ Ui1** (byte non elaborati), **VT \_ BSTR** (String) **, VT \_ UI4** (Integer) o **VT \_ bool** (Boolean).</span><span class="sxs-lookup"><span data-stu-id="b5b7d-116">This value can be one of the following **VARIANT** types: **VT\_ARRAY**\|**VT\_UI1** (raw bytes), **VT\_BSTR** (string), **VT\_UI4** (integer), or **VT\_BOOL** (Boolean).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5b7d-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b5b7d-117">Return value</span></span>

<span data-ttu-id="b5b7d-118">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="b5b7d-118">This method can return one of these values.</span></span>



| <span data-ttu-id="b5b7d-119">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="b5b7d-119">Return code/value</span></span>                                                                                                                                                      | <span data-ttu-id="b5b7d-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b5b7d-120">Description</span></span>                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b5b7d-121"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b5b7d-121"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="b5b7d-122">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="b5b7d-122">The operation was successful.</span></span><br/>                                                                                       |
| <dl> <span data-ttu-id="b5b7d-123"><dt>**E \_**</dt> <dt>0x80000003</dt> INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="b5b7d-123"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>           | <span data-ttu-id="b5b7d-124">Il parametro *attivazione* è **null** o vuoto oppure il parametro *activationValue* non è un tipo Variant valido.</span><span class="sxs-lookup"><span data-stu-id="b5b7d-124">The *activationKey* parameter is **NULL** or empty, or the *activationValue* parameter is not a valid variant type.</span></span><br/> |
| <dl> <span data-ttu-id="b5b7d-125"><dt>**Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="b5b7d-125"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>      | <span data-ttu-id="b5b7d-126">La configurazione è sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="b5b7d-126">The configuration is unknown.</span></span><br/>                                                                                       |
| <dl> <span data-ttu-id="b5b7d-127"><dt>**Macchina virtuale \_ E \_ pref \_ non \_ trovato**</dt> <dt>0xA0040300</dt></span><span class="sxs-lookup"><span data-stu-id="b5b7d-127"><dt>**VM\_E\_PREF\_NOT\_FOUND**</dt> <dt>0xA0040300</dt></span></span> </dl> | <span data-ttu-id="b5b7d-128">La configurazione non ha un'attivazione valida.</span><span class="sxs-lookup"><span data-stu-id="b5b7d-128">The configuration has no valid activation.</span></span><br/>                                                                          |
| <dl> <span data-ttu-id="b5b7d-129"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="b5b7d-129"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="b5b7d-130">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="b5b7d-130">An unexpected error has occurred.</span></span><br/>                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="b5b7d-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="b5b7d-131">Remarks</span></span>

<span data-ttu-id="b5b7d-132">Questo metodo fornisce l'accesso di basso livello a qualsiasi valore di attivazione.</span><span class="sxs-lookup"><span data-stu-id="b5b7d-132">This method provides low-level access to any activation value.</span></span> <span data-ttu-id="b5b7d-133">Può essere usato per impostare i valori di attivazione per le chiavi definite dal cliente.</span><span class="sxs-lookup"><span data-stu-id="b5b7d-133">It can be used to set activation values for customer-defined keys.</span></span> <span data-ttu-id="b5b7d-134">Prestare attenzione se si utilizza questo metodo per impostare i valori di attivazione del sistema, poiché non viene eseguito alcun controllo degli errori sul valore di attivazione.</span><span class="sxs-lookup"><span data-stu-id="b5b7d-134">Be careful if you use this method to set system activation values, since no error checking is performed on the activation value.</span></span> <span data-ttu-id="b5b7d-135">Inoltre, alcuni valori di attivazione non possono essere modificati mentre la macchina virtuale è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="b5b7d-135">Also, some activation values cannot be changed while the virtual machine is running.</span></span> <span data-ttu-id="b5b7d-136">Quando viene avviata una macchina virtuale, viene creata una copia dei valori di configurazione, che diventa il set di valori di attivazione.</span><span class="sxs-lookup"><span data-stu-id="b5b7d-136">When a virtual machine is started, a copy is made of its configuration values, which becomes its set of activation values.</span></span> <span data-ttu-id="b5b7d-137">I valori di attivazione vengono mantenuti fino a quando la macchina virtuale non viene arrestata o riavviata.</span><span class="sxs-lookup"><span data-stu-id="b5b7d-137">Activation values are maintained until the virtual machine is shut down or restarted.</span></span> <span data-ttu-id="b5b7d-138">Si noti che Windows Virtual PC può utilizzare la configurazione solo per archiviare i valori per determinate chiavi, ovvero il valore di attivazione non può mai essere utilizzato.</span><span class="sxs-lookup"><span data-stu-id="b5b7d-138">Note that Windows Virtual PC may only use the configuration to store values for certain keys, that is, the activation value may never be used.</span></span>

> [!Note]  
> <span data-ttu-id="b5b7d-139">Per modificare i valori di attivazione, è necessario che la sessione della macchina virtuale sia in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="b5b7d-139">The virtual machine session must be running before any activation values can be changed.</span></span>

 

<span data-ttu-id="b5b7d-140">Le chiavi di attivazione sono archiviate internamente in modo gerarchico Analogamente alle chiavi del registro di sistema di Windows.</span><span class="sxs-lookup"><span data-stu-id="b5b7d-140">Activation keys are stored internally in a hierarchical manner similar to the registry keys in Windows.</span></span> <span data-ttu-id="b5b7d-141">Per specificare una sottochiave specifica, viene creato un "percorso della chiave" che specifica le varie chiavi in un formato delimitato da barre.</span><span class="sxs-lookup"><span data-stu-id="b5b7d-141">To specify a specific subkey, a "key path" is constructed which specifies the various keys in a slash mark delimited format.</span></span>

<span data-ttu-id="b5b7d-142">Ad esempio, per impostare il valore della \_ chiave "azione predefinita" situata nell'albero delle chiavi seguente:</span><span class="sxs-lookup"><span data-stu-id="b5b7d-142">For example, to set the value of the "default\_action" key located in the following key tree:</span></span>

``` syntax
<settings>
    <undo_drives>
        <default_action type="integer">1</default_action>
```

<span data-ttu-id="b5b7d-143">La stringa di percorso *attivazione* viene specificata come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="b5b7d-143">The *activationKey* path string would be specified as follows:</span></span>

``` syntax
"settings/undo_drives/default_action"
```

## <a name="requirements"></a><span data-ttu-id="b5b7d-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b5b7d-144">Requirements</span></span>



| <span data-ttu-id="b5b7d-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5b7d-145">Requirement</span></span> | <span data-ttu-id="b5b7d-146">Valore</span><span class="sxs-lookup"><span data-stu-id="b5b7d-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5b7d-147">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b5b7d-147">Minimum supported client</span></span><br/> | <span data-ttu-id="b5b7d-148">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b5b7d-148">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b5b7d-149">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b5b7d-149">Minimum supported server</span></span><br/> | <span data-ttu-id="b5b7d-150">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="b5b7d-150">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b5b7d-151">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="b5b7d-151">End of client support</span></span><br/>    | <span data-ttu-id="b5b7d-152">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b5b7d-152">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b5b7d-153">Prodotto</span><span class="sxs-lookup"><span data-stu-id="b5b7d-153">Product</span></span><br/>                  | <span data-ttu-id="b5b7d-154">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b5b7d-154">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b5b7d-155">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b5b7d-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5b7d-156"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5b7d-156"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b5b7d-157">IID</span><span class="sxs-lookup"><span data-stu-id="b5b7d-157">IID</span></span><br/>                      | <span data-ttu-id="b5b7d-158">IID \_ IVMVirtualMachine è definito come f7092aa1-33ed-4F78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="b5b7d-158">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="b5b7d-159">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b5b7d-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5b7d-160">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="b5b7d-160">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

