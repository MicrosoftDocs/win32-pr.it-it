---
description: Associa una macchina virtuale e i dati delle impostazioni di esportazione.
ms.assetid: FAAE7F74-07C0-4638-ABF9-5DEDBF2B9DD6
title: Classe Msvm_SystemExportSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SystemExportSettingData
- Msvm_SystemExportSettingData.ManagedElement
- Msvm_SystemExportSettingData.SettingData
- Msvm_SystemExportSettingData.IsDefault
- Msvm_SystemExportSettingData.IsCurrent
- Msvm_SystemExportSettingData.IsNext
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8203a45bb911743bb064c1a686da0b3d8abe99bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306024"
---
# <a name="msvm_systemexportsettingdata-class"></a><span data-ttu-id="53daf-103">\_Classe MSVM SystemExportSettingData</span><span class="sxs-lookup"><span data-stu-id="53daf-103">Msvm\_SystemExportSettingData class</span></span>

<span data-ttu-id="53daf-104">Associa una macchina virtuale e i dati delle impostazioni di esportazione.</span><span class="sxs-lookup"><span data-stu-id="53daf-104">Associates a virtual machine and its export setting data.</span></span> <span data-ttu-id="53daf-105">Prima di chiamare il metodo [**ExportSystemDefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md) della classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) , è possibile recuperare un'istanza di [**MSVM \_ VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md) utilizzando questa associazione.</span><span class="sxs-lookup"><span data-stu-id="53daf-105">Before calling the [**ExportSystemDefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class, an instance of [**Msvm\_VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md) can be retrieved using this association.</span></span>

<span data-ttu-id="53daf-106">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="53daf-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="53daf-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="53daf-107">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SystemExportSettingData : CIM_ElementSettingData
{
  CIM_ComputerSystem                  REF ManagedElement;
  Msvm_VirtualSystemExportSettingData REF SettingData;
  uint16                                  IsDefault = 1;
  uint16                                  IsCurrent = 1;
  uint16                                  IsNext = 0;
};
```

## <a name="members"></a><span data-ttu-id="53daf-108">Members</span><span class="sxs-lookup"><span data-stu-id="53daf-108">Members</span></span>

<span data-ttu-id="53daf-109">La **classe \_ SystemExportSettingData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="53daf-109">The **Msvm\_SystemExportSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="53daf-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="53daf-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="53daf-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="53daf-111">Properties</span></span>

<span data-ttu-id="53daf-112">La **classe \_ SystemExportSettingData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="53daf-112">The **Msvm\_SystemExportSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="53daf-113">**IsCurrent**</span><span class="sxs-lookup"><span data-stu-id="53daf-113">**IsCurrent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53daf-114">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="53daf-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="53daf-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="53daf-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="53daf-116">Indica se l'impostazione a cui si fa riferimento è attualmente utilizzata nell'operazione dell'elemento o se queste informazioni sono sconosciute.</span><span class="sxs-lookup"><span data-stu-id="53daf-116">Indicates if the referenced setting is currently being used in the operation of the element, or that this information is unknown.</span></span> <span data-ttu-id="53daf-117">Questa proprietà viene ereditata da [**CIM \_ ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span><span class="sxs-lookup"><span data-stu-id="53daf-117">This property is inherited from [**CIM\_ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span></span>



| <span data-ttu-id="53daf-118">Valore</span><span class="sxs-lookup"><span data-stu-id="53daf-118">Value</span></span>                                                                        | <span data-ttu-id="53daf-119">Significato</span><span class="sxs-lookup"><span data-stu-id="53daf-119">Meaning</span></span>                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <span data-ttu-id="53daf-120"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="53daf-120"><dt>0</dt></span></span> </dl> | <span data-ttu-id="53daf-121">Sconosciuto</span><span class="sxs-lookup"><span data-stu-id="53daf-121">Unknown</span></span><br/>     |
| <dl> <span data-ttu-id="53daf-122"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="53daf-122"><dt>1</dt></span></span> </dl> | <span data-ttu-id="53daf-123">Corrente</span><span class="sxs-lookup"><span data-stu-id="53daf-123">Current</span></span><br/>     |
| <dl> <span data-ttu-id="53daf-124"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="53daf-124"><dt>2</dt></span></span> </dl> | <span data-ttu-id="53daf-125">Non corrente</span><span class="sxs-lookup"><span data-stu-id="53daf-125">Not Current</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="53daf-126">**IsDefault**</span><span class="sxs-lookup"><span data-stu-id="53daf-126">**IsDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53daf-127">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="53daf-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="53daf-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="53daf-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="53daf-129">Indica se l'impostazione a cui si fa riferimento è un'impostazione predefinita per l'elemento o che queste informazioni sono sconosciute.</span><span class="sxs-lookup"><span data-stu-id="53daf-129">Indicates if the referenced setting is a default setting for the element, or that this information is unknown.</span></span> <span data-ttu-id="53daf-130">Questa proprietà viene ereditata da [**CIM \_ ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span><span class="sxs-lookup"><span data-stu-id="53daf-130">This property is inherited from [**CIM\_ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span></span>



| <span data-ttu-id="53daf-131">Valore</span><span class="sxs-lookup"><span data-stu-id="53daf-131">Value</span></span>                                                                        | <span data-ttu-id="53daf-132">Significato</span><span class="sxs-lookup"><span data-stu-id="53daf-132">Meaning</span></span>                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <span data-ttu-id="53daf-133"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="53daf-133"><dt>0</dt></span></span> </dl> | <span data-ttu-id="53daf-134">Sconosciuto</span><span class="sxs-lookup"><span data-stu-id="53daf-134">Unknown</span></span><br/>     |
| <dl> <span data-ttu-id="53daf-135"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="53daf-135"><dt>1</dt></span></span> </dl> | <span data-ttu-id="53daf-136">Predefinito</span><span class="sxs-lookup"><span data-stu-id="53daf-136">Default</span></span><br/>     |
| <dl> <span data-ttu-id="53daf-137"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="53daf-137"><dt>2</dt></span></span> </dl> | <span data-ttu-id="53daf-138">Non predefinito</span><span class="sxs-lookup"><span data-stu-id="53daf-138">Not Default</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="53daf-139">**IsNext**</span><span class="sxs-lookup"><span data-stu-id="53daf-139">**IsNext**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53daf-140">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="53daf-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="53daf-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="53daf-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="53daf-142">Indica se l'impostazione a cui si fa riferimento è l'impostazione successiva da applicare.</span><span class="sxs-lookup"><span data-stu-id="53daf-142">Indicates whether or not the referenced setting is the next setting to be applied.</span></span> <span data-ttu-id="53daf-143">È ad esempio possibile che l'applicazione venga eseguita in una richiesta di reinizializzazione, reimpostazione o riconfigurazione.</span><span class="sxs-lookup"><span data-stu-id="53daf-143">For example, the application could take place on a re-initialization, reset, reconfiguration request.</span></span> <span data-ttu-id="53daf-144">Potrebbe trattarsi di un'impostazione permanente o di un'impostazione utilizzata solo una volta, come indicato dal flag.</span><span class="sxs-lookup"><span data-stu-id="53daf-144">This could be a permanent setting, or a setting used only one time, as indicated by the flag.</span></span> <span data-ttu-id="53daf-145">Se si tratta di un'impostazione permanente, l'impostazione viene applicata ogni volta che l'elemento gestito viene reinizializzato, finché questo flag non viene reimpostato manualmente.</span><span class="sxs-lookup"><span data-stu-id="53daf-145">If it is a permanent setting then the setting is applied every time the managed element reinitializes, until this flag is manually reset.</span></span> <span data-ttu-id="53daf-146">Tuttavia, se è monouso, il flag viene cancellato automaticamente dopo l'applicazione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="53daf-146">However, if it is single use, then the flag is automatically cleared after the settings are applied.</span></span> <span data-ttu-id="53daf-147">Inoltre, se questo flag è specificato (ad esempio, impostato su un valore diverso da 0 (sconosciuto)), questo ha la precedenza su tutti i dati di impostazione che potrebbero essere stati specificati come predefiniti.</span><span class="sxs-lookup"><span data-stu-id="53daf-147">Also, if this flag is specified (i.e. set to value other than 0 (Unknown)), then this takes precedence over any setting data that may have been specified as default.</span></span> <span data-ttu-id="53daf-148">Ad esempio, se l'elemento gestito è un computer e il valore di questo flag è 1 (è successivo), l'impostazione sarà effettiva al successivo ripristino del sistema.</span><span class="sxs-lookup"><span data-stu-id="53daf-148">For example: If the managed element is a computer system, and the value of this flag is 1 (Is Next), then the setting will be effective next time the system resets.</span></span> <span data-ttu-id="53daf-149">A meno che il flag non venga modificato, verrà mantenuto per le successive reimpostazioni di sistema.</span><span class="sxs-lookup"><span data-stu-id="53daf-149">And, unless this flag is changed, it will persist for subsequent system resets.</span></span> <span data-ttu-id="53daf-150">Tuttavia, se questo flag è impostato su 3 (è Next per l'uso singolo), questa impostazione verrà usata una sola volta e il flag verrebbe reimpostato dopo tale operazione su 2 (non è successivo).</span><span class="sxs-lookup"><span data-stu-id="53daf-150">However, if this flag is set to 3 (Is Next For Single Use), then this setting will only be used once and the flag would be reset after that to 2 (Is Not Next).</span></span> <span data-ttu-id="53daf-151">Nell'esempio precedente, se il sistema viene riavviato in una rapida successione, l'impostazione non verrà usata al secondo riavvio.</span><span class="sxs-lookup"><span data-stu-id="53daf-151">So, in the above example, if the system reboots in a quick succession, the setting will not be used at the second reboot.</span></span>

<span data-ttu-id="53daf-152">Questa proprietà viene ereditata da [**CIM \_ ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span><span class="sxs-lookup"><span data-stu-id="53daf-152">This property is inherited from [**CIM\_ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span></span>



| <span data-ttu-id="53daf-153">Valore</span><span class="sxs-lookup"><span data-stu-id="53daf-153">Value</span></span>                                                                        | <span data-ttu-id="53daf-154">Significato</span><span class="sxs-lookup"><span data-stu-id="53daf-154">Meaning</span></span>                           |
|------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="53daf-155"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="53daf-155"><dt>0</dt></span></span> </dl> | <span data-ttu-id="53daf-156">Sconosciuto</span><span class="sxs-lookup"><span data-stu-id="53daf-156">Unknown</span></span><br/>                |
| <dl> <span data-ttu-id="53daf-157"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="53daf-157"><dt>1</dt></span></span> </dl> | <span data-ttu-id="53daf-158">Successivo</span><span class="sxs-lookup"><span data-stu-id="53daf-158">Is Next</span></span><br/>                |
| <dl> <span data-ttu-id="53daf-159"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="53daf-159"><dt>2</dt></span></span> </dl> | <span data-ttu-id="53daf-160">Non è successivo</span><span class="sxs-lookup"><span data-stu-id="53daf-160">Is Not Next</span></span><br/>            |
| <dl> <span data-ttu-id="53daf-161"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="53daf-161"><dt>3</dt></span></span> </dl> | <span data-ttu-id="53daf-162">È Next per uso singolo</span><span class="sxs-lookup"><span data-stu-id="53daf-162">Is Next For Single Use</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="53daf-163">**ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="53daf-163">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53daf-164">Tipo di dati: **[ **CIM \_ ComputerSystem**](msvm-computersystem.md)**</span><span class="sxs-lookup"><span data-stu-id="53daf-164">Data type: **[**CIM\_ComputerSystem**](msvm-computersystem.md)**</span></span>
</dt> <dt>

<span data-ttu-id="53daf-165">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="53daf-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53daf-166">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ ElementSettingData. Managed")</span><span class="sxs-lookup"><span data-stu-id="53daf-166">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_ElementSettingData.ManagedElement")</span></span>
</dt> </dl>

<span data-ttu-id="53daf-167">Riferimento alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="53daf-167">Reference to the virtual machine.</span></span> <span data-ttu-id="53daf-168">Questa proprietà viene ereditata da [**CIM \_ ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span><span class="sxs-lookup"><span data-stu-id="53daf-168">This property is inherited from [**CIM\_ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="53daf-169">**SettingData**</span><span class="sxs-lookup"><span data-stu-id="53daf-169">**SettingData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53daf-170">Tipo di dati: **[ **MSVM \_ VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md)**</span><span class="sxs-lookup"><span data-stu-id="53daf-170">Data type: **[**Msvm\_VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md)**</span></span>
</dt> <dt>

<span data-ttu-id="53daf-171">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="53daf-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53daf-172">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ ElementSettingData. SettingData")</span><span class="sxs-lookup"><span data-stu-id="53daf-172">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_ElementSettingData.SettingData")</span></span>
</dt> </dl>

<span data-ttu-id="53daf-173">Riferimento ai dati delle impostazioni di esportazione per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="53daf-173">Reference to the export setting data for the virtual machine.</span></span> <span data-ttu-id="53daf-174">Questa proprietà viene ereditata da [**CIM \_ ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span><span class="sxs-lookup"><span data-stu-id="53daf-174">This property is inherited from [**CIM\_ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="53daf-175">Commenti</span><span class="sxs-lookup"><span data-stu-id="53daf-175">Remarks</span></span>

<span data-ttu-id="53daf-176">L'accesso alla **classe \_ SystemExportSettingData di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="53daf-176">Access to the **Msvm\_SystemExportSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="53daf-177">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="53daf-177">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="53daf-178">Requisiti</span><span class="sxs-lookup"><span data-stu-id="53daf-178">Requirements</span></span>



| <span data-ttu-id="53daf-179">Requisito</span><span class="sxs-lookup"><span data-stu-id="53daf-179">Requirement</span></span> | <span data-ttu-id="53daf-180">Valore</span><span class="sxs-lookup"><span data-stu-id="53daf-180">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53daf-181">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="53daf-181">Minimum supported client</span></span><br/> | <span data-ttu-id="53daf-182">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="53daf-182">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="53daf-183">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="53daf-183">Minimum supported server</span></span><br/> | <span data-ttu-id="53daf-184">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="53daf-184">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="53daf-185">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="53daf-185">Namespace</span></span><br/>                | <span data-ttu-id="53daf-186">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="53daf-186">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="53daf-187">MOF</span><span class="sxs-lookup"><span data-stu-id="53daf-187">MOF</span></span><br/>                      | <dl> <span data-ttu-id="53daf-188"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="53daf-188"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="53daf-189">DLL</span><span class="sxs-lookup"><span data-stu-id="53daf-189">DLL</span></span><br/>                      | <dl> <span data-ttu-id="53daf-190"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="53daf-190"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

