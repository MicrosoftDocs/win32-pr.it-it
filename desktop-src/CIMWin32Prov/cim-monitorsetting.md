---
description: La \_ classe CIM MonitorSetting associa la risoluzione del monitoraggio al monitor desktop a cui si applica.
ms.assetid: 4bf0b2d5-b901-4294-a33b-9c8a87785af0
ms.tgt_platform: multiple
title: Classe CIM_MonitorSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MonitorSetting
- CIM_MonitorSetting.Setting
- CIM_MonitorSetting.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: dc947f4bb484ec5392204747e583fbf80bbf88cf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877969"
---
# <a name="cim_monitorsetting-class"></a><span data-ttu-id="ef72d-103">CIM \_ MonitorSetting (classe)</span><span class="sxs-lookup"><span data-stu-id="ef72d-103">CIM\_MonitorSetting class</span></span>

<span data-ttu-id="ef72d-104">La classe **CIM \_ MonitorSetting** associa la risoluzione del monitoraggio al monitor desktop a cui si applica.</span><span class="sxs-lookup"><span data-stu-id="ef72d-104">The **CIM\_MonitorSetting** class associates the monitor resolution with the desktop monitor to which it applies.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ef72d-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="ef72d-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ef72d-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="ef72d-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="ef72d-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="ef72d-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="ef72d-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="ef72d-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef72d-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ef72d-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{1008CCED-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class CIM_MonitorSetting : CIM_ElementSetting
{
  CIM_MonitorResolution REF Setting;
  CIM_DesktopMonitor    REF Element;
};
```

## <a name="members"></a><span data-ttu-id="ef72d-110">Members</span><span class="sxs-lookup"><span data-stu-id="ef72d-110">Members</span></span>

<span data-ttu-id="ef72d-111">La classe **CIM \_ MonitorSetting** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ef72d-111">The **CIM\_MonitorSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="ef72d-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ef72d-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ef72d-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ef72d-113">Properties</span></span>

<span data-ttu-id="ef72d-114">La classe **CIM \_ MonitorSetting** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="ef72d-114">The **CIM\_MonitorSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ef72d-115">**elemento**</span><span class="sxs-lookup"><span data-stu-id="ef72d-115">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef72d-116">Tipo di dati: **CIM \_ DesktopMonitor**</span><span class="sxs-lookup"><span data-stu-id="ef72d-116">Data type: **CIM\_DesktopMonitor**</span></span>
</dt> <dt>

<span data-ttu-id="ef72d-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ef72d-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef72d-118">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("elemento")</span><span class="sxs-lookup"><span data-stu-id="ef72d-118">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Element")</span></span>
</dt> </dl>

<span data-ttu-id="ef72d-119">Un [**\_ DesktopMonitor CIM**](cim-desktopmonitor.md) che descrive il monitor del desktop.</span><span class="sxs-lookup"><span data-stu-id="ef72d-119">A [**CIM\_DesktopMonitor**](cim-desktopmonitor.md) describing the desktop monitor.</span></span>

</dd> <dt>

<span data-ttu-id="ef72d-120">**Impostazione**</span><span class="sxs-lookup"><span data-stu-id="ef72d-120">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef72d-121">Tipo di dati: **CIM \_ MonitorResolution**</span><span class="sxs-lookup"><span data-stu-id="ef72d-121">Data type: **CIM\_MonitorResolution**</span></span>
</dt> <dt>

<span data-ttu-id="ef72d-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ef72d-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef72d-123">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("impostazione")</span><span class="sxs-lookup"><span data-stu-id="ef72d-123">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Setting")</span></span>
</dt> </dl>

<span data-ttu-id="ef72d-124">Un [**\_ MonitorResolution CIM**](cim-monitorresolution.md) che descrive la risoluzione del monitoraggio associata a monitoraggio desktop.</span><span class="sxs-lookup"><span data-stu-id="ef72d-124">A [**CIM\_MonitorResolution**](cim-monitorresolution.md) describing the monitor resolution associated with the desktop monitor.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ef72d-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="ef72d-125">Remarks</span></span>

<span data-ttu-id="ef72d-126">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="ef72d-126">WMI does not implement this class.</span></span>

<span data-ttu-id="ef72d-127">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="ef72d-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ef72d-128">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="ef72d-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef72d-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ef72d-129">Requirements</span></span>



| <span data-ttu-id="ef72d-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef72d-130">Requirement</span></span> | <span data-ttu-id="ef72d-131">Valore</span><span class="sxs-lookup"><span data-stu-id="ef72d-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ef72d-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ef72d-132">Minimum supported client</span></span><br/> | <span data-ttu-id="ef72d-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ef72d-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ef72d-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ef72d-134">Minimum supported server</span></span><br/> | <span data-ttu-id="ef72d-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ef72d-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ef72d-136">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ef72d-136">Namespace</span></span><br/>                | <span data-ttu-id="ef72d-137">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="ef72d-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ef72d-138">MOF</span><span class="sxs-lookup"><span data-stu-id="ef72d-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ef72d-139"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ef72d-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ef72d-140">DLL</span><span class="sxs-lookup"><span data-stu-id="ef72d-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef72d-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef72d-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef72d-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ef72d-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef72d-143">**\_ELEMENTSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="ef72d-143">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> </dl>

 

