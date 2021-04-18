---
description: Rappresenta lo stato di configurazione delle impostazioni di merge del disco per una macchina virtuale.
ms.assetid: b4c0afeb-ce37-4eec-8aba-0d74115c463f
title: Classe Msvm_DiskMergeSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DiskMergeSettingData
- Msvm_DiskMergeSettingData.InstanceID
- Msvm_DiskMergeSettingData.Caption
- Msvm_DiskMergeSettingData.Description
- Msvm_DiskMergeSettingData.ElementName
- Msvm_DiskMergeSettingData.EnabledState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: fe702c382fb0636579a8ab1355bfd1299657b214
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317190"
---
# <a name="msvm_diskmergesettingdata-class"></a><span data-ttu-id="d333e-103">\_Classe MSVM DiskMergeSettingData</span><span class="sxs-lookup"><span data-stu-id="d333e-103">Msvm\_DiskMergeSettingData class</span></span>

<span data-ttu-id="d333e-104">Rappresenta lo stato di configurazione delle impostazioni di merge del disco per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d333e-104">Represents the configuration state of the disk merge settings for a virtual machine.</span></span>

<span data-ttu-id="d333e-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="d333e-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d333e-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d333e-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_DiskMergeSettingData : CIM_SettingData
{
  string InstanceID = "Microsoft:GUID\DeviceSpecificData";
  string Caption = "Disk Merge Setting Data";
  string Description = "Microsoft Disk Merge Setting Data";
  string ElementName = "Disk Merge Setting Data";
  uint32 EnabledState = 1;
};
```

## <a name="members"></a><span data-ttu-id="d333e-107">Members</span><span class="sxs-lookup"><span data-stu-id="d333e-107">Members</span></span>

<span data-ttu-id="d333e-108">La **classe \_ DiskMergeSettingData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="d333e-108">The **Msvm\_DiskMergeSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="d333e-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d333e-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d333e-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d333e-110">Properties</span></span>

<span data-ttu-id="d333e-111">La **classe \_ DiskMergeSettingData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="d333e-111">The **Msvm\_DiskMergeSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d333e-112">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="d333e-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d333e-113">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d333e-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d333e-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d333e-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d333e-115">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d333e-115">A short description of the object.</span></span> <span data-ttu-id="d333e-116">Questa proprietà viene ereditata dalla classe [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) ed è sempre impostata su "dati di impostazione Unione dischi".</span><span class="sxs-lookup"><span data-stu-id="d333e-116">This property is inherited from the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class and is always set to "Disk Merge Setting Data".</span></span>

</dd> <dt>

<span data-ttu-id="d333e-117">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="d333e-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d333e-118">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d333e-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d333e-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d333e-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d333e-120">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="d333e-120">A description of the object.</span></span> <span data-ttu-id="d333e-121">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Microsoft Disk merge data setting data".</span><span class="sxs-lookup"><span data-stu-id="d333e-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft Disk Merge Setting Data".</span></span>

</dd> <dt>

<span data-ttu-id="d333e-122">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="d333e-122">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d333e-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d333e-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d333e-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d333e-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d333e-125">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d333e-125">A display name for the object.</span></span> <span data-ttu-id="d333e-126">Questa proprietà viene ereditata da [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))ed è sempre impostata su "disk merge setting data".</span><span class="sxs-lookup"><span data-stu-id="d333e-126">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)), and it is always set to "Disk Merge Setting Data".</span></span> <span data-ttu-id="d333e-127">La modifica di questa proprietà comporterà la modifica della proprietà **ElementName** del derivato [**\_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) associato.</span><span class="sxs-lookup"><span data-stu-id="d333e-127">Changing this property will change the **ElementName** property of the associated [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) derivative.</span></span>

<span data-ttu-id="d333e-128">Si tratta di una proprietà di sola lettura, ma può essere modificata tramite il metodo [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) della classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="d333e-128">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="d333e-129">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="d333e-129">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d333e-130">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d333e-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d333e-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d333e-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d333e-132">Specifica lo stato abilitato della funzionalità di Unione dischi.</span><span class="sxs-lookup"><span data-stu-id="d333e-132">Specifies the enabled state of the disk merge functionality.</span></span>

<dt>

<span id="Temporarily_disabled"></span><span id="temporarily_disabled"></span><span id="TEMPORARILY_DISABLED"></span>

<span data-ttu-id="d333e-133">**Disabilitato temporaneamente** (0)</span><span class="sxs-lookup"><span data-stu-id="d333e-133">**Temporarily disabled** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="d333e-134">**Abilitato** (1)</span><span class="sxs-lookup"><span data-stu-id="d333e-134">**Enabled** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d333e-135">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d333e-135">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d333e-136">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d333e-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d333e-137">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d333e-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d333e-138">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="d333e-138">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="d333e-139">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="d333e-139">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="d333e-140">Questa proprietà viene ereditata da [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)) ed è sempre impostata su "Microsoft:*GUID* \\ *DeviceSpecificData*".</span><span class="sxs-lookup"><span data-stu-id="d333e-140">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)) and is always set to "Microsoft:*GUID*\\*DeviceSpecificData*".</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d333e-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d333e-141">Requirements</span></span>



| <span data-ttu-id="d333e-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="d333e-142">Requirement</span></span> | <span data-ttu-id="d333e-143">Valore</span><span class="sxs-lookup"><span data-stu-id="d333e-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d333e-144">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d333e-144">Minimum supported client</span></span><br/> | <span data-ttu-id="d333e-145">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="d333e-145">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d333e-146">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d333e-146">Minimum supported server</span></span><br/> | <span data-ttu-id="d333e-147">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="d333e-147">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d333e-148">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d333e-148">Namespace</span></span><br/>                | <span data-ttu-id="d333e-149">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="d333e-149">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d333e-150">MOF</span><span class="sxs-lookup"><span data-stu-id="d333e-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d333e-151"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d333e-151"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d333e-152">DLL</span><span class="sxs-lookup"><span data-stu-id="d333e-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d333e-153"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d333e-153"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

