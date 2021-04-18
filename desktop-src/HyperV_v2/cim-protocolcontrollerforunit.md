---
description: Rappresenta un'associazione tra un controller di protocollo e un'unità logica esposta.
ms.assetid: e8bf2b32-b4a6-4963-8a50-2b06776965e8
title: Classe CIM_ProtocolControllerForUnit
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProtocolControllerForUnit
- CIM_ProtocolControllerForUnit.Antecedent
- CIM_ProtocolControllerForUnit.Dependent
- CIM_ProtocolControllerForUnit.DeviceAccess
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 26020745057d5963ed4a892ba8639ac078aaa20b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314840"
---
# <a name="cim_protocolcontrollerforunit-class"></a><span data-ttu-id="c85f8-103">CIM \_ ProtocolControllerForUnit (classe)</span><span class="sxs-lookup"><span data-stu-id="c85f8-103">CIM\_ProtocolControllerForUnit class</span></span>

<span data-ttu-id="c85f8-104">Rappresenta un'associazione tra un controller di protocollo e un'unità logica esposta.</span><span class="sxs-lookup"><span data-stu-id="c85f8-104">Represents an association between a protocol controller and an exposed logical unit.</span></span>

## <a name="syntax"></a><span data-ttu-id="c85f8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c85f8-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.8.0"), UMLPackagePath("CIM::Device::ProtocolController"), AMENDMENT]
class CIM_ProtocolControllerForUnit : CIM_ProtocolControllerForDevice
{
  CIM_ProtocolController REF Antecedent;
  CIM_LogicalDevice      REF Dependent;
  uint16                     DeviceAccess;
};
```

## <a name="members"></a><span data-ttu-id="c85f8-106">Members</span><span class="sxs-lookup"><span data-stu-id="c85f8-106">Members</span></span>

<span data-ttu-id="c85f8-107">La classe **CIM \_ ProtocolControllerForUnit** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="c85f8-107">The **CIM\_ProtocolControllerForUnit** class has these types of members:</span></span>

-   [<span data-ttu-id="c85f8-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c85f8-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c85f8-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c85f8-109">Properties</span></span>

<span data-ttu-id="c85f8-110">La classe **CIM \_ ProtocolControllerForUnit** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="c85f8-110">The **CIM\_ProtocolControllerForUnit** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c85f8-111">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="c85f8-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c85f8-112">Tipo di dati: **CIM \_ ProtocolController**</span><span class="sxs-lookup"><span data-stu-id="c85f8-112">Data type: **CIM\_ProtocolController**</span></span>
</dt> <dt>

<span data-ttu-id="c85f8-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c85f8-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c85f8-114">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="c85f8-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="c85f8-115">Controller del protocollo.</span><span class="sxs-lookup"><span data-stu-id="c85f8-115">The protocol controller.</span></span>

</dd> <dt>

<span data-ttu-id="c85f8-116">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="c85f8-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c85f8-117">Tipo di dati: **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="c85f8-117">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="c85f8-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c85f8-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c85f8-119">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="c85f8-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="c85f8-120">Unità logica associata al controller del protocollo.</span><span class="sxs-lookup"><span data-stu-id="c85f8-120">The logical unit associated with the protocol controller.</span></span>

</dd> <dt>

<span data-ttu-id="c85f8-121">**DeviceAccess**</span><span class="sxs-lookup"><span data-stu-id="c85f8-121">**DeviceAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c85f8-122">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c85f8-122">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c85f8-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c85f8-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c85f8-124">Diritti di accesso concessi all'unità logica tramite il controller di protocollo.</span><span class="sxs-lookup"><span data-stu-id="c85f8-124">The access rights granted to the logical unit through the protocol controller.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c85f8-125">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="c85f8-125">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write"></span><span id="read_write"></span><span id="READ_WRITE"></span>

<span data-ttu-id="c85f8-126">**Lettura/scrittura** (2)</span><span class="sxs-lookup"><span data-stu-id="c85f8-126">**Read Write** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read-Only"></span><span id="read-only"></span><span id="READ-ONLY"></span>

<span data-ttu-id="c85f8-127">Sola **lettura** (3)</span><span class="sxs-lookup"><span data-stu-id="c85f8-127">**Read-Only** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Access"></span><span id="no_access"></span><span id="NO_ACCESS"></span>

<span data-ttu-id="c85f8-128">**Nessun accesso** (4)</span><span class="sxs-lookup"><span data-stu-id="c85f8-128">**No Access** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="c85f8-129">**DMTF riservato** (5.. 15999)</span><span class="sxs-lookup"><span data-stu-id="c85f8-129">**DMTF Reserved** (5..15999)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="c85f8-130">**Fornitore riservato** (16000...)</span><span class="sxs-lookup"><span data-stu-id="c85f8-130">**Vendor Reserved** (16000..)</span></span>


<span data-ttu-id="c85f8-131"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="c85f8-131"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="c85f8-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c85f8-132">Requirements</span></span>



| <span data-ttu-id="c85f8-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="c85f8-133">Requirement</span></span> | <span data-ttu-id="c85f8-134">Valore</span><span class="sxs-lookup"><span data-stu-id="c85f8-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c85f8-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c85f8-135">Minimum supported client</span></span><br/> | <span data-ttu-id="c85f8-136">Windows 8</span><span class="sxs-lookup"><span data-stu-id="c85f8-136">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="c85f8-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c85f8-137">Minimum supported server</span></span><br/> | <span data-ttu-id="c85f8-138">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c85f8-138">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="c85f8-139">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c85f8-139">Namespace</span></span><br/>                | <span data-ttu-id="c85f8-140">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="c85f8-140">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c85f8-141">MOF</span><span class="sxs-lookup"><span data-stu-id="c85f8-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c85f8-142"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c85f8-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c85f8-143">DLL</span><span class="sxs-lookup"><span data-stu-id="c85f8-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c85f8-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c85f8-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c85f8-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c85f8-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c85f8-146">**\_PROTOCOLCONTROLLERFORDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="c85f8-146">**CIM\_ProtocolControllerForDevice**</span></span>](cim-protocolcontrollerfordevice.md)
</dt> </dl>

 

