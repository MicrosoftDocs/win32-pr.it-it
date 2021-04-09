---
description: La \_ classe CIM ErrorCountersForDevice associa la \_ classe CIM DeviceErrorCounts al dispositivo logico a cui si applica.
ms.assetid: 200971ab-df85-4a45-beb3-4ffe11ce92dc
ms.tgt_platform: multiple
title: Classe CIM_ErrorCountersForDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ErrorCountersForDevice
- CIM_ErrorCountersForDevice.Element
- CIM_ErrorCountersForDevice.Stats
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7c4e11b1f58cae7b544b251044657bb737525b37
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877909"
---
# <a name="cim_errorcountersfordevice-class"></a><span data-ttu-id="3c647-103">CIM \_ ErrorCountersForDevice (classe)</span><span class="sxs-lookup"><span data-stu-id="3c647-103">CIM\_ErrorCountersForDevice class</span></span>

<span data-ttu-id="3c647-104">La classe **CIM \_ ErrorCountersForDevice** associa la classe [**CIM \_ DeviceErrorCounts**](cim-deviceerrorcounts.md) al dispositivo logico a cui si applica.</span><span class="sxs-lookup"><span data-stu-id="3c647-104">The **CIM\_ErrorCountersForDevice** class associates the [**CIM\_DeviceErrorCounts**](cim-deviceerrorcounts.md) class to the logical device to which it applies.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3c647-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="3c647-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="3c647-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="3c647-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="3c647-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="3c647-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="3c647-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="3c647-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c647-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3c647-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{2D79F3A0-D025-11d2-85F5-0000F8102E5F}"), AMENDMENT]
class CIM_ErrorCountersForDevice : CIM_Statistics
{
  CIM_LogicalDevice     REF Element;
  CIM_DeviceErrorCounts REF Stats;
};
```

## <a name="members"></a><span data-ttu-id="3c647-110">Members</span><span class="sxs-lookup"><span data-stu-id="3c647-110">Members</span></span>

<span data-ttu-id="3c647-111">La classe **CIM \_ ErrorCountersForDevice** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="3c647-111">The **CIM\_ErrorCountersForDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="3c647-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3c647-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3c647-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3c647-113">Properties</span></span>

<span data-ttu-id="3c647-114">La classe **CIM \_ ErrorCountersForDevice** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="3c647-114">The **CIM\_ErrorCountersForDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3c647-115">**elemento**</span><span class="sxs-lookup"><span data-stu-id="3c647-115">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c647-116">Tipo di dati: **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="3c647-116">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="3c647-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3c647-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c647-118">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("element"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="3c647-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Element"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="3c647-119">Un [**\_ LogicalDevice CIM**](cim-logicaldevice.md) che descrive il dispositivo a cui si applicano i contatori degli errori.</span><span class="sxs-lookup"><span data-stu-id="3c647-119">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the device to which the error counters apply.</span></span>

</dd> <dt>

<span data-ttu-id="3c647-120">**Statistiche**</span><span class="sxs-lookup"><span data-stu-id="3c647-120">**Stats**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c647-121">Tipo di dati: **CIM \_ DeviceErrorCounts**</span><span class="sxs-lookup"><span data-stu-id="3c647-121">Data type: **CIM\_DeviceErrorCounts**</span></span>
</dt> <dt>

<span data-ttu-id="3c647-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3c647-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c647-123">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("stats"), [**debole**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3c647-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Stats"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3c647-124">Un [**\_ DeviceErrorCounts CIM**](cim-deviceerrorcounts.md) che descrive l'oggetto statistico, in questo caso la classe del contatore degli errori.</span><span class="sxs-lookup"><span data-stu-id="3c647-124">A [**CIM\_DeviceErrorCounts**](cim-deviceerrorcounts.md) describing the statistical object - in this case, the error counter class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3c647-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="3c647-125">Remarks</span></span>

<span data-ttu-id="3c647-126">La classe **CIM \_ ErrorCountersForDevice** viene ereditata [**dalle \_ statistiche CIM**](cim-statistics.md).</span><span class="sxs-lookup"><span data-stu-id="3c647-126">The **CIM\_ErrorCountersForDevice** class is inherited from [**CIM\_Statistics**](cim-statistics.md).</span></span>

<span data-ttu-id="3c647-127">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="3c647-127">WMI does not implement this class.</span></span>

<span data-ttu-id="3c647-128">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="3c647-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="3c647-129">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="3c647-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c647-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3c647-130">Requirements</span></span>



| <span data-ttu-id="3c647-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c647-131">Requirement</span></span> | <span data-ttu-id="3c647-132">Valore</span><span class="sxs-lookup"><span data-stu-id="3c647-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3c647-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3c647-133">Minimum supported client</span></span><br/> | <span data-ttu-id="3c647-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3c647-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3c647-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3c647-135">Minimum supported server</span></span><br/> | <span data-ttu-id="3c647-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3c647-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3c647-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3c647-137">Namespace</span></span><br/>                | <span data-ttu-id="3c647-138">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="3c647-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3c647-139">MOF</span><span class="sxs-lookup"><span data-stu-id="3c647-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3c647-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3c647-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3c647-141">DLL</span><span class="sxs-lookup"><span data-stu-id="3c647-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c647-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c647-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c647-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3c647-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c647-144">**\_Statistiche CIM**</span><span class="sxs-lookup"><span data-stu-id="3c647-144">**CIM\_Statistics**</span></span>](cim-statistics.md)
</dt> </dl>

 

