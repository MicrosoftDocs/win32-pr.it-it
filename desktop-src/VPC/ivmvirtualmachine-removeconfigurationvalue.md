---
title: Metodo IVMVirtualMachine RemoveConfigurationValue (VPCCOMInterfaces. h)
description: Rimuove il valore dell'impostazione di configurazione specificata per questa macchina virtuale.
ms.assetid: 2d75a667-9656-4d4c-bafe-f3f8be3763f5
keywords:
- Metodo RemoveConfigurationValue Virtual PC
- Metodo RemoveConfigurationValue Virtual PC, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC, metodo RemoveConfigurationValue
topic_type:
- apiref
api_name:
- IVMVirtualMachine.RemoveConfigurationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 683cad2c7cce34822f6f5607ea2676902284baf0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477986"
---
# <a name="ivmvirtualmachineremoveconfigurationvalue-method"></a><span data-ttu-id="bf744-106">Metodo IVMVirtualMachine:: RemoveConfigurationValue</span><span class="sxs-lookup"><span data-stu-id="bf744-106">IVMVirtualMachine::RemoveConfigurationValue method</span></span>

<span data-ttu-id="bf744-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="bf744-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="bf744-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="bf744-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="bf744-109">Rimuove il valore dell'impostazione di configurazione specificata per questa macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="bf744-109">Removes the value of the specified configuration setting for this virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf744-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bf744-110">Syntax</span></span>


```C++
HRESULT RemoveConfigurationValue(
  [in] BSTR configurationKey
);
```



## <a name="parameters"></a><span data-ttu-id="bf744-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="bf744-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf744-112">*configurationKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bf744-112">*configurationKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf744-113">Chiave utilizzata per identificare il valore di configurazione archiviato nel \* file ". vmc".</span><span class="sxs-lookup"><span data-stu-id="bf744-113">The key used to identify the configuration value as stored in the "\*.vmc" file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf744-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bf744-114">Return value</span></span>

<span data-ttu-id="bf744-115">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="bf744-115">This method can return one of these values.</span></span>



| <span data-ttu-id="bf744-116">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="bf744-116">Return code/value</span></span>                                                                                                                                                      | <span data-ttu-id="bf744-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bf744-117">Description</span></span>                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="bf744-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="bf744-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="bf744-119">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="bf744-119">The operation was successful.</span></span><br/>       |
| <dl> <span data-ttu-id="bf744-120"><dt>**E \_**</dt> <dt>0x80000003</dt> INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="bf744-120"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>           | <span data-ttu-id="bf744-121">Il parametro è **null** o vuoto.</span><span class="sxs-lookup"><span data-stu-id="bf744-121">The parameter is **NULL** or empty.</span></span><br/> |
| <dl> <span data-ttu-id="bf744-122"><dt>**Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="bf744-122"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>      | <span data-ttu-id="bf744-123">La configurazione è sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="bf744-123">The configuration is unknown.</span></span><br/>       |
| <dl> <span data-ttu-id="bf744-124"><dt>**Macchina virtuale \_ E \_ pref \_ non \_ trovato**</dt> <dt>0xA0040300</dt></span><span class="sxs-lookup"><span data-stu-id="bf744-124"><dt>**VM\_E\_PREF\_NOT\_FOUND**</dt> <dt>0xA0040300</dt></span></span> </dl> | <span data-ttu-id="bf744-125">La preferenza non è stata trovata.</span><span class="sxs-lookup"><span data-stu-id="bf744-125">The preference was not found.</span></span><br/>       |
| <dl> <span data-ttu-id="bf744-126"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="bf744-126"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="bf744-127">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="bf744-127">An unexpected error has occurred.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="bf744-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="bf744-128">Remarks</span></span>

<span data-ttu-id="bf744-129">Questo metodo fornisce l'accesso di basso livello a qualsiasi valore di configurazione.</span><span class="sxs-lookup"><span data-stu-id="bf744-129">This method provides low-level access to any configuration value.</span></span> <span data-ttu-id="bf744-130">Può essere usato per rimuovere i valori di configurazione per le chiavi definite dal cliente.</span><span class="sxs-lookup"><span data-stu-id="bf744-130">It can be used to remove configuration values for customer-defined keys.</span></span> <span data-ttu-id="bf744-131">Prestare attenzione se si utilizza questo metodo per rimuovere i valori di configurazione di sistema, poiché alcuni valori non possono essere modificati mentre la macchina virtuale è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="bf744-131">Be careful if you use this method to remove system configuration values, since some values cannot be changed while the virtual machine is running.</span></span>

<span data-ttu-id="bf744-132">Le chiavi di configurazione si trovano nel \* file ". vmc" della macchina virtuale in formato XML.</span><span class="sxs-lookup"><span data-stu-id="bf744-132">Configuration keys are located in the virtual machine's "\*.vmc" file in XML format.</span></span> <span data-ttu-id="bf744-133">Le chiavi vengono archiviate in modo gerarchico come le chiavi del registro di sistema di Windows.</span><span class="sxs-lookup"><span data-stu-id="bf744-133">The keys are stored in a hierarchical manner similar to the registry keys in Windows.</span></span> <span data-ttu-id="bf744-134">Per specificare una sottochiave specifica, viene creato un "percorso della chiave" che specifica le varie chiavi in un formato delimitato da barre.</span><span class="sxs-lookup"><span data-stu-id="bf744-134">To specify a specific subkey, a "key path" is constructed which specifies the various keys in a slash mark delimited format.</span></span>

<span data-ttu-id="bf744-135">Ad esempio, per rimuovere il valore della chiave "RAM \_ size" situata nell'albero delle chiavi seguente:</span><span class="sxs-lookup"><span data-stu-id="bf744-135">For example, to remove the value of the "ram\_size" key located in the following key tree:</span></span>

``` syntax
<hardware>
    <memory>
        <ram_size type="integer">128</ram_size>
```

<span data-ttu-id="bf744-136">La stringa di percorso *configurationKey* viene specificata come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="bf744-136">The *configurationKey* path string would be specified as follows:</span></span>

``` syntax
"hardware/memory/ram_size"
```

<span data-ttu-id="bf744-137">Se una delle chiavi nell'albero desiderato ha un valore di attributo "ID", l'attributo e il relativo valore vengono incorporati nella stringa del percorso *configurationKey* immediatamente dopo la chiave di configurazione associata usando il formato racchiuso tra parentesi: " \[ @id ="*\_ valore ID*" \] ".</span><span class="sxs-lookup"><span data-stu-id="bf744-137">If any of the keys in the desired tree have an "id" attribute value, the attribute and its value is embedded in the *configurationKey* path string immediately after its associated configuration key using the following bracketed format: "\[@id="*id\_value*"\]".</span></span>

<span data-ttu-id="bf744-138">Ad esempio, per rimuovere il valore della chiave "Absolute" che si trova nell'albero delle chiavi seguente:</span><span class="sxs-lookup"><span data-stu-id="bf744-138">For example, to remove the value of the "absolute" key located in the following key tree:</span></span>

``` syntax
<hardware>
    <pci_bus>
        <ide_adapter>
            <ide_controller id="1">
                <location id="0">
                    <pathname>
                        <absolute type="string">D</absolute>
```

<span data-ttu-id="bf744-139">La stringa di percorso *configurationKey* viene specificata come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="bf744-139">The *configurationKey* path string would be specified as follows:</span></span>

``` syntax
"hardware/pci_bus/ide_adapter/ide_controller[@id=1]/location[@id=0]/pathname/absolute"
```

## <a name="requirements"></a><span data-ttu-id="bf744-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bf744-140">Requirements</span></span>



| <span data-ttu-id="bf744-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf744-141">Requirement</span></span> | <span data-ttu-id="bf744-142">Valore</span><span class="sxs-lookup"><span data-stu-id="bf744-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf744-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bf744-143">Minimum supported client</span></span><br/> | <span data-ttu-id="bf744-144">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="bf744-144">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bf744-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bf744-145">Minimum supported server</span></span><br/> | <span data-ttu-id="bf744-146">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="bf744-146">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="bf744-147">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="bf744-147">End of client support</span></span><br/>    | <span data-ttu-id="bf744-148">Windows 7</span><span class="sxs-lookup"><span data-stu-id="bf744-148">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="bf744-149">Prodotto</span><span class="sxs-lookup"><span data-stu-id="bf744-149">Product</span></span><br/>                  | <span data-ttu-id="bf744-150">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="bf744-150">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="bf744-151">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bf744-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf744-152"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf744-152"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="bf744-153">IID</span><span class="sxs-lookup"><span data-stu-id="bf744-153">IID</span></span><br/>                      | <span data-ttu-id="bf744-154">IID \_ IVMVirtualMachine è definito come f7092aa1-33ed-4F78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="bf744-154">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="bf744-155">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bf744-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf744-156">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="bf744-156">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

