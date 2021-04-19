---
description: Rappresenta le impostazioni del profilo di porta.
ms.assetid: 43ddb0a3-8621-4993-b0a9-8ddcfb0eaad5
title: Classe Msvm_EthernetSwitchPortProfileSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortProfileSettingData
- Msvm_EthernetSwitchPortProfileSettingData.InstanceID
- Msvm_EthernetSwitchPortProfileSettingData.Caption
- Msvm_EthernetSwitchPortProfileSettingData.Description
- Msvm_EthernetSwitchPortProfileSettingData.ElementName
- Msvm_EthernetSwitchPortProfileSettingData.ProfileName
- Msvm_EthernetSwitchPortProfileSettingData.ProfileId
- Msvm_EthernetSwitchPortProfileSettingData.VendorName
- Msvm_EthernetSwitchPortProfileSettingData.VendorId
- Msvm_EthernetSwitchPortProfileSettingData.ProfileData
- Msvm_EthernetSwitchPortProfileSettingData.NetCfgInstanceId
- Msvm_EthernetSwitchPortProfileSettingData.PciSegmentNumber
- Msvm_EthernetSwitchPortProfileSettingData.PciBusNumber
- Msvm_EthernetSwitchPortProfileSettingData.PciDeviceNumber
- Msvm_EthernetSwitchPortProfileSettingData.PciFunctionNumber
- Msvm_EthernetSwitchPortProfileSettingData.CdnLabelId
- Msvm_EthernetSwitchPortProfileSettingData.CdnLabelString
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 611fd40b14b961369a847d6bb7b7746ceec2bb85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106320020"
---
# <a name="msvm_ethernetswitchportprofilesettingdata-class"></a><span data-ttu-id="0660c-103">\_Classe MSVM EthernetSwitchPortProfileSettingData</span><span class="sxs-lookup"><span data-stu-id="0660c-103">Msvm\_EthernetSwitchPortProfileSettingData class</span></span>

<span data-ttu-id="0660c-104">Rappresenta le impostazioni del profilo di porta.</span><span class="sxs-lookup"><span data-stu-id="0660c-104">Represents the port profile settings.</span></span>

<span data-ttu-id="0660c-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="0660c-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0660c-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0660c-106">Syntax</span></span>

``` syntax
[Dynamic, UUID("9940CD46-8B06-43BB-B9D5-93D50381FD56"), Provider("VmmsWmiInstanceAndMethodProvider"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Profile Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortProfileSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string InstanceID;
  string Caption = "Ethernet Switch Port Profile Settings";
  string Description = "Represents the port profile settings.";
  string ElementName = "Ethernet Switch Port Profile Settings";
  string ProfileName = "";
  string ProfileId = "";
  string VendorName = "";
  string VendorId = 00000000-0000-0000-0000-000000000000}";
  uint32 ProfileData = 0;
  string NetCfgInstanceId = 00000000-0000-0000-0000-000000000000}";
  uint32 PciSegmentNumber = 0;
  uint32 PciBusNumber = 0;
  uint32 PciDeviceNumber = 0;
  uint32 PciFunctionNumber = 0;
  uint32 CdnLabelId = 0;
  string CdnLabelString = 0;
};
```

## <a name="members"></a><span data-ttu-id="0660c-107">Members</span><span class="sxs-lookup"><span data-stu-id="0660c-107">Members</span></span>

<span data-ttu-id="0660c-108">La **classe \_ EthernetSwitchPortProfileSettingData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="0660c-108">The **Msvm\_EthernetSwitchPortProfileSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="0660c-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0660c-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0660c-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0660c-110">Properties</span></span>

<span data-ttu-id="0660c-111">La **classe \_ EthernetSwitchPortProfileSettingData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="0660c-111">The **Msvm\_EthernetSwitchPortProfileSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0660c-112">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="0660c-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0660c-113">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0660c-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0660c-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0660c-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0660c-115">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="0660c-115">A short description of the object.</span></span> <span data-ttu-id="0660c-116">Questa proprietà viene ereditata da [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Ethernet Switch Port Profile Settings".</span><span class="sxs-lookup"><span data-stu-id="0660c-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Profile Settings".</span></span>

</dd> <dt>

<span data-ttu-id="0660c-117">**CdnLabelId**</span><span class="sxs-lookup"><span data-stu-id="0660c-117">**CdnLabelId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0660c-118">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0660c-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0660c-119">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="0660c-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0660c-120">Qualificatori: **WmiDataId** (11), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="0660c-120">Qualifiers: **WmiDataId** (11), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="0660c-121">Identificatore dell'etichetta della rete CDN.</span><span class="sxs-lookup"><span data-stu-id="0660c-121">The CDN label identifier.</span></span>

</dd> <dt>

<span data-ttu-id="0660c-122">**CdnLabelString**</span><span class="sxs-lookup"><span data-stu-id="0660c-122">**CdnLabelString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0660c-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0660c-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0660c-124">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="0660c-124">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0660c-125">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (12), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="0660c-125">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (12), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="0660c-126">Stringa dell'etichetta della rete CDN.</span><span class="sxs-lookup"><span data-stu-id="0660c-126">The CDN label string.</span></span>

</dd> <dt>

<span data-ttu-id="0660c-127">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="0660c-127">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0660c-128">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0660c-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0660c-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0660c-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0660c-130">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="0660c-130">A description of the object.</span></span> <span data-ttu-id="0660c-131">Questa proprietà viene ereditata da [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "rappresenta le impostazioni del profilo di porta".</span><span class="sxs-lookup"><span data-stu-id="0660c-131">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Represents the port profile settings.".</span></span>

</dd> <dt>

<span data-ttu-id="0660c-132">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="0660c-132">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0660c-133">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0660c-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0660c-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0660c-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0660c-135">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="0660c-135">A display name for the object.</span></span> <span data-ttu-id="0660c-136">Questa proprietà viene ereditata da [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Ethernet Switch Port Profile Settings".</span><span class="sxs-lookup"><span data-stu-id="0660c-136">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Profile Settings".</span></span>

</dd> <dt>

<span data-ttu-id="0660c-137">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="0660c-137">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0660c-138">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0660c-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0660c-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0660c-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0660c-140">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="0660c-140">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="0660c-141">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="0660c-141">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="0660c-142">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="0660c-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="0660c-143">**Parametro NetCfgInstanceId**</span><span class="sxs-lookup"><span data-stu-id="0660c-143">**NetCfgInstanceId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0660c-144">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0660c-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0660c-145">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="0660c-145">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0660c-146">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (38), **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="0660c-146">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (38), **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="0660c-147">Identificatore univoco del dispositivo della sottointerfaccia.</span><span class="sxs-lookup"><span data-stu-id="0660c-147">An unique device identifier of the subinterface.</span></span>

</dd> <dt>

<span data-ttu-id="0660c-148">**PciBusNumber**</span><span class="sxs-lookup"><span data-stu-id="0660c-148">**PciBusNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0660c-149">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0660c-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0660c-150">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="0660c-150">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0660c-151">Qualificatori: **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="0660c-151">Qualifiers: **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="0660c-152">Numero del bus PCI.</span><span class="sxs-lookup"><span data-stu-id="0660c-152">The PCI bus number.</span></span>

</dd> <dt>

<span data-ttu-id="0660c-153">**PciDeviceNumber**</span><span class="sxs-lookup"><span data-stu-id="0660c-153">**PciDeviceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0660c-154">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0660c-154">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0660c-155">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="0660c-155">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0660c-156">Qualificatori: **WmiDataId** (9), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="0660c-156">Qualifiers: **WmiDataId** (9), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="0660c-157">Numero del dispositivo PCI.</span><span class="sxs-lookup"><span data-stu-id="0660c-157">The PCI device number.</span></span>

</dd> <dt>

<span data-ttu-id="0660c-158">**PciFunctionNumber**</span><span class="sxs-lookup"><span data-stu-id="0660c-158">**PciFunctionNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0660c-159">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0660c-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0660c-160">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="0660c-160">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0660c-161">Qualificatori: **WmiDataId** (10), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="0660c-161">Qualifiers: **WmiDataId** (10), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="0660c-162">Numero della funzione PCI.</span><span class="sxs-lookup"><span data-stu-id="0660c-162">The PCI function number.</span></span>

</dd> <dt>

<span data-ttu-id="0660c-163">**PciSegmentNumber**</span><span class="sxs-lookup"><span data-stu-id="0660c-163">**PciSegmentNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0660c-164">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0660c-164">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0660c-165">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="0660c-165">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0660c-166">Qualificatori: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="0660c-166">Qualifiers: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="0660c-167">Numero del segmento PCI.</span><span class="sxs-lookup"><span data-stu-id="0660c-167">The PCI segment number.</span></span>

</dd> <dt>

<span data-ttu-id="0660c-168">**ProfileData**</span><span class="sxs-lookup"><span data-stu-id="0660c-168">**ProfileData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0660c-169">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0660c-169">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0660c-170">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="0660c-170">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0660c-171">Qualificatori: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="0660c-171">Qualifiers: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="0660c-172">Dati aggiuntivi per il profilo di porta.</span><span class="sxs-lookup"><span data-stu-id="0660c-172">Additional data for the port profile.</span></span>

</dd> <dt>

<span data-ttu-id="0660c-173">**ProfileId**</span><span class="sxs-lookup"><span data-stu-id="0660c-173">**ProfileId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0660c-174">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0660c-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0660c-175">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="0660c-175">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0660c-176">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (38), **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="0660c-176">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (38), **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="0660c-177">Identificatore del profilo di porta.</span><span class="sxs-lookup"><span data-stu-id="0660c-177">The identifier of the port profile.</span></span>

</dd> <dt>

<span data-ttu-id="0660c-178">**ProfileName**</span><span class="sxs-lookup"><span data-stu-id="0660c-178">**ProfileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0660c-179">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0660c-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0660c-180">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="0660c-180">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0660c-181">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="0660c-181">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="0660c-182">Nome del profilo di porta.</span><span class="sxs-lookup"><span data-stu-id="0660c-182">The name of the port profile.</span></span>

</dd> <dt>

<span data-ttu-id="0660c-183">**VendorId**</span><span class="sxs-lookup"><span data-stu-id="0660c-183">**VendorId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0660c-184">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0660c-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0660c-185">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="0660c-185">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0660c-186">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (38), **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="0660c-186">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (38), **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="0660c-187">Identificatore del fornitore che definisce il profilo.</span><span class="sxs-lookup"><span data-stu-id="0660c-187">The identifier of the vendor defining the profile.</span></span>

</dd> <dt>

<span data-ttu-id="0660c-188">**NomeFornitore**</span><span class="sxs-lookup"><span data-stu-id="0660c-188">**VendorName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0660c-189">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0660c-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0660c-190">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="0660c-190">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0660c-191">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="0660c-191">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="0660c-192">Nome del fornitore che definisce il profilo.</span><span class="sxs-lookup"><span data-stu-id="0660c-192">The name of the vendor defining the profile.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0660c-193">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0660c-193">Requirements</span></span>



| <span data-ttu-id="0660c-194">Requisito</span><span class="sxs-lookup"><span data-stu-id="0660c-194">Requirement</span></span> | <span data-ttu-id="0660c-195">Valore</span><span class="sxs-lookup"><span data-stu-id="0660c-195">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0660c-196">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0660c-196">Minimum supported client</span></span><br/> | <span data-ttu-id="0660c-197">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="0660c-197">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="0660c-198">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0660c-198">Minimum supported server</span></span><br/> | <span data-ttu-id="0660c-199">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="0660c-199">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0660c-200">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0660c-200">Namespace</span></span><br/>                | <span data-ttu-id="0660c-201">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="0660c-201">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="0660c-202">MOF</span><span class="sxs-lookup"><span data-stu-id="0660c-202">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0660c-203"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0660c-203"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0660c-204">DLL</span><span class="sxs-lookup"><span data-stu-id="0660c-204">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0660c-205"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0660c-205"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

