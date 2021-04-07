---
description: La \_ dipendenza CIM AssociatedAlarm associa un allarme a un dispositivo logico.
ms.assetid: ed0ccc81-6d1b-45b0-abf0-7a2bd9a50193
ms.tgt_platform: multiple
title: Classe CIM_AssociatedAlarm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AssociatedAlarm
- CIM_AssociatedAlarm.Dependent
- CIM_AssociatedAlarm.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fe6a637482526feecc7528eadc70dc695dafca9b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748706"
---
# <a name="cim_associatedalarm-class"></a><span data-ttu-id="9c150-103">CIM \_ AssociatedAlarm (classe)</span><span class="sxs-lookup"><span data-stu-id="9c150-103">CIM\_AssociatedAlarm class</span></span>

<span data-ttu-id="9c150-104">La dipendenza **CIM \_ AssociatedAlarm** associa un allarme a un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="9c150-104">The **CIM\_AssociatedAlarm** dependency associates an alarm with a logical device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9c150-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="9c150-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="9c150-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="9c150-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="9c150-107">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="9c150-107">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c150-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9c150-108">Syntax</span></span>

``` syntax
[Abstract, UUID("{2280CB02-DB35-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_AssociatedAlarm : CIM_Dependency
{
  CIM_LogicalDevice REF Dependent;
  CIM_AlarmDevice   REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="9c150-109">Members</span><span class="sxs-lookup"><span data-stu-id="9c150-109">Members</span></span>

<span data-ttu-id="9c150-110">La classe **CIM \_ AssociatedAlarm** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="9c150-110">The **CIM\_AssociatedAlarm** class has these types of members:</span></span>

-   [<span data-ttu-id="9c150-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9c150-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9c150-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9c150-112">Properties</span></span>

<span data-ttu-id="9c150-113">La classe **CIM \_ AssociatedAlarm** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="9c150-113">The **CIM\_AssociatedAlarm** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9c150-114">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="9c150-114">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c150-115">Tipo di dati: **CIM \_ AlarmDevice**</span><span class="sxs-lookup"><span data-stu-id="9c150-115">Data type: **CIM\_AlarmDevice**</span></span>
</dt> <dt>

<span data-ttu-id="9c150-116">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9c150-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c150-117">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="9c150-117">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="9c150-118">Un [**\_ AlarmDevice CIM**](cim-alarmdevice.md) che contiene il dispositivo Alarm.</span><span class="sxs-lookup"><span data-stu-id="9c150-118">A [**CIM\_AlarmDevice**](cim-alarmdevice.md) that contains the alarm device.</span></span>

</dd> <dt>

<span data-ttu-id="9c150-119">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="9c150-119">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c150-120">Tipo di dati: **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="9c150-120">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="9c150-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9c150-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c150-122">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="9c150-122">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="9c150-123">Un [**\_ LogicalDevice CIM**](cim-logicaldevice.md) che contiene il dispositivo logico che è allarmato.</span><span class="sxs-lookup"><span data-stu-id="9c150-123">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that contains the logical device that is alarmed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9c150-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="9c150-124">Remarks</span></span>

<span data-ttu-id="9c150-125">La classe **CIM \_ AssociatedAlarm** è derivata dalla [**\_ dipendenza CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="9c150-125">The **CIM\_AssociatedAlarm** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="9c150-126">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="9c150-126">WMI does not implement this class.</span></span>

<span data-ttu-id="9c150-127">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="9c150-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="9c150-128">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="9c150-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c150-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9c150-129">Requirements</span></span>



| <span data-ttu-id="9c150-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c150-130">Requirement</span></span> | <span data-ttu-id="9c150-131">Valore</span><span class="sxs-lookup"><span data-stu-id="9c150-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9c150-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9c150-132">Minimum supported client</span></span><br/> | <span data-ttu-id="9c150-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9c150-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9c150-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9c150-134">Minimum supported server</span></span><br/> | <span data-ttu-id="9c150-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9c150-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9c150-136">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9c150-136">Namespace</span></span><br/>                | <span data-ttu-id="9c150-137">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="9c150-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9c150-138">MOF</span><span class="sxs-lookup"><span data-stu-id="9c150-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9c150-139"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9c150-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9c150-140">DLL</span><span class="sxs-lookup"><span data-stu-id="9c150-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9c150-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c150-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c150-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9c150-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c150-143">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="9c150-143">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

