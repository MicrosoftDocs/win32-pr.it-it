---
description: La \_ classe WMI dell'associazione SystemDevices Win32 mette in correlazione un computer e un dispositivo logico installato nel sistema.
ms.assetid: 84dfcb75-3b44-4b27-8eee-779be522eb1f
ms.tgt_platform: multiple
title: Classe Win32_SystemDevices
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDevices
- Win32_SystemDevices.GroupComponent
- Win32_SystemDevices.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b2b28c11e10318e3bca562baf93bc20df9b756cf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878217"
---
# <a name="win32_systemdevices-class"></a><span data-ttu-id="df44b-103">Win32 \_ SystemDevices (classe)</span><span class="sxs-lookup"><span data-stu-id="df44b-103">Win32\_SystemDevices class</span></span>

<span data-ttu-id="df44b-104">La [classe WMI](../wmisdk/retrieving-a-class.md) dell'associazione **\_ SystemDevices Win32** mette in correlazione un computer e un dispositivo logico installato nel sistema.</span><span class="sxs-lookup"><span data-stu-id="df44b-104">The **Win32\_SystemDevices** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and a logical device installed on that system.</span></span>

<span data-ttu-id="df44b-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="df44b-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="df44b-106">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="df44b-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="df44b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="df44b-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F4-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemDevices : CIM_SystemDevice
{
  Win32_ComputerSystem REF GroupComponent;
  CIM_LogicalDevice    REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="df44b-108">Members</span><span class="sxs-lookup"><span data-stu-id="df44b-108">Members</span></span>

<span data-ttu-id="df44b-109">La classe **Win32 \_ SystemDevices** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="df44b-109">The **Win32\_SystemDevices** class has these types of members:</span></span>

-   [<span data-ttu-id="df44b-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="df44b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="df44b-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="df44b-111">Properties</span></span>

<span data-ttu-id="df44b-112">La classe **Win32 \_ SystemDevices** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="df44b-112">The **Win32\_SystemDevices** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="df44b-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="df44b-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df44b-114">Tipo di dati: **Win32 \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="df44b-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="df44b-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="df44b-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df44b-116">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")</span><span class="sxs-lookup"><span data-stu-id="df44b-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="df44b-117">Riferimento all'istanza di che rappresenta le proprietà del computer in cui è presente il dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="df44b-117">Reference to the instance representing the properties of the computer system where the logical device exists.</span></span>

</dd> <dt>

<span data-ttu-id="df44b-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="df44b-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df44b-119">Tipo di dati: **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="df44b-119">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="df44b-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="df44b-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df44b-121">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ LogicalDevice")</span><span class="sxs-lookup"><span data-stu-id="df44b-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="df44b-122">Riferimento all'istanza di che rappresenta le proprietà di un dispositivo logico esistente nel computer.</span><span class="sxs-lookup"><span data-stu-id="df44b-122">Reference to the instance representing the properties of a logical device that exists on the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="df44b-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="df44b-123">Remarks</span></span>

<span data-ttu-id="df44b-124">La classe **Win32 \_ SystemDevices** è derivata da [**CIM \_ SystemDevice**](cim-systemdevice.md).</span><span class="sxs-lookup"><span data-stu-id="df44b-124">The **Win32\_SystemDevices** class is derived from [**CIM\_SystemDevice**](cim-systemdevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="df44b-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="df44b-125">Requirements</span></span>



| <span data-ttu-id="df44b-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="df44b-126">Requirement</span></span> | <span data-ttu-id="df44b-127">Valore</span><span class="sxs-lookup"><span data-stu-id="df44b-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="df44b-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="df44b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="df44b-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="df44b-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="df44b-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="df44b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="df44b-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="df44b-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="df44b-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="df44b-132">Namespace</span></span><br/>                | <span data-ttu-id="df44b-133">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="df44b-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="df44b-134">MOF</span><span class="sxs-lookup"><span data-stu-id="df44b-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="df44b-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="df44b-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="df44b-136">DLL</span><span class="sxs-lookup"><span data-stu-id="df44b-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df44b-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df44b-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df44b-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="df44b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df44b-139">**\_SYSTEMDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="df44b-139">**CIM\_SystemDevice**</span></span>](cim-systemdevice.md)
</dt> <dt>

[<span data-ttu-id="df44b-140">Classi del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="df44b-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
