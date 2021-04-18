---
description: Associa un elemento gestito ai relativi dati di configurazione.
ms.assetid: 4DB78E43-E387-478E-999C-770B35925721
title: Classe Msvm_ElementSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ElementSettingData
- Msvm_ElementSettingData.ManagedElement
- Msvm_ElementSettingData.SettingData
- Msvm_ElementSettingData.IsDefault
- Msvm_ElementSettingData.IsCurrent
- Msvm_ElementSettingData.IsNext
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9f4d2af614e3b161f49a0d37d1e4d1ee48ce0aad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307930"
---
# <a name="msvm_elementsettingdata-class"></a><span data-ttu-id="e4adc-103">\_Classe MSVM ElementSettingData</span><span class="sxs-lookup"><span data-stu-id="e4adc-103">Msvm\_ElementSettingData class</span></span>

<span data-ttu-id="e4adc-104">Associa un elemento gestito ai relativi dati di configurazione.</span><span class="sxs-lookup"><span data-stu-id="e4adc-104">Associates a managed element with its configuration data.</span></span> <span data-ttu-id="e4adc-105">Alcune delle applicazioni più importanti di questa associazione sono l'uso del collegamento di una macchina virtuale e dei dispositivi logici assegnati a tale sistema con le relative informazioni di configurazione dello snapshot.</span><span class="sxs-lookup"><span data-stu-id="e4adc-105">Some of the more notable applications of this association are its use in linking a virtual machine and the logical devices that have been assigned to that system with their snapshot configuration information.</span></span> <span data-ttu-id="e4adc-106">Le informazioni di configurazione correnti sono associate alla macchina virtuale e ai relativi dispositivi mediante l'associazione [**MSVM \_ SettingsDefineState**](msvm-settingsdefinestate.md) .</span><span class="sxs-lookup"><span data-stu-id="e4adc-106">Current configuration information is associated with the virtual machine and its devices through the [**Msvm\_SettingsDefineState**](msvm-settingsdefinestate.md) association.</span></span>

<span data-ttu-id="e4adc-107">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="e4adc-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4adc-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e4adc-108">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ElementSettingData : CIM_ElementSettingData
{
  CIM_ManagedElement REF ManagedElement;
  CIM_SettingData    REF SettingData;
  uint16                 IsDefault = 0;
  uint16                 IsCurrent = 0;
  uint16                 IsNext = 0;
};
```

## <a name="members"></a><span data-ttu-id="e4adc-109">Members</span><span class="sxs-lookup"><span data-stu-id="e4adc-109">Members</span></span>

<span data-ttu-id="e4adc-110">La **classe \_ ElementSettingData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e4adc-110">The **Msvm\_ElementSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="e4adc-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e4adc-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e4adc-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e4adc-112">Properties</span></span>

<span data-ttu-id="e4adc-113">La **classe \_ ElementSettingData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="e4adc-113">The **Msvm\_ElementSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e4adc-114">**IsCurrent**</span><span class="sxs-lookup"><span data-stu-id="e4adc-114">**IsCurrent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4adc-115">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e4adc-115">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e4adc-116">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e4adc-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4adc-117">Indica che l'impostazione a cui si fa riferimento è attualmente utilizzata nell'operazione dell'elemento o che queste informazioni sono sconosciute.</span><span class="sxs-lookup"><span data-stu-id="e4adc-117">Indicates that the referenced setting is currently being used in the operation of the element or that this information is unknown.</span></span> <span data-ttu-id="e4adc-118">Questa proprietà viene ereditata da [**CIM \_ ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span><span class="sxs-lookup"><span data-stu-id="e4adc-118">This property is inherited from [**CIM\_ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span></span> <span data-ttu-id="e4adc-119">Il valore predefinito è 0 (sconosciuto).</span><span class="sxs-lookup"><span data-stu-id="e4adc-119">The default value is 0 (Unknown).</span></span>

<dl> <dt>

<span data-ttu-id="e4adc-120"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="e4adc-120"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e4adc-121"><span id="Is_Current"></span><span id="is_current"></span><span id="IS_CURRENT"></span>**È corrente** (1)</span><span class="sxs-lookup"><span data-stu-id="e4adc-121"><span id="Is_Current"></span><span id="is_current"></span><span id="IS_CURRENT"></span>**Is Current** (1)</span></span>
</dt> <dt>

<span data-ttu-id="e4adc-122"><span id="Is_Not_Current"></span><span id="is_not_current"></span><span id="IS_NOT_CURRENT"></span>**Non è corrente** (2)</span><span class="sxs-lookup"><span data-stu-id="e4adc-122"><span id="Is_Not_Current"></span><span id="is_not_current"></span><span id="IS_NOT_CURRENT"></span>**Is Not Current** (2)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e4adc-123">**IsDefault**</span><span class="sxs-lookup"><span data-stu-id="e4adc-123">**IsDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4adc-124">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e4adc-124">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e4adc-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e4adc-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4adc-126">Indica che l'impostazione a cui si fa riferimento è un'impostazione predefinita per l'elemento o che queste informazioni sono sconosciute.</span><span class="sxs-lookup"><span data-stu-id="e4adc-126">Indicates that the referenced setting is a default setting for the element or that this information is unknown.</span></span> <span data-ttu-id="e4adc-127">Questa proprietà viene ereditata da [**CIM \_ ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span><span class="sxs-lookup"><span data-stu-id="e4adc-127">This property is inherited from [**CIM\_ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span></span> <span data-ttu-id="e4adc-128">Il valore predefinito è 0 (sconosciuto).</span><span class="sxs-lookup"><span data-stu-id="e4adc-128">The default value is 0 (Unknown).</span></span>

<dl> <dt>

<span data-ttu-id="e4adc-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="e4adc-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e4adc-130"><span id="Is_Default"></span><span id="is_default"></span><span id="IS_DEFAULT"></span>**È il valore predefinito** (1)</span><span class="sxs-lookup"><span data-stu-id="e4adc-130"><span id="Is_Default"></span><span id="is_default"></span><span id="IS_DEFAULT"></span>**Is Default** (1)</span></span>
</dt> <dt>

<span data-ttu-id="e4adc-131"><span id="Is_Not_Default"></span><span id="is_not_default"></span><span id="IS_NOT_DEFAULT"></span>**Non è predefinito** (2)</span><span class="sxs-lookup"><span data-stu-id="e4adc-131"><span id="Is_Not_Default"></span><span id="is_not_default"></span><span id="IS_NOT_DEFAULT"></span>**Is Not Default** (2)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e4adc-132">**IsNext**</span><span class="sxs-lookup"><span data-stu-id="e4adc-132">**IsNext**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4adc-133">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e4adc-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e4adc-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e4adc-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4adc-135">Indica se l'impostazione a cui si fa riferimento è l'impostazione successiva da applicare.</span><span class="sxs-lookup"><span data-stu-id="e4adc-135">Indicates whether the referenced setting is the next setting to be applied.</span></span> <span data-ttu-id="e4adc-136">Questa proprietà viene ereditata da [**CIM \_ ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span><span class="sxs-lookup"><span data-stu-id="e4adc-136">This property is inherited from [**CIM\_ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span></span> <span data-ttu-id="e4adc-137">Il valore predefinito è 0 (sconosciuto).</span><span class="sxs-lookup"><span data-stu-id="e4adc-137">The default value is 0 (Unknown).</span></span>

<dl> <dt>

<span data-ttu-id="e4adc-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="e4adc-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e4adc-139"><span id="Is_Next"></span><span id="is_next"></span><span id="IS_NEXT"></span>**Successivo** (1)</span><span class="sxs-lookup"><span data-stu-id="e4adc-139"><span id="Is_Next"></span><span id="is_next"></span><span id="IS_NEXT"></span>**Is Next** (1)</span></span>
</dt> <dt>

<span data-ttu-id="e4adc-140"><span id="Is_Not_Next"></span><span id="is_not_next"></span><span id="IS_NOT_NEXT"></span>**Non è Next** (2)</span><span class="sxs-lookup"><span data-stu-id="e4adc-140"><span id="Is_Not_Next"></span><span id="is_not_next"></span><span id="IS_NOT_NEXT"></span>**Is Not Next** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e4adc-141"><span id="Is_Next_For_Single_Use"></span><span id="is_next_for_single_use"></span><span id="IS_NEXT_FOR_SINGLE_USE"></span>**È successivo per uso singolo** (3)</span><span class="sxs-lookup"><span data-stu-id="e4adc-141"><span id="Is_Next_For_Single_Use"></span><span id="is_next_for_single_use"></span><span id="IS_NEXT_FOR_SINGLE_USE"></span>**Is Next For Single Use** (3)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e4adc-142">**ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="e4adc-142">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4adc-143">Tipo di dati: **[ **CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="e4adc-143">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="e4adc-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e4adc-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4adc-145">Riferimento alla macchina virtuale o al dispositivo virtuale.</span><span class="sxs-lookup"><span data-stu-id="e4adc-145">Reference to the virtual machine or virtual device.</span></span> <span data-ttu-id="e4adc-146">Questa proprietà viene ereditata da [**CIM \_ ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span><span class="sxs-lookup"><span data-stu-id="e4adc-146">This property is inherited from [**CIM\_ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="e4adc-147">**SettingData**</span><span class="sxs-lookup"><span data-stu-id="e4adc-147">**SettingData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4adc-148">Tipo di dati: **[ **CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="e4adc-148">Data type: **[**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="e4adc-149">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e4adc-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4adc-150">Riferimento alle impostazioni di snapshotted per la macchina virtuale o il dispositivo virtuale.</span><span class="sxs-lookup"><span data-stu-id="e4adc-150">Reference to the snapshotted settings for the virtual machine or virtual device.</span></span> <span data-ttu-id="e4adc-151">Questa proprietà viene ereditata da [**CIM \_ ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span><span class="sxs-lookup"><span data-stu-id="e4adc-151">This property is inherited from [**CIM\_ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e4adc-152">Commenti</span><span class="sxs-lookup"><span data-stu-id="e4adc-152">Remarks</span></span>

<span data-ttu-id="e4adc-153">L'accesso alla **classe \_ ElementSettingData di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="e4adc-153">Access to the **Msvm\_ElementSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="e4adc-154">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="e4adc-154">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="e4adc-155">Esempio</span><span class="sxs-lookup"><span data-stu-id="e4adc-155">Examples</span></span>

<span data-ttu-id="e4adc-156">Vedere [esecuzione di query sugli oggetti di rete](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="e4adc-156">See [Querying Networking Objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e4adc-157">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e4adc-157">Requirements</span></span>



| <span data-ttu-id="e4adc-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4adc-158">Requirement</span></span> | <span data-ttu-id="e4adc-159">Valore</span><span class="sxs-lookup"><span data-stu-id="e4adc-159">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4adc-160">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e4adc-160">Minimum supported client</span></span><br/> | <span data-ttu-id="e4adc-161">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="e4adc-161">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e4adc-162">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e4adc-162">Minimum supported server</span></span><br/> | <span data-ttu-id="e4adc-163">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="e4adc-163">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e4adc-164">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e4adc-164">Namespace</span></span><br/>                | <span data-ttu-id="e4adc-165">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="e4adc-165">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e4adc-166">MOF</span><span class="sxs-lookup"><span data-stu-id="e4adc-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e4adc-167"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e4adc-167"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e4adc-168">DLL</span><span class="sxs-lookup"><span data-stu-id="e4adc-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e4adc-169"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e4adc-169"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e4adc-170">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e4adc-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4adc-171">**\_ELEMENTSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="e4adc-171">**CIM\_ElementSettingData**</span></span>](cim-elementsettingdata.md)
</dt> <dt>

[<span data-ttu-id="e4adc-172">**\_ELEMENTSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="e4adc-172">**CIM\_ElementSettingData**</span></span>](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata)
</dt> <dt>

[<span data-ttu-id="e4adc-173">Classi di gestione del sistema virtuale</span><span class="sxs-lookup"><span data-stu-id="e4adc-173">Virtual System Management Classes</span></span>](virtual-system-management-classes.md)
</dt> </dl>

 

