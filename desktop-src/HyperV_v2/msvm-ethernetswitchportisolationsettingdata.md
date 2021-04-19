---
description: Rappresenta i dati dell'impostazione di isolamento.
ms.assetid: f6bf5fcf-61c4-4e69-8ba0-fff4c4873368
title: Classe Msvm_EthernetSwitchPortIsolationSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortIsolationSettingData
- Msvm_EthernetSwitchPortIsolationSettingData.IsolationMode
- Msvm_EthernetSwitchPortIsolationSettingData.AllowUntaggedTraffic
- Msvm_EthernetSwitchPortIsolationSettingData.DefaultIsolationId
- Msvm_EthernetSwitchPortIsolationSettingData.EnableMultiTenantStack
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3d7761b090cfd3bf2ae6aaaa92e9c5d09d55eae6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313856"
---
# <a name="msvm_ethernetswitchportisolationsettingdata-class"></a><span data-ttu-id="5c61a-103">\_Classe MSVM EthernetSwitchPortIsolationSettingData</span><span class="sxs-lookup"><span data-stu-id="5c61a-103">Msvm\_EthernetSwitchPortIsolationSettingData class</span></span>

<span data-ttu-id="5c61a-104">Rappresenta i dati dell'impostazione di isolamento.</span><span class="sxs-lookup"><span data-stu-id="5c61a-104">Represents the Isolation setting data.</span></span>

<span data-ttu-id="5c61a-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="5c61a-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c61a-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5c61a-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("83AF2CCB-72C9-4479-A285-94E58A98CAA6"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Isolation Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortIsolationSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  uint32  IsolationMode = 0;
  boolean AllowUntaggedTraffic = FALSE;
  uint32  DefaultIsolationId = 0;
  Boolean EnableMultiTenantStack = FALSE;
};
```

## <a name="members"></a><span data-ttu-id="5c61a-107">Members</span><span class="sxs-lookup"><span data-stu-id="5c61a-107">Members</span></span>

<span data-ttu-id="5c61a-108">La **classe \_ EthernetSwitchPortIsolationSettingData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="5c61a-108">The **Msvm\_EthernetSwitchPortIsolationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="5c61a-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5c61a-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5c61a-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5c61a-110">Properties</span></span>

<span data-ttu-id="5c61a-111">La **classe \_ EthernetSwitchPortIsolationSettingData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="5c61a-111">The **Msvm\_EthernetSwitchPortIsolationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5c61a-112">**AllowUntaggedTraffic**</span><span class="sxs-lookup"><span data-stu-id="5c61a-112">**AllowUntaggedTraffic**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c61a-113">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="5c61a-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5c61a-114">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5c61a-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5c61a-115">Qualificatori: **WmiDataId** (2), [**versione**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revisione**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="5c61a-115">Qualifiers: **WmiDataId** (2), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="5c61a-116">Indica se la porta è autorizzata a inviare/ricevere traffico senza tag.</span><span class="sxs-lookup"><span data-stu-id="5c61a-116">Whether the port is allowed to send/receive untagged traffic.</span></span>

</dd> <dt>

<span data-ttu-id="5c61a-117">**DefaultIsolationId**</span><span class="sxs-lookup"><span data-stu-id="5c61a-117">**DefaultIsolationId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c61a-118">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5c61a-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5c61a-119">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5c61a-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5c61a-120">Qualificatori: **WmiDataId** (3), [**versione**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revisione**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="5c61a-120">Qualifiers: **WmiDataId** (3), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="5c61a-121">Il valore predefinito di VirtualSubnetId o VLAN che verrà impostato su tutto il traffico di invio/ricezione se **AllowedUntaggedTraffic** è **true**.</span><span class="sxs-lookup"><span data-stu-id="5c61a-121">The default VirtualSubnetId or VLAN that will be set on all send/receive traffic if **AllowedUntaggedTraffic** is **true**.</span></span>

</dd> <dt>

<span data-ttu-id="5c61a-122">**EnableMultiTenantStack**</span><span class="sxs-lookup"><span data-stu-id="5c61a-122">**EnableMultiTenantStack**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c61a-123">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="5c61a-123">Data type: **Boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5c61a-124">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5c61a-124">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5c61a-125">Qualificatori: **WmiDataId** (4), [**versione**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revisione**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="5c61a-125">Qualifiers: **WmiDataId** (4), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="5c61a-126">Se **true**, lo stack di rete nella macchina virtuale sarà in grado di accedere alla configurazione di isolamento.</span><span class="sxs-lookup"><span data-stu-id="5c61a-126">If **true**, the network stack in the VM will be able to access the isolation configuration.</span></span> <span data-ttu-id="5c61a-127">Il valore predefinito è **false**.</span><span class="sxs-lookup"><span data-stu-id="5c61a-127">The default value is **false**.</span></span>

</dd> <dt>

<span data-ttu-id="5c61a-128">**IsolationMode**</span><span class="sxs-lookup"><span data-stu-id="5c61a-128">**IsolationMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c61a-129">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5c61a-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5c61a-130">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5c61a-130">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5c61a-131">Qualificatori: **WmiDataId** (1), [**versione**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revisione**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="5c61a-131">Qualifiers: **WmiDataId** (1), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="5c61a-132">Indica se la porta usa **VLAN** o **VirtualSubnetId** per l'isolamento.</span><span class="sxs-lookup"><span data-stu-id="5c61a-132">Whether the port is using **VLAN** or **VirtualSubnetId** for isolation.</span></span> <span data-ttu-id="5c61a-133">**NativeVirtualSubnetId** viene usato per le reti basate su VirtualSubnetId WNV.</span><span class="sxs-lookup"><span data-stu-id="5c61a-133">**NativeVirtualSubnetId** is used for WNV VirtualSubnetId-based networks.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="5c61a-134">**Nessuno** (0)</span><span class="sxs-lookup"><span data-stu-id="5c61a-134">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="NativeVirtualSubnetId"></span><span id="nativevirtualsubnetid"></span><span id="NATIVEVIRTUALSUBNETID"></span>

<span data-ttu-id="5c61a-135">**NativeVirtualSubnetId** (1)</span><span class="sxs-lookup"><span data-stu-id="5c61a-135">**NativeVirtualSubnetId** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="ExternalVirtualSubnetId"></span><span id="externalvirtualsubnetid"></span><span id="EXTERNALVIRTUALSUBNETID"></span>

<span data-ttu-id="5c61a-136">**ExternalVirtualSubnetId** (2)</span><span class="sxs-lookup"><span data-stu-id="5c61a-136">**ExternalVirtualSubnetId** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="VLAN"></span><span id="vlan"></span>

<span data-ttu-id="5c61a-137">**VLAN** (3)</span><span class="sxs-lookup"><span data-stu-id="5c61a-137">**VLAN** (3)</span></span>


<span data-ttu-id="5c61a-138"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="5c61a-138"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="5c61a-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5c61a-139">Requirements</span></span>



| <span data-ttu-id="5c61a-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c61a-140">Requirement</span></span> | <span data-ttu-id="5c61a-141">Valore</span><span class="sxs-lookup"><span data-stu-id="5c61a-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c61a-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5c61a-142">Minimum supported client</span></span><br/> | <span data-ttu-id="5c61a-143">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="5c61a-143">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="5c61a-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5c61a-144">Minimum supported server</span></span><br/> | <span data-ttu-id="5c61a-145">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="5c61a-145">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="5c61a-146">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5c61a-146">Namespace</span></span><br/>                | <span data-ttu-id="5c61a-147">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="5c61a-147">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="5c61a-148">MOF</span><span class="sxs-lookup"><span data-stu-id="5c61a-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5c61a-149"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5c61a-149"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5c61a-150">DLL</span><span class="sxs-lookup"><span data-stu-id="5c61a-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c61a-151"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5c61a-151"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5c61a-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5c61a-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c61a-153">**\_EthernetSwitchPortFeatureSettingData MSVM**</span><span class="sxs-lookup"><span data-stu-id="5c61a-153">**Msvm\_EthernetSwitchPortFeatureSettingData**</span></span>](msvm-ethernetswitchportfeaturesettingdata.md)
</dt> </dl>

 

