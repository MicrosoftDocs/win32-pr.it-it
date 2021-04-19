---
description: Rappresenta i dati delle impostazioni della LAN virtuale (VLAN).
ms.assetid: c3a49021-5256-4751-a5a5-81bf1c6d6e6d
title: Classe Msvm_EthernetSwitchPortVlanSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortVlanSettingData
- Msvm_EthernetSwitchPortVlanSettingData.InstanceID
- Msvm_EthernetSwitchPortVlanSettingData.Caption
- Msvm_EthernetSwitchPortVlanSettingData.Description
- Msvm_EthernetSwitchPortVlanSettingData.ElementName
- Msvm_EthernetSwitchPortVlanSettingData.OperationMode
- Msvm_EthernetSwitchPortVlanSettingData.AccessVlanId
- Msvm_EthernetSwitchPortVlanSettingData.NativeVlanId
- Msvm_EthernetSwitchPortVlanSettingData.PvlanMode
- Msvm_EthernetSwitchPortVlanSettingData.PrimaryVlanId
- Msvm_EthernetSwitchPortVlanSettingData.SecondaryVlanId
- Msvm_EthernetSwitchPortVlanSettingData.PruneVlanIdArray
- Msvm_EthernetSwitchPortVlanSettingData.TrunkVlanIdArray
- Msvm_EthernetSwitchPortVlanSettingData.SecondaryVlanIdArray
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6fce6416696a99e5d928b774e2ba2a05b1dc21d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106320013"
---
# <a name="msvm_ethernetswitchportvlansettingdata-class"></a><span data-ttu-id="2a9c0-103">\_Classe MSVM EthernetSwitchPortVlanSettingData</span><span class="sxs-lookup"><span data-stu-id="2a9c0-103">Msvm\_EthernetSwitchPortVlanSettingData class</span></span>

<span data-ttu-id="2a9c0-104">Rappresenta i dati delle impostazioni della LAN virtuale (VLAN).</span><span class="sxs-lookup"><span data-stu-id="2a9c0-104">Represents the virtual LAN (VLAN) setting data.</span></span>

<span data-ttu-id="2a9c0-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="2a9c0-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a9c0-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2a9c0-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("952C5004-4465-451C-8CB8-FA9AB382B773"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port VLAN Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortVlanSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string InstanceID;
  string Caption = "Ethernet Switch Port VLAN Settings";
  string Description = "Represents the vlan setting data.";
  string ElementName = "Ethernet Switch Port VLAN Settings";
  uint32 OperationMode = 0;
  uint16 AccessVlanId = 0;
  uint16 NativeVlanId = 0;
  uint32 PvlanMode = 0;
  uint16 PrimaryVlanId = 0;
  uint16 SecondaryVlanId = 0;
  uint16 PruneVlanIdArray[] = {};
  uint16 TrunkVlanIdArray[] = {};
  uint16 SecondaryVlanIdArray[] = {};
};
```

## <a name="members"></a><span data-ttu-id="2a9c0-107">Members</span><span class="sxs-lookup"><span data-stu-id="2a9c0-107">Members</span></span>

<span data-ttu-id="2a9c0-108">La **classe \_ EthernetSwitchPortVlanSettingData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="2a9c0-108">The **Msvm\_EthernetSwitchPortVlanSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="2a9c0-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2a9c0-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2a9c0-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2a9c0-110">Properties</span></span>

<span data-ttu-id="2a9c0-111">La **classe \_ EthernetSwitchPortVlanSettingData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="2a9c0-111">The **Msvm\_EthernetSwitchPortVlanSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2a9c0-112">**AccessVlanId**</span><span class="sxs-lookup"><span data-stu-id="2a9c0-112">**AccessVlanId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a9c0-113">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2a9c0-113">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2a9c0-114">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="2a9c0-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="2a9c0-115">Qualificatori: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="2a9c0-115">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="2a9c0-116">Specifica l'identificatore VLAN in modalità di accesso.</span><span class="sxs-lookup"><span data-stu-id="2a9c0-116">Specifies the VLAN identifier in access mode.</span></span>

</dd> <dt>

<span data-ttu-id="2a9c0-117">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="2a9c0-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a9c0-118">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2a9c0-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a9c0-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a9c0-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a9c0-120">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2a9c0-120">A short description of the object.</span></span> <span data-ttu-id="2a9c0-121">Questa proprietà viene ereditata da [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Ethernet Switch Port VLAN Settings".</span><span class="sxs-lookup"><span data-stu-id="2a9c0-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port VLAN Settings".</span></span>

</dd> <dt>

<span data-ttu-id="2a9c0-122">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="2a9c0-122">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a9c0-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2a9c0-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a9c0-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a9c0-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a9c0-125">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="2a9c0-125">A description of the object.</span></span> <span data-ttu-id="2a9c0-126">Questa proprietà viene ereditata da [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "rappresenta i dati delle impostazioni VLAN".</span><span class="sxs-lookup"><span data-stu-id="2a9c0-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Represents the vlan setting data.".</span></span>

</dd> <dt>

<span data-ttu-id="2a9c0-127">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="2a9c0-127">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a9c0-128">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2a9c0-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a9c0-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a9c0-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a9c0-130">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2a9c0-130">A display name for the object.</span></span> <span data-ttu-id="2a9c0-131">Questa proprietà viene ereditata da [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Ethernet Switch Port VLAN Settings".</span><span class="sxs-lookup"><span data-stu-id="2a9c0-131">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port VLAN Settings".</span></span>

</dd> <dt>

<span data-ttu-id="2a9c0-132">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2a9c0-132">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a9c0-133">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2a9c0-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a9c0-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a9c0-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a9c0-135">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="2a9c0-135">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="2a9c0-136">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="2a9c0-136">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="2a9c0-137">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="2a9c0-137">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2a9c0-138">**NativeVlanId**</span><span class="sxs-lookup"><span data-stu-id="2a9c0-138">**NativeVlanId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a9c0-139">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2a9c0-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2a9c0-140">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="2a9c0-140">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="2a9c0-141">Qualificatori: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="2a9c0-141">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="2a9c0-142">Specifica l'identificatore VLAN in modalità trunk.</span><span class="sxs-lookup"><span data-stu-id="2a9c0-142">Specifies the VLAN identifier in trunk mode.</span></span>

</dd> <dt>

<span data-ttu-id="2a9c0-143">**OperationMode**</span><span class="sxs-lookup"><span data-stu-id="2a9c0-143">**OperationMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a9c0-144">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2a9c0-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2a9c0-145">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="2a9c0-145">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="2a9c0-146">Qualificatori: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="2a9c0-146">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="2a9c0-147">Specifica la modalità operativa VLAN.</span><span class="sxs-lookup"><span data-stu-id="2a9c0-147">Specifies the VLAN operation mode.</span></span>

<dt>

<span id="Access"></span><span id="access"></span><span id="ACCESS"></span>

<span data-ttu-id="2a9c0-148">**Accesso** (1)</span><span class="sxs-lookup"><span data-stu-id="2a9c0-148">**Access** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Trunk"></span><span id="trunk"></span><span id="TRUNK"></span>

<span data-ttu-id="2a9c0-149">**Trunk** (2)</span><span class="sxs-lookup"><span data-stu-id="2a9c0-149">**Trunk** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Private"></span><span id="private"></span><span id="PRIVATE"></span>

<span data-ttu-id="2a9c0-150">**Privato** (3)</span><span class="sxs-lookup"><span data-stu-id="2a9c0-150">**Private** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2a9c0-151">**PrimaryVlanId**</span><span class="sxs-lookup"><span data-stu-id="2a9c0-151">**PrimaryVlanId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a9c0-152">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2a9c0-152">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2a9c0-153">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="2a9c0-153">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="2a9c0-154">Qualificatori: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="2a9c0-154">Qualifiers: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="2a9c0-155">Specifica l'identificatore VLAN primario in modalità privata.</span><span class="sxs-lookup"><span data-stu-id="2a9c0-155">Specifies the primary VLAN identifier in private mode.</span></span>

</dd> <dt>

<span data-ttu-id="2a9c0-156">**PruneVlanIdArray**</span><span class="sxs-lookup"><span data-stu-id="2a9c0-156">**PruneVlanIdArray**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a9c0-157">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2a9c0-157">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2a9c0-158">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="2a9c0-158">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="2a9c0-159">Qualificatori: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="2a9c0-159">Qualifiers: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="2a9c0-160">Specifica la bitmap dell'identificatore della VLAN per la potatura in modalità trunk.</span><span class="sxs-lookup"><span data-stu-id="2a9c0-160">Specifies the prune VLAN identifier bitmap in trunk mode.</span></span>

</dd> <dt>

<span data-ttu-id="2a9c0-161">**PvlanMode**</span><span class="sxs-lookup"><span data-stu-id="2a9c0-161">**PvlanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a9c0-162">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2a9c0-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2a9c0-163">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="2a9c0-163">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="2a9c0-164">Qualificatori: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="2a9c0-164">Qualifiers: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="2a9c0-165">Specifica la modalità VLAN privata.</span><span class="sxs-lookup"><span data-stu-id="2a9c0-165">Specifies the private VLAN mode.</span></span>

<dt>

<span id="Isolated"></span><span id="isolated"></span><span id="ISOLATED"></span>

<span data-ttu-id="2a9c0-166">**Isolated** (1)</span><span class="sxs-lookup"><span data-stu-id="2a9c0-166">**Isolated** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Community"></span><span id="community"></span><span id="COMMUNITY"></span>

<span data-ttu-id="2a9c0-167">**Community** (2)</span><span class="sxs-lookup"><span data-stu-id="2a9c0-167">**Community** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Promiscuous"></span><span id="promiscuous"></span><span id="PROMISCUOUS"></span>

<span data-ttu-id="2a9c0-168">**Promiscua** (3)</span><span class="sxs-lookup"><span data-stu-id="2a9c0-168">**Promiscuous** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2a9c0-169">**SecondaryVlanId**</span><span class="sxs-lookup"><span data-stu-id="2a9c0-169">**SecondaryVlanId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a9c0-170">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2a9c0-170">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2a9c0-171">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="2a9c0-171">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="2a9c0-172">Qualificatori: **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="2a9c0-172">Qualifiers: **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="2a9c0-173">Specifica l'identificatore della VLAN secondaria in modalità privata.</span><span class="sxs-lookup"><span data-stu-id="2a9c0-173">Specifies the secondary VLAN identifier in private mode.</span></span>

</dd> <dt>

<span data-ttu-id="2a9c0-174">**SecondaryVlanIdArray**</span><span class="sxs-lookup"><span data-stu-id="2a9c0-174">**SecondaryVlanIdArray**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a9c0-175">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2a9c0-175">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2a9c0-176">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="2a9c0-176">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="2a9c0-177">Qualificatori: **WmiDataId** (9), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="2a9c0-177">Qualifiers: **WmiDataId** (9), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="2a9c0-178">Specifica la bitmap dell'identificatore della VLAN secondaria in modalità privata.</span><span class="sxs-lookup"><span data-stu-id="2a9c0-178">Specifies the secondary VLAN identifier bitmap in private mode.</span></span>

</dd> <dt>

<span data-ttu-id="2a9c0-179">**TrunkVlanIdArray**</span><span class="sxs-lookup"><span data-stu-id="2a9c0-179">**TrunkVlanIdArray**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a9c0-180">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2a9c0-180">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2a9c0-181">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="2a9c0-181">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="2a9c0-182">Qualificatori: **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="2a9c0-182">Qualifiers: **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="2a9c0-183">Specifica la bitmap dell'identificatore della VLAN Trunk in modalità trunk.</span><span class="sxs-lookup"><span data-stu-id="2a9c0-183">Specifies the trunk VLAN identifier bitmap in trunk mode.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2a9c0-184">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2a9c0-184">Requirements</span></span>



| <span data-ttu-id="2a9c0-185">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a9c0-185">Requirement</span></span> | <span data-ttu-id="2a9c0-186">Valore</span><span class="sxs-lookup"><span data-stu-id="2a9c0-186">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a9c0-187">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2a9c0-187">Minimum supported client</span></span><br/> | <span data-ttu-id="2a9c0-188">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="2a9c0-188">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="2a9c0-189">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2a9c0-189">Minimum supported server</span></span><br/> | <span data-ttu-id="2a9c0-190">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="2a9c0-190">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2a9c0-191">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2a9c0-191">Namespace</span></span><br/>                | <span data-ttu-id="2a9c0-192">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="2a9c0-192">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="2a9c0-193">MOF</span><span class="sxs-lookup"><span data-stu-id="2a9c0-193">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2a9c0-194"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2a9c0-194"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2a9c0-195">DLL</span><span class="sxs-lookup"><span data-stu-id="2a9c0-195">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2a9c0-196"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2a9c0-196"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

