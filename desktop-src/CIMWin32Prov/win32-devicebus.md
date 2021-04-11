---
description: La \_ classe WMI dell'associazione DeviceBus Win32 mette in correlazione un bus di sistema e un dispositivo logico utilizzando il bus. Questa classe viene usata per individuare i dispositivi in cui si trova il bus.
ms.assetid: 2d7d83a5-c058-40c0-aab3-7700f4067a16
ms.tgt_platform: multiple
title: Classe Win32_DeviceBus
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DeviceBus
- Win32_DeviceBus.Dependent
- Win32_DeviceBus.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2dde01ee6b3f3be026dbc19f8c4b8e2c238f4ff2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127722"
---
# <a name="win32_devicebus-class"></a><span data-ttu-id="cbd2e-104">Win32 \_ DeviceBus (classe)</span><span class="sxs-lookup"><span data-stu-id="cbd2e-104">Win32\_DeviceBus class</span></span>

<span data-ttu-id="cbd2e-105">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) dell'associazione **\_ DeviceBus Win32** mette in correlazione un bus di sistema e un dispositivo logico utilizzando il bus.</span><span class="sxs-lookup"><span data-stu-id="cbd2e-105">The **Win32\_DeviceBus** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a system bus and a logical device using the bus.</span></span> <span data-ttu-id="cbd2e-106">Questa classe viene usata per individuare i dispositivi in cui si trova il bus.</span><span class="sxs-lookup"><span data-stu-id="cbd2e-106">This class is used to discover which devices are on which bus.</span></span>

<span data-ttu-id="cbd2e-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="cbd2e-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="cbd2e-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="cbd2e-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbd2e-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cbd2e-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C50F-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DeviceBus : CIM_Dependency
{
  CIM_LogicalDevice REF Dependent;
  Win32_Bus         REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="cbd2e-110">Members</span><span class="sxs-lookup"><span data-stu-id="cbd2e-110">Members</span></span>

<span data-ttu-id="cbd2e-111">La classe **Win32 \_ DeviceBus** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="cbd2e-111">The **Win32\_DeviceBus** class has these types of members:</span></span>

-   [<span data-ttu-id="cbd2e-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="cbd2e-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cbd2e-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="cbd2e-113">Properties</span></span>

<span data-ttu-id="cbd2e-114">La classe **Win32 \_ DeviceBus** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="cbd2e-114">The **Win32\_DeviceBus** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cbd2e-115">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="cbd2e-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbd2e-116">Tipo di dati **: \_ bus Win32**</span><span class="sxs-lookup"><span data-stu-id="cbd2e-116">Data type: **Win32\_Bus**</span></span>
</dt> <dt>

<span data-ttu-id="cbd2e-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cbd2e-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cbd2e-118">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| bus Win32 WMI \_ ")</span><span class="sxs-lookup"><span data-stu-id="cbd2e-118">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_Bus")</span></span>
</dt> </dl>

<span data-ttu-id="cbd2e-119">Un [**\_ bus Win32**](win32-bus.md) che descrive le proprietà del bus di sistema usato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="cbd2e-119">A [**Win32\_Bus**](win32-bus.md) that describes the properties of the system bus that is used by the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="cbd2e-120">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="cbd2e-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbd2e-121">Tipo di dati: **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="cbd2e-121">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="cbd2e-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cbd2e-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cbd2e-123">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| CIM \_ LogicalDevice")</span><span class="sxs-lookup"><span data-stu-id="cbd2e-123">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="cbd2e-124">Un [**\_ LogicalDevice CIM**](cim-logicaldevice.md) che descrive le proprietà del dispositivo logico che usa il bus di sistema.</span><span class="sxs-lookup"><span data-stu-id="cbd2e-124">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the properties of the logical device that is using the system bus.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cbd2e-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="cbd2e-125">Remarks</span></span>

<span data-ttu-id="cbd2e-126">La classe **Win32 \_ DeviceBus** è derivata dalla [**\_ dipendenza CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="cbd2e-126">The **Win32\_DeviceBus** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cbd2e-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cbd2e-127">Requirements</span></span>



| <span data-ttu-id="cbd2e-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="cbd2e-128">Requirement</span></span> | <span data-ttu-id="cbd2e-129">Valore</span><span class="sxs-lookup"><span data-stu-id="cbd2e-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cbd2e-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cbd2e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="cbd2e-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cbd2e-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cbd2e-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cbd2e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="cbd2e-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cbd2e-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cbd2e-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="cbd2e-134">Namespace</span></span><br/>                | <span data-ttu-id="cbd2e-135">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="cbd2e-135">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cbd2e-136">MOF</span><span class="sxs-lookup"><span data-stu-id="cbd2e-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cbd2e-137"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cbd2e-137"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cbd2e-138">DLL</span><span class="sxs-lookup"><span data-stu-id="cbd2e-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cbd2e-139"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cbd2e-139"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cbd2e-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cbd2e-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbd2e-141">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="cbd2e-141">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

[<span data-ttu-id="cbd2e-142">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="cbd2e-142">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

