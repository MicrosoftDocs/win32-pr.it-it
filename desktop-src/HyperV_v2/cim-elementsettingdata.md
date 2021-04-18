---
description: Rappresenta un'associazione tra un elemento gestito e i dati di impostazione associati. Questa associazione descrive anche se si tratta di un'impostazione predefinita o corrente.
ms.assetid: 0df2b235-76d9-4899-938b-274ec5471324
title: Classe CIM_ElementSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementSettingData
- CIM_ElementSettingData.ManagedElement
- CIM_ElementSettingData.SettingData
- CIM_ElementSettingData.IsDefault
- CIM_ElementSettingData.IsCurrent
- CIM_ElementSettingData.IsNext
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e22dbd221f2e83009e4268cc0de337374e04298a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312932"
---
# <a name="cim_elementsettingdata-class"></a><span data-ttu-id="4da6e-104">CIM \_ ElementSettingData (classe)</span><span class="sxs-lookup"><span data-stu-id="4da6e-104">CIM\_ElementSettingData class</span></span>

<span data-ttu-id="4da6e-105">Rappresenta un'associazione tra un elemento gestito e i dati di impostazione associati.</span><span class="sxs-lookup"><span data-stu-id="4da6e-105">Represents an association between a managed element and its associated setting data.</span></span> <span data-ttu-id="4da6e-106">Questa associazione descrive anche se si tratta di un'impostazione predefinita o corrente.</span><span class="sxs-lookup"><span data-stu-id="4da6e-106">This association also describes whether this is a default or current setting.</span></span>

## <a name="syntax"></a><span data-ttu-id="4da6e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4da6e-107">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.19.1"), UMLPackagePath("CIM::Core::Settings"), AMENDMENT]
class CIM_ElementSettingData
{
  CIM_ManagedElement REF ManagedElement;
  CIM_SettingData    REF SettingData;
  uint16                 IsDefault;
  uint16                 IsCurrent;
  uint16                 IsNext;
};
```

## <a name="members"></a><span data-ttu-id="4da6e-108">Members</span><span class="sxs-lookup"><span data-stu-id="4da6e-108">Members</span></span>

<span data-ttu-id="4da6e-109">La classe **CIM \_ ElementSettingData** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="4da6e-109">The **CIM\_ElementSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="4da6e-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4da6e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4da6e-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4da6e-111">Properties</span></span>

<span data-ttu-id="4da6e-112">La classe **CIM \_ ElementSettingData** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="4da6e-112">The **CIM\_ElementSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4da6e-113">**IsCurrent**</span><span class="sxs-lookup"><span data-stu-id="4da6e-113">**IsCurrent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4da6e-114">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4da6e-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4da6e-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4da6e-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4da6e-116">Indica se l'impostazione a cui si fa riferimento è attualmente utilizzata dall'elemento.</span><span class="sxs-lookup"><span data-stu-id="4da6e-116">Indicates whether the referenced setting is currently being used by the element.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4da6e-117">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="4da6e-117">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Is_Current"></span><span id="is_current"></span><span id="IS_CURRENT"></span>

<span data-ttu-id="4da6e-118">**È corrente** (1)</span><span class="sxs-lookup"><span data-stu-id="4da6e-118">**Is Current** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Is_Not_Current"></span><span id="is_not_current"></span><span id="IS_NOT_CURRENT"></span>

<span data-ttu-id="4da6e-119">**Non è corrente** (2)</span><span class="sxs-lookup"><span data-stu-id="4da6e-119">**Is Not Current** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4da6e-120">**IsDefault**</span><span class="sxs-lookup"><span data-stu-id="4da6e-120">**IsDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4da6e-121">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4da6e-121">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4da6e-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4da6e-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4da6e-123">Che indica se l'impostazione è un'impostazione predefinita per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="4da6e-123">Indicating whether the setting is a default setting for the element.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4da6e-124">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="4da6e-124">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Is_Default"></span><span id="is_default"></span><span id="IS_DEFAULT"></span>

<span data-ttu-id="4da6e-125">**È il valore predefinito** (1)</span><span class="sxs-lookup"><span data-stu-id="4da6e-125">**Is Default** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Is_Not_Default"></span><span id="is_not_default"></span><span id="IS_NOT_DEFAULT"></span>

<span data-ttu-id="4da6e-126">**Non è predefinito** (2)</span><span class="sxs-lookup"><span data-stu-id="4da6e-126">**Is Not Default** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4da6e-127">**IsNext**</span><span class="sxs-lookup"><span data-stu-id="4da6e-127">**IsNext**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4da6e-128">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4da6e-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4da6e-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4da6e-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4da6e-130">Flag che indica quando e con quale frequenza applicare l'impostazione.</span><span class="sxs-lookup"><span data-stu-id="4da6e-130">A flag that indicates when and how often to apply the setting.</span></span>

<span data-ttu-id="4da6e-131">Ad esempio, l'impostazione può essere applicata a una richiesta di reinizializzazione, reimpostazione o riconfigurazione.</span><span class="sxs-lookup"><span data-stu-id="4da6e-131">For example, the setting could be applied on a re-initialization, reset, reconfiguration request.</span></span> <span data-ttu-id="4da6e-132">Potrebbe trattarsi di un'impostazione permanente o di un'impostazione utilizzata solo una volta, come indicato dal flag.</span><span class="sxs-lookup"><span data-stu-id="4da6e-132">This could be a permanent setting, or a setting used only one time, as indicated by the flag.</span></span> <span data-ttu-id="4da6e-133">Se si tratta di un'impostazione permanente, l'impostazione viene applicata ogni volta che l'elemento gestito viene reinizializzato, finché questo flag non viene reimpostato manualmente.</span><span class="sxs-lookup"><span data-stu-id="4da6e-133">If it is a permanent setting then the setting is applied every time the managed element reinitializes, until this flag is manually reset.</span></span> <span data-ttu-id="4da6e-134">Tuttavia, se è monouso, il flag viene cancellato automaticamente dopo l'applicazione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="4da6e-134">However, if it is single use, then the flag is automatically cleared after the settings are applied.</span></span> <span data-ttu-id="4da6e-135">Inoltre, se questo flag è impostato su un valore diverso da 0 (sconosciuto), ha la precedenza su una proprietà **SettingData** impostata su "default".</span><span class="sxs-lookup"><span data-stu-id="4da6e-135">In addition, if this flag is set to value other than 0 (Unknown), then this takes precedence over a **SettingData** property that is set to "Default".</span></span>

<span data-ttu-id="4da6e-136">Se l'elemento gestito è un computer e il valore di questo flag è "Next", l'impostazione sarà valida al successivo ripristino del sistema.</span><span class="sxs-lookup"><span data-stu-id="4da6e-136">If the managed element is a computer system, and the value of this flag is "Is Next", then the setting will be effective next time the system resets.</span></span> <span data-ttu-id="4da6e-137">A meno che il flag non venga modificato, verrà mantenuto per le successive reimpostazioni di sistema.</span><span class="sxs-lookup"><span data-stu-id="4da6e-137">And, unless this flag is changed, it will persist for subsequent system resets.</span></span> <span data-ttu-id="4da6e-138">Tuttavia, se questo flag è impostato su "è successivo per l'uso singolo", questa impostazione verrà usata una sola volta e il flag verrà reimpostato dopo tale operazione su 2 (non è successivo).</span><span class="sxs-lookup"><span data-stu-id="4da6e-138">However, if this flag is set to "Is Next For Single Use", then this setting will only be used once and the flag would be reset after that to 2 (Is Not Next).</span></span> <span data-ttu-id="4da6e-139">Nell'esempio precedente, se il sistema viene riavviato in una rapida successione, l'impostazione non verrà usata al secondo riavvio.</span><span class="sxs-lookup"><span data-stu-id="4da6e-139">So, in the above example, if the system reboots in a quick succession, the setting will not be used at the second reboot.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4da6e-140">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="4da6e-140">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Is_Next"></span><span id="is_next"></span><span id="IS_NEXT"></span>

<span data-ttu-id="4da6e-141">**Successivo** (1)</span><span class="sxs-lookup"><span data-stu-id="4da6e-141">**Is Next** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Is_Not_Next"></span><span id="is_not_next"></span><span id="IS_NOT_NEXT"></span>

<span data-ttu-id="4da6e-142">**Non è Next** (2)</span><span class="sxs-lookup"><span data-stu-id="4da6e-142">**Is Not Next** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Is_Next_For_Single_Use"></span><span id="is_next_for_single_use"></span><span id="IS_NEXT_FOR_SINGLE_USE"></span>

<span data-ttu-id="4da6e-143">**È successivo per uso singolo** (3)</span><span class="sxs-lookup"><span data-stu-id="4da6e-143">**Is Next For Single Use** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4da6e-144">**ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="4da6e-144">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4da6e-145">Tipo di dati: **CIM \_ Managed**</span><span class="sxs-lookup"><span data-stu-id="4da6e-145">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="4da6e-146">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4da6e-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4da6e-147">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4da6e-147">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="4da6e-148">Elemento gestito.</span><span class="sxs-lookup"><span data-stu-id="4da6e-148">The managed element.</span></span>

</dd> <dt>

<span data-ttu-id="4da6e-149">**SettingData**</span><span class="sxs-lookup"><span data-stu-id="4da6e-149">**SettingData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4da6e-150">Tipo di dati: **CIM \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="4da6e-150">Data type: **CIM\_SettingData**</span></span>
</dt> <dt>

<span data-ttu-id="4da6e-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4da6e-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4da6e-152">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4da6e-152">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="4da6e-153">Dati dell'impostazione associati all'elemento.</span><span class="sxs-lookup"><span data-stu-id="4da6e-153">The setting data associated with the element.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4da6e-154">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4da6e-154">Requirements</span></span>



| <span data-ttu-id="4da6e-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="4da6e-155">Requirement</span></span> | <span data-ttu-id="4da6e-156">Valore</span><span class="sxs-lookup"><span data-stu-id="4da6e-156">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4da6e-157">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4da6e-157">Minimum supported client</span></span><br/> | <span data-ttu-id="4da6e-158">Windows 8</span><span class="sxs-lookup"><span data-stu-id="4da6e-158">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="4da6e-159">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4da6e-159">Minimum supported server</span></span><br/> | <span data-ttu-id="4da6e-160">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4da6e-160">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="4da6e-161">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4da6e-161">Namespace</span></span><br/>                | <span data-ttu-id="4da6e-162">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="4da6e-162">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="4da6e-163">MOF</span><span class="sxs-lookup"><span data-stu-id="4da6e-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4da6e-164"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4da6e-164"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4da6e-165">DLL</span><span class="sxs-lookup"><span data-stu-id="4da6e-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4da6e-166"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4da6e-166"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

