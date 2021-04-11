---
description: L' \_ associazione CIM PackageTempSensor rappresenta la relazione in cui un sensore di temperatura viene spesso installato in un pacchetto, ad esempio uno chassis o un rack, per monitorare l'ambiente del pacchetto.
ms.assetid: 79f2c4d1-5e1a-4c5f-9ef4-0c8bc3926a13
ms.tgt_platform: multiple
title: Classe CIM_PackageTempSensor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PackageTempSensor
- CIM_PackageTempSensor.Dependent
- CIM_PackageTempSensor.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 28c3fa3ba569a2bf3101d62734bb9e4d5372fcf0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126934"
---
# <a name="cim_packagetempsensor-class"></a><span data-ttu-id="7176a-103">CIM \_ PackageTempSensor (classe)</span><span class="sxs-lookup"><span data-stu-id="7176a-103">CIM\_PackageTempSensor class</span></span>

<span data-ttu-id="7176a-104">L'associazione **CIM \_ PackageTempSensor** rappresenta la relazione in cui un sensore di temperatura viene spesso installato in un pacchetto, ad esempio uno chassis o un rack, per monitorare l'ambiente del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="7176a-104">The **CIM\_PackageTempSensor** association represents the relationship in which a temperature sensor is often installed in a package, such as a chassis or a rack, to monitor the package's environment.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7176a-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="7176a-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="7176a-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="7176a-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="7176a-107">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="7176a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="7176a-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="7176a-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7176a-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7176a-109">Syntax</span></span>

``` syntax
[Abstract, Aggregation, UUID("{FAF76B8F-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PackageTempSensor : CIM_Dependency
{
  CIM_PhysicalPackage   REF Dependent;
  CIM_TemperatureSensor REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="7176a-110">Members</span><span class="sxs-lookup"><span data-stu-id="7176a-110">Members</span></span>

<span data-ttu-id="7176a-111">La classe **CIM \_ PackageTempSensor** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="7176a-111">The **CIM\_PackageTempSensor** class has these types of members:</span></span>

-   [<span data-ttu-id="7176a-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7176a-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7176a-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7176a-113">Properties</span></span>

<span data-ttu-id="7176a-114">La classe **CIM \_ PackageTempSensor** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="7176a-114">The **CIM\_PackageTempSensor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7176a-115">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="7176a-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7176a-116">Tipo di dati: **CIM \_ sensore**</span><span class="sxs-lookup"><span data-stu-id="7176a-116">Data type: **CIM\_TemperatureSensor**</span></span>
</dt> <dt>

<span data-ttu-id="7176a-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7176a-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7176a-118">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="7176a-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="7176a-119">[**\_ Sensore CIM**](cim-temperaturesensor.md) che descrive il sensore di temperatura per il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="7176a-119">A [**CIM\_TemperatureSensor**](cim-temperaturesensor.md) describing the temperature sensor for the package.</span></span>

</dd> <dt>

<span data-ttu-id="7176a-120">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="7176a-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7176a-121">Tipo di dati: **CIM \_ PhysicalPackage**</span><span class="sxs-lookup"><span data-stu-id="7176a-121">Data type: **CIM\_PhysicalPackage**</span></span>
</dt> <dt>

<span data-ttu-id="7176a-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7176a-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7176a-123">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="7176a-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="7176a-124">Un [**\_ PhysicalPackage CIM**](cim-physicalpackage.md) che descrive il pacchetto fisico il cui ambiente viene monitorato.</span><span class="sxs-lookup"><span data-stu-id="7176a-124">A [**CIM\_PhysicalPackage**](cim-physicalpackage.md) describing the physical package whose environment is monitored.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7176a-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="7176a-125">Remarks</span></span>

<span data-ttu-id="7176a-126">**CIM \_ PackageTempSensor** è derivato dalla [**\_ dipendenza CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="7176a-126">**CIM\_PackageTempSensor** is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="7176a-127">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="7176a-127">WMI does not implement this class.</span></span>

<span data-ttu-id="7176a-128">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="7176a-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="7176a-129">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="7176a-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="7176a-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7176a-130">Requirements</span></span>



| <span data-ttu-id="7176a-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="7176a-131">Requirement</span></span> | <span data-ttu-id="7176a-132">Valore</span><span class="sxs-lookup"><span data-stu-id="7176a-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7176a-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7176a-133">Minimum supported client</span></span><br/> | <span data-ttu-id="7176a-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7176a-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7176a-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7176a-135">Minimum supported server</span></span><br/> | <span data-ttu-id="7176a-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7176a-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7176a-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7176a-137">Namespace</span></span><br/>                | <span data-ttu-id="7176a-138">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="7176a-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7176a-139">MOF</span><span class="sxs-lookup"><span data-stu-id="7176a-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7176a-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7176a-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7176a-141">DLL</span><span class="sxs-lookup"><span data-stu-id="7176a-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7176a-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7176a-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7176a-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7176a-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7176a-144">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="7176a-144">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

