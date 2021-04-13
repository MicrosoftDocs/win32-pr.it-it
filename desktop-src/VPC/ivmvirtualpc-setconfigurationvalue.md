---
title: Metodo IVMVirtualPC SetConfigurationValue (VPCCOMInterfaces. h)
description: Imposta il valore dell'impostazione di configurazione specificata.
ms.assetid: 7760b81e-734d-4970-8875-f2d310ff6c5c
keywords:
- Metodo SetConfigurationValue Virtual PC
- Metodo SetConfigurationValue Virtual PC, interfaccia IVMVirtualPC
- Interfaccia IVMVirtualPC Virtual PC, metodo SetConfigurationValue
topic_type:
- apiref
api_name:
- IVMVirtualPC.SetConfigurationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecb8ff3bb68829e944461cedb1c86904c7150593
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518466"
---
# <a name="ivmvirtualpcsetconfigurationvalue-method"></a><span data-ttu-id="f2362-106">Metodo IVMVirtualPC:: SetConfigurationValue</span><span class="sxs-lookup"><span data-stu-id="f2362-106">IVMVirtualPC::SetConfigurationValue method</span></span>

<span data-ttu-id="f2362-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f2362-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f2362-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f2362-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f2362-109">Imposta il valore dell'impostazione di configurazione specificata.</span><span class="sxs-lookup"><span data-stu-id="f2362-109">Sets the value of the specified configuration setting.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2362-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f2362-110">Syntax</span></span>


```C++
HRESULT SetConfigurationValue(
  [in] BSTR    preferenceKey,
  [in] VARIANT preferenceValue
);
```



## <a name="parameters"></a><span data-ttu-id="f2362-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="f2362-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2362-112">*preferenceKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f2362-112">*preferenceKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2362-113">Chiave utilizzata per identificare la preferenza, archiviata nel file di configurazione per utente (Options.xml in "% LocalAppData% \\ Microsoft \\ Windows Virtual PC").</span><span class="sxs-lookup"><span data-stu-id="f2362-113">The key used to identify the preference, as stored in the per-user configuration file (Options.xml in "%LocalAppData%\\Microsoft\\Windows Virtual PC").</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f2362-114">Le modifiche devono essere apportate Options.xml solo usando il metodo **SetConfigurationValue** .</span><span class="sxs-lookup"><span data-stu-id="f2362-114">Changes should be made to Options.xml only using the **SetConfigurationValue** method.</span></span> <span data-ttu-id="f2362-115">Non è supportata la modifica di Options.xml con altri metodi.</span><span class="sxs-lookup"><span data-stu-id="f2362-115">Changing Options.xml using any other method is not supported.</span></span>

 

</dd> <dt>

<span data-ttu-id="f2362-116">*preferenceValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f2362-116">*preferenceValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2362-117">Valore di preferenza.</span><span class="sxs-lookup"><span data-stu-id="f2362-117">The preference value.</span></span> <span data-ttu-id="f2362-118">Questo valore può essere uno dei tipi **Variant** seguenti: VT **\_ Array** VT \| **\_ Ui1** (byte non elaborati), **VT \_ BSTR** (String) **, VT \_ UI4** (Integer) o **VT \_ bool** (Boolean).</span><span class="sxs-lookup"><span data-stu-id="f2362-118">This value may be one of the following **VARIANT** types: **VT\_ARRAY**\|**VT\_UI1** (raw bytes), **VT\_BSTR** (string), **VT\_UI4** (integer), or **VT\_BOOL** (Boolean).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2362-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f2362-119">Return value</span></span>

<span data-ttu-id="f2362-120">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="f2362-120">This method can return one of these values.</span></span>



| <span data-ttu-id="f2362-121">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="f2362-121">Return code/value</span></span>                                                                                                                                                                        | <span data-ttu-id="f2362-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f2362-122">Description</span></span>                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f2362-123"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f2362-123"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="f2362-124">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="f2362-124">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="f2362-125"><dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="f2362-125"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="f2362-126">Il parametro *preferenceKey* o *preferenceValue* è **null**.</span><span class="sxs-lookup"><span data-stu-id="f2362-126">The *preferenceKey* or *preferenceValue* parameter is **NULL**.</span></span><br/>                      |
| <dl> <span data-ttu-id="f2362-127"><dt>**E \_**</dt> <dt>0x80000003</dt> INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="f2362-127"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                             | <span data-ttu-id="f2362-128">Il parametro *preferenceKey* non è valido o è una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="f2362-128">The *preferenceKey* parameter is not valid or is an empty string.</span></span><br/>                    |
| <dl> <span data-ttu-id="f2362-129"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="f2362-129"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="f2362-130">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="f2362-130">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="f2362-131"><dt>**E \_**</dt> <dt>0x80070005</dt> AccessDenied</span><span class="sxs-lookup"><span data-stu-id="f2362-131"><dt>**E\_ACCESSDENIED**</dt> <dt>0x80070005</dt></span></span> </dl>                           | <span data-ttu-id="f2362-132">L'utente corrente non dispone di accesso sufficiente al file di configurazione.</span><span class="sxs-lookup"><span data-stu-id="f2362-132">The current user has insufficient access to the configuration file.</span></span><br/>                  |
| <dl> <span data-ttu-id="f2362-133"><dt>**Macchina virtuale \_ E \_ \_ virtualizzazione hardware \_ disabilitato**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="f2362-133"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="f2362-134">Il processore non supporta le estensioni di virtualizzazione accelerata hardware (HAV).</span><span class="sxs-lookup"><span data-stu-id="f2362-134">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f2362-135">Commenti</span><span class="sxs-lookup"><span data-stu-id="f2362-135">Remarks</span></span>

<span data-ttu-id="f2362-136">Per il parametro *preferenceKey* sono supportati i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="f2362-136">The following values are supported for the *preferenceKey* parameter.</span></span>



| <span data-ttu-id="f2362-137">valore *preferenceKey*</span><span class="sxs-lookup"><span data-stu-id="f2362-137">*preferenceKey* value</span></span>      | <span data-ttu-id="f2362-138">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f2362-138">Description</span></span>                                                                                                                                                                           | <span data-ttu-id="f2362-139">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="f2362-139">Data type</span></span>            | <span data-ttu-id="f2362-140">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="f2362-140">Default value</span></span>   |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|-----------------|
| <span data-ttu-id="f2362-141">"timeout di inattività \_ "</span><span class="sxs-lookup"><span data-stu-id="f2362-141">"idle\_timeout"</span></span><br/> | <span data-ttu-id="f2362-142">Numero di secondi che vpc.exe deve attendere prima di uscire se non sono presenti macchine virtuali o applicazioni attive che utilizzano le [interfacce di Windows Virtual PC](virtual-pc-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="f2362-142">Number of seconds that vpc.exe should wait before exiting if there are no active VMs or applications using the [Windows Virtual PC Interfaces](virtual-pc-interfaces.md).</span></span><br/> | <span data-ttu-id="f2362-143">intero</span><span class="sxs-lookup"><span data-stu-id="f2362-143">"integer"</span></span><br/> | <span data-ttu-id="f2362-144">30</span><span class="sxs-lookup"><span data-stu-id="f2362-144">"30"</span></span><br/> |



 

<span data-ttu-id="f2362-145">Questo metodo fornisce l'accesso di basso livello a qualsiasi valore di configurazione.</span><span class="sxs-lookup"><span data-stu-id="f2362-145">This method provides low-level access to any configuration value.</span></span> <span data-ttu-id="f2362-146">Può essere usato per impostare i valori di configurazione per le chiavi definite dal cliente.</span><span class="sxs-lookup"><span data-stu-id="f2362-146">It can be used to set configuration values for customer-defined keys.</span></span> <span data-ttu-id="f2362-147">Prestare attenzione se si utilizza questo metodo per impostare i valori di configurazione di sistema, in quanto non viene eseguito alcun controllo degli errori sul valore di configurazione.</span><span class="sxs-lookup"><span data-stu-id="f2362-147">Be careful if you use this method to set system configuration values, because no error checking is performed on the configuration value.</span></span> <span data-ttu-id="f2362-148">Inoltre, alcuni valori di configurazione non possono essere modificati mentre una macchina virtuale è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="f2362-148">Also, some configuration values cannot be changed while a virtual machine is running.</span></span>

<span data-ttu-id="f2362-149">Le chiavi di configurazione si trovano nel file "Options.xml" della macchina virtuale in formato XML.</span><span class="sxs-lookup"><span data-stu-id="f2362-149">Configuration keys are located in the virtual machine's "Options.xml" file in XML format.</span></span> <span data-ttu-id="f2362-150">Le chiavi vengono archiviate in modo gerarchico come le chiavi del registro di sistema di Windows.</span><span class="sxs-lookup"><span data-stu-id="f2362-150">The keys are stored in a hierarchical manner similar to the registry keys in Windows.</span></span> <span data-ttu-id="f2362-151">Per specificare una sottochiave specifica, viene creato un "percorso della chiave" che specifica le varie chiavi in un formato delimitato da barre.</span><span class="sxs-lookup"><span data-stu-id="f2362-151">To specify a specific subkey, a "key path" is constructed which specifies the various keys in a slash mark delimited format.</span></span>

<span data-ttu-id="f2362-152">Ad esempio, per impostare il valore della chiave "Idle \_ timeout" presente nell'albero delle chiavi seguente:</span><span class="sxs-lookup"><span data-stu-id="f2362-152">For example, to set the value of the "idle\_timeout" key located in the following key tree:</span></span>

``` syntax
<preferences>
  <idle_timeout type="integer">60</idle_timeout>
```

<span data-ttu-id="f2362-153">La stringa di percorso *preferenceKey* viene specificata come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="f2362-153">The *preferenceKey* path string would be specified as follows:</span></span>

``` syntax
"idle_timeout"
```

<span data-ttu-id="f2362-154">Se una delle chiavi nell'albero desiderato ha un valore di attributo "ID", l'attributo e il relativo valore vengono incorporati nella stringa del percorso *preferenceKey* immediatamente dopo la chiave di configurazione associata usando il formato racchiuso tra parentesi: " \[ @id ="*\_ valore ID*" \] ".</span><span class="sxs-lookup"><span data-stu-id="f2362-154">If any of the keys in the desired tree have an "id" attribute value, the attribute and its value is embedded in the *preferenceKey* path string immediately after its associated configuration key using the following bracketed format: "\[@id="*id\_value*"\]".</span></span>

<span data-ttu-id="f2362-155">Ad esempio, per impostare il valore della chiave "Golf" situata nell'albero delle chiavi seguente:</span><span class="sxs-lookup"><span data-stu-id="f2362-155">For example, to set the value of the "golf" key located in the following key tree:</span></span>

``` syntax
<preferences>
  <alpha>
    <bravo>
      <charlie>
        <delta id="1">
          <echo id="0">
            <foxtrot>
              <golf type="string">D</golf>
```

<span data-ttu-id="f2362-156">La stringa di percorso *preferenceKey* viene specificata come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="f2362-156">The *preferenceKey* path string would be specified as follows:</span></span>

``` syntax
"alpha/bravo/charlie/delta[@id=1]/echo[@id=0]/foxtrot/golf"
```

## <a name="requirements"></a><span data-ttu-id="f2362-157">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f2362-157">Requirements</span></span>



| <span data-ttu-id="f2362-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2362-158">Requirement</span></span> | <span data-ttu-id="f2362-159">Valore</span><span class="sxs-lookup"><span data-stu-id="f2362-159">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2362-160">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f2362-160">Minimum supported client</span></span><br/> | <span data-ttu-id="f2362-161">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f2362-161">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f2362-162">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f2362-162">Minimum supported server</span></span><br/> | <span data-ttu-id="f2362-163">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="f2362-163">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f2362-164">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="f2362-164">End of client support</span></span><br/>    | <span data-ttu-id="f2362-165">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f2362-165">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f2362-166">Prodotto</span><span class="sxs-lookup"><span data-stu-id="f2362-166">Product</span></span><br/>                  | <span data-ttu-id="f2362-167">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f2362-167">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f2362-168">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f2362-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2362-169"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2362-169"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="f2362-170">IID</span><span class="sxs-lookup"><span data-stu-id="f2362-170">IID</span></span><br/>                      | <span data-ttu-id="f2362-171">IID \_ IVMVirtualPC è definito come 236ba0d9-A24A-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="f2362-171">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="f2362-172">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f2362-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2362-173">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="f2362-173">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> <dt>

[<span data-ttu-id="f2362-174">**IVMVirtualMachine::SetConfigurationValue**</span><span class="sxs-lookup"><span data-stu-id="f2362-174">**IVMVirtualMachine::SetConfigurationValue**</span></span>](ivmvirtualmachine-setconfigurationvalue.md)
</dt> </dl>

 

