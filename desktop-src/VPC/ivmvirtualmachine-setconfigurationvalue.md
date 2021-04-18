---
title: Metodo IVMVirtualMachine SetConfigurationValue (VPCCOMInterfaces. h)
description: Imposta il valore dell'impostazione di configurazione specificata per la macchina virtuale (VM).
ms.assetid: 43c3ac88-2e25-4c9e-a2ac-fcae5add62c5
keywords:
- Metodo SetConfigurationValue Virtual PC
- Metodo SetConfigurationValue Virtual PC, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC, metodo SetConfigurationValue
topic_type:
- apiref
api_name:
- IVMVirtualMachine.SetConfigurationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1ebafd53a2eb82ea1869b5522d0258ece67d110
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302214"
---
# <a name="ivmvirtualmachinesetconfigurationvalue-method"></a><span data-ttu-id="dcb2c-106">Metodo IVMVirtualMachine:: SetConfigurationValue</span><span class="sxs-lookup"><span data-stu-id="dcb2c-106">IVMVirtualMachine::SetConfigurationValue method</span></span>

<span data-ttu-id="dcb2c-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="dcb2c-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="dcb2c-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="dcb2c-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="dcb2c-109">Imposta il valore dell'impostazione di configurazione specificata per la macchina virtuale (VM).</span><span class="sxs-lookup"><span data-stu-id="dcb2c-109">Sets the value of the specified configuration setting for this virtual machine (VM).</span></span>

## <a name="syntax"></a><span data-ttu-id="dcb2c-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dcb2c-110">Syntax</span></span>


```C++
HRESULT SetConfigurationValue(
  [in] BSTR    configurationKey,
  [in] VARIANT configurationValue
);
```



## <a name="parameters"></a><span data-ttu-id="dcb2c-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="dcb2c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dcb2c-112">*configurationKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dcb2c-112">*configurationKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcb2c-113">Chiave utilizzata per identificare il valore di configurazione archiviato nel \* file ". vmc".</span><span class="sxs-lookup"><span data-stu-id="dcb2c-113">The key used to identify the configuration value as stored in the "\*.vmc" file.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dcb2c-114">Le modifiche devono essere apportate a " \* . vmc" solo usando il metodo **SetConfigurationValue** .</span><span class="sxs-lookup"><span data-stu-id="dcb2c-114">Changes should be made to "\*.vmc" only using the **SetConfigurationValue** method.</span></span> <span data-ttu-id="dcb2c-115">La modifica di " \* . vmc" con qualsiasi altro metodo non è supportata.</span><span class="sxs-lookup"><span data-stu-id="dcb2c-115">Changing "\*.vmc" using any other method is not supported.</span></span>

 

</dd> <dt>

<span data-ttu-id="dcb2c-116">*configurationValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dcb2c-116">*configurationValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcb2c-117">Valore di configurazione.</span><span class="sxs-lookup"><span data-stu-id="dcb2c-117">The configuration value.</span></span> <span data-ttu-id="dcb2c-118">Questo valore Cay è uno dei seguenti tipi **Variant** : VT **\_ Array** VT \| **\_ Ui1** (byte non elaborati), **VT \_ BSTR** (String), **VT \_ UI4** (Integer) o **VT \_ bool** (Boolean).</span><span class="sxs-lookup"><span data-stu-id="dcb2c-118">This value cay be one of the following **VARIANT** types: **VT\_ARRAY**\|**VT\_UI1** (raw bytes), **VT\_BSTR** (string), **VT\_UI4** (integer), or **VT\_BOOL** (Boolean).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dcb2c-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dcb2c-119">Return value</span></span>

<span data-ttu-id="dcb2c-120">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="dcb2c-120">This method can return one of these values.</span></span>



| <span data-ttu-id="dcb2c-121">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="dcb2c-121">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="dcb2c-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dcb2c-122">Description</span></span>                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="dcb2c-123"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="dcb2c-123"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="dcb2c-124">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="dcb2c-124">The operation was successful.</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="dcb2c-125"><dt>**E \_**</dt> <dt>0x80000003</dt> INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="dcb2c-125"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>      | <span data-ttu-id="dcb2c-126">Il parametro *configurationKey* è **null** o vuoto oppure il parametro *configurationValue* non è un tipo Variant valido.</span><span class="sxs-lookup"><span data-stu-id="dcb2c-126">The *configurationKey* parameter is **NULL** or empty or the *configurationValue* parameter is not a valid variant type.</span></span><br/> |
| <dl> <span data-ttu-id="dcb2c-127"><dt>**Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="dcb2c-127"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="dcb2c-128">La configurazione è sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="dcb2c-128">The configuration is unknown.</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="dcb2c-129"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="dcb2c-129"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="dcb2c-130">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="dcb2c-130">An unexpected error has occurred.</span></span><br/>                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="dcb2c-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="dcb2c-131">Remarks</span></span>

<span data-ttu-id="dcb2c-132">Per il parametro *configurationKey* sono supportati i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="dcb2c-132">The following values are supported for the *configurationKey* parameter.</span></span>



| <span data-ttu-id="dcb2c-133">valore *configurationKey*</span><span class="sxs-lookup"><span data-stu-id="dcb2c-133">*configurationKey* value</span></span>                                     | <span data-ttu-id="dcb2c-134">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dcb2c-134">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          | <span data-ttu-id="dcb2c-135">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="dcb2c-135">Data type</span></span>            | <span data-ttu-id="dcb2c-136">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="dcb2c-136">Default value</span></span>     |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|-------------------|
| <span data-ttu-id="dcb2c-137">"hardware/BIOS/ \_ sincronizzazione ora \_ all' \_ avvio"</span><span class="sxs-lookup"><span data-stu-id="dcb2c-137">"hardware/bios/time\_sync\_at\_boot"</span></span><br/>              | <span data-ttu-id="dcb2c-138">"true" Se il clock della macchina virtuale CMOS deve essere sincronizzato con il clock host all'avvio; "false" in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="dcb2c-138">"true" if the VM CMOS clock is to be synchronized with the host clock at boot; "false" otherwise.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         | <span data-ttu-id="dcb2c-139">Boolean</span><span class="sxs-lookup"><span data-stu-id="dcb2c-139">"boolean"</span></span><br/> | <span data-ttu-id="dcb2c-140">"true"</span><span class="sxs-lookup"><span data-stu-id="dcb2c-140">"true"</span></span><br/> |
| <span data-ttu-id="dcb2c-141">"Integration/Microsoft/host \_ time \_ Sync/Enabled" "</span><span class="sxs-lookup"><span data-stu-id="dcb2c-141">"integration/microsoft/host\_time\_sync/enabled""</span></span><br/> | <span data-ttu-id="dcb2c-142">"true" se la sincronizzazione dell'ora dell'host è abilitata nei componenti di integrazione; "false" in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="dcb2c-142">"true" if host time synchronization is enabled in the integration components; "false" otherwise.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          | <span data-ttu-id="dcb2c-143">Boolean</span><span class="sxs-lookup"><span data-stu-id="dcb2c-143">"boolean"</span></span><br/> | <span data-ttu-id="dcb2c-144">"true"</span><span class="sxs-lookup"><span data-stu-id="dcb2c-144">"true"</span></span><br/> |
| <span data-ttu-id="dcb2c-145">"Opzioni interfaccia utente \_ / \_ pubblicazione automatica app \_ "</span><span class="sxs-lookup"><span data-stu-id="dcb2c-145">"ui\_options/auto\_app\_publish"</span></span><br/>                  | <span data-ttu-id="dcb2c-146">"true" se la pubblicazione automatica delle applicazioni è abilitata nei componenti di integrazione; "false" in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="dcb2c-146">"true" if automatic publishing of applications is enabled in the integration components; "false" otherwise.</span></span> <span data-ttu-id="dcb2c-147">Questa operazione è detta anche applicazioni virtuali.</span><span class="sxs-lookup"><span data-stu-id="dcb2c-147">This is also called virtual applications.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | <span data-ttu-id="dcb2c-148">Boolean</span><span class="sxs-lookup"><span data-stu-id="dcb2c-148">"boolean"</span></span><br/> | <span data-ttu-id="dcb2c-149">"true"</span><span class="sxs-lookup"><span data-stu-id="dcb2c-149">"true"</span></span><br/> |
| <span data-ttu-id="dcb2c-150">"Opzioni interfaccia utente \_ /secondi \_ per il \_ salvataggio"</span><span class="sxs-lookup"><span data-stu-id="dcb2c-150">"ui\_options/seconds\_to\_save"</span></span><br/>                   | <span data-ttu-id="dcb2c-151">Numero di secondi di attesa prima del salvataggio della macchina virtuale dopo la chiusura di tutte le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="dcb2c-151">Number of seconds to wait before saving the VM after all applications are closed.</span></span> <span data-ttu-id="dcb2c-152">Tuttavia, i valori inferiori a 20 e più di 4.294.968 hanno un significato speciale.</span><span class="sxs-lookup"><span data-stu-id="dcb2c-152">However, values below 20 and more than 4,294,968 have special meanings.</span></span> <span data-ttu-id="dcb2c-153">Per informazioni dettagliate, vedere l'elenco seguente</span><span class="sxs-lookup"><span data-stu-id="dcb2c-153">For details, see the following list</span></span><br/> <dl> <span data-ttu-id="dcb2c-154"><dt><span id="0"></span>0</dt></span><span class="sxs-lookup"><span data-stu-id="dcb2c-154"><dt><span id="0"></span>0</dt></span></span> <dd> <span data-ttu-id="dcb2c-155">Non salvare mai la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="dcb2c-155">Never save the VM.</span></span><br/> </dd> <span data-ttu-id="dcb2c-156"><dt><span id="120"></span>1 20</dt></span><span class="sxs-lookup"><span data-stu-id="dcb2c-156"><dt><span id="120"></span>1 20</dt></span></span> <dd> <span data-ttu-id="dcb2c-157">Attendere 20 secondi prima di salvare la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="dcb2c-157">Wait 20 seconds before saving the VM.</span></span><br/> </dd> <span data-ttu-id="dcb2c-158"><dt><span id="214_294_967"></span>21 4.294.967</dt></span><span class="sxs-lookup"><span data-stu-id="dcb2c-158"><dt><span id="214_294_967"></span>21 4,294,967</dt></span></span> <dd> <span data-ttu-id="dcb2c-159">Attendere il numero di secondi specificato prima di salvare la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="dcb2c-159">Wait the specified number of seconds before saving the VM.</span></span><br/> </dd> <span data-ttu-id="dcb2c-160"><dt><span id="4_294_9684_294_967_295"></span>4.294.968 4.294.967.295</dt></span><span class="sxs-lookup"><span data-stu-id="dcb2c-160"><dt><span id="4_294_9684_294_967_295"></span>4,294,968 4,294,967,295</dt></span></span> <dd> <span data-ttu-id="dcb2c-161">Attendere 4.294.968 secondi prima di salvare la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="dcb2c-161">Wait 4,294,968 seconds before saving the VM.</span></span><br/> </dd> </dl> | <span data-ttu-id="dcb2c-162">intero</span><span class="sxs-lookup"><span data-stu-id="dcb2c-162">"integer"</span></span><br/> | <span data-ttu-id="dcb2c-163">300</span><span class="sxs-lookup"><span data-stu-id="dcb2c-163">300</span></span><br/>    |



 

<span data-ttu-id="dcb2c-164">Questo metodo fornisce l'accesso di basso livello a qualsiasi valore di configurazione.</span><span class="sxs-lookup"><span data-stu-id="dcb2c-164">This method provides low-level access to any configuration value.</span></span> <span data-ttu-id="dcb2c-165">Può essere usato per impostare i valori di configurazione per le chiavi definite dal cliente.</span><span class="sxs-lookup"><span data-stu-id="dcb2c-165">It can be used to set configuration values for customer-defined keys.</span></span> <span data-ttu-id="dcb2c-166">Prestare attenzione se si utilizza questo metodo per impostare i valori di configurazione di sistema, in quanto non viene eseguito alcun controllo degli errori sul valore di configurazione.</span><span class="sxs-lookup"><span data-stu-id="dcb2c-166">Be careful if you use this method to set system configuration values, because no error checking is performed on the configuration value.</span></span> <span data-ttu-id="dcb2c-167">Inoltre, alcuni valori di configurazione non possono essere modificati mentre la macchina virtuale è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="dcb2c-167">Also, some configuration values cannot be changed while the virtual machine is running.</span></span>

<span data-ttu-id="dcb2c-168">Le chiavi di configurazione si trovano nel \* file ". vmc" della macchina virtuale in formato XML.</span><span class="sxs-lookup"><span data-stu-id="dcb2c-168">Configuration keys are located in the virtual machine's "\*.vmc" file in XML format.</span></span> <span data-ttu-id="dcb2c-169">Le chiavi vengono archiviate in modo gerarchico come le chiavi del registro di sistema di Windows.</span><span class="sxs-lookup"><span data-stu-id="dcb2c-169">The keys are stored in a hierarchical manner similar to the registry keys in Windows.</span></span> <span data-ttu-id="dcb2c-170">Per specificare una sottochiave specifica, viene creato un "percorso della chiave" che specifica le varie chiavi in un formato delimitato da barre.</span><span class="sxs-lookup"><span data-stu-id="dcb2c-170">To specify a specific subkey, a "key path" is constructed which specifies the various keys in a slash mark delimited format.</span></span>

<span data-ttu-id="dcb2c-171">Ad esempio, per impostare il valore della chiave "RAM \_ size" situata nell'albero delle chiavi seguente:</span><span class="sxs-lookup"><span data-stu-id="dcb2c-171">For example, to set the value of the "ram\_size" key located in the following key tree:</span></span>

``` syntax
<preferences>
  <hardware>
    <bios>
      <time_sync_at_boot type="boolean">true</time_sync_at_boot>
```

<span data-ttu-id="dcb2c-172">La stringa di percorso *configurationKey* viene specificata come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="dcb2c-172">The *configurationKey* path string would be specified as follows:</span></span>

``` syntax
"hardware/memory/ram_size"
```

<span data-ttu-id="dcb2c-173">Se una delle chiavi nell'albero desiderato ha un valore di attributo "ID", l'attributo e il relativo valore vengono incorporati nella stringa del percorso *configurationKey* immediatamente dopo la chiave di configurazione associata usando il formato racchiuso tra parentesi: " \[ @id ="*\_ valore ID*" \] ".</span><span class="sxs-lookup"><span data-stu-id="dcb2c-173">If any of the keys in the desired tree have an "id" attribute value, the attribute and its value is embedded in the *configurationKey* path string immediately after its associated configuration key using the following bracketed format: "\[@id="*id\_value*"\]".</span></span>

<span data-ttu-id="dcb2c-174">Ad esempio, per impostare il valore della chiave "Golf" situata nell'albero delle chiavi seguente:</span><span class="sxs-lookup"><span data-stu-id="dcb2c-174">For example, to set the value of the "golf" key located in the following key tree:</span></span>

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

<span data-ttu-id="dcb2c-175">La stringa di percorso *configurationKey* viene specificata come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="dcb2c-175">The *configurationKey* path string would be specified as follows:</span></span>

``` syntax
"alpha/bravo/charlie/delta[@id=1]/echo[@id=0]/foxtrot/golf"
```

## <a name="requirements"></a><span data-ttu-id="dcb2c-176">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dcb2c-176">Requirements</span></span>



| <span data-ttu-id="dcb2c-177">Requisito</span><span class="sxs-lookup"><span data-stu-id="dcb2c-177">Requirement</span></span> | <span data-ttu-id="dcb2c-178">Valore</span><span class="sxs-lookup"><span data-stu-id="dcb2c-178">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="dcb2c-179">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dcb2c-179">Minimum supported client</span></span><br/> | <span data-ttu-id="dcb2c-180">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="dcb2c-180">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="dcb2c-181">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dcb2c-181">Minimum supported server</span></span><br/> | <span data-ttu-id="dcb2c-182">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="dcb2c-182">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="dcb2c-183">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="dcb2c-183">End of client support</span></span><br/>    | <span data-ttu-id="dcb2c-184">Windows 7</span><span class="sxs-lookup"><span data-stu-id="dcb2c-184">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="dcb2c-185">Prodotto</span><span class="sxs-lookup"><span data-stu-id="dcb2c-185">Product</span></span><br/>                  | <span data-ttu-id="dcb2c-186">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="dcb2c-186">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="dcb2c-187">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dcb2c-187">Header</span></span><br/>                   | <dl> <span data-ttu-id="dcb2c-188"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="dcb2c-188"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="dcb2c-189">IID</span><span class="sxs-lookup"><span data-stu-id="dcb2c-189">IID</span></span><br/>                      | <span data-ttu-id="dcb2c-190">IID \_ IVMVirtualMachine è definito come f7092aa1-33ed-4F78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="dcb2c-190">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="dcb2c-191">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dcb2c-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcb2c-192">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="dcb2c-192">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> <dt>

[<span data-ttu-id="dcb2c-193">**IVMVirtualPC::SetConfigurationValue**</span><span class="sxs-lookup"><span data-stu-id="dcb2c-193">**IVMVirtualPC::SetConfigurationValue**</span></span>](ivmvirtualpc-setconfigurationvalue.md)
</dt> </dl>

 

