---
description: Rappresenta i dati di stato della funzionalità della larghezza di banda della porta.
ms.assetid: 1f7be0dd-3d2f-49ef-aff0-cb162389194a
title: Classe Msvm_EthernetSwitchPortBandwidthData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortBandwidthData
- Msvm_EthernetSwitchPortBandwidthData.InstanceID
- Msvm_EthernetSwitchPortBandwidthData.Caption
- Msvm_EthernetSwitchPortBandwidthData.Description
- Msvm_EthernetSwitchPortBandwidthData.ElementName
- Msvm_EthernetSwitchPortBandwidthData.SystemCreationClassName
- Msvm_EthernetSwitchPortBandwidthData.SystemName
- Msvm_EthernetSwitchPortBandwidthData.DeviceCreationClassName
- Msvm_EthernetSwitchPortBandwidthData.DeviceID
- Msvm_EthernetSwitchPortBandwidthData.CreationClassName
- Msvm_EthernetSwitchPortBandwidthData.Name
- Msvm_EthernetSwitchPortBandwidthData.CurrentBandwidthReservationPercentage
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 55e8ad735d712bdd388e42b1f4174ee1a78af184
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308212"
---
# <a name="msvm_ethernetswitchportbandwidthdata-class"></a><span data-ttu-id="0133d-103">\_Classe MSVM EthernetSwitchPortBandwidthData</span><span class="sxs-lookup"><span data-stu-id="0133d-103">Msvm\_EthernetSwitchPortBandwidthData class</span></span>

<span data-ttu-id="0133d-104">Rappresenta i dati di stato della funzionalità della larghezza di banda della porta.</span><span class="sxs-lookup"><span data-stu-id="0133d-104">Represents the port bandwidth feature status data.</span></span>

<span data-ttu-id="0133d-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="0133d-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0133d-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0133d-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("24AD3CE1-69BD-4978-B2AC-DAAD389D699C"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Bandwidth Feature Status"), AMENDMENT]
class Msvm_EthernetSwitchPortBandwidthData : Msvm_EthernetPortData
{
  string InstanceID;
  string Caption = "Ethernet Switch Port Bandwidth Feature Status";
  string Description = "Represents the port bandwidth feature status data.";
  string ElementName = "Ethernet Switch Port Bandwidth Feature Status";
  string SystemCreationClassName = "Msvm_VirtualEthernetSwitch";
  string SystemName;
  string DeviceCreationClassName = "Msvm_EthernetSwitchPort";
  string DeviceID;
  string CreationClassName = "Msvm_EthernetSwitchPortBandwidthData";
  string Name;
  uint32 CurrentBandwidthReservationPercentage = 0;
};
```

## <a name="members"></a><span data-ttu-id="0133d-107">Members</span><span class="sxs-lookup"><span data-stu-id="0133d-107">Members</span></span>

<span data-ttu-id="0133d-108">La **classe \_ EthernetSwitchPortBandwidthData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="0133d-108">The **Msvm\_EthernetSwitchPortBandwidthData** class has these types of members:</span></span>

-   [<span data-ttu-id="0133d-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0133d-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0133d-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0133d-110">Properties</span></span>

<span data-ttu-id="0133d-111">La **classe \_ EthernetSwitchPortBandwidthData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="0133d-111">The **Msvm\_EthernetSwitchPortBandwidthData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0133d-112">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="0133d-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0133d-113">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0133d-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0133d-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0133d-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0133d-115">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="0133d-115">A short description of the object.</span></span> <span data-ttu-id="0133d-116">Questa proprietà viene ereditata da [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Ethernet Switch Port Bandwidth status feature status".</span><span class="sxs-lookup"><span data-stu-id="0133d-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Bandwidth Feature Status".</span></span>

</dd> <dt>

<span data-ttu-id="0133d-117">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0133d-117">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0133d-118">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0133d-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0133d-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0133d-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0133d-120">Qualificatori: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="0133d-120">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="0133d-121">Nome della sottoclasse utilizzata per la creazione di questa istanza di dati di porta.</span><span class="sxs-lookup"><span data-stu-id="0133d-121">The name of the subclass used in the creation of this port data instance.</span></span> <span data-ttu-id="0133d-122">Questa proprietà viene ereditata da [**MSVM \_ EthernetPortData**](msvm-ethernetportdata.md)ed è sempre impostata su "MSVM \_ EthernetSwitchPortBandwidthData".</span><span class="sxs-lookup"><span data-stu-id="0133d-122">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md), and it is always set to "Msvm\_EthernetSwitchPortBandwidthData".</span></span>

</dd> <dt>

<span data-ttu-id="0133d-123">**CurrentBandwidthReservationPercentage**</span><span class="sxs-lookup"><span data-stu-id="0133d-123">**CurrentBandwidthReservationPercentage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0133d-124">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0133d-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0133d-125">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="0133d-125">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0133d-126">Qualificatori: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="0133d-126">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="0133d-127">Percentuale di larghezza di banda corrente riservata per questa porta.</span><span class="sxs-lookup"><span data-stu-id="0133d-127">The current percentage of bandwidth reserved for this port.</span></span>

</dd> <dt>

<span data-ttu-id="0133d-128">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="0133d-128">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0133d-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0133d-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0133d-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0133d-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0133d-131">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="0133d-131">A description of the object.</span></span> <span data-ttu-id="0133d-132">Questa proprietà viene ereditata da [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "rappresenta i dati di stato della funzionalità della larghezza di banda della porta".</span><span class="sxs-lookup"><span data-stu-id="0133d-132">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Represents the port bandwidth feature status data.".</span></span>

</dd> <dt>

<span data-ttu-id="0133d-133">**DeviceCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0133d-133">**DeviceCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0133d-134">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0133d-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0133d-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0133d-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0133d-136">Qualificatori: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="0133d-136">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="0133d-137">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="0133d-137">The scoping system's creation class name.</span></span> <span data-ttu-id="0133d-138">Questa proprietà viene ereditata da [**MSVM \_ EthernetPortData**](msvm-ethernetportdata.md)ed è sempre impostata su "MSVM \_ EthernetSwitchPort".</span><span class="sxs-lookup"><span data-stu-id="0133d-138">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md), and it is always set to "Msvm\_EthernetSwitchPort".</span></span>

</dd> <dt>

<span data-ttu-id="0133d-139">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="0133d-139">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0133d-140">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0133d-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0133d-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0133d-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0133d-142">Qualificatori: **Key**, **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="0133d-142">Qualifiers: **Key**, **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="0133d-143">ID dispositivo della porta che ha come ambito questa istanza di dati di porta.</span><span class="sxs-lookup"><span data-stu-id="0133d-143">The Device ID of the port that scopes this port data instance.</span></span> <span data-ttu-id="0133d-144">Questa proprietà viene ereditata da [**MSVM \_ EthernetPortData**](msvm-ethernetportdata.md).</span><span class="sxs-lookup"><span data-stu-id="0133d-144">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="0133d-145">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="0133d-145">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0133d-146">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0133d-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0133d-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0133d-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0133d-148">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="0133d-148">A display name for the object.</span></span> <span data-ttu-id="0133d-149">Questa proprietà viene ereditata da [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Ethernet Switch Port Bandwidth status feature status".</span><span class="sxs-lookup"><span data-stu-id="0133d-149">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Bandwidth Feature Status".</span></span>

</dd> <dt>

<span data-ttu-id="0133d-150">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="0133d-150">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0133d-151">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0133d-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0133d-152">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0133d-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0133d-153">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="0133d-153">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="0133d-154">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="0133d-154">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="0133d-155">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="0133d-155">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="0133d-156">**Nome**</span><span class="sxs-lookup"><span data-stu-id="0133d-156">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0133d-157">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0133d-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0133d-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0133d-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0133d-159">Qualificatori: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="0133d-159">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="0133d-160">Stringa che identifica in modo univoco questa istanza di dati di porta nell'ambito dell'opzione e della porta.</span><span class="sxs-lookup"><span data-stu-id="0133d-160">A string that uniquely identifies this port data instance within the scope of the switch and port.</span></span> <span data-ttu-id="0133d-161">Questa proprietà viene ereditata da [**MSVM \_ EthernetPortData**](msvm-ethernetportdata.md).</span><span class="sxs-lookup"><span data-stu-id="0133d-161">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="0133d-162">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0133d-162">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0133d-163">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0133d-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0133d-164">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0133d-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0133d-165">Qualificatori: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="0133d-165">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="0133d-166">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="0133d-166">The scoping system's creation class name.</span></span> <span data-ttu-id="0133d-167">Questa proprietà viene ereditata da [**MSVM \_ EthernetPortData**](msvm-ethernetportdata.md)ed è sempre impostata su "MSVM \_ VirtualEthernetSwitch".</span><span class="sxs-lookup"><span data-stu-id="0133d-167">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md), and it is always set to "Msvm\_VirtualEthernetSwitch".</span></span>

</dd> <dt>

<span data-ttu-id="0133d-168">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="0133d-168">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0133d-169">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0133d-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0133d-170">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0133d-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0133d-171">Qualificatori: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="0133d-171">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="0133d-172">Nome del Commuter virtuale che ha come ambito questa istanza di dati di porta.</span><span class="sxs-lookup"><span data-stu-id="0133d-172">The name of the virtual switch that scopes this port data instance.</span></span> <span data-ttu-id="0133d-173">Questa proprietà viene ereditata da [**MSVM \_ EthernetPortData**](msvm-ethernetportdata.md).</span><span class="sxs-lookup"><span data-stu-id="0133d-173">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0133d-174">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0133d-174">Requirements</span></span>



| <span data-ttu-id="0133d-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="0133d-175">Requirement</span></span> | <span data-ttu-id="0133d-176">Valore</span><span class="sxs-lookup"><span data-stu-id="0133d-176">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0133d-177">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0133d-177">Minimum supported client</span></span><br/> | <span data-ttu-id="0133d-178">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="0133d-178">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="0133d-179">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0133d-179">Minimum supported server</span></span><br/> | <span data-ttu-id="0133d-180">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="0133d-180">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0133d-181">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0133d-181">Namespace</span></span><br/>                | <span data-ttu-id="0133d-182">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="0133d-182">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="0133d-183">MOF</span><span class="sxs-lookup"><span data-stu-id="0133d-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0133d-184"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0133d-184"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0133d-185">DLL</span><span class="sxs-lookup"><span data-stu-id="0133d-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0133d-186"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0133d-186"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

