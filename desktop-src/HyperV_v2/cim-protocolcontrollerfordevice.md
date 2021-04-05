---
description: Rappresenta un'associazione tra un dispositivo logico e un controller di protocollo connesso al dispositivo.
ms.assetid: 1a1efc60-6108-4376-9f73-d2dd41443645
title: Classe CIM_ProtocolControllerForDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProtocolControllerForDevice
- CIM_ProtocolControllerForDevice.Antecedent
- CIM_ProtocolControllerForDevice.Dependent
- CIM_ProtocolControllerForDevice.DeviceNumber
- CIM_ProtocolControllerForDevice.AccessPriority
- CIM_ProtocolControllerForDevice.AccessState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7d3ef7799cccc6e8fe8e219cddfba37cf12b8637
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883378"
---
# <a name="cim_protocolcontrollerfordevice-class"></a><span data-ttu-id="eea9c-103">CIM \_ ProtocolControllerForDevice (classe)</span><span class="sxs-lookup"><span data-stu-id="eea9c-103">CIM\_ProtocolControllerForDevice class</span></span>

<span data-ttu-id="eea9c-104">Rappresenta un'associazione tra un dispositivo logico e un controller di protocollo connesso al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="eea9c-104">Represents an association between a logical device and a protocol controller that is connected to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="eea9c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="eea9c-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.8.1000"), UMLPackagePath("CIM::Device::ProtocolController"), AMENDMENT]
class CIM_ProtocolControllerForDevice : CIM_Dependency
{
  CIM_ProtocolController REF Antecedent;
  CIM_LogicalDevice      REF Dependent;
  string                     DeviceNumber;
  uint16                     AccessPriority;
  uint16                     AccessState;
};
```

## <a name="members"></a><span data-ttu-id="eea9c-106">Members</span><span class="sxs-lookup"><span data-stu-id="eea9c-106">Members</span></span>

<span data-ttu-id="eea9c-107">La classe **CIM \_ ProtocolControllerForDevice** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="eea9c-107">The **CIM\_ProtocolControllerForDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="eea9c-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="eea9c-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="eea9c-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="eea9c-109">Properties</span></span>

<span data-ttu-id="eea9c-110">La classe **CIM \_ ProtocolControllerForDevice** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="eea9c-110">The **CIM\_ProtocolControllerForDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="eea9c-111">**AccessPriority**</span><span class="sxs-lookup"><span data-stu-id="eea9c-111">**AccessPriority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eea9c-112">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="eea9c-112">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="eea9c-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eea9c-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eea9c-114">Priorità di accesso assegnata al dispositivo tramite il controller di protocollo.</span><span class="sxs-lookup"><span data-stu-id="eea9c-114">The access priority given to the device through the protocol controller.</span></span> <span data-ttu-id="eea9c-115">La priorità più alta è il valore più basso.</span><span class="sxs-lookup"><span data-stu-id="eea9c-115">The highest priority has the lowest value.</span></span>

</dd> <dt>

<span data-ttu-id="eea9c-116">**AccessState**</span><span class="sxs-lookup"><span data-stu-id="eea9c-116">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eea9c-117">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="eea9c-117">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="eea9c-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eea9c-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eea9c-119">Accessibilità del dispositivo logico tramite il controller di protocollo</span><span class="sxs-lookup"><span data-stu-id="eea9c-119">The accessibility of the logical device through the protocol controller</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="eea9c-120">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="eea9c-120">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

<span data-ttu-id="eea9c-121">**Attivo** (2)</span><span class="sxs-lookup"><span data-stu-id="eea9c-121">**Active** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

<span data-ttu-id="eea9c-122">**Inattivo** (3)</span><span class="sxs-lookup"><span data-stu-id="eea9c-122">**Inactive** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Replication_In_Progress"></span><span id="replication_in_progress"></span><span id="REPLICATION_IN_PROGRESS"></span>

<span data-ttu-id="eea9c-123">**Replica in corso** (4)</span><span class="sxs-lookup"><span data-stu-id="eea9c-123">**Replication In Progress** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Mapping_Inconsistency"></span><span id="mapping_inconsistency"></span><span id="MAPPING_INCONSISTENCY"></span>

<span data-ttu-id="eea9c-124">**Incoerenza di mapping** (5)</span><span class="sxs-lookup"><span data-stu-id="eea9c-124">**Mapping Inconsistency** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="eea9c-125">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="eea9c-125">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eea9c-126">Tipo di dati: **CIM \_ ProtocolController**</span><span class="sxs-lookup"><span data-stu-id="eea9c-126">Data type: **CIM\_ProtocolController**</span></span>
</dt> <dt>

<span data-ttu-id="eea9c-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eea9c-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eea9c-128">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="eea9c-128">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="eea9c-129">Controller di protocollo nell'associazione.</span><span class="sxs-lookup"><span data-stu-id="eea9c-129">The protocol controller in the association.</span></span>

</dd> <dt>

<span data-ttu-id="eea9c-130">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="eea9c-130">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eea9c-131">Tipo di dati: **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="eea9c-131">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="eea9c-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eea9c-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eea9c-133">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="eea9c-133">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="eea9c-134">Dispositivo logico nell'associazione.</span><span class="sxs-lookup"><span data-stu-id="eea9c-134">The logical device in the association.</span></span>

</dd> <dt>

<span data-ttu-id="eea9c-135">**DeviceNumber**</span><span class="sxs-lookup"><span data-stu-id="eea9c-135">**DeviceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eea9c-136">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="eea9c-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eea9c-137">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eea9c-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eea9c-138">Indirizzo del dispositivo associato nel contesto del controllo del protocollo.</span><span class="sxs-lookup"><span data-stu-id="eea9c-138">The address of the associated device in the context of the protocol controler.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="eea9c-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eea9c-139">Requirements</span></span>



| <span data-ttu-id="eea9c-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="eea9c-140">Requirement</span></span> | <span data-ttu-id="eea9c-141">Valore</span><span class="sxs-lookup"><span data-stu-id="eea9c-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eea9c-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eea9c-142">Minimum supported client</span></span><br/> | <span data-ttu-id="eea9c-143">Windows 8</span><span class="sxs-lookup"><span data-stu-id="eea9c-143">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="eea9c-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eea9c-144">Minimum supported server</span></span><br/> | <span data-ttu-id="eea9c-145">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="eea9c-145">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="eea9c-146">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="eea9c-146">Namespace</span></span><br/>                | <span data-ttu-id="eea9c-147">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="eea9c-147">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="eea9c-148">MOF</span><span class="sxs-lookup"><span data-stu-id="eea9c-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eea9c-149"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="eea9c-149"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="eea9c-150">DLL</span><span class="sxs-lookup"><span data-stu-id="eea9c-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eea9c-151"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="eea9c-151"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="eea9c-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eea9c-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eea9c-153">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="eea9c-153">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

