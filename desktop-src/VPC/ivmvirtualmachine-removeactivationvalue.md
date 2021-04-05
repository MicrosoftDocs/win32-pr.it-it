---
title: Metodo IVMVirtualMachine RemoveActivationValue (VPCCOMInterfaces. h)
description: Rimuove il valore dell'impostazione di attivazione specificata per questa macchina virtuale.
ms.assetid: 8e9b9d95-aec9-4b73-afc3-cd0d7300f40f
keywords:
- Metodo RemoveActivationValue Virtual PC
- Metodo RemoveActivationValue Virtual PC, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC, metodo RemoveActivationValue
topic_type:
- apiref
api_name:
- IVMVirtualMachine.RemoveActivationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b0461b27e43066f32c25663e3b38dab9b3b71b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048457"
---
# <a name="ivmvirtualmachineremoveactivationvalue-method"></a><span data-ttu-id="a3120-106">Metodo IVMVirtualMachine:: RemoveActivationValue</span><span class="sxs-lookup"><span data-stu-id="a3120-106">IVMVirtualMachine::RemoveActivationValue method</span></span>

<span data-ttu-id="a3120-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a3120-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a3120-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a3120-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a3120-109">Rimuove il valore dell'impostazione di attivazione specificata per questa macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a3120-109">Removes the value of the specified activation setting for this virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3120-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a3120-110">Syntax</span></span>


```C++
HRESULT RemoveActivationValue(
  [in] BSTR activationKey
);
```



## <a name="parameters"></a><span data-ttu-id="a3120-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="a3120-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3120-112">*attivazione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a3120-112">*activationKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3120-113">Chiave utilizzata per identificare il valore di attivazione archiviato nel \* file ". vmc".</span><span class="sxs-lookup"><span data-stu-id="a3120-113">The key used to identify the activation value as stored in the "\*.vmc" file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3120-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a3120-114">Return value</span></span>

<span data-ttu-id="a3120-115">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="a3120-115">This method can return one of these values.</span></span>



| <span data-ttu-id="a3120-116">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="a3120-116">Return code/value</span></span>                                                                                                                                                      | <span data-ttu-id="a3120-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a3120-117">Description</span></span>                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a3120-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a3120-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="a3120-119">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="a3120-119">The operation was successful.</span></span><br/>                                                |
| <dl> <span data-ttu-id="a3120-120"><dt>**E \_**</dt> <dt>0x80000003</dt> INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="a3120-120"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>           | <span data-ttu-id="a3120-121">Il parametro è **null** o vuoto.</span><span class="sxs-lookup"><span data-stu-id="a3120-121">The parameter is **NULL** or empty.</span></span><br/>                                          |
| <dl> <span data-ttu-id="a3120-122"><dt>**Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="a3120-122"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>      | <span data-ttu-id="a3120-123">La configurazione è sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="a3120-123">The configuration is unknown.</span></span><br/>                                                |
| <dl> <span data-ttu-id="a3120-124"><dt>**Macchina virtuale \_ E \_ pref \_ non \_ trovato**</dt> <dt>0xA0040300</dt></span><span class="sxs-lookup"><span data-stu-id="a3120-124"><dt>**VM\_E\_PREF\_NOT\_FOUND**</dt> <dt>0xA0040300</dt></span></span> </dl> | <span data-ttu-id="a3120-125">La preferenza non è stata trovata o questa configurazione non ha un'attivazione valida.</span><span class="sxs-lookup"><span data-stu-id="a3120-125">The preference was not found, or this configuration has no valid activation.</span></span><br/> |
| <dl> <span data-ttu-id="a3120-126"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="a3120-126"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="a3120-127">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="a3120-127">An unexpected error has occurred.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="a3120-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="a3120-128">Remarks</span></span>

<span data-ttu-id="a3120-129">Questo metodo fornisce l'accesso di basso livello a qualsiasi valore di attivazione.</span><span class="sxs-lookup"><span data-stu-id="a3120-129">This method provides low-level access to any activation value.</span></span> <span data-ttu-id="a3120-130">Può essere usato per rimuovere i valori di attivazione per le chiavi definite dal cliente.</span><span class="sxs-lookup"><span data-stu-id="a3120-130">It can be used to remove activation values for customer-defined keys.</span></span> <span data-ttu-id="a3120-131">Prestare attenzione se si utilizza questo metodo per rimuovere i valori di attivazione del sistema, poiché alcuni valori non possono essere modificati mentre la macchina virtuale è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="a3120-131">Be careful if you use this method to remove system activation values, since some values cannot be changed while the virtual machine is running.</span></span> <span data-ttu-id="a3120-132">Quando viene avviata una macchina virtuale, viene creata una copia dei valori di configurazione, che diventa il set di valori di attivazione.</span><span class="sxs-lookup"><span data-stu-id="a3120-132">When a virtual machine is started, a copy is made of its configuration values, which becomes its set of activation values.</span></span> <span data-ttu-id="a3120-133">I valori di attivazione vengono mantenuti fino a quando la macchina virtuale non viene arrestata o riavviata.</span><span class="sxs-lookup"><span data-stu-id="a3120-133">Activation values are maintained until the virtual machine is shut down or restarted.</span></span> <span data-ttu-id="a3120-134">Si noti che Windows Virtual PC può utilizzare la configurazione solo per archiviare i valori per determinate chiavi, ovvero il valore di attivazione non può mai essere utilizzato.</span><span class="sxs-lookup"><span data-stu-id="a3120-134">Note that Windows Virtual PC may only use the configuration to store values for certain keys, that is, the activation value may never be used.</span></span>

> [!Note]  
> <span data-ttu-id="a3120-135">Per modificare i valori di attivazione, è necessario che la sessione della macchina virtuale sia in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="a3120-135">The virtual machine session must be running before any activation values can be changed.</span></span>

 

<span data-ttu-id="a3120-136">Le chiavi di attivazione sono archiviate internamente in modo gerarchico Analogamente alle chiavi del registro di sistema di Windows.</span><span class="sxs-lookup"><span data-stu-id="a3120-136">Activation keys are stored internally in a hierarchical manner similar to the registry keys in Windows.</span></span> <span data-ttu-id="a3120-137">Per specificare una sottochiave specifica, viene creato un "percorso della chiave" che specifica le varie chiavi in un formato delimitato da barre.</span><span class="sxs-lookup"><span data-stu-id="a3120-137">To specify a specific subkey, a "key path" is constructed which specifies the various keys in a slash mark delimited format.</span></span>

<span data-ttu-id="a3120-138">Ad esempio, per rimuovere il valore della \_ chiave "azione predefinita" situata nell'albero delle chiavi seguente:</span><span class="sxs-lookup"><span data-stu-id="a3120-138">For example, to remove the value of the "default\_action" key located in the following key tree:</span></span>

``` syntax
<settings>
    <undo_drives>
        <default_action type="integer">1</default_action>
```

<span data-ttu-id="a3120-139">La stringa di percorso *attivazione* viene specificata come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="a3120-139">The *activationKey* path string would be specified as follows:</span></span>

``` syntax
"settings/undo_drives/default_action"
```

## <a name="requirements"></a><span data-ttu-id="a3120-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a3120-140">Requirements</span></span>



| <span data-ttu-id="a3120-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3120-141">Requirement</span></span> | <span data-ttu-id="a3120-142">Valore</span><span class="sxs-lookup"><span data-stu-id="a3120-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3120-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a3120-143">Minimum supported client</span></span><br/> | <span data-ttu-id="a3120-144">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="a3120-144">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a3120-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a3120-145">Minimum supported server</span></span><br/> | <span data-ttu-id="a3120-146">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a3120-146">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="a3120-147">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="a3120-147">End of client support</span></span><br/>    | <span data-ttu-id="a3120-148">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a3120-148">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a3120-149">Prodotto</span><span class="sxs-lookup"><span data-stu-id="a3120-149">Product</span></span><br/>                  | <span data-ttu-id="a3120-150">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a3120-150">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="a3120-151">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a3120-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3120-152"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3120-152"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="a3120-153">IID</span><span class="sxs-lookup"><span data-stu-id="a3120-153">IID</span></span><br/>                      | <span data-ttu-id="a3120-154">IID \_ IVMVirtualMachine è definito come f7092aa1-33ed-4F78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="a3120-154">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="a3120-155">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a3120-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3120-156">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="a3120-156">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

