---
description: L' \_ associazione CIM SystemDevice rappresenta una relazione esplicita in cui i dispositivi logici possono essere aggregati da un sistema.
ms.assetid: df624a9f-0c10-44a3-8075-908e5e481e3c
ms.tgt_platform: multiple
title: Classe CIM_SystemDevice (provider WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SystemDevice
- CIM_SystemDevice.PartComponent
- CIM_SystemDevice.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: dbff9a0ead8790de9ab323509c8b2f1392e6ed6e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304970"
---
# <a name="cim_systemdevice-class-cimwin32-wmi-providers"></a><span data-ttu-id="057c7-103">Classe CIM_SystemDevice (provider WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="057c7-103">CIM_SystemDevice class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="057c7-104">L'associazione **CIM \_ SystemDevice** rappresenta una relazione esplicita in cui i dispositivi logici possono essere aggregati da un sistema.</span><span class="sxs-lookup"><span data-stu-id="057c7-104">The **CIM\_SystemDevice** association represents an explicit relationship in which logical devices can be aggregated by a system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="057c7-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="057c7-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="057c7-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="057c7-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="057c7-107">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="057c7-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="057c7-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="057c7-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="057c7-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="057c7-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{4B2C30D7-BAFE-11d2-85E5-0000F8102E5F}"), AMENDMENT]
class CIM_SystemDevice : CIM_SystemComponent
{
  CIM_LogicalDevice REF PartComponent;
  CIM_System        REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="057c7-110">Members</span><span class="sxs-lookup"><span data-stu-id="057c7-110">Members</span></span>

<span data-ttu-id="057c7-111">La classe **CIM \_ SystemDevice** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="057c7-111">The **CIM\_SystemDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="057c7-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="057c7-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="057c7-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="057c7-113">Properties</span></span>

<span data-ttu-id="057c7-114">La classe **CIM \_ SystemDevice** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="057c7-114">The **CIM\_SystemDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="057c7-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="057c7-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="057c7-116">Tipo di dati **: \_ sistema CIM**</span><span class="sxs-lookup"><span data-stu-id="057c7-116">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="057c7-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="057c7-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="057c7-118">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="057c7-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="057c7-119">[**\_ Sistema CIM**](cim-system.md) che descrive il sistema padre nell'associazione.</span><span class="sxs-lookup"><span data-stu-id="057c7-119">A [**CIM\_System**](cim-system.md) that describes the parent system in the association.</span></span>

</dd> <dt>

<span data-ttu-id="057c7-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="057c7-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="057c7-121">Tipo di dati: **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="057c7-121">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="057c7-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="057c7-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="057c7-123">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**debole**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="057c7-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="057c7-124">Un [**\_ LogicalDevice CIM**](cim-logicaldevice.md) che descrive il dispositivo logico che è un componente di un sistema.</span><span class="sxs-lookup"><span data-stu-id="057c7-124">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the logical device that is a component of a system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="057c7-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="057c7-125">Remarks</span></span>

<span data-ttu-id="057c7-126">La classe **CIM \_ SystemDevice** è derivata da [**CIM \_ SystemComponent**](cim-systemcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="057c7-126">The **CIM\_SystemDevice** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

<span data-ttu-id="057c7-127">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="057c7-127">WMI does not implement this class.</span></span> <span data-ttu-id="057c7-128">Per le classi WMI derivate da **CIM \_ SystemDevice**, vedere [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="057c7-128">For WMI classes derived from **CIM\_SystemDevice**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="057c7-129">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="057c7-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="057c7-130">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="057c7-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="057c7-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="057c7-131">Requirements</span></span>



| <span data-ttu-id="057c7-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="057c7-132">Requirement</span></span> | <span data-ttu-id="057c7-133">Valore</span><span class="sxs-lookup"><span data-stu-id="057c7-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="057c7-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="057c7-134">Minimum supported client</span></span><br/> | <span data-ttu-id="057c7-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="057c7-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="057c7-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="057c7-136">Minimum supported server</span></span><br/> | <span data-ttu-id="057c7-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="057c7-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="057c7-138">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="057c7-138">Namespace</span></span><br/>                | <span data-ttu-id="057c7-139">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="057c7-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="057c7-140">MOF</span><span class="sxs-lookup"><span data-stu-id="057c7-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="057c7-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="057c7-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="057c7-142">DLL</span><span class="sxs-lookup"><span data-stu-id="057c7-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="057c7-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="057c7-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="057c7-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="057c7-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="057c7-145">**\_SYSTEMCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="057c7-145">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> </dl>

 

