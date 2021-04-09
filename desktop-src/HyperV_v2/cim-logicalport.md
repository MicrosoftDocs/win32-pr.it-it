---
description: Astrazione di una porta o di un punto di connessione di un dispositivo.
ms.assetid: ee725c64-587b-4e5f-9b1c-7a58902b0631
title: Classe CIM_LogicalPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalPort
- CIM_LogicalPort.Speed
- CIM_LogicalPort.MaxSpeed
- CIM_LogicalPort.RequestedSpeed
- CIM_LogicalPort.UsageRestriction
- CIM_LogicalPort.PortType
- CIM_LogicalPort.OtherPortType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: eeed69e9669048377340cb0ca21e7a2e89f4baff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966437"
---
# <a name="cim_logicalport-class"></a><span data-ttu-id="d646f-103">CIM \_ LogicalPort (classe)</span><span class="sxs-lookup"><span data-stu-id="d646f-103">CIM\_LogicalPort class</span></span>

<span data-ttu-id="d646f-104">Astrazione di una porta o di un punto di connessione di un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d646f-104">The abstraction of a port or connection point of a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="d646f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d646f-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::Ports"), AMENDMENT]
class CIM_LogicalPort : CIM_LogicalDevice
{
  uint64 Speed;
  uint64 MaxSpeed;
  uint64 RequestedSpeed;
  uint16 UsageRestriction;
  uint16 PortType;
  string OtherPortType;
};
```

## <a name="members"></a><span data-ttu-id="d646f-106">Members</span><span class="sxs-lookup"><span data-stu-id="d646f-106">Members</span></span>

<span data-ttu-id="d646f-107">La classe **CIM \_ LogicalPort** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="d646f-107">The **CIM\_LogicalPort** class has these types of members:</span></span>

-   [<span data-ttu-id="d646f-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d646f-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d646f-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d646f-109">Properties</span></span>

<span data-ttu-id="d646f-110">La classe **CIM \_ LogicalPort** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="d646f-110">The **CIM\_LogicalPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d646f-111">**MaxSpeed**</span><span class="sxs-lookup"><span data-stu-id="d646f-111">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d646f-112">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d646f-112">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d646f-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d646f-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d646f-114">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("bit al secondo"), **punito** ("bit/secondo")</span><span class="sxs-lookup"><span data-stu-id="d646f-114">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits per Second"), **PUnit** ("bit / second")</span></span>
</dt> </dl>

<span data-ttu-id="d646f-115">Larghezza di banda massima della porta, in bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="d646f-115">The maximum bandwidth of the port, in bits per second.</span></span>

</dd> <dt>

<span data-ttu-id="d646f-116">**OtherPortType**</span><span class="sxs-lookup"><span data-stu-id="d646f-116">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d646f-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d646f-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d646f-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d646f-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d646f-119">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ LogicalPort**.**PortType**")</span><span class="sxs-lookup"><span data-stu-id="d646f-119">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_LogicalPort**.**PortType**")</span></span>
</dt> </dl>

<span data-ttu-id="d646f-120">Descrive il tipo di modulo quando **portType** è impostato su **other** ("1").</span><span class="sxs-lookup"><span data-stu-id="d646f-120">Describes the type of module, when **PortType** is set to **Other** ("1").</span></span>

</dd> <dt>

<span data-ttu-id="d646f-121">**PortType**</span><span class="sxs-lookup"><span data-stu-id="d646f-121">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d646f-122">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d646f-122">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d646f-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d646f-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d646f-124">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ NetworkPort**](cim-networkport.md).**OtherNetworkPortType**")</span><span class="sxs-lookup"><span data-stu-id="d646f-124">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_NetworkPort**](cim-networkport.md).**OtherNetworkPortType**")</span></span>
</dt> </dl>

<span data-ttu-id="d646f-125">Tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="d646f-125">The port type.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d646f-126">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="d646f-126">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d646f-127">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="d646f-127">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="d646f-128">**Non applicabile** (2)</span><span class="sxs-lookup"><span data-stu-id="d646f-128">**Not Applicable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="d646f-129">**DMTF riservato** (3.. 15999)</span><span class="sxs-lookup"><span data-stu-id="d646f-129">**DMTF Reserved** (3..15999)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="d646f-130">**Fornitore riservato** (16000.65535)</span><span class="sxs-lookup"><span data-stu-id="d646f-130">**Vendor Reserved** (16000..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d646f-131">**RequestedSpeed**</span><span class="sxs-lookup"><span data-stu-id="d646f-131">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d646f-132">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d646f-132">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d646f-133">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d646f-133">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d646f-134">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("bit al secondo"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ LogicalPort**.**Velocità**"), **punito** (" bit/secondo ")</span><span class="sxs-lookup"><span data-stu-id="d646f-134">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits per Second"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_LogicalPort**.**Speed**"), **PUnit** ("bit / second")</span></span>
</dt> </dl>

<span data-ttu-id="d646f-135">Larghezza di banda richiesta della porta, in bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="d646f-135">The requested bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="d646f-136">La larghezza di banda effettiva viene segnalata nella proprietà **velocità** .</span><span class="sxs-lookup"><span data-stu-id="d646f-136">The actual bandwidth is reported in the **Speed** property.</span></span>

</dd> <dt>

<span data-ttu-id="d646f-137">**Velocità**</span><span class="sxs-lookup"><span data-stu-id="d646f-137">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d646f-138">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d646f-138">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d646f-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d646f-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d646f-140">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("bit al secondo"), **punito** ("bit/secondo")</span><span class="sxs-lookup"><span data-stu-id="d646f-140">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits per Second"), **PUnit** ("bit / second")</span></span>
</dt> </dl>

<span data-ttu-id="d646f-141">Larghezza di banda della porta, in bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="d646f-141">The bandwidth of the port, in bits per second.</span></span>

</dd> <dt>

<span data-ttu-id="d646f-142">**UsageRestriction**</span><span class="sxs-lookup"><span data-stu-id="d646f-142">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d646f-143">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d646f-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d646f-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d646f-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d646f-145">Indica se la porta è limitata a una porta front-end o back-end.</span><span class="sxs-lookup"><span data-stu-id="d646f-145">Indicates whether the port is restricted to being a front-end or back-end port.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d646f-146">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="d646f-146">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>

<span data-ttu-id="d646f-147">**Solo front-end** (2)</span><span class="sxs-lookup"><span data-stu-id="d646f-147">**Front-end only** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>

<span data-ttu-id="d646f-148">**Solo back-end** (3)</span><span class="sxs-lookup"><span data-stu-id="d646f-148">**Back-end only** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_restricted"></span><span id="not_restricted"></span><span id="NOT_RESTRICTED"></span>

<span data-ttu-id="d646f-149">**Senza restrizioni** (4)</span><span class="sxs-lookup"><span data-stu-id="d646f-149">**Not restricted** (4)</span></span>


<span data-ttu-id="d646f-150"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="d646f-150"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="d646f-151">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d646f-151">Requirements</span></span>



| <span data-ttu-id="d646f-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="d646f-152">Requirement</span></span> | <span data-ttu-id="d646f-153">Valore</span><span class="sxs-lookup"><span data-stu-id="d646f-153">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d646f-154">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d646f-154">Minimum supported client</span></span><br/> | <span data-ttu-id="d646f-155">Windows 8</span><span class="sxs-lookup"><span data-stu-id="d646f-155">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="d646f-156">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d646f-156">Minimum supported server</span></span><br/> | <span data-ttu-id="d646f-157">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d646f-157">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="d646f-158">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d646f-158">Namespace</span></span><br/>                | <span data-ttu-id="d646f-159">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="d646f-159">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d646f-160">MOF</span><span class="sxs-lookup"><span data-stu-id="d646f-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d646f-161"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d646f-161"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d646f-162">DLL</span><span class="sxs-lookup"><span data-stu-id="d646f-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d646f-163"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d646f-163"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d646f-164">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d646f-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d646f-165">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="d646f-165">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

