---
description: L' \_ associazione CIM CollectionOfSensors rappresenta i sensori binari che compongono il sensore multistato.
ms.assetid: d9494716-bb4e-4aa2-9e3b-e865360c740f
ms.tgt_platform: multiple
title: Classe CIM_CollectionOfSensors
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectionOfSensors
- CIM_CollectionOfSensors.PartComponent
- CIM_CollectionOfSensors.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 06f33d3b55c2c35526495d492b0f063fee9c1a0c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966204"
---
# <a name="cim_collectionofsensors-class"></a><span data-ttu-id="4dc79-103">CIM \_ CollectionOfSensors (classe)</span><span class="sxs-lookup"><span data-stu-id="4dc79-103">CIM\_CollectionOfSensors class</span></span>

<span data-ttu-id="4dc79-104">L'associazione **CIM \_ CollectionOfSensors** rappresenta i sensori binari che compongono il sensore multistato.</span><span class="sxs-lookup"><span data-stu-id="4dc79-104">The **CIM\_CollectionOfSensors** association represents the binary sensors that make up the multistate sensor.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4dc79-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="4dc79-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4dc79-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="4dc79-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="4dc79-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="4dc79-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="4dc79-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="4dc79-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4dc79-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4dc79-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{A2ABF536-DB35-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_CollectionOfSensors : CIM_Component
{
  CIM_BinarySensor     REF PartComponent;
  CIM_MultiStateSensor REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="4dc79-110">Members</span><span class="sxs-lookup"><span data-stu-id="4dc79-110">Members</span></span>

<span data-ttu-id="4dc79-111">La classe **CIM \_ CollectionOfSensors** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="4dc79-111">The **CIM\_CollectionOfSensors** class has these types of members:</span></span>

-   [<span data-ttu-id="4dc79-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4dc79-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4dc79-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4dc79-113">Properties</span></span>

<span data-ttu-id="4dc79-114">La classe **CIM \_ CollectionOfSensors** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="4dc79-114">The **CIM\_CollectionOfSensors** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4dc79-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="4dc79-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4dc79-116">Tipo di dati: **CIM \_ MultiStateSensor**</span><span class="sxs-lookup"><span data-stu-id="4dc79-116">Data type: **CIM\_MultiStateSensor**</span></span>
</dt> <dt>

<span data-ttu-id="4dc79-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4dc79-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4dc79-118">Qualificatori: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="4dc79-118">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="4dc79-119">Un [**\_ MultiStateSensor CIM**](cim-multistatesensor.md) che descrive il sensore multistato.</span><span class="sxs-lookup"><span data-stu-id="4dc79-119">A [**CIM\_MultiStateSensor**](cim-multistatesensor.md) that describes the multi-state sensor.</span></span>

</dd> <dt>

<span data-ttu-id="4dc79-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="4dc79-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4dc79-121">Tipo di dati: **CIM \_ BinarySensor**</span><span class="sxs-lookup"><span data-stu-id="4dc79-121">Data type: **CIM\_BinarySensor**</span></span>
</dt> <dt>

<span data-ttu-id="4dc79-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4dc79-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4dc79-123">Qualificatori: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (2), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="4dc79-123">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (2), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="4dc79-124">Un [**\_ BinarySensor CIM**](cim-binarysensor.md) che descrive un sensore binario che fa parte del sensore multistato.</span><span class="sxs-lookup"><span data-stu-id="4dc79-124">A [**CIM\_BinarySensor**](cim-binarysensor.md) that describes a binary sensor that is part of the multi-state sensor.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4dc79-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="4dc79-125">Remarks</span></span>

<span data-ttu-id="4dc79-126">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="4dc79-126">WMI does not implement this class.</span></span>

<span data-ttu-id="4dc79-127">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="4dc79-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4dc79-128">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="4dc79-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4dc79-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4dc79-129">Requirements</span></span>



| <span data-ttu-id="4dc79-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="4dc79-130">Requirement</span></span> | <span data-ttu-id="4dc79-131">Valore</span><span class="sxs-lookup"><span data-stu-id="4dc79-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4dc79-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4dc79-132">Minimum supported client</span></span><br/> | <span data-ttu-id="4dc79-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4dc79-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4dc79-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4dc79-134">Minimum supported server</span></span><br/> | <span data-ttu-id="4dc79-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4dc79-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4dc79-136">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4dc79-136">Namespace</span></span><br/>                | <span data-ttu-id="4dc79-137">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="4dc79-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4dc79-138">MOF</span><span class="sxs-lookup"><span data-stu-id="4dc79-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4dc79-139"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4dc79-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4dc79-140">DLL</span><span class="sxs-lookup"><span data-stu-id="4dc79-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4dc79-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4dc79-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4dc79-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4dc79-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4dc79-143">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="4dc79-143">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

