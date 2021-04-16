---
description: Descrive le funzionalità del VirtualSystemManagementService MSVM associato \_ .
ms.assetid: 3a167b06-bddd-4bac-95c0-ecf14e01eec0
title: Classe Msvm_VirtualSystemManagementCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementCapabilities
- Msvm_VirtualSystemManagementCapabilities.InstanceID
- Msvm_VirtualSystemManagementCapabilities.Caption
- Msvm_VirtualSystemManagementCapabilities.Description
- Msvm_VirtualSystemManagementCapabilities.ElementName
- Msvm_VirtualSystemManagementCapabilities.ElementNameEditSupported
- Msvm_VirtualSystemManagementCapabilities.MaxElementNameLen
- Msvm_VirtualSystemManagementCapabilities.RequestedStatesSupported
- Msvm_VirtualSystemManagementCapabilities.ElementNameMask
- Msvm_VirtualSystemManagementCapabilities.VirtualSystemTypesSupported
- Msvm_VirtualSystemManagementCapabilities.SynchronousMethodsSupported
- Msvm_VirtualSystemManagementCapabilities.AsynchronousMethodsSupported
- Msvm_VirtualSystemManagementCapabilities.IndicationsSupported
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 24bc8ce66393a5e9ccd13848ab74640aec8d1760
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342791"
---
# <a name="msvm_virtualsystemmanagementcapabilities-class"></a><span data-ttu-id="19023-103">\_Classe MSVM VirtualSystemManagementCapabilities</span><span class="sxs-lookup"><span data-stu-id="19023-103">Msvm\_VirtualSystemManagementCapabilities class</span></span>

<span data-ttu-id="19023-104">Descrive le funzionalità del [**\_ VirtualSystemManagementService MSVM**](msvm-virtualsystemmanagementservice.md)associato.</span><span class="sxs-lookup"><span data-stu-id="19023-104">Describes the capabilities of the associated [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md).</span></span>

<span data-ttu-id="19023-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="19023-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="19023-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="19023-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemManagementCapabilities : CIM_VirtualSystemManagementCapabilities
{
  string  InstanceID;
  string  Caption = "Hyper-V Virtual System Management Service Capabilities";
  string  Description = "Defines Virtual System Management Service Capabilities";
  string  ElementName = "Hyper-V Virtual System Management Service Capabilities";
  boolean ElementNameEditSupported;
  unit16  MaxElementNameLen;
  unit16  RequestedStatesSupported[];
  string  ElementNameMask;
  string  VirtualSystemTypesSupported[];
  uint16  SynchronousMethodsSupported[];
  uint16  AsynchronousMethodsSupported[];
  uint16  IndicationsSupported[];
};
```

## <a name="members"></a><span data-ttu-id="19023-107">Members</span><span class="sxs-lookup"><span data-stu-id="19023-107">Members</span></span>

<span data-ttu-id="19023-108">La **classe \_ VirtualSystemManagementCapabilities di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="19023-108">The **Msvm\_VirtualSystemManagementCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="19023-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="19023-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="19023-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="19023-110">Properties</span></span>

<span data-ttu-id="19023-111">La **classe \_ VirtualSystemManagementCapabilities di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="19023-111">The **Msvm\_VirtualSystemManagementCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="19023-112">**AsynchronousMethodsSupported**</span><span class="sxs-lookup"><span data-stu-id="19023-112">**AsynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19023-113">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="19023-113">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="19023-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="19023-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19023-115">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ VirtualSystemManagementCapabilities. AsynchronousMethodsSupported")</span><span class="sxs-lookup"><span data-stu-id="19023-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VirtualSystemManagementCapabilities.AsynchronousMethodsSupported")</span></span>
</dt> </dl>

<span data-ttu-id="19023-116">Specifica i [**metodi \_ VirtualSystemManagementService MSVM**](msvm-virtualsystemmanagementservice.md) supportati in modo asincrono dall'implementazione di.</span><span class="sxs-lookup"><span data-stu-id="19023-116">Specifies the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) methods that are supported asynchronously by the implementation.</span></span>

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="19023-117">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="19023-117">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="ValidatePlannedSystem"></span><span id="validateplannedsystem"></span><span id="VALIDATEPLANNEDSYSTEM"></span>

<span data-ttu-id="19023-118">**[**ValidatePlannedSystem**](validateplannedsystem-msvm-virtualsystemmanagementservice.md)** (32767)</span><span class="sxs-lookup"><span data-stu-id="19023-118">**[**ValidatePlannedSystem**](validateplannedsystem-msvm-virtualsystemmanagementservice.md)** (32767)</span></span>


</dt> <dd></dd> <dt>

<span id="ImportSystemDefinition"></span><span id="importsystemdefinition"></span><span id="IMPORTSYSTEMDEFINITION"></span>

<span data-ttu-id="19023-119">**[**ImportSystemDefinition**](importsystemdefinition-msvm-virtualsystemmanagementservice.md)** (32770)</span><span class="sxs-lookup"><span data-stu-id="19023-119">**[**ImportSystemDefinition**](importsystemdefinition-msvm-virtualsystemmanagementservice.md)** (32770)</span></span>


</dt> <dd></dd> <dt>

<span id="ImportSnapshotDefinitions"></span><span id="importsnapshotdefinitions"></span><span id="IMPORTSNAPSHOTDEFINITIONS"></span>

<span data-ttu-id="19023-120">**[**ImportSnapshotDefinitions**](importsnapshotdefinitions-msvm-virtualsystemmanagementservice.md)** (32771)</span><span class="sxs-lookup"><span data-stu-id="19023-120">**[**ImportSnapshotDefinitions**](importsnapshotdefinitions-msvm-virtualsystemmanagementservice.md)** (32771)</span></span>


</dt> <dd></dd> <dt>

<span id="RealizePlannedSystem"></span><span id="realizeplannedsystem"></span><span id="REALIZEPLANNEDSYSTEM"></span>

<span data-ttu-id="19023-121">**[**RealizePlannedSystem**](realizeplannedsystem-msvm-virtualsystemmanagementservice.md)** (32772)</span><span class="sxs-lookup"><span data-stu-id="19023-121">**[**RealizePlannedSystem**](realizeplannedsystem-msvm-virtualsystemmanagementservice.md)** (32772)</span></span>


</dt> <dd></dd> <dt>

<span id="ExportSystemDefinition"></span><span id="exportsystemdefinition"></span><span id="EXPORTSYSTEMDEFINITION"></span>

<span data-ttu-id="19023-122">**[**ExportSystemDefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md)** (32778)</span><span class="sxs-lookup"><span data-stu-id="19023-122">**[**ExportSystemDefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md)** (32778)</span></span>


</dt> <dd></dd> <dt>

<span id="AddFeatureSettings"></span><span id="addfeaturesettings"></span><span id="ADDFEATURESETTINGS"></span>

<span data-ttu-id="19023-123">**[**AddFeatureSettings**](addfeaturesettings-msvm-virtualsystemmanagementservice.md)** (32779)</span><span class="sxs-lookup"><span data-stu-id="19023-123">**[**AddFeatureSettings**](addfeaturesettings-msvm-virtualsystemmanagementservice.md)** (32779)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyFeatureSettings"></span><span id="modifyfeaturesettings"></span><span id="MODIFYFEATURESETTINGS"></span>

<span data-ttu-id="19023-124">**[**ModifyFeatureSettings**](modifyfeaturesettings-msvm-virtualsystemmanagementservice.md)** (32780)</span><span class="sxs-lookup"><span data-stu-id="19023-124">**[**ModifyFeatureSettings**](modifyfeaturesettings-msvm-virtualsystemmanagementservice.md)** (32780)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveFeatureSettings"></span><span id="removefeaturesettings"></span><span id="REMOVEFEATURESETTINGS"></span>

<span data-ttu-id="19023-125">**[**RemoveFeatureSettings**](removefeaturesettings-msvm-virtualsystemmanagementservice.md)** (32781)</span><span class="sxs-lookup"><span data-stu-id="19023-125">**[**RemoveFeatureSettings**](removefeaturesettings-msvm-virtualsystemmanagementservice.md)** (32781)</span></span>


</dt> <dd></dd> <dt>

<span id="GetVirtualSystemThumbnailImage"></span><span id="getvirtualsystemthumbnailimage"></span><span id="GETVIRTUALSYSTEMTHUMBNAILIMAGE"></span>

<span data-ttu-id="19023-126">**[**GetVirtualSystemThumbnailImage**](getvirtualsystemthumbnailimage-msvm-virtualsystemmanagementservice.md)** (32782)</span><span class="sxs-lookup"><span data-stu-id="19023-126">**[**GetVirtualSystemThumbnailImage**](getvirtualsystemthumbnailimage-msvm-virtualsystemmanagementservice.md)** (32782)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyServiceSettings"></span><span id="modifyservicesettings"></span><span id="MODIFYSERVICESETTINGS"></span>

<span data-ttu-id="19023-127">**[**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md)** (32783)</span><span class="sxs-lookup"><span data-stu-id="19023-127">**[**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md)** (32783)</span></span>


</dt> <dd></dd> <dt>

<span id="GetSummaryInformation"></span><span id="getsummaryinformation"></span><span id="GETSUMMARYINFORMATION"></span>

<span data-ttu-id="19023-128">**[**GetSummaryInformation**](getsummaryinformation-msvm-virtualsystemmanagementservice.md)** (32784)</span><span class="sxs-lookup"><span data-stu-id="19023-128">**[**GetSummaryInformation**](getsummaryinformation-msvm-virtualsystemmanagementservice.md)** (32784)</span></span>


</dt> <dd></dd> <dt>

<span id="AddKvpItems"></span><span id="addkvpitems"></span><span id="ADDKVPITEMS"></span>

<span data-ttu-id="19023-129">**[**AddKvpItems**](addkvpitems-msvm-virtualsystemmanagementservice.md)** (32785)</span><span class="sxs-lookup"><span data-stu-id="19023-129">**[**AddKvpItems**](addkvpitems-msvm-virtualsystemmanagementservice.md)** (32785)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyKvpItems"></span><span id="modifykvpitems"></span><span id="MODIFYKVPITEMS"></span>

<span data-ttu-id="19023-130">**[**ModifyKvpItems**](modifykvpitems-msvm-virtualsystemmanagementservice.md)** (32786)</span><span class="sxs-lookup"><span data-stu-id="19023-130">**[**ModifyKvpItems**](modifykvpitems-msvm-virtualsystemmanagementservice.md)** (32786)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveKvpItems"></span><span id="removekvpitems"></span><span id="REMOVEKVPITEMS"></span>

<span data-ttu-id="19023-131">**[**RemoveKvpItems**](removekvpitems-msvm-virtualsystemmanagementservice.md)** (32787)</span><span class="sxs-lookup"><span data-stu-id="19023-131">**[**RemoveKvpItems**](removekvpitems-msvm-virtualsystemmanagementservice.md)** (32787)</span></span>


</dt> <dd></dd> <dt>

<span id="FormatError"></span><span id="formaterror"></span><span id="FORMATERROR"></span>

<span data-ttu-id="19023-132">**[**FormatError**](formaterror-msvm-virtualsystemmanagementservice.md)** (32788)</span><span class="sxs-lookup"><span data-stu-id="19023-132">**[**FormatError**](formaterror-msvm-virtualsystemmanagementservice.md)** (32788)</span></span>


</dt> <dd></dd> <dt>

<span id="RequestStateChangeSupported"></span><span id="requeststatechangesupported"></span><span id="REQUESTSTATECHANGESUPPORTED"></span>

<span data-ttu-id="19023-133">**RequestStateChangeSupported** (32789)</span><span class="sxs-lookup"><span data-stu-id="19023-133">**RequestStateChangeSupported** (32789)</span></span>


</dt> <dd></dd> <dt>

<span id="StartServiceSupported"></span><span id="startservicesupported"></span><span id="STARTSERVICESUPPORTED"></span>

<span data-ttu-id="19023-134">**StartServiceSupported** (32790)</span><span class="sxs-lookup"><span data-stu-id="19023-134">**StartServiceSupported** (32790)</span></span>


</dt> <dd></dd> <dt>

<span id="StopServiceSupported"></span><span id="stopservicesupported"></span><span id="STOPSERVICESUPPORTED"></span>

<span data-ttu-id="19023-135">**StopServiceSupported** (32791)</span><span class="sxs-lookup"><span data-stu-id="19023-135">**StopServiceSupported** (32791)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyDiskMergeSettings"></span><span id="modifydiskmergesettings"></span><span id="MODIFYDISKMERGESETTINGS"></span>

<span data-ttu-id="19023-136">**[**ModifyDiskMergeSettings**](modifydiskmergesettings-msvm-virtualsystemmanagementservice.md)** (32792)</span><span class="sxs-lookup"><span data-stu-id="19023-136">**[**ModifyDiskMergeSettings**](modifydiskmergesettings-msvm-virtualsystemmanagementservice.md)** (32792)</span></span>


</dt> <dd></dd> <dt>

<span id="GenerateWwpn"></span><span id="generatewwpn"></span><span id="GENERATEWWPN"></span>

<span data-ttu-id="19023-137">**[**GenerateWwpn**](generatewwpn-msvm-virtualsystemmanagementservice.md)** (32793)</span><span class="sxs-lookup"><span data-stu-id="19023-137">**[**GenerateWwpn**](generatewwpn-msvm-virtualsystemmanagementservice.md)** (32793)</span></span>


</dt> <dd></dd> <dt>

<span id="AddFibreChannelChap"></span><span id="addfibrechannelchap"></span><span id="ADDFIBRECHANNELCHAP"></span>

<span data-ttu-id="19023-138">**[**AddFibreChannelChap**](addfibrechannelchap-msvm-virtualsystemmanagementservice.md)** (32794)</span><span class="sxs-lookup"><span data-stu-id="19023-138">**[**AddFibreChannelChap**](addfibrechannelchap-msvm-virtualsystemmanagementservice.md)** (32794)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveFibreChannelChap"></span><span id="removefibrechannelchap"></span><span id="REMOVEFIBRECHANNELCHAP"></span>

<span data-ttu-id="19023-139">**[**RemoveFibreChannelChap**](removefibrechannelchap-msvm-virtualsystemmanagementservice.md)** (32795)</span><span class="sxs-lookup"><span data-stu-id="19023-139">**[**RemoveFibreChannelChap**](removefibrechannelchap-msvm-virtualsystemmanagementservice.md)** (32795)</span></span>


</dt> <dd></dd> <dt>

<span id="SetGuestNetworkAdapterConfiguration"></span><span id="setguestnetworkadapterconfiguration"></span><span id="SETGUESTNETWORKADAPTERCONFIGURATION"></span>

<span data-ttu-id="19023-140">**[**SetGuestNetworkAdapterConfiguration**](setguestnetworkadapterconfiguration-msvm-virtualsystemmanagementservice.md)** (32796)</span><span class="sxs-lookup"><span data-stu-id="19023-140">**[**SetGuestNetworkAdapterConfiguration**](setguestnetworkadapterconfiguration-msvm-virtualsystemmanagementservice.md)** (32796)</span></span>


</dt> <dd></dd> <dt>

<span id="GetSizeOfSystemFiles"></span><span id="getsizeofsystemfiles"></span><span id="GETSIZEOFSYSTEMFILES"></span>

<span data-ttu-id="19023-141">**[**GetSizeOfSystemFiles**](getsizeofsystemfiles-msvm-virtualsystemmanagementservice.md)** (32797)</span><span class="sxs-lookup"><span data-stu-id="19023-141">**[**GetSizeOfSystemFiles**](getsizeofsystemfiles-msvm-virtualsystemmanagementservice.md)** (32797)</span></span>


</dt> <dd></dd> <dt>

<span id="GetCurrentWwpnFromGenerator"></span><span id="getcurrentwwpnfromgenerator"></span><span id="GETCURRENTWWPNFROMGENERATOR"></span>

<span data-ttu-id="19023-142">**[**GetCurrentWwpnFromGenerator**](getcurrentwwpnfromgenerator-msvm-virtualsystemmanagementservice.md)** (32798)</span><span class="sxs-lookup"><span data-stu-id="19023-142">**[**GetCurrentWwpnFromGenerator**](getcurrentwwpnfromgenerator-msvm-virtualsystemmanagementservice.md)** (32798)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="19023-143">**Fornitore riservato** (32799.. 65535)</span><span class="sxs-lookup"><span data-stu-id="19023-143">**Vendor Reserved** (32799..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="19023-144">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="19023-144">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19023-145">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="19023-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19023-146">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="19023-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="19023-147">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="19023-147">A short description of the object.</span></span> <span data-ttu-id="19023-148">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="19023-148">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="19023-149">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="19023-149">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19023-150">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="19023-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19023-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="19023-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="19023-152">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="19023-152">A description of the object.</span></span> <span data-ttu-id="19023-153">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="19023-153">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="19023-154">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="19023-154">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19023-155">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="19023-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19023-156">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="19023-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="19023-157">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="19023-157">A display name for the object.</span></span> <span data-ttu-id="19023-158">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="19023-158">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="19023-159">**ElementNameEditSupported**</span><span class="sxs-lookup"><span data-stu-id="19023-159">**ElementNameEditSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19023-160">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="19023-160">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="19023-161">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="19023-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="19023-162">Indica se la proprietà **ElementName** può essere modificata.</span><span class="sxs-lookup"><span data-stu-id="19023-162">Indicates whether the **ElementName** property can be modified.</span></span> <span data-ttu-id="19023-163">Questa proprietà viene ereditata da **CIM \_ EnabledLogicalElementCapabilities**.</span><span class="sxs-lookup"><span data-stu-id="19023-163">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="19023-164">**ElementNameMask**</span><span class="sxs-lookup"><span data-stu-id="19023-164">**ElementNameMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19023-165">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="19023-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19023-166">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="19023-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="19023-167">Specifica le restrizioni per **ElementName**, espresse come espressione regolare.</span><span class="sxs-lookup"><span data-stu-id="19023-167">Specifies the restrictions on **ElementName**, expressed as a regular expression.</span></span> <span data-ttu-id="19023-168">Questa proprietà viene ereditata da **CIM \_ EnabledLogicalElementCapabilities**.</span><span class="sxs-lookup"><span data-stu-id="19023-168">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="19023-169">**IndicationsSupported**</span><span class="sxs-lookup"><span data-stu-id="19023-169">**IndicationsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19023-170">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="19023-170">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="19023-171">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="19023-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19023-172">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ VirtualSystemManagementCapabilities. IndicationsSupported")</span><span class="sxs-lookup"><span data-stu-id="19023-172">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VirtualSystemManagementCapabilities.IndicationsSupported")</span></span>
</dt> </dl>

<span data-ttu-id="19023-173">Specifica le indicazioni supportate dall'implementazione di.</span><span class="sxs-lookup"><span data-stu-id="19023-173">Specifies the indications supported by the implementation.</span></span>

<span data-ttu-id="19023-174">Enumerazione degli identificatori di indicazione che identificano ogni indicazione supportata dall'implementazione.</span><span class="sxs-lookup"><span data-stu-id="19023-174">Enumeration of indication identifiers each identifying an indication that is supported by the implementation.</span></span>

<dt>

<span id="VirtualResourceStateChangeIndicationsSupported"></span><span id="virtualresourcestatechangeindicationssupported"></span><span id="VIRTUALRESOURCESTATECHANGEINDICATIONSSUPPORTED"></span>

<span data-ttu-id="19023-175"><span id="VirtualResourceStateChangeIndicationsSupported"></span><span id="virtualresourcestatechangeindicationssupported"></span><span id="VIRTUALRESOURCESTATECHANGEINDICATIONSSUPPORTED"></span>**VirtualResourceStateChangeIndicationsSupported** (2)</span><span class="sxs-lookup"><span data-stu-id="19023-175"><span id="VirtualResourceStateChangeIndicationsSupported"></span><span id="virtualresourcestatechangeindicationssupported"></span><span id="VIRTUALRESOURCESTATECHANGEINDICATIONSSUPPORTED"></span>**VirtualResourceStateChangeIndicationsSupported** (2)</span></span>


</dt> <dd>

<span data-ttu-id="19023-176">L'implementazione supporta la notifica delle modifiche di stato delle istanze [**\_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) che rappresentano le risorse dei sistemi virtuali.</span><span class="sxs-lookup"><span data-stu-id="19023-176">The implementation supports notification of state changes of [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) instances representing resources of virtual systems.</span></span>

</dd> <dt>

<span id="ConcreteJobStateChangeIndicationsSupported"></span><span id="concretejobstatechangeindicationssupported"></span><span id="CONCRETEJOBSTATECHANGEINDICATIONSSUPPORTED"></span>

<span data-ttu-id="19023-177"><span id="ConcreteJobStateChangeIndicationsSupported"></span><span id="concretejobstatechangeindicationssupported"></span><span id="CONCRETEJOBSTATECHANGEINDICATIONSSUPPORTED"></span>**ConcreteJobStateChangeIndicationsSupported** (3)</span><span class="sxs-lookup"><span data-stu-id="19023-177"><span id="ConcreteJobStateChangeIndicationsSupported"></span><span id="concretejobstatechangeindicationssupported"></span><span id="CONCRETEJOBSTATECHANGEINDICATIONSSUPPORTED"></span>**ConcreteJobStateChangeIndicationsSupported** (3)</span></span>


</dt> <dd>

<span data-ttu-id="19023-178">L'implementazione supporta la notifica delle modifiche di stato delle istanze di [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="19023-178">The implementation supports notification of state changes of [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)) instances.</span></span>

</dd> <dt>

<span id="VirtualSystemStateChangeIndicationsSupported"></span><span id="virtualsystemstatechangeindicationssupported"></span><span id="VIRTUALSYSTEMSTATECHANGEINDICATIONSSUPPORTED"></span>

<span data-ttu-id="19023-179"><span id="VirtualSystemStateChangeIndicationsSupported"></span><span id="virtualsystemstatechangeindicationssupported"></span><span id="VIRTUALSYSTEMSTATECHANGEINDICATIONSSUPPORTED"></span>**VirtualSystemStateChangeIndicationsSupported** (4)</span><span class="sxs-lookup"><span data-stu-id="19023-179"><span id="VirtualSystemStateChangeIndicationsSupported"></span><span id="virtualsystemstatechangeindicationssupported"></span><span id="VIRTUALSYSTEMSTATECHANGEINDICATIONSSUPPORTED"></span>**VirtualSystemStateChangeIndicationsSupported** (4)</span></span>


</dt> <dd>

<span data-ttu-id="19023-180">L'implementazione supporta la notifica delle modifiche di stato delle istanze [**\_ ComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) che rappresentano i sistemi virtuali.</span><span class="sxs-lookup"><span data-stu-id="19023-180">The implementation supports notification of state changes of [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instances representing virtual systems.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="19023-181"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="19023-181"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="19023-182"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornitore riservato** (32767.. 65535)</span><span class="sxs-lookup"><span data-stu-id="19023-182"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32767..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="19023-183">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="19023-183">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19023-184">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="19023-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19023-185">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="19023-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19023-186">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="19023-186">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="19023-187">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="19023-187">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="19023-188">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="19023-188">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="19023-189">**MaxElementNameLen**</span><span class="sxs-lookup"><span data-stu-id="19023-189">**MaxElementNameLen**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19023-190">Tipo di dati: **unit16**</span><span class="sxs-lookup"><span data-stu-id="19023-190">Data type: **unit16**</span></span>
</dt> <dt>

<span data-ttu-id="19023-191">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="19023-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19023-192">Qualificatori: **MaxValue** (256)</span><span class="sxs-lookup"><span data-stu-id="19023-192">Qualifiers: **MaxValue** (256)</span></span>
</dt> </dl>

<span data-ttu-id="19023-193">Specifica la lunghezza massima supportata della proprietà **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="19023-193">Specifies the maximum supported length of the **ElementName** property.</span></span> <span data-ttu-id="19023-194">Questa proprietà viene ereditata da **CIM \_ EnabledLogicalElementCapabilities**.</span><span class="sxs-lookup"><span data-stu-id="19023-194">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="19023-195">**RequestedStatesSupported**</span><span class="sxs-lookup"><span data-stu-id="19023-195">**RequestedStatesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19023-196">Tipo di dati: matrice **unit16**</span><span class="sxs-lookup"><span data-stu-id="19023-196">Data type: **unit16** array</span></span>
</dt> <dt>

<span data-ttu-id="19023-197">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="19023-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="19023-198">Indica gli stati possibili che è possibile richiedere quando si utilizza il metodo **RequestStateChange** sull'elemento logico Enabled.</span><span class="sxs-lookup"><span data-stu-id="19023-198">Indicates the possible states that can be requested when using the **RequestStateChange** method on the enabled logical element.</span></span> <span data-ttu-id="19023-199">Questa proprietà viene ereditata da **CIM \_ EnabledLogicalElementCapabilities**.</span><span class="sxs-lookup"><span data-stu-id="19023-199">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>



| <span data-ttu-id="19023-200">Valore</span><span class="sxs-lookup"><span data-stu-id="19023-200">Value</span></span>                                                                         | <span data-ttu-id="19023-201">Significato</span><span class="sxs-lookup"><span data-stu-id="19023-201">Meaning</span></span>              |
|-------------------------------------------------------------------------------|----------------------|
| <dl> <span data-ttu-id="19023-202"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="19023-202"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="19023-203">Abilitato</span><span class="sxs-lookup"><span data-stu-id="19023-203">Enabled</span></span><br/>   |
| <dl> <span data-ttu-id="19023-204"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="19023-204"><dt>3</dt></span></span> </dl>  | <span data-ttu-id="19023-205">Disabilita</span><span class="sxs-lookup"><span data-stu-id="19023-205">Disables</span></span><br/>  |
| <dl> <span data-ttu-id="19023-206"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="19023-206"><dt>4</dt></span></span> </dl>  | <span data-ttu-id="19023-207">Arresta</span><span class="sxs-lookup"><span data-stu-id="19023-207">Shut Down</span></span><br/> |
| <dl> <span data-ttu-id="19023-208"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="19023-208"><dt>6</dt></span></span> </dl>  | <span data-ttu-id="19023-209">Offline</span><span class="sxs-lookup"><span data-stu-id="19023-209">Offline</span></span><br/>   |
| <dl> <span data-ttu-id="19023-210"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="19023-210"><dt>7</dt></span></span> </dl>  | <span data-ttu-id="19023-211">Test</span><span class="sxs-lookup"><span data-stu-id="19023-211">Test</span></span><br/>      |
| <dl> <span data-ttu-id="19023-212"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="19023-212"><dt>8</dt></span></span> </dl>  | <span data-ttu-id="19023-213">Rinviare</span><span class="sxs-lookup"><span data-stu-id="19023-213">Defer</span></span><br/>     |
| <dl> <span data-ttu-id="19023-214"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="19023-214"><dt>9</dt></span></span> </dl>  | <span data-ttu-id="19023-215">Disattivazione</span><span class="sxs-lookup"><span data-stu-id="19023-215">Quiesce</span></span><br/>   |
| <dl> <span data-ttu-id="19023-216"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="19023-216"><dt>10</dt></span></span> </dl> | <span data-ttu-id="19023-217">Riavvio</span><span class="sxs-lookup"><span data-stu-id="19023-217">Reboot</span></span><br/>    |
| <dl> <span data-ttu-id="19023-218"><dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="19023-218"><dt>11</dt></span></span> </dl> | <span data-ttu-id="19023-219">Reset</span><span class="sxs-lookup"><span data-stu-id="19023-219">Reset</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="19023-220">**SynchronousMethodsSupported**</span><span class="sxs-lookup"><span data-stu-id="19023-220">**SynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19023-221">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="19023-221">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="19023-222">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="19023-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19023-223">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ VirtualSystemManagementCapabilities. SynchronousMethodsSupported")</span><span class="sxs-lookup"><span data-stu-id="19023-223">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VirtualSystemManagementCapabilities.SynchronousMethodsSupported")</span></span>
</dt> </dl>

<span data-ttu-id="19023-224">Specifica i [**metodi \_ VirtualSystemManagementService MSVM**](msvm-virtualsystemmanagementservice.md) che sono supportati in modo sincrono dall'implementazione di.</span><span class="sxs-lookup"><span data-stu-id="19023-224">Specifies the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) methods that are supported synchronously by the implementation.</span></span>

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="19023-225">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="19023-225">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="ValidatePlannedSystem"></span><span id="validateplannedsystem"></span><span id="VALIDATEPLANNEDSYSTEM"></span>

<span data-ttu-id="19023-226">**[**ValidatePlannedSystem**](validateplannedsystem-msvm-virtualsystemmanagementservice.md)** (32767)</span><span class="sxs-lookup"><span data-stu-id="19023-226">**[**ValidatePlannedSystem**](validateplannedsystem-msvm-virtualsystemmanagementservice.md)** (32767)</span></span>


</dt> <dd></dd> <dt>

<span id="ImportSystemDefinition"></span><span id="importsystemdefinition"></span><span id="IMPORTSYSTEMDEFINITION"></span>

<span data-ttu-id="19023-227">**[**ImportSystemDefinition**](importsystemdefinition-msvm-virtualsystemmanagementservice.md)** (32770)</span><span class="sxs-lookup"><span data-stu-id="19023-227">**[**ImportSystemDefinition**](importsystemdefinition-msvm-virtualsystemmanagementservice.md)** (32770)</span></span>


</dt> <dd></dd> <dt>

<span id="ImportSnapshotDefinitions"></span><span id="importsnapshotdefinitions"></span><span id="IMPORTSNAPSHOTDEFINITIONS"></span>

<span data-ttu-id="19023-228">**[**ImportSnapshotDefinitions**](importsnapshotdefinitions-msvm-virtualsystemmanagementservice.md)** (32771)</span><span class="sxs-lookup"><span data-stu-id="19023-228">**[**ImportSnapshotDefinitions**](importsnapshotdefinitions-msvm-virtualsystemmanagementservice.md)** (32771)</span></span>


</dt> <dd></dd> <dt>

<span id="RealizePlannedSystem"></span><span id="realizeplannedsystem"></span><span id="REALIZEPLANNEDSYSTEM"></span>

<span data-ttu-id="19023-229">**[**RealizePlannedSystem**](realizeplannedsystem-msvm-virtualsystemmanagementservice.md)** (32772)</span><span class="sxs-lookup"><span data-stu-id="19023-229">**[**RealizePlannedSystem**](realizeplannedsystem-msvm-virtualsystemmanagementservice.md)** (32772)</span></span>


</dt> <dd></dd> <dt>

<span id="ExportSystemDefinition"></span><span id="exportsystemdefinition"></span><span id="EXPORTSYSTEMDEFINITION"></span>

<span data-ttu-id="19023-230">**[**ExportSystemDefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md)** (32778)</span><span class="sxs-lookup"><span data-stu-id="19023-230">**[**ExportSystemDefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md)** (32778)</span></span>


</dt> <dd></dd> <dt>

<span id="AddFeatureSettings"></span><span id="addfeaturesettings"></span><span id="ADDFEATURESETTINGS"></span>

<span data-ttu-id="19023-231">**[**AddFeatureSettings**](addfeaturesettings-msvm-virtualsystemmanagementservice.md)** (32779)</span><span class="sxs-lookup"><span data-stu-id="19023-231">**[**AddFeatureSettings**](addfeaturesettings-msvm-virtualsystemmanagementservice.md)** (32779)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyFeatureSettings"></span><span id="modifyfeaturesettings"></span><span id="MODIFYFEATURESETTINGS"></span>

<span data-ttu-id="19023-232">**[**ModifyFeatureSettings**](modifyfeaturesettings-msvm-virtualsystemmanagementservice.md)** (32780)</span><span class="sxs-lookup"><span data-stu-id="19023-232">**[**ModifyFeatureSettings**](modifyfeaturesettings-msvm-virtualsystemmanagementservice.md)** (32780)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveFeatureSettings"></span><span id="removefeaturesettings"></span><span id="REMOVEFEATURESETTINGS"></span>

<span data-ttu-id="19023-233">**[**RemoveFeatureSettings**](removefeaturesettings-msvm-virtualsystemmanagementservice.md)** (32781)</span><span class="sxs-lookup"><span data-stu-id="19023-233">**[**RemoveFeatureSettings**](removefeaturesettings-msvm-virtualsystemmanagementservice.md)** (32781)</span></span>


</dt> <dd></dd> <dt>

<span id="GetVirtualSystemThumbnailImage"></span><span id="getvirtualsystemthumbnailimage"></span><span id="GETVIRTUALSYSTEMTHUMBNAILIMAGE"></span>

<span data-ttu-id="19023-234">**[**GetVirtualSystemThumbnailImage**](getvirtualsystemthumbnailimage-msvm-virtualsystemmanagementservice.md)** (32782)</span><span class="sxs-lookup"><span data-stu-id="19023-234">**[**GetVirtualSystemThumbnailImage**](getvirtualsystemthumbnailimage-msvm-virtualsystemmanagementservice.md)** (32782)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyServiceSettings"></span><span id="modifyservicesettings"></span><span id="MODIFYSERVICESETTINGS"></span>

<span data-ttu-id="19023-235">**[**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md)** (32783)</span><span class="sxs-lookup"><span data-stu-id="19023-235">**[**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md)** (32783)</span></span>


</dt> <dd></dd> <dt>

<span id="GetSummaryInformation"></span><span id="getsummaryinformation"></span><span id="GETSUMMARYINFORMATION"></span>

<span data-ttu-id="19023-236">**[**GetSummaryInformation**](getsummaryinformation-msvm-virtualsystemmanagementservice.md)** (32784)</span><span class="sxs-lookup"><span data-stu-id="19023-236">**[**GetSummaryInformation**](getsummaryinformation-msvm-virtualsystemmanagementservice.md)** (32784)</span></span>


</dt> <dd></dd> <dt>

<span id="AddKvpItems"></span><span id="addkvpitems"></span><span id="ADDKVPITEMS"></span>

<span data-ttu-id="19023-237">**[**AddKvpItems**](addkvpitems-msvm-virtualsystemmanagementservice.md)** (32785)</span><span class="sxs-lookup"><span data-stu-id="19023-237">**[**AddKvpItems**](addkvpitems-msvm-virtualsystemmanagementservice.md)** (32785)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyKvpItems"></span><span id="modifykvpitems"></span><span id="MODIFYKVPITEMS"></span>

<span data-ttu-id="19023-238">**[**ModifyKvpItems**](modifykvpitems-msvm-virtualsystemmanagementservice.md)** (32786)</span><span class="sxs-lookup"><span data-stu-id="19023-238">**[**ModifyKvpItems**](modifykvpitems-msvm-virtualsystemmanagementservice.md)** (32786)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveKvpItems"></span><span id="removekvpitems"></span><span id="REMOVEKVPITEMS"></span>

<span data-ttu-id="19023-239">**[**RemoveKvpItems**](removekvpitems-msvm-virtualsystemmanagementservice.md)** (32787)</span><span class="sxs-lookup"><span data-stu-id="19023-239">**[**RemoveKvpItems**](removekvpitems-msvm-virtualsystemmanagementservice.md)** (32787)</span></span>


</dt> <dd></dd> <dt>

<span id="FormatError"></span><span id="formaterror"></span><span id="FORMATERROR"></span>

<span data-ttu-id="19023-240">**[**FormatError**](formaterror-msvm-virtualsystemmanagementservice.md)** (32788)</span><span class="sxs-lookup"><span data-stu-id="19023-240">**[**FormatError**](formaterror-msvm-virtualsystemmanagementservice.md)** (32788)</span></span>


</dt> <dd></dd> <dt>

<span id="RequestStateChangeSupported"></span><span id="requeststatechangesupported"></span><span id="REQUESTSTATECHANGESUPPORTED"></span>

<span data-ttu-id="19023-241">**RequestStateChangeSupported** (32789)</span><span class="sxs-lookup"><span data-stu-id="19023-241">**RequestStateChangeSupported** (32789)</span></span>


</dt> <dd></dd> <dt>

<span id="StartServiceSupported"></span><span id="startservicesupported"></span><span id="STARTSERVICESUPPORTED"></span>

<span data-ttu-id="19023-242">**StartServiceSupported** (32790)</span><span class="sxs-lookup"><span data-stu-id="19023-242">**StartServiceSupported** (32790)</span></span>


</dt> <dd></dd> <dt>

<span id="StopServiceSupported"></span><span id="stopservicesupported"></span><span id="STOPSERVICESUPPORTED"></span>

<span data-ttu-id="19023-243">**StopServiceSupported** (32791)</span><span class="sxs-lookup"><span data-stu-id="19023-243">**StopServiceSupported** (32791)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyDiskMergeSettings"></span><span id="modifydiskmergesettings"></span><span id="MODIFYDISKMERGESETTINGS"></span>

<span data-ttu-id="19023-244">**[**ModifyDiskMergeSettings**](modifydiskmergesettings-msvm-virtualsystemmanagementservice.md)** (32792)</span><span class="sxs-lookup"><span data-stu-id="19023-244">**[**ModifyDiskMergeSettings**](modifydiskmergesettings-msvm-virtualsystemmanagementservice.md)** (32792)</span></span>


</dt> <dd></dd> <dt>

<span id="GenerateWwpn"></span><span id="generatewwpn"></span><span id="GENERATEWWPN"></span>

<span data-ttu-id="19023-245">**[**GenerateWwpn**](generatewwpn-msvm-virtualsystemmanagementservice.md)** (32793)</span><span class="sxs-lookup"><span data-stu-id="19023-245">**[**GenerateWwpn**](generatewwpn-msvm-virtualsystemmanagementservice.md)** (32793)</span></span>


</dt> <dd></dd> <dt>

<span id="AddFibreChannelChap"></span><span id="addfibrechannelchap"></span><span id="ADDFIBRECHANNELCHAP"></span>

<span data-ttu-id="19023-246">**[**AddFibreChannelChap**](addfibrechannelchap-msvm-virtualsystemmanagementservice.md)** (32794)</span><span class="sxs-lookup"><span data-stu-id="19023-246">**[**AddFibreChannelChap**](addfibrechannelchap-msvm-virtualsystemmanagementservice.md)** (32794)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveFibreChannelChap"></span><span id="removefibrechannelchap"></span><span id="REMOVEFIBRECHANNELCHAP"></span>

<span data-ttu-id="19023-247">**[**RemoveFibreChannelChap**](removefibrechannelchap-msvm-virtualsystemmanagementservice.md)** (32795)</span><span class="sxs-lookup"><span data-stu-id="19023-247">**[**RemoveFibreChannelChap**](removefibrechannelchap-msvm-virtualsystemmanagementservice.md)** (32795)</span></span>


</dt> <dd></dd> <dt>

<span id="SetGuestNetworkAdapterConfiguration"></span><span id="setguestnetworkadapterconfiguration"></span><span id="SETGUESTNETWORKADAPTERCONFIGURATION"></span>

<span data-ttu-id="19023-248">**[**SetGuestNetworkAdapterConfiguration**](setguestnetworkadapterconfiguration-msvm-virtualsystemmanagementservice.md)** (32796)</span><span class="sxs-lookup"><span data-stu-id="19023-248">**[**SetGuestNetworkAdapterConfiguration**](setguestnetworkadapterconfiguration-msvm-virtualsystemmanagementservice.md)** (32796)</span></span>


</dt> <dd></dd> <dt>

<span id="GetSizeOfSystemFiles"></span><span id="getsizeofsystemfiles"></span><span id="GETSIZEOFSYSTEMFILES"></span>

<span data-ttu-id="19023-249">**[**GetSizeOfSystemFiles**](getsizeofsystemfiles-msvm-virtualsystemmanagementservice.md)** (32797)</span><span class="sxs-lookup"><span data-stu-id="19023-249">**[**GetSizeOfSystemFiles**](getsizeofsystemfiles-msvm-virtualsystemmanagementservice.md)** (32797)</span></span>


</dt> <dd></dd> <dt>

<span id="GetCurrentWwpnFromGenerator"></span><span id="getcurrentwwpnfromgenerator"></span><span id="GETCURRENTWWPNFROMGENERATOR"></span>

<span data-ttu-id="19023-250">**[**GetCurrentWwpnFromGenerator**](getcurrentwwpnfromgenerator-msvm-virtualsystemmanagementservice.md)** (32798)</span><span class="sxs-lookup"><span data-stu-id="19023-250">**[**GetCurrentWwpnFromGenerator**](getcurrentwwpnfromgenerator-msvm-virtualsystemmanagementservice.md)** (32798)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="19023-251">**Fornitore riservato** (32799.. 65535)</span><span class="sxs-lookup"><span data-stu-id="19023-251">**Vendor Reserved** (32799..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="19023-252">**VirtualSystemTypesSupported**</span><span class="sxs-lookup"><span data-stu-id="19023-252">**VirtualSystemTypesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19023-253">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="19023-253">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="19023-254">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="19023-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="19023-255">Matrice di stringhe che designa ogni tipo di sistema virtuale supportato dall'implementazione di.</span><span class="sxs-lookup"><span data-stu-id="19023-255">An array of strings each designating a type of virtual system that the implementation supports.</span></span> <span data-ttu-id="19023-256">Il valore di ogni elemento di matrice non **null** deve essere conforme alle stringhe definite per la proprietà [**MSVM \_ VirtualSystemSettingData. VirtualSystemType**](msvm-virtualsystemsettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="19023-256">The value of each non-**NULL** array element must conform to the strings defined for the [**Msvm\_VirtualSystemSettingData.VirtualSystemType**](msvm-virtualsystemsettingdata.md) property.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="19023-257">Requisiti</span><span class="sxs-lookup"><span data-stu-id="19023-257">Requirements</span></span>



| <span data-ttu-id="19023-258">Requisito</span><span class="sxs-lookup"><span data-stu-id="19023-258">Requirement</span></span> | <span data-ttu-id="19023-259">Valore</span><span class="sxs-lookup"><span data-stu-id="19023-259">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19023-260">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="19023-260">Minimum supported client</span></span><br/> | <span data-ttu-id="19023-261">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="19023-261">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="19023-262">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="19023-262">Minimum supported server</span></span><br/> | <span data-ttu-id="19023-263">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="19023-263">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="19023-264">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="19023-264">Namespace</span></span><br/>                | <span data-ttu-id="19023-265">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="19023-265">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="19023-266">MOF</span><span class="sxs-lookup"><span data-stu-id="19023-266">MOF</span></span><br/>                      | <dl> <span data-ttu-id="19023-267"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="19023-267"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="19023-268">DLL</span><span class="sxs-lookup"><span data-stu-id="19023-268">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19023-269"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="19023-269"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

