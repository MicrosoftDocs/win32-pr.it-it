---
description: La \_ classe CIM AssociatedSensor associa un sensore installato a un dispositivo logico. Il sensore misura le proprietà di input e output critiche e può essere incluso nel dispositivo o installato nelle vicinanze.
ms.assetid: 8ccaa37f-b95f-4582-a694-23bdc15b8c8b
ms.tgt_platform: multiple
title: Classe CIM_AssociatedSensor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AssociatedSensor
- CIM_AssociatedSensor.Dependent
- CIM_AssociatedSensor.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 50eac6b8bd933762df0da0213c420f5895b74640
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878065"
---
# <a name="cim_associatedsensor-class"></a><span data-ttu-id="ccf6b-104">CIM \_ AssociatedSensor (classe)</span><span class="sxs-lookup"><span data-stu-id="ccf6b-104">CIM\_AssociatedSensor class</span></span>

<span data-ttu-id="ccf6b-105">La classe **CIM \_ AssociatedSensor** associa un sensore installato a un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="ccf6b-105">The **CIM\_AssociatedSensor** class associates an installed sensor with a logical device.</span></span> <span data-ttu-id="ccf6b-106">Il sensore misura le proprietà di input e output critiche e può essere incluso nel dispositivo o installato nelle vicinanze.</span><span class="sxs-lookup"><span data-stu-id="ccf6b-106">The sensor measures critical input and output properties, and can be included with the device or installed nearby.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ccf6b-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="ccf6b-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ccf6b-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="ccf6b-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="ccf6b-109">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="ccf6b-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="ccf6b-110">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="ccf6b-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccf6b-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ccf6b-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{956597A0-7D80-11D2-AAD3-006008C78BC7}"), AMENDMENT]
class CIM_AssociatedSensor : CIM_Dependency
{
  CIM_LogicalDevice REF Dependent;
  CIM_Sensor        REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="ccf6b-112">Members</span><span class="sxs-lookup"><span data-stu-id="ccf6b-112">Members</span></span>

<span data-ttu-id="ccf6b-113">La classe **CIM \_ AssociatedSensor** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ccf6b-113">The **CIM\_AssociatedSensor** class has these types of members:</span></span>

-   [<span data-ttu-id="ccf6b-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ccf6b-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ccf6b-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ccf6b-115">Properties</span></span>

<span data-ttu-id="ccf6b-116">La classe **CIM \_ AssociatedSensor** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="ccf6b-116">The **CIM\_AssociatedSensor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ccf6b-117">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="ccf6b-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccf6b-118">Tipo di dati **: \_ sensore CIM**</span><span class="sxs-lookup"><span data-stu-id="ccf6b-118">Data type: **CIM\_Sensor**</span></span>
</dt> <dt>

<span data-ttu-id="ccf6b-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ccf6b-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ccf6b-120">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="ccf6b-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="ccf6b-121">Un [**\_ sensore CIM**](cim-sensor.md) che descrive il sensore.</span><span class="sxs-lookup"><span data-stu-id="ccf6b-121">A [**CIM\_Sensor**](cim-sensor.md) that describes the sensor.</span></span>

</dd> <dt>

<span data-ttu-id="ccf6b-122">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="ccf6b-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccf6b-123">Tipo di dati: **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="ccf6b-123">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="ccf6b-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ccf6b-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ccf6b-125">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="ccf6b-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="ccf6b-126">Un [**\_ LogicalDevice CIM**](cim-logicaldevice.md) che descrive il dispositivo logico per il quale le informazioni vengono misurate dal sensore.</span><span class="sxs-lookup"><span data-stu-id="ccf6b-126">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the logical device for which information is measured by the sensor.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ccf6b-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="ccf6b-127">Remarks</span></span>

<span data-ttu-id="ccf6b-128">La classe **CIM \_ AssociatedSensor** è derivata dalla [**\_ dipendenza CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="ccf6b-128">The **CIM\_AssociatedSensor** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="ccf6b-129">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="ccf6b-129">WMI does not implement this class.</span></span> <span data-ttu-id="ccf6b-130">Per ulteriori informazioni sulle classi derivate da **CIM \_ AssociatedSensor**, vedere [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="ccf6b-130">For more information about classes derived from **CIM\_AssociatedSensor**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="ccf6b-131">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="ccf6b-131">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ccf6b-132">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="ccf6b-132">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ccf6b-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ccf6b-133">Requirements</span></span>



| <span data-ttu-id="ccf6b-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="ccf6b-134">Requirement</span></span> | <span data-ttu-id="ccf6b-135">Valore</span><span class="sxs-lookup"><span data-stu-id="ccf6b-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ccf6b-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ccf6b-136">Minimum supported client</span></span><br/> | <span data-ttu-id="ccf6b-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ccf6b-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ccf6b-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ccf6b-138">Minimum supported server</span></span><br/> | <span data-ttu-id="ccf6b-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ccf6b-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ccf6b-140">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ccf6b-140">Namespace</span></span><br/>                | <span data-ttu-id="ccf6b-141">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="ccf6b-141">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ccf6b-142">MOF</span><span class="sxs-lookup"><span data-stu-id="ccf6b-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ccf6b-143"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ccf6b-143"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ccf6b-144">DLL</span><span class="sxs-lookup"><span data-stu-id="ccf6b-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ccf6b-145"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ccf6b-145"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ccf6b-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ccf6b-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccf6b-147">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="ccf6b-147">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

