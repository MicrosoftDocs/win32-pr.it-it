---
description: Descrive le funzionalità del VirtualEthernetSwitchManagementService MSVM associato \_ .
ms.assetid: daed7a02-bae8-4bda-abc6-0657df7dc4f8
title: Classe Msvm_VirtualEthernetSwitchManagementCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementCapabilities
- Msvm_VirtualEthernetSwitchManagementCapabilities.InstanceID
- Msvm_VirtualEthernetSwitchManagementCapabilities.Caption
- Msvm_VirtualEthernetSwitchManagementCapabilities.Description
- Msvm_VirtualEthernetSwitchManagementCapabilities.ElementName
- Msvm_VirtualEthernetSwitchManagementCapabilities.ElementNameEditSupported
- Msvm_VirtualEthernetSwitchManagementCapabilities.MaxElementNameLen
- Msvm_VirtualEthernetSwitchManagementCapabilities.RequestedStatesSupported
- Msvm_VirtualEthernetSwitchManagementCapabilities.ElementNameMask
- Msvm_VirtualEthernetSwitchManagementCapabilities.VirtualSystemTypesSupported
- Msvm_VirtualEthernetSwitchManagementCapabilities.SynchronousMethodsSupported
- Msvm_VirtualEthernetSwitchManagementCapabilities.AsynchronousMethodsSupported
- Msvm_VirtualEthernetSwitchManagementCapabilities.IndicationsSupported
- Msvm_VirtualEthernetSwitchManagementCapabilities.IOVSupport
- Msvm_VirtualEthernetSwitchManagementCapabilities.IOVSupportReasons
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d66d73773b956ecbbbf4ca102b18bb6f8ece4190
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313844"
---
# <a name="msvm_virtualethernetswitchmanagementcapabilities-class"></a><span data-ttu-id="13cde-103">\_Classe MSVM VirtualEthernetSwitchManagementCapabilities</span><span class="sxs-lookup"><span data-stu-id="13cde-103">Msvm\_VirtualEthernetSwitchManagementCapabilities class</span></span>

<span data-ttu-id="13cde-104">Descrive le funzionalità del [**\_ VirtualEthernetSwitchManagementService MSVM**](msvm-virtualethernetswitchmanagementservice.md)associato.</span><span class="sxs-lookup"><span data-stu-id="13cde-104">Describes the capabilities of the associated [**Msvm\_VirtualEthernetSwitchManagementService**](msvm-virtualethernetswitchmanagementservice.md).</span></span>

<span data-ttu-id="13cde-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="13cde-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="13cde-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="13cde-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualEthernetSwitchManagementCapabilities : CIM_VirtualSystemManagementCapabilities
{
  string  InstanceID;
  string  Caption = "Hyper-V Virtual Ethernet Switch Management Service Capabilities";
  string  Description = "Defines Virtual Ethernet Switch Management Service Capabilities";
  string  ElementName = "Hyper-V Virtual Ethernet Switch Management Service Capabilities";
  boolean ElementNameEditSupported;
  unit16  MaxElementNameLen;
  unit16  RequestedStatesSupported[];
  string  ElementNameMask;
  string  VirtualSystemTypesSupported[];
  uint16  SynchronousMethodsSupported[];
  uint16  AsynchronousMethodsSupported[];
  uint16  IndicationsSupported[];
  boolean IOVSupport;
  string  IOVSupportReasons[];
};
```

## <a name="members"></a><span data-ttu-id="13cde-107">Members</span><span class="sxs-lookup"><span data-stu-id="13cde-107">Members</span></span>

<span data-ttu-id="13cde-108">La **classe \_ VirtualEthernetSwitchManagementCapabilities di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="13cde-108">The **Msvm\_VirtualEthernetSwitchManagementCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="13cde-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="13cde-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="13cde-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="13cde-110">Properties</span></span>

<span data-ttu-id="13cde-111">La **classe \_ VirtualEthernetSwitchManagementCapabilities di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="13cde-111">The **Msvm\_VirtualEthernetSwitchManagementCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="13cde-112">**AsynchronousMethodsSupported**</span><span class="sxs-lookup"><span data-stu-id="13cde-112">**AsynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13cde-113">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="13cde-113">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="13cde-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="13cde-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13cde-115">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ VirtualSystemManagementCapabilities. AsynchronousMethodsSupported")</span><span class="sxs-lookup"><span data-stu-id="13cde-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VirtualSystemManagementCapabilities.AsynchronousMethodsSupported")</span></span>
</dt> </dl>

<span data-ttu-id="13cde-116">Matrice di identificatori di metodi, ognuno dei quali identifica un metodo della classe [**\_ VirtualEthernetSwitchManagementService MSVM**](msvm-virtualethernetswitchmanagementservice.md) supportata in modo asincrono dall'implementazione.</span><span class="sxs-lookup"><span data-stu-id="13cde-116">An array of method identifiers, each identifying a method of the [**Msvm\_VirtualEthernetSwitchManagementService**](msvm-virtualethernetswitchmanagementservice.md) class that is supported asynchronously by the implementation.</span></span> <span data-ttu-id="13cde-117">Questa proprietà viene ereditata da **CIM \_ VirtualSystemManagementCapabilities**.</span><span class="sxs-lookup"><span data-stu-id="13cde-117">This property is inherited from **CIM\_VirtualSystemManagementCapabilities**.</span></span>

<dt>

<span id="DefineSystem"></span><span id="definesystem"></span><span id="DEFINESYSTEM"></span>

<span data-ttu-id="13cde-118">**DefineSystem** (2)</span><span class="sxs-lookup"><span data-stu-id="13cde-118">**DefineSystem** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="DestroySystem"></span><span id="destroysystem"></span><span id="DESTROYSYSTEM"></span>

<span data-ttu-id="13cde-119">**DestroySystem** (3)</span><span class="sxs-lookup"><span data-stu-id="13cde-119">**DestroySystem** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DestroySystemConfiguration"></span><span id="destroysystemconfiguration"></span><span id="DESTROYSYSTEMCONFIGURATION"></span>

<span data-ttu-id="13cde-120">**DestroySystemConfiguration** (4)</span><span class="sxs-lookup"><span data-stu-id="13cde-120">**DestroySystemConfiguration** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyResourceSettings"></span><span id="modifyresourcesettings"></span><span id="MODIFYRESOURCESETTINGS"></span>

<span data-ttu-id="13cde-121">**ModifyResourceSettings** (5)</span><span class="sxs-lookup"><span data-stu-id="13cde-121">**ModifyResourceSettings** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifySystemSettings"></span><span id="modifysystemsettings"></span><span id="MODIFYSYSTEMSETTINGS"></span>

<span data-ttu-id="13cde-122">**ModifySystemSettings** (6)</span><span class="sxs-lookup"><span data-stu-id="13cde-122">**ModifySystemSettings** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveResources"></span><span id="removeresources"></span><span id="REMOVERESOURCES"></span>

<span data-ttu-id="13cde-123">**RemoveResources** (7)</span><span class="sxs-lookup"><span data-stu-id="13cde-123">**RemoveResources** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SelectSystemConfiguration"></span><span id="selectsystemconfiguration"></span><span id="SELECTSYSTEMCONFIGURATION"></span>

<span data-ttu-id="13cde-124">**SelectSystemConfiguration** (8)</span><span class="sxs-lookup"><span data-stu-id="13cde-124">**SelectSystemConfiguration** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SnapshotSystem"></span><span id="snapshotsystem"></span><span id="SNAPSHOTSYSTEM"></span>

<span data-ttu-id="13cde-125">**SnapshotSystem** (9)</span><span class="sxs-lookup"><span data-stu-id="13cde-125">**SnapshotSystem** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="AddResources"></span><span id="addresources"></span><span id="ADDRESOURCES"></span>

<span data-ttu-id="13cde-126">**AddResources** (10)</span><span class="sxs-lookup"><span data-stu-id="13cde-126">**AddResources** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="AddFeatureSettingsSupported"></span><span id="addfeaturesettingssupported"></span><span id="ADDFEATURESETTINGSSUPPORTED"></span>

<span data-ttu-id="13cde-127">**AddFeatureSettingsSupported** (32779)</span><span class="sxs-lookup"><span data-stu-id="13cde-127">**AddFeatureSettingsSupported** (32779)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyFeatureSettingsSupported"></span><span id="modifyfeaturesettingssupported"></span><span id="MODIFYFEATURESETTINGSSUPPORTED"></span>

<span data-ttu-id="13cde-128">**ModifyFeatureSettingsSupported** (32780)</span><span class="sxs-lookup"><span data-stu-id="13cde-128">**ModifyFeatureSettingsSupported** (32780)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveFeatureSettingsSupported"></span><span id="removefeaturesettingssupported"></span><span id="REMOVEFEATURESETTINGSSUPPORTED"></span>

<span data-ttu-id="13cde-129">**RemoveFeatureSettingsSupported** (32781)</span><span class="sxs-lookup"><span data-stu-id="13cde-129">**RemoveFeatureSettingsSupported** (32781)</span></span>


</dt> <dd></dd> <dt>

<span id="AddFeatureSettingsSupported"></span><span id="addfeaturesettingssupported"></span><span id="ADDFEATURESETTINGSSUPPORTED"></span>

<span data-ttu-id="13cde-130">**AddFeatureSettingsSupported** (32779)</span><span class="sxs-lookup"><span data-stu-id="13cde-130">**AddFeatureSettingsSupported** (32779)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyFeatureSettingsSupported"></span><span id="modifyfeaturesettingssupported"></span><span id="MODIFYFEATURESETTINGSSUPPORTED"></span>

<span data-ttu-id="13cde-131">**ModifyFeatureSettingsSupported** (32780)</span><span class="sxs-lookup"><span data-stu-id="13cde-131">**ModifyFeatureSettingsSupported** (32780)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveFeatureSettingsSupported"></span><span id="removefeaturesettingssupported"></span><span id="REMOVEFEATURESETTINGSSUPPORTED"></span>

<span data-ttu-id="13cde-132">**RemoveFeatureSettingsSupported** (32781)</span><span class="sxs-lookup"><span data-stu-id="13cde-132">**RemoveFeatureSettingsSupported** (32781)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="13cde-133">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="13cde-133">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13cde-134">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="13cde-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13cde-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="13cde-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13cde-136">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="13cde-136">A short description of the object.</span></span> <span data-ttu-id="13cde-137">Questa proprietà viene ereditata da [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Hyper-V Virtual Ethernet Switch Management Service Capabilities".</span><span class="sxs-lookup"><span data-stu-id="13cde-137">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Virtual Ethernet Switch Management Service Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="13cde-138">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="13cde-138">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13cde-139">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="13cde-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13cde-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="13cde-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13cde-141">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="13cde-141">A description of the object.</span></span> <span data-ttu-id="13cde-142">Questa proprietà viene ereditata da [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "definisce le funzionalità del servizio di gestione del comcambio Ethernet virtuale".</span><span class="sxs-lookup"><span data-stu-id="13cde-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Defines Virtual Ethernet Switch Management Service Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="13cde-143">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="13cde-143">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13cde-144">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="13cde-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13cde-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="13cde-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13cde-146">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="13cde-146">A display name for the object.</span></span> <span data-ttu-id="13cde-147">Questa proprietà viene ereditata da [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Hyper-V Virtual Ethernet Switch Management Service Capabilities".</span><span class="sxs-lookup"><span data-stu-id="13cde-147">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Virtual Ethernet Switch Management Service Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="13cde-148">**ElementNameEditSupported**</span><span class="sxs-lookup"><span data-stu-id="13cde-148">**ElementNameEditSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13cde-149">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="13cde-149">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="13cde-150">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="13cde-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13cde-151">Indica se la proprietà **ElementName** può essere modificata.</span><span class="sxs-lookup"><span data-stu-id="13cde-151">Indicates whether the **ElementName** property can be modified.</span></span> <span data-ttu-id="13cde-152">Questa proprietà viene ereditata da **CIM \_ EnabledLogicalElementCapabilities**.</span><span class="sxs-lookup"><span data-stu-id="13cde-152">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="13cde-153">**ElementNameMask**</span><span class="sxs-lookup"><span data-stu-id="13cde-153">**ElementNameMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13cde-154">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="13cde-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13cde-155">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="13cde-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13cde-156">Specifica le restrizioni per **ElementName**, espresse come espressione regolare.</span><span class="sxs-lookup"><span data-stu-id="13cde-156">Specifies the restrictions on **ElementName**, expressed as a regular expression.</span></span> <span data-ttu-id="13cde-157">Questa proprietà viene ereditata da **CIM \_ EnabledLogicalElementCapabilities**.</span><span class="sxs-lookup"><span data-stu-id="13cde-157">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="13cde-158">**IndicationsSupported**</span><span class="sxs-lookup"><span data-stu-id="13cde-158">**IndicationsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13cde-159">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="13cde-159">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="13cde-160">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="13cde-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13cde-161">Matrice di identificatori di indicazione, ciascuno dei quali identifica un'indicazione supportata dall'implementazione.</span><span class="sxs-lookup"><span data-stu-id="13cde-161">An array of indication identifiers, each identifying an indication that is supported by the implementation.</span></span> <span data-ttu-id="13cde-162">Questa proprietà viene ereditata da **CIM \_ VirtualSystemManagementCapabilities**.</span><span class="sxs-lookup"><span data-stu-id="13cde-162">This property is inherited from **CIM\_VirtualSystemManagementCapabilities**.</span></span>



| <span data-ttu-id="13cde-163">Valore</span><span class="sxs-lookup"><span data-stu-id="13cde-163">Value</span></span>                                                                                                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="13cde-164">Significato</span><span class="sxs-lookup"><span data-stu-id="13cde-164">Meaning</span></span>                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="VirtualResourceStateChangeIndicationsSupported"></span><span id="virtualresourcestatechangeindicationssupported"></span><span id="VIRTUALRESOURCESTATECHANGEINDICATIONSSUPPORTED"></span><dl> <span data-ttu-id="13cde-165"><dt>**VirtualResourceStateChangeIndicationsSupported**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="13cde-165"><dt>**VirtualResourceStateChangeIndicationsSupported**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="13cde-166">Indica se l'implementazione supporta la notifica sulle modifiche di stato delle istanze [**\_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) che rappresentano le risorse dei sistemi virtuali.</span><span class="sxs-lookup"><span data-stu-id="13cde-166">Indicates whether the implementation supports notification on state changes of [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) instances that represent resources of virtual systems.</span></span><br/> |
| <span id="ConcreteJobStateChangeIndicationsSupported"></span><span id="concretejobstatechangeindicationssupported"></span><span id="CONCRETEJOBSTATECHANGEINDICATIONSSUPPORTED"></span><dl> <span data-ttu-id="13cde-167"><dt>**ConcreteJobStateChangeIndicationsSupported**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="13cde-167"><dt>**ConcreteJobStateChangeIndicationsSupported**</dt> <dt>3</dt></span></span> </dl>                 | <span data-ttu-id="13cde-168">Indica se l'implementazione supporta la notifica sulle modifiche dello stato delle istanze di [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="13cde-168">Indicates whether the implementation supports notification on state changes of [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)) instances.</span></span><br/>                                                      |
| <span id="VirtualSystemStateChangeIndicationsSupported"></span><span id="virtualsystemstatechangeindicationssupported"></span><span id="VIRTUALSYSTEMSTATECHANGEINDICATIONSSUPPORTED"></span><dl> <span data-ttu-id="13cde-169"><dt>**VirtualSystemStateChangeIndicationsSupported**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="13cde-169"><dt>**VirtualSystemStateChangeIndicationsSupported**</dt> <dt>4</dt></span></span> </dl>         | <span data-ttu-id="13cde-170">Indica se l'implementazione supporta la notifica sulle modifiche di stato delle istanze [**\_ ComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) che rappresentano i sistemi virtuali.</span><span class="sxs-lookup"><span data-stu-id="13cde-170">Indicates whether the implementation supports notification on state changes of [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instances that represent virtual systems.</span></span><br/>            |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="13cde-171"><dt>**DMTF riservato**</dt> <dt>..</dt></span><span class="sxs-lookup"><span data-stu-id="13cde-171"><dt>**DMTF Reserved**</dt> <dt>..</dt></span></span> </dl>                                                                                                                                    |                                                                                                                                                                                                       |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <span data-ttu-id="13cde-172">32767 <dt> **riservato al fornitore**</dt> <dt>.. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="13cde-172"><dt>**Vendor Reserved** </dt> <dt>32767..65535 </dt></span></span> </dl>                                                                                                             |                                                                                                                                                                                                       |



 

</dd> <dt>

<span data-ttu-id="13cde-173">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="13cde-173">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13cde-174">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="13cde-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13cde-175">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="13cde-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13cde-176">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="13cde-176">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="13cde-177">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="13cde-177">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="13cde-178">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="13cde-178">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="13cde-179">**IOVSupport**</span><span class="sxs-lookup"><span data-stu-id="13cde-179">**IOVSupport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13cde-180">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="13cde-180">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="13cde-181">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="13cde-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13cde-182">Valore booleano che indica se la virtualizzazione di I/O (IOV) è supportata dalla piattaforma.</span><span class="sxs-lookup"><span data-stu-id="13cde-182">A boolean value that indicates whether I/O virtualization (IOV) is supported by the platform.</span></span> <span data-ttu-id="13cde-183">Se il valore è **true**, IOV è supportato dalla piattaforma e **IOVSupportReasons** sarà vuoto.</span><span class="sxs-lookup"><span data-stu-id="13cde-183">If the value is **True**, then IOV is supported by the platform and **IOVSupportReasons** will be empty.</span></span> <span data-ttu-id="13cde-184">In caso contrario, la proprietà **IOVSupportReasons** avrà i motivi per cui non è possibile supportare IOV.</span><span class="sxs-lookup"><span data-stu-id="13cde-184">Otherwise the **IOVSupportReasons** property will have the reasons why IOV cannot be supported.</span></span>

</dd> <dt>

<span data-ttu-id="13cde-185">**IOVSupportReasons**</span><span class="sxs-lookup"><span data-stu-id="13cde-185">**IOVSupportReasons**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13cde-186">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="13cde-186">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="13cde-187">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="13cde-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13cde-188">Matrice di stringhe che indica i possibili motivi per cui IOV non è supportato.</span><span class="sxs-lookup"><span data-stu-id="13cde-188">An array of strings that indicates the possible reasons why IOV is not supported.</span></span> <span data-ttu-id="13cde-189">Se il valore di **IOVSupport** è **true**, questa matrice sarà vuota.</span><span class="sxs-lookup"><span data-stu-id="13cde-189">If the value of **IOVSupport** is **True**, this array will be empty.</span></span>

</dd> <dt>

<span data-ttu-id="13cde-190">**MaxElementNameLen**</span><span class="sxs-lookup"><span data-stu-id="13cde-190">**MaxElementNameLen**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13cde-191">Tipo di dati: **unit16**</span><span class="sxs-lookup"><span data-stu-id="13cde-191">Data type: **unit16**</span></span>
</dt> <dt>

<span data-ttu-id="13cde-192">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="13cde-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13cde-193">Qualificatori: **MaxValue** (256)</span><span class="sxs-lookup"><span data-stu-id="13cde-193">Qualifiers: **MaxValue** (256)</span></span>
</dt> </dl>

<span data-ttu-id="13cde-194">Specifica la lunghezza massima supportata della proprietà **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="13cde-194">Specifies the maximum supported length of the **ElementName** property.</span></span> <span data-ttu-id="13cde-195">Questa proprietà viene ereditata da **CIM \_ EnabledLogicalElementCapabilities**.</span><span class="sxs-lookup"><span data-stu-id="13cde-195">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="13cde-196">**RequestedStatesSupported**</span><span class="sxs-lookup"><span data-stu-id="13cde-196">**RequestedStatesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13cde-197">Tipo di dati: matrice **unit16**</span><span class="sxs-lookup"><span data-stu-id="13cde-197">Data type: **unit16** array</span></span>
</dt> <dt>

<span data-ttu-id="13cde-198">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="13cde-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13cde-199">Indica gli stati possibili che è possibile richiedere quando si utilizza il metodo **RequestStateChange** sull'elemento logico Enabled.</span><span class="sxs-lookup"><span data-stu-id="13cde-199">Indicates the possible states that can be requested when using the **RequestStateChange** method on the enabled logical element.</span></span> <span data-ttu-id="13cde-200">Questa proprietà viene ereditata da **CIM \_ EnabledLogicalElementCapabilities** ed è sempre **null**.</span><span class="sxs-lookup"><span data-stu-id="13cde-200">This property is inherited from **CIM\_EnabledLogicalElementCapabilities** and is always **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="13cde-201">**SynchronousMethodsSupported**</span><span class="sxs-lookup"><span data-stu-id="13cde-201">**SynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13cde-202">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="13cde-202">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="13cde-203">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="13cde-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13cde-204">Matrice di identificatori di metodi, ognuno dei quali identifica un metodo della classe [**\_ VirtualEthernetSwitchManagementService MSVM**](msvm-virtualethernetswitchmanagementservice.md) supportata in modo sincrono dall'implementazione di.</span><span class="sxs-lookup"><span data-stu-id="13cde-204">An array of method identifiers, each identifying a method of the [**Msvm\_VirtualEthernetSwitchManagementService**](msvm-virtualethernetswitchmanagementservice.md) class that is supported synchronously by the implementation.</span></span> <span data-ttu-id="13cde-205">Questa proprietà viene ereditata da **CIM \_ VirtualSystemManagementCapabilities**.</span><span class="sxs-lookup"><span data-stu-id="13cde-205">This property is inherited from **CIM\_VirtualSystemManagementCapabilities**.</span></span>

<dl> <dt>

<span data-ttu-id="13cde-206"><span id="DefineSystem"></span><span id="definesystem"></span><span id="DEFINESYSTEM"></span>**DefineSystem** (2)</span><span class="sxs-lookup"><span data-stu-id="13cde-206"><span id="DefineSystem"></span><span id="definesystem"></span><span id="DEFINESYSTEM"></span>**DefineSystem** (2)</span></span>
</dt> <dt>

<span data-ttu-id="13cde-207"><span id="DestroySystem"></span><span id="destroysystem"></span><span id="DESTROYSYSTEM"></span>**DestroySystem** (3)</span><span class="sxs-lookup"><span data-stu-id="13cde-207"><span id="DestroySystem"></span><span id="destroysystem"></span><span id="DESTROYSYSTEM"></span>**DestroySystem** (3)</span></span>
</dt> <dt>

<span data-ttu-id="13cde-208"><span id="DestroySystemConfiguration"></span><span id="destroysystemconfiguration"></span><span id="DESTROYSYSTEMCONFIGURATION"></span>**DestroySystemConfiguration** (4)</span><span class="sxs-lookup"><span data-stu-id="13cde-208"><span id="DestroySystemConfiguration"></span><span id="destroysystemconfiguration"></span><span id="DESTROYSYSTEMCONFIGURATION"></span>**DestroySystemConfiguration** (4)</span></span>
</dt> <dt>

<span data-ttu-id="13cde-209"><span id="ModifyResourceSettings"></span><span id="modifyresourcesettings"></span><span id="MODIFYRESOURCESETTINGS"></span>**ModifyResourceSettings** (5)</span><span class="sxs-lookup"><span data-stu-id="13cde-209"><span id="ModifyResourceSettings"></span><span id="modifyresourcesettings"></span><span id="MODIFYRESOURCESETTINGS"></span>**ModifyResourceSettings** (5)</span></span>
</dt> <dt>

<span data-ttu-id="13cde-210"><span id="ModifySystemSettings"></span><span id="modifysystemsettings"></span><span id="MODIFYSYSTEMSETTINGS"></span>**ModifySystemSettings** (6)</span><span class="sxs-lookup"><span data-stu-id="13cde-210"><span id="ModifySystemSettings"></span><span id="modifysystemsettings"></span><span id="MODIFYSYSTEMSETTINGS"></span>**ModifySystemSettings** (6)</span></span>
</dt> <dt>

<span data-ttu-id="13cde-211"><span id="RemoveResources"></span><span id="removeresources"></span><span id="REMOVERESOURCES"></span>**RemoveResources** (7)</span><span class="sxs-lookup"><span data-stu-id="13cde-211"><span id="RemoveResources"></span><span id="removeresources"></span><span id="REMOVERESOURCES"></span>**RemoveResources** (7)</span></span>
</dt> <dt>

<span data-ttu-id="13cde-212"><span id="SelectSystemConfiguration"></span><span id="selectsystemconfiguration"></span><span id="SELECTSYSTEMCONFIGURATION"></span>**SelectSystemConfiguration** (8)</span><span class="sxs-lookup"><span data-stu-id="13cde-212"><span id="SelectSystemConfiguration"></span><span id="selectsystemconfiguration"></span><span id="SELECTSYSTEMCONFIGURATION"></span>**SelectSystemConfiguration** (8)</span></span>
</dt> <dt>

<span data-ttu-id="13cde-213"><span id="SnapshotSystem"></span><span id="snapshotsystem"></span><span id="SNAPSHOTSYSTEM"></span>**SnapshotSystem** (9)</span><span class="sxs-lookup"><span data-stu-id="13cde-213"><span id="SnapshotSystem"></span><span id="snapshotsystem"></span><span id="SNAPSHOTSYSTEM"></span>**SnapshotSystem** (9)</span></span>
</dt> <dt>

<span data-ttu-id="13cde-214"><span id="AddResources"></span><span id="addresources"></span><span id="ADDRESOURCES"></span>**AddResources** (10)</span><span class="sxs-lookup"><span data-stu-id="13cde-214"><span id="AddResources"></span><span id="addresources"></span><span id="ADDRESOURCES"></span>**AddResources** (10)</span></span>
</dt> <dt>

<span data-ttu-id="13cde-215"><span id="AddFeatureSettings"></span><span id="addfeaturesettings"></span><span id="ADDFEATURESETTINGS"></span>**AddFeatureSettings** (32779)</span><span class="sxs-lookup"><span data-stu-id="13cde-215"><span id="AddFeatureSettings"></span><span id="addfeaturesettings"></span><span id="ADDFEATURESETTINGS"></span>**AddFeatureSettings** (32779)</span></span>
</dt> <dt>

<span data-ttu-id="13cde-216"><span id="ModifyFeatureSettings"></span><span id="modifyfeaturesettings"></span><span id="MODIFYFEATURESETTINGS"></span>**ModifyFeatureSettings** (32780)</span><span class="sxs-lookup"><span data-stu-id="13cde-216"><span id="ModifyFeatureSettings"></span><span id="modifyfeaturesettings"></span><span id="MODIFYFEATURESETTINGS"></span>**ModifyFeatureSettings** (32780)</span></span>
</dt> <dt>

<span data-ttu-id="13cde-217"><span id="RemoveFeatureSettings"></span><span id="removefeaturesettings"></span><span id="REMOVEFEATURESETTINGS"></span>**RemoveFeatureSettings** (32781)</span><span class="sxs-lookup"><span data-stu-id="13cde-217"><span id="RemoveFeatureSettings"></span><span id="removefeaturesettings"></span><span id="REMOVEFEATURESETTINGS"></span>**RemoveFeatureSettings** (32781 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="13cde-218">**VirtualSystemTypesSupported**</span><span class="sxs-lookup"><span data-stu-id="13cde-218">**VirtualSystemTypesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13cde-219">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="13cde-219">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="13cde-220">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="13cde-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13cde-221">Matrice di stringhe, ognuna delle quali designa un tipo di sistema virtuale supportato dall'implementazione di.</span><span class="sxs-lookup"><span data-stu-id="13cde-221">An array of strings, each designating a type of virtual system that the implementation supports.</span></span> <span data-ttu-id="13cde-222">Il valore di ogni elemento di matrice non **null** deve essere conforme al formato definito per la proprietà **VirtualSystemType** della [**classe \_ VirtualSystemSettingData di MSVM**](msvm-virtualsystemsettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="13cde-222">The value of each non-**Null** array element must conform to the format defined for the **VirtualSystemType** property of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class.</span></span> <span data-ttu-id="13cde-223">Questa proprietà viene ereditata da **CIM \_ VirtualSystemManagementCapabilities**.</span><span class="sxs-lookup"><span data-stu-id="13cde-223">This property is inherited from **CIM\_VirtualSystemManagementCapabilities**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="13cde-224">Requisiti</span><span class="sxs-lookup"><span data-stu-id="13cde-224">Requirements</span></span>



| <span data-ttu-id="13cde-225">Requisito</span><span class="sxs-lookup"><span data-stu-id="13cde-225">Requirement</span></span> | <span data-ttu-id="13cde-226">Valore</span><span class="sxs-lookup"><span data-stu-id="13cde-226">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13cde-227">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="13cde-227">Minimum supported client</span></span><br/> | <span data-ttu-id="13cde-228">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="13cde-228">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="13cde-229">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="13cde-229">Minimum supported server</span></span><br/> | <span data-ttu-id="13cde-230">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="13cde-230">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="13cde-231">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="13cde-231">Namespace</span></span><br/>                | <span data-ttu-id="13cde-232">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="13cde-232">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="13cde-233">MOF</span><span class="sxs-lookup"><span data-stu-id="13cde-233">MOF</span></span><br/>                      | <dl> <span data-ttu-id="13cde-234"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="13cde-234"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="13cde-235">DLL</span><span class="sxs-lookup"><span data-stu-id="13cde-235">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13cde-236"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="13cde-236"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

