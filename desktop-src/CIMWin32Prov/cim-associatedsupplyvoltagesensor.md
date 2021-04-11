---
description: Associa un alimentatore a un sensore di tensione che monitora la tensione di input.
ms.assetid: 4164320e-8362-4ce2-9949-f14669278bd8
ms.tgt_platform: multiple
title: Classe CIM_AssociatedSupplyVoltageSensor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AssociatedSupplyVoltageSensor
- CIM_AssociatedSupplyVoltageSensor.Dependent
- CIM_AssociatedSupplyVoltageSensor.Antecedent
- CIM_AssociatedSupplyVoltageSensor.MonitoringRange
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ce597fb9e170b63335c56e30f8f8c4ddb30af66c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127206"
---
# <a name="cim_associatedsupplyvoltagesensor-class"></a><span data-ttu-id="d8d07-103">CIM \_ AssociatedSupplyVoltageSensor (classe)</span><span class="sxs-lookup"><span data-stu-id="d8d07-103">CIM\_AssociatedSupplyVoltageSensor class</span></span>

<span data-ttu-id="d8d07-104">La classe **CIM \_ AssociatedSupplyVoltageSensor** associa un alimentatore a un sensore di tensione che monitora la tensione di input.</span><span class="sxs-lookup"><span data-stu-id="d8d07-104">The **CIM\_AssociatedSupplyVoltageSensor** class associates a power supply with a voltage sensor that monitors its input voltage.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d8d07-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="d8d07-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="d8d07-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="d8d07-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="d8d07-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="d8d07-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="d8d07-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="d8d07-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8d07-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d8d07-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{327ABD78-E3D3-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_AssociatedSupplyVoltageSensor : CIM_AssociatedSensor
{
  CIM_PowerSupply   REF Dependent;
  CIM_VoltageSensor REF Antecedent;
  uint16                MonitoringRange;
};
```

## <a name="members"></a><span data-ttu-id="d8d07-110">Members</span><span class="sxs-lookup"><span data-stu-id="d8d07-110">Members</span></span>

<span data-ttu-id="d8d07-111">La classe **CIM \_ AssociatedSupplyVoltageSensor** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="d8d07-111">The **CIM\_AssociatedSupplyVoltageSensor** class has these types of members:</span></span>

-   [<span data-ttu-id="d8d07-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d8d07-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d8d07-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d8d07-113">Properties</span></span>

<span data-ttu-id="d8d07-114">La classe **CIM \_ AssociatedSupplyVoltageSensor** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="d8d07-114">The **CIM\_AssociatedSupplyVoltageSensor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d8d07-115">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="d8d07-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8d07-116">Tipo di dati: **CIM \_ sensore**</span><span class="sxs-lookup"><span data-stu-id="d8d07-116">Data type: **CIM\_VoltageSensor**</span></span>
</dt> <dt>

<span data-ttu-id="d8d07-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d8d07-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8d07-118">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="d8d07-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="d8d07-119">Un [**\_ sensore CIM**](cim-voltagesensor.md) che descrive il sensore di tensione.</span><span class="sxs-lookup"><span data-stu-id="d8d07-119">A [**CIM\_VoltageSensor**](cim-voltagesensor.md) that describes the voltage sensor.</span></span>

</dd> <dt>

<span data-ttu-id="d8d07-120">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="d8d07-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8d07-121">Tipo di dati: **CIM \_ alimentatore**</span><span class="sxs-lookup"><span data-stu-id="d8d07-121">Data type: **CIM\_PowerSupply**</span></span>
</dt> <dt>

<span data-ttu-id="d8d07-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d8d07-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8d07-123">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="d8d07-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="d8d07-124">Un [**\_ alimentatore CIM**](cim-powersupply.md) che descrive l'alimentatore associato al sensore di tensione.</span><span class="sxs-lookup"><span data-stu-id="d8d07-124">A [**CIM\_PowerSupply**](cim-powersupply.md) that describes the power supply associated with the voltage sensor.</span></span>

</dd> <dt>

<span data-ttu-id="d8d07-125">**MonitoringRange**</span><span class="sxs-lookup"><span data-stu-id="d8d07-125">**MonitoringRange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8d07-126">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d8d07-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d8d07-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d8d07-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8d07-128">Indica l'intervallo di tensione di input dell'alimentatore misurato dal sensore associato.</span><span class="sxs-lookup"><span data-stu-id="d8d07-128">Indicates the power supply's input voltage range measured by the associated sensor.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d8d07-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="d8d07-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d8d07-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="d8d07-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Range_1"></span><span id="range_1"></span><span id="RANGE_1"></span>

<span data-ttu-id="d8d07-131"><span id="Range_1"></span><span id="range_1"></span><span id="RANGE_1"></span>**Intervallo 1** (2)</span><span class="sxs-lookup"><span data-stu-id="d8d07-131"><span id="Range_1"></span><span id="range_1"></span><span id="RANGE_1"></span>**Range 1** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Range_2"></span><span id="range_2"></span><span id="RANGE_2"></span>

<span data-ttu-id="d8d07-132"><span id="Range_2"></span><span id="range_2"></span><span id="RANGE_2"></span>**Intervallo 2** (3)</span><span class="sxs-lookup"><span data-stu-id="d8d07-132"><span id="Range_2"></span><span id="range_2"></span><span id="RANGE_2"></span>**Range 2** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Both_Range_1_and_2"></span><span id="both_range_1_and_2"></span><span id="BOTH_RANGE_1_AND_2"></span>

<span data-ttu-id="d8d07-133"><span id="Both_Range_1_and_2"></span><span id="both_range_1_and_2"></span><span id="BOTH_RANGE_1_AND_2"></span>**Entrambi i valori sono compresi tra 1 e 2** (4)</span><span class="sxs-lookup"><span data-stu-id="d8d07-133"><span id="Both_Range_1_and_2"></span><span id="both_range_1_and_2"></span><span id="BOTH_RANGE_1_AND_2"></span>**Both Range 1 and 2** (4)</span></span>


</dt> <dd>

<span data-ttu-id="d8d07-134">Intervallo 1 e 2</span><span class="sxs-lookup"><span data-stu-id="d8d07-134">Range 1 and 2</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d8d07-135">Commenti</span><span class="sxs-lookup"><span data-stu-id="d8d07-135">Remarks</span></span>

<span data-ttu-id="d8d07-136">La classe **CIM \_ AssociatedSupplyVoltageSensor** è derivata da [**CIM \_ AssociatedSensor**](cim-associatedsensor.md).</span><span class="sxs-lookup"><span data-stu-id="d8d07-136">The **CIM\_AssociatedSupplyVoltageSensor** class is derived from [**CIM\_AssociatedSensor**](cim-associatedsensor.md).</span></span>

<span data-ttu-id="d8d07-137">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="d8d07-137">WMI does not implement this class.</span></span>

<span data-ttu-id="d8d07-138">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="d8d07-138">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="d8d07-139">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="d8d07-139">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8d07-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d8d07-140">Requirements</span></span>



| <span data-ttu-id="d8d07-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8d07-141">Requirement</span></span> | <span data-ttu-id="d8d07-142">Valore</span><span class="sxs-lookup"><span data-stu-id="d8d07-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d8d07-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d8d07-143">Minimum supported client</span></span><br/> | <span data-ttu-id="d8d07-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d8d07-144">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d8d07-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d8d07-145">Minimum supported server</span></span><br/> | <span data-ttu-id="d8d07-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d8d07-146">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d8d07-147">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d8d07-147">Namespace</span></span><br/>                | <span data-ttu-id="d8d07-148">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="d8d07-148">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d8d07-149">MOF</span><span class="sxs-lookup"><span data-stu-id="d8d07-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d8d07-150"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d8d07-150"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d8d07-151">DLL</span><span class="sxs-lookup"><span data-stu-id="d8d07-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8d07-152"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8d07-152"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8d07-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d8d07-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8d07-154">**\_ASSOCIATEDSENSOR CIM**</span><span class="sxs-lookup"><span data-stu-id="d8d07-154">**CIM\_AssociatedSensor**</span></span>](cim-associatedsensor.md)
</dt> </dl>

 

