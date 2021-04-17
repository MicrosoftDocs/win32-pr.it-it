---
title: Metodo IVMVirtualMachine GetConfigurationValue (VPCCOMInterfaces. h)
description: Recupera il valore dell'impostazione di configurazione specificata per questa macchina virtuale.
ms.assetid: fd3c509e-8a40-4828-b866-6bd2cb455ab2
keywords:
- Metodo GetConfigurationValue Virtual PC
- Metodo GetConfigurationValue Virtual PC, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC, metodo GetConfigurationValue
topic_type:
- apiref
api_name:
- IVMVirtualMachine.GetConfigurationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e98e37bd4bd5ec4ba9843ae2fdb33874a4303f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400694"
---
# <a name="ivmvirtualmachinegetconfigurationvalue-method"></a><span data-ttu-id="107e2-106">Metodo IVMVirtualMachine:: GetConfigurationValue</span><span class="sxs-lookup"><span data-stu-id="107e2-106">IVMVirtualMachine::GetConfigurationValue method</span></span>

<span data-ttu-id="107e2-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="107e2-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="107e2-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="107e2-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="107e2-109">Recupera il valore dell'impostazione di configurazione specificata per questa macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="107e2-109">Retrieves the value of the specified configuration setting for this virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="107e2-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="107e2-110">Syntax</span></span>


```C++
HRESULT GetConfigurationValue(
  [in]          BSTR    configurationKey,
  [out, retval] VARIANT *configurationValue
);
```



## <a name="parameters"></a><span data-ttu-id="107e2-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="107e2-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="107e2-112">*configurationKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="107e2-112">*configurationKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="107e2-113">Chiave utilizzata per identificare il valore di configurazione archiviato nel \* file ". vmc".</span><span class="sxs-lookup"><span data-stu-id="107e2-113">The key used to identify the configuration value as stored in the "\*.vmc" file.</span></span>

</dd> <dt>

<span data-ttu-id="107e2-114">*configurationValue* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="107e2-114">*configurationValue* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="107e2-115">Valore di configurazione.</span><span class="sxs-lookup"><span data-stu-id="107e2-115">The configuration value.</span></span> <span data-ttu-id="107e2-116">Questo valore può essere uno dei tipi **Variant** seguenti: VT **\_ Array** VT \| **\_ Ui1** (byte non elaborati), **VT \_ BSTR** (String) **, VT \_ I4** (Integer) o **VT \_ bool** (Boolean).</span><span class="sxs-lookup"><span data-stu-id="107e2-116">This value can be one of the following **VARIANT** types: **VT\_ARRAY**\|**VT\_UI1** (raw bytes), **VT\_BSTR** (string), **VT\_I4** (integer), or **VT\_BOOL** (Boolean).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="107e2-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="107e2-117">Return value</span></span>

<span data-ttu-id="107e2-118">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="107e2-118">This method can return one of these values.</span></span>



| <span data-ttu-id="107e2-119">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="107e2-119">Return code/value</span></span>                                                                                                                                                      | <span data-ttu-id="107e2-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="107e2-120">Description</span></span>                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <span data-ttu-id="107e2-121"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="107e2-121"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="107e2-122">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="107e2-122">The operation was successful.</span></span><br/>                          |
| <dl> <span data-ttu-id="107e2-123"><dt>**E \_**</dt> <dt>0x80000003</dt> INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="107e2-123"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>           | <span data-ttu-id="107e2-124">Il parametro *configurationKey* è **null** o vuoto.</span><span class="sxs-lookup"><span data-stu-id="107e2-124">The *configurationKey* parameter is **NULL** or empty.</span></span><br/> |
| <dl> <span data-ttu-id="107e2-125"><dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="107e2-125"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>              | <span data-ttu-id="107e2-126">Il parametro *configurationValue* è **null**.</span><span class="sxs-lookup"><span data-stu-id="107e2-126">The *configurationValue* parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="107e2-127"><dt>**Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="107e2-127"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>      | <span data-ttu-id="107e2-128">La configurazione è sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="107e2-128">The configuration is unknown.</span></span><br/>                          |
| <dl> <span data-ttu-id="107e2-129"><dt>**Macchina virtuale \_ E \_ pref \_ non \_ trovato**</dt> <dt>0xA0040300</dt></span><span class="sxs-lookup"><span data-stu-id="107e2-129"><dt>**VM\_E\_PREF\_NOT\_FOUND**</dt> <dt>0xA0040300</dt></span></span> </dl> | <span data-ttu-id="107e2-130">La preferenza non è stata trovata.</span><span class="sxs-lookup"><span data-stu-id="107e2-130">The preference was not found.</span></span><br/>                          |
| <dl> <span data-ttu-id="107e2-131"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="107e2-131"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="107e2-132">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="107e2-132">An unexpected error has occurred.</span></span><br/>                      |



 

## <a name="remarks"></a><span data-ttu-id="107e2-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="107e2-133">Remarks</span></span>

<span data-ttu-id="107e2-134">Questo metodo fornisce l'accesso di basso livello a qualsiasi valore di configurazione.</span><span class="sxs-lookup"><span data-stu-id="107e2-134">This method provides low-level access to any configuration value.</span></span> <span data-ttu-id="107e2-135">Può essere usato per leggere i valori di configurazione per le chiavi definite dal cliente.</span><span class="sxs-lookup"><span data-stu-id="107e2-135">It can be used to read configuration values for customer-defined keys.</span></span>

<span data-ttu-id="107e2-136">Le chiavi di configurazione si trovano nel \* file ". vmc" della macchina virtuale in formato XML.</span><span class="sxs-lookup"><span data-stu-id="107e2-136">Configuration keys are located in the virtual machine's "\*.vmc" file in XML format.</span></span> <span data-ttu-id="107e2-137">Le chiavi vengono archiviate in modo gerarchico come le chiavi del registro di sistema di Windows.</span><span class="sxs-lookup"><span data-stu-id="107e2-137">The keys are stored in a hierarchical manner similar to the registry keys in Windows.</span></span> <span data-ttu-id="107e2-138">Per specificare una sottochiave specifica, viene creato un "percorso della chiave" che specifica le varie chiavi in un formato delimitato da barre.</span><span class="sxs-lookup"><span data-stu-id="107e2-138">To specify a specific subkey, a "key path" is constructed which specifies the various keys in a slash mark delimited format.</span></span>

<span data-ttu-id="107e2-139">Ad esempio, per leggere il valore della chiave "RAM \_ size" situata nell'albero delle chiavi seguente:</span><span class="sxs-lookup"><span data-stu-id="107e2-139">For example, to read the value of the "ram\_size" key located in the following key tree:</span></span>

``` syntax
<hardware>
    <memory>
        <ram_size type="integer">128</ram_size>
```

<span data-ttu-id="107e2-140">La stringa di percorso *configurationKey* viene specificata come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="107e2-140">The *configurationKey* path string would be specified as follows:</span></span>

``` syntax
"hardware/memory/ram_size"
```

<span data-ttu-id="107e2-141">Se una delle chiavi nell'albero desiderato ha un valore di attributo "ID", l'attributo e il relativo valore vengono incorporati nella stringa del percorso *configurationKey* immediatamente dopo la chiave di configurazione associata usando il formato racchiuso tra parentesi: " \[ @id ="*\_ valore ID*" \] ".</span><span class="sxs-lookup"><span data-stu-id="107e2-141">If any of the keys in the desired tree have an "id" attribute value, the attribute and its value is embedded in the *configurationKey* path string immediately after its associated configuration key using the following bracketed format: "\[@id="*id\_value*"\]".</span></span>

<span data-ttu-id="107e2-142">Ad esempio, per leggere il valore della chiave "Absolute" situata nell'albero delle chiavi seguente:</span><span class="sxs-lookup"><span data-stu-id="107e2-142">For example, to read the value of the "absolute" key located in the following key tree:</span></span>

``` syntax
<hardware>
    <pci_bus>
        <ide_adapter>
            <ide_controller id="1">
                <location id="0">
                    <pathname>
                        <absolute type="string">D</absolute>
```

<span data-ttu-id="107e2-143">La stringa di percorso *configurationKey* viene specificata come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="107e2-143">The *configurationKey* path string would be specified as follows:</span></span>

``` syntax
"hardware/pci_bus/ide_adapter/ide_controller[@id=1]/location[@id=0]/pathname/absolute"
```

## <a name="requirements"></a><span data-ttu-id="107e2-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="107e2-144">Requirements</span></span>



| <span data-ttu-id="107e2-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="107e2-145">Requirement</span></span> | <span data-ttu-id="107e2-146">Valore</span><span class="sxs-lookup"><span data-stu-id="107e2-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="107e2-147">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="107e2-147">Minimum supported client</span></span><br/> | <span data-ttu-id="107e2-148">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="107e2-148">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="107e2-149">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="107e2-149">Minimum supported server</span></span><br/> | <span data-ttu-id="107e2-150">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="107e2-150">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="107e2-151">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="107e2-151">End of client support</span></span><br/>    | <span data-ttu-id="107e2-152">Windows 7</span><span class="sxs-lookup"><span data-stu-id="107e2-152">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="107e2-153">Prodotto</span><span class="sxs-lookup"><span data-stu-id="107e2-153">Product</span></span><br/>                  | <span data-ttu-id="107e2-154">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="107e2-154">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="107e2-155">Intestazione</span><span class="sxs-lookup"><span data-stu-id="107e2-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="107e2-156"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="107e2-156"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="107e2-157">IID</span><span class="sxs-lookup"><span data-stu-id="107e2-157">IID</span></span><br/>                      | <span data-ttu-id="107e2-158">IID \_ IVMVirtualMachine è definito come f7092aa1-33ed-4F78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="107e2-158">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="107e2-159">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="107e2-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="107e2-160">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="107e2-160">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

