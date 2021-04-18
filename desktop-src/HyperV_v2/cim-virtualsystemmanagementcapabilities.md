---
description: Rappresenta le funzionalità di un \_ oggetto VIRTUALSYSTEMMANAGEMENTSERVICE CIM.
ms.assetid: 484b0378-b354-49c4-b98b-a960a7b07b92
title: Classe CIM_VirtualSystemManagementCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementCapabilities
- CIM_VirtualSystemManagementCapabilities.VirtualSystemTypesSupported
- CIM_VirtualSystemManagementCapabilities.SynchronousMethodsSupported
- CIM_VirtualSystemManagementCapabilities.AsynchronousMethodsSupported
- CIM_VirtualSystemManagementCapabilities.IndicationsSupported
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2772068ed011a2a61cdd4f5c1396e057838b7720
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310555"
---
# <a name="cim_virtualsystemmanagementcapabilities-class"></a><span data-ttu-id="19185-103">CIM \_ VirtualSystemManagementCapabilities (classe)</span><span class="sxs-lookup"><span data-stu-id="19185-103">CIM\_VirtualSystemManagementCapabilities class</span></span>

<span data-ttu-id="19185-104">Rappresenta le funzionalità di un [**oggetto \_ VirtualSystemManagementService CIM**](cim-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="19185-104">Represents the capabilities of a [**CIM\_VirtualSystemManagementService**](cim-virtualsystemmanagementservice.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="19185-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="19185-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.23.0"), UMLPackagePath("CIM::Core::Virtualization"), AMENDMENT]
class CIM_VirtualSystemManagementCapabilities : CIM_EnabledLogicalElementCapabilities
{
  string VirtualSystemTypesSupported[];
  uint16 SynchronousMethodsSupported[];
  uint16 AsynchronousMethodsSupported[];
  uint16 IndicationsSupported[];
};
```

## <a name="members"></a><span data-ttu-id="19185-106">Members</span><span class="sxs-lookup"><span data-stu-id="19185-106">Members</span></span>

<span data-ttu-id="19185-107">La classe **CIM \_ VirtualSystemManagementCapabilities** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="19185-107">The **CIM\_VirtualSystemManagementCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="19185-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="19185-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="19185-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="19185-109">Properties</span></span>

<span data-ttu-id="19185-110">La classe **CIM \_ VirtualSystemManagementCapabilities** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="19185-110">The **CIM\_VirtualSystemManagementCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="19185-111">**AsynchronousMethodsSupported**</span><span class="sxs-lookup"><span data-stu-id="19185-111">**AsynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19185-112">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="19185-112">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="19185-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="19185-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="19185-114">Matrice che contiene i nomi di metodo per i metodi della classe [**CIM \_ VirtualSystemManagementService**](cim-virtualsystemmanagementservice.md) supportati per le operazioni asincrone.</span><span class="sxs-lookup"><span data-stu-id="19185-114">An array that contains method names for the [**CIM\_VirtualSystemManagementService**](cim-virtualsystemmanagementservice.md) class methods that are supported for asynchronous operations.</span></span>

<dt>

<span id="DefineSystemSupported"></span><span id="definesystemsupported"></span><span id="DEFINESYSTEMSUPPORTED"></span>

<span data-ttu-id="19185-115">**DefineSystemSupported** (2)</span><span class="sxs-lookup"><span data-stu-id="19185-115">**DefineSystemSupported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="DestroySystemSupported"></span><span id="destroysystemsupported"></span><span id="DESTROYSYSTEMSUPPORTED"></span>

<span data-ttu-id="19185-116">**DestroySystemSupported** (3)</span><span class="sxs-lookup"><span data-stu-id="19185-116">**DestroySystemSupported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DestroySystemConfigurationSupported"></span><span id="destroysystemconfigurationsupported"></span><span id="DESTROYSYSTEMCONFIGURATIONSUPPORTED"></span>

<span data-ttu-id="19185-117">**DestroySystemConfigurationSupported** (4)</span><span class="sxs-lookup"><span data-stu-id="19185-117">**DestroySystemConfigurationSupported** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyResourceSettingsSupported"></span><span id="modifyresourcesettingssupported"></span><span id="MODIFYRESOURCESETTINGSSUPPORTED"></span>

<span data-ttu-id="19185-118">**ModifyResourceSettingsSupported** (5)</span><span class="sxs-lookup"><span data-stu-id="19185-118">**ModifyResourceSettingsSupported** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifySystemSettingsSupported"></span><span id="modifysystemsettingssupported"></span><span id="MODIFYSYSTEMSETTINGSSUPPORTED"></span>

<span data-ttu-id="19185-119">**ModifySystemSettingsSupported** (6)</span><span class="sxs-lookup"><span data-stu-id="19185-119">**ModifySystemSettingsSupported** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveResourcesSupported"></span><span id="removeresourcessupported"></span><span id="REMOVERESOURCESSUPPORTED"></span>

<span data-ttu-id="19185-120">**RemoveResourcesSupported** (7)</span><span class="sxs-lookup"><span data-stu-id="19185-120">**RemoveResourcesSupported** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SelectSystemConfigurationSupported"></span><span id="selectsystemconfigurationsupported"></span><span id="SELECTSYSTEMCONFIGURATIONSUPPORTED"></span>

<span data-ttu-id="19185-121">**SelectSystemConfigurationSupported** (8)</span><span class="sxs-lookup"><span data-stu-id="19185-121">**SelectSystemConfigurationSupported** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SnapshotSystemSupported"></span><span id="snapshotsystemsupported"></span><span id="SNAPSHOTSYSTEMSUPPORTED"></span>

<span data-ttu-id="19185-122">**SnapshotSystemSupported** (9)</span><span class="sxs-lookup"><span data-stu-id="19185-122">**SnapshotSystemSupported** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="AddResourcesSupported"></span><span id="addresourcessupported"></span><span id="ADDRESOURCESSUPPORTED"></span>

<span data-ttu-id="19185-123">**AddResourcesSupported** (10)</span><span class="sxs-lookup"><span data-stu-id="19185-123">**AddResourcesSupported** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="19185-124">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="19185-124">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="19185-125">**Fornitore riservato** (32767.. 65535)</span><span class="sxs-lookup"><span data-stu-id="19185-125">**Vendor Reserved** (32767..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="19185-126">**IndicationsSupported**</span><span class="sxs-lookup"><span data-stu-id="19185-126">**IndicationsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19185-127">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="19185-127">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="19185-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="19185-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="19185-129">Matrice che contiene i tipi di indicazioni supportati dell'implementazione.</span><span class="sxs-lookup"><span data-stu-id="19185-129">An array that contains the supported indications types of the implementation.</span></span>

<dt>

<span id="VirtualResourceStateChangeIndicationsSupported"></span><span id="virtualresourcestatechangeindicationssupported"></span><span id="VIRTUALRESOURCESTATECHANGEINDICATIONSSUPPORTED"></span>

<span data-ttu-id="19185-130">**VirtualResourceStateChangeIndicationsSupported** (2)</span><span class="sxs-lookup"><span data-stu-id="19185-130">**VirtualResourceStateChangeIndicationsSupported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="ConcreteJobStateChangeIndicationsSupported"></span><span id="concretejobstatechangeindicationssupported"></span><span id="CONCRETEJOBSTATECHANGEINDICATIONSSUPPORTED"></span>

<span data-ttu-id="19185-131">**ConcreteJobStateChangeIndicationsSupported** (3)</span><span class="sxs-lookup"><span data-stu-id="19185-131">**ConcreteJobStateChangeIndicationsSupported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="VirtualSystemStateChangeIndicationsSupported"></span><span id="virtualsystemstatechangeindicationssupported"></span><span id="VIRTUALSYSTEMSTATECHANGEINDICATIONSSUPPORTED"></span>

<span data-ttu-id="19185-132">**VirtualSystemStateChangeIndicationsSupported** (4)</span><span class="sxs-lookup"><span data-stu-id="19185-132">**VirtualSystemStateChangeIndicationsSupported** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="19185-133">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="19185-133">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="19185-134">**Fornitore riservato** (32767.. 65535)</span><span class="sxs-lookup"><span data-stu-id="19185-134">**Vendor Reserved** (32767..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="19185-135">**SynchronousMethodsSupported**</span><span class="sxs-lookup"><span data-stu-id="19185-135">**SynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19185-136">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="19185-136">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="19185-137">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="19185-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="19185-138">Matrice che contiene i nomi di metodo per i metodi della classe [**CIM \_ VirtualSystemManagementService**](cim-virtualsystemmanagementservice.md) supportati per le operazioni sincrone.</span><span class="sxs-lookup"><span data-stu-id="19185-138">An array that contains method names for the [**CIM\_VirtualSystemManagementService**](cim-virtualsystemmanagementservice.md) class methods that are supported for synchronous operations.</span></span>

<dt>

<span id="DefineSystemSupported"></span><span id="definesystemsupported"></span><span id="DEFINESYSTEMSUPPORTED"></span>

<span data-ttu-id="19185-139">**DefineSystemSupported** (2)</span><span class="sxs-lookup"><span data-stu-id="19185-139">**DefineSystemSupported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="DestroySystemSupported"></span><span id="destroysystemsupported"></span><span id="DESTROYSYSTEMSUPPORTED"></span>

<span data-ttu-id="19185-140">**DestroySystemSupported** (3)</span><span class="sxs-lookup"><span data-stu-id="19185-140">**DestroySystemSupported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DestroySystemConfigurationSupported"></span><span id="destroysystemconfigurationsupported"></span><span id="DESTROYSYSTEMCONFIGURATIONSUPPORTED"></span>

<span data-ttu-id="19185-141">**DestroySystemConfigurationSupported** (4)</span><span class="sxs-lookup"><span data-stu-id="19185-141">**DestroySystemConfigurationSupported** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyResourceSettingsSupported"></span><span id="modifyresourcesettingssupported"></span><span id="MODIFYRESOURCESETTINGSSUPPORTED"></span>

<span data-ttu-id="19185-142">**ModifyResourceSettingsSupported** (5)</span><span class="sxs-lookup"><span data-stu-id="19185-142">**ModifyResourceSettingsSupported** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifySystemSettingsSupported"></span><span id="modifysystemsettingssupported"></span><span id="MODIFYSYSTEMSETTINGSSUPPORTED"></span>

<span data-ttu-id="19185-143">**ModifySystemSettingsSupported** (6)</span><span class="sxs-lookup"><span data-stu-id="19185-143">**ModifySystemSettingsSupported** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveResourcesSupported"></span><span id="removeresourcessupported"></span><span id="REMOVERESOURCESSUPPORTED"></span>

<span data-ttu-id="19185-144">**RemoveResourcesSupported** (7)</span><span class="sxs-lookup"><span data-stu-id="19185-144">**RemoveResourcesSupported** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SelectSystemConfigurationSupported"></span><span id="selectsystemconfigurationsupported"></span><span id="SELECTSYSTEMCONFIGURATIONSUPPORTED"></span>

<span data-ttu-id="19185-145">**SelectSystemConfigurationSupported** (8)</span><span class="sxs-lookup"><span data-stu-id="19185-145">**SelectSystemConfigurationSupported** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SnapshotSystemSupported"></span><span id="snapshotsystemsupported"></span><span id="SNAPSHOTSYSTEMSUPPORTED"></span>

<span data-ttu-id="19185-146">**SnapshotSystemSupported** (9)</span><span class="sxs-lookup"><span data-stu-id="19185-146">**SnapshotSystemSupported** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="AddResourcesSupported"></span><span id="addresourcessupported"></span><span id="ADDRESOURCESSUPPORTED"></span>

<span data-ttu-id="19185-147">**AddResourcesSupported** (10)</span><span class="sxs-lookup"><span data-stu-id="19185-147">**AddResourcesSupported** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="19185-148">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="19185-148">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="19185-149">**Fornitore riservato** (32767.. 65535)</span><span class="sxs-lookup"><span data-stu-id="19185-149">**Vendor Reserved** (32767..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="19185-150">**VirtualSystemTypesSupported**</span><span class="sxs-lookup"><span data-stu-id="19185-150">**VirtualSystemTypesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19185-151">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="19185-151">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="19185-152">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="19185-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19185-153">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md).**VirtualSystemType**")</span><span class="sxs-lookup"><span data-stu-id="19185-153">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md).**VirtualSystemType**")</span></span>
</dt> </dl>

<span data-ttu-id="19185-154">Tipo di sistemi virtuali supportati dall'implementazione di.</span><span class="sxs-lookup"><span data-stu-id="19185-154">The type of virtual systems supported by the implementation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="19185-155">Requisiti</span><span class="sxs-lookup"><span data-stu-id="19185-155">Requirements</span></span>



| <span data-ttu-id="19185-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="19185-156">Requirement</span></span> | <span data-ttu-id="19185-157">Valore</span><span class="sxs-lookup"><span data-stu-id="19185-157">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19185-158">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="19185-158">Minimum supported client</span></span><br/> | <span data-ttu-id="19185-159">Windows 8</span><span class="sxs-lookup"><span data-stu-id="19185-159">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="19185-160">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="19185-160">Minimum supported server</span></span><br/> | <span data-ttu-id="19185-161">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="19185-161">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="19185-162">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="19185-162">Namespace</span></span><br/>                | <span data-ttu-id="19185-163">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="19185-163">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="19185-164">MOF</span><span class="sxs-lookup"><span data-stu-id="19185-164">MOF</span></span><br/>                      | <dl> <span data-ttu-id="19185-165"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="19185-165"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="19185-166">DLL</span><span class="sxs-lookup"><span data-stu-id="19185-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19185-167"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="19185-167"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="19185-168">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="19185-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19185-169">**\_ENABLEDLOGICALELEMENTCAPABILITIES CIM**</span><span class="sxs-lookup"><span data-stu-id="19185-169">**CIM\_EnabledLogicalElementCapabilities**</span></span>](cim-enabledlogicalelementcapabilities.md)
</dt> </dl>

 

