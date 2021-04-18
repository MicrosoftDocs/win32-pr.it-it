---
description: Rappresenta lo stato della risorsa per la larghezza di banda
ms.assetid: 9aa3e57e-9452-4c60-a052-83ae35b3607c
title: Classe Msvm_EthernetSwitchBandwidthData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchBandwidthData
- Msvm_EthernetSwitchBandwidthData.InstanceID
- Msvm_EthernetSwitchBandwidthData.Caption
- Msvm_EthernetSwitchBandwidthData.Description
- Msvm_EthernetSwitchBandwidthData.ElementName
- Msvm_EthernetSwitchBandwidthData.SystemCreationClassName
- Msvm_EthernetSwitchBandwidthData.SystemName
- Msvm_EthernetSwitchBandwidthData.CreationClassName
- Msvm_EthernetSwitchBandwidthData.Name
- Msvm_EthernetSwitchBandwidthData.Capacity
- Msvm_EthernetSwitchBandwidthData.Reservation
- Msvm_EthernetSwitchBandwidthData.DefaultFlowReservationPercentage
- Msvm_EthernetSwitchBandwidthData.DefaultFlowReservation
- Msvm_EthernetSwitchBandwidthData.DefaultFlowWeight
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d238b8ddc40506a3eae8a6c7c089de2ebd87db5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306634"
---
# <a name="msvm_ethernetswitchbandwidthdata-class"></a><span data-ttu-id="6406a-103">\_Classe MSVM EthernetSwitchBandwidthData</span><span class="sxs-lookup"><span data-stu-id="6406a-103">Msvm\_EthernetSwitchBandwidthData class</span></span>

<span data-ttu-id="6406a-104">Rappresenta lo stato della risorsa per la larghezza di banda</span><span class="sxs-lookup"><span data-stu-id="6406a-104">Represents the switch bandwidth resource status.</span></span>

<span data-ttu-id="6406a-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="6406a-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6406a-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6406a-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("8F425906-034D-42AB-BD16-EDB31CEC55EF"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Bandwidth data"), AMENDMENT]
class Msvm_EthernetSwitchBandwidthData : Msvm_EthernetSwitchData
{
  string InstanceID;
  string Caption = "Ethernet Switch Bandwidth data";
  string Description = "Represents the switch bandwidth resource status.";
  string ElementName = "Ethernet Switch Bandwidth data";
  string SystemCreationClassName = "Msvm_VirtualEthernetSwitch";
  string SystemName;
  string CreationClassName = "Msvm_EthernetSwitchBandwidthData";
  string Name;
  uint64 Capacity = 100000000;
  uint64 Reservation = 100000000;
  uint32 DefaultFlowReservationPercentage = 10;
  uint64 DefaultFlowReservation = 100000000;
  uint64 DefaultFlowWeight = 0;
};
```

## <a name="members"></a><span data-ttu-id="6406a-107">Members</span><span class="sxs-lookup"><span data-stu-id="6406a-107">Members</span></span>

<span data-ttu-id="6406a-108">La **classe \_ EthernetSwitchBandwidthData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="6406a-108">The **Msvm\_EthernetSwitchBandwidthData** class has these types of members:</span></span>

-   [<span data-ttu-id="6406a-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6406a-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6406a-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6406a-110">Properties</span></span>

<span data-ttu-id="6406a-111">La **classe \_ EthernetSwitchBandwidthData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="6406a-111">The **Msvm\_EthernetSwitchBandwidthData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6406a-112">**Capacity**</span><span class="sxs-lookup"><span data-stu-id="6406a-112">**Capacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6406a-113">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6406a-113">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6406a-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6406a-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6406a-115">Qualificatori: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="6406a-115">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="6406a-116">Larghezza di banda massima disponibile sul Commuter.</span><span class="sxs-lookup"><span data-stu-id="6406a-116">The maximum bandwidth available on the switch.</span></span>

</dd> <dt>

<span data-ttu-id="6406a-117">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="6406a-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6406a-118">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6406a-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6406a-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6406a-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6406a-120">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="6406a-120">A short description of the object.</span></span> <span data-ttu-id="6406a-121">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="6406a-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="6406a-122">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="6406a-122">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6406a-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6406a-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6406a-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6406a-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6406a-125">Qualificatori: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="6406a-125">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="6406a-126">Nome della classe o della sottoclasse utilizzata per la creazione di questa istanza.</span><span class="sxs-lookup"><span data-stu-id="6406a-126">The name of the class or subclass used in the creation of this instance.</span></span>

</dd> <dt>

<span data-ttu-id="6406a-127">**DefaultFlowReservation**</span><span class="sxs-lookup"><span data-stu-id="6406a-127">**DefaultFlowReservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6406a-128">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6406a-128">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6406a-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6406a-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6406a-130">Qualificatori: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="6406a-130">Qualifiers: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="6406a-131">Larghezza di banda assoluta corrente riservata nell'opzione per il flusso predefinito.</span><span class="sxs-lookup"><span data-stu-id="6406a-131">The current absolute bandwidth reserved on the switch for default flow.</span></span>

</dd> <dt>

<span data-ttu-id="6406a-132">**DefaultFlowReservationPercentage**</span><span class="sxs-lookup"><span data-stu-id="6406a-132">**DefaultFlowReservationPercentage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6406a-133">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6406a-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6406a-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6406a-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6406a-135">Qualificatori: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="6406a-135">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="6406a-136">Percentuale corrente della larghezza di banda riservata nell'opzione per il flusso predefinito.</span><span class="sxs-lookup"><span data-stu-id="6406a-136">The current percentage of bandwidth reserved on the switch for default flow.</span></span>

</dd> <dt>

<span data-ttu-id="6406a-137">**DefaultFlowWeight**</span><span class="sxs-lookup"><span data-stu-id="6406a-137">**DefaultFlowWeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6406a-138">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6406a-138">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6406a-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6406a-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6406a-140">Qualificatori: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="6406a-140">Qualifiers: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="6406a-141">Spessore corrente del flusso predefinito dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="6406a-141">The current weight for the default flow on the switch.</span></span>

</dd> <dt>

<span data-ttu-id="6406a-142">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="6406a-142">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6406a-143">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6406a-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6406a-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6406a-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6406a-145">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="6406a-145">A description of the object.</span></span> <span data-ttu-id="6406a-146">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="6406a-146">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="6406a-147">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="6406a-147">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6406a-148">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6406a-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6406a-149">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6406a-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6406a-150">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="6406a-150">A display name for the object.</span></span> <span data-ttu-id="6406a-151">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="6406a-151">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="6406a-152">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="6406a-152">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6406a-153">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6406a-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6406a-154">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6406a-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6406a-155">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="6406a-155">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="6406a-156">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="6406a-156">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="6406a-157">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="6406a-157">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="6406a-158">**Nome**</span><span class="sxs-lookup"><span data-stu-id="6406a-158">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6406a-159">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6406a-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6406a-160">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6406a-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6406a-161">Qualificatori: **chiave**, **override**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="6406a-161">Qualifiers: **Key**, **Override**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="6406a-162">Nome univoco della risorsa.</span><span class="sxs-lookup"><span data-stu-id="6406a-162">The unique name of the resource.</span></span>

</dd> <dt>

<span data-ttu-id="6406a-163">**Prenotazione**</span><span class="sxs-lookup"><span data-stu-id="6406a-163">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6406a-164">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6406a-164">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6406a-165">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6406a-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6406a-166">Qualificatori: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="6406a-166">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="6406a-167">Larghezza di banda corrente riservata sull'opzione.</span><span class="sxs-lookup"><span data-stu-id="6406a-167">The current bandwidth reserved on the switch.</span></span>

</dd> <dt>

<span data-ttu-id="6406a-168">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="6406a-168">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6406a-169">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6406a-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6406a-170">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6406a-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6406a-171">Qualificatori: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="6406a-171">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="6406a-172">Nome della classe di creazione del sistema di hosting.</span><span class="sxs-lookup"><span data-stu-id="6406a-172">The hosting system's creation class name.</span></span> <span data-ttu-id="6406a-173">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="6406a-173">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="6406a-174">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="6406a-174">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6406a-175">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6406a-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6406a-176">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6406a-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6406a-177">Qualificatori: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="6406a-177">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="6406a-178">Nome del commutire virtuale a cui è associata l'istanza della risorsa associata.</span><span class="sxs-lookup"><span data-stu-id="6406a-178">The name of the virtual switch to which the associated resource instance is bound.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6406a-179">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6406a-179">Requirements</span></span>



| <span data-ttu-id="6406a-180">Requisito</span><span class="sxs-lookup"><span data-stu-id="6406a-180">Requirement</span></span> | <span data-ttu-id="6406a-181">Valore</span><span class="sxs-lookup"><span data-stu-id="6406a-181">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6406a-182">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6406a-182">Minimum supported client</span></span><br/> | <span data-ttu-id="6406a-183">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="6406a-183">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="6406a-184">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6406a-184">Minimum supported server</span></span><br/> | <span data-ttu-id="6406a-185">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="6406a-185">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6406a-186">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6406a-186">Namespace</span></span><br/>                | <span data-ttu-id="6406a-187">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="6406a-187">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="6406a-188">MOF</span><span class="sxs-lookup"><span data-stu-id="6406a-188">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6406a-189"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6406a-189"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6406a-190">DLL</span><span class="sxs-lookup"><span data-stu-id="6406a-190">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6406a-191"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6406a-191"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

