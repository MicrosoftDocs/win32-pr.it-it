---
description: La \_ classe WMI dell'associazione MemoryDeviceLocation Win32 mette in correlazione un dispositivo di memoria e la memoria fisica in cui è presente.
ms.assetid: 6fef916e-44e2-4b9f-94b7-c7204259004a
ms.tgt_platform: multiple
title: Classe Win32_MemoryDeviceLocation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_MemoryDeviceLocation
- Win32_MemoryDeviceLocation.Dependent
- Win32_MemoryDeviceLocation.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5cf1ba93a2574810892443aefa43e1c7c501636c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103965982"
---
# <a name="win32_memorydevicelocation-class"></a><span data-ttu-id="c6edc-103">Win32 \_ MemoryDeviceLocation (classe)</span><span class="sxs-lookup"><span data-stu-id="c6edc-103">Win32\_MemoryDeviceLocation class</span></span>

<span data-ttu-id="c6edc-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) dell'associazione **\_ MemoryDeviceLocation Win32** mette in correlazione un dispositivo di memoria e la memoria fisica in cui è presente.</span><span class="sxs-lookup"><span data-stu-id="c6edc-104">The **Win32\_MemoryDeviceLocation** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a memory device and the physical memory on which it exists.</span></span>

<span data-ttu-id="c6edc-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="c6edc-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="c6edc-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="c6edc-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6edc-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c6edc-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B9C-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_MemoryDeviceLocation : CIM_Realizes
{
  Win32_MemoryDevice   REF Dependent;
  Win32_PhysicalMemory REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="c6edc-108">Members</span><span class="sxs-lookup"><span data-stu-id="c6edc-108">Members</span></span>

<span data-ttu-id="c6edc-109">La classe **Win32 \_ MemoryDeviceLocation** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="c6edc-109">The **Win32\_MemoryDeviceLocation** class has these types of members:</span></span>

-   [<span data-ttu-id="c6edc-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c6edc-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c6edc-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c6edc-111">Properties</span></span>

<span data-ttu-id="c6edc-112">La classe **Win32 \_ MemoryDeviceLocation** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="c6edc-112">The **Win32\_MemoryDeviceLocation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c6edc-113">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="c6edc-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6edc-114">Tipo di dati: **Win32 \_ PhysicalMemory**</span><span class="sxs-lookup"><span data-stu-id="c6edc-114">Data type: **Win32\_PhysicalMemory**</span></span>
</dt> <dt>

<span data-ttu-id="c6edc-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c6edc-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6edc-116">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ PhysicalMemory")</span><span class="sxs-lookup"><span data-stu-id="c6edc-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_PhysicalMemory")</span></span>
</dt> </dl>

<span data-ttu-id="c6edc-117">[**\_ PhysicalMemory Win32**](win32-physicalmemory.md) che rappresenta la memoria fisica che contiene il dispositivo di memoria.</span><span class="sxs-lookup"><span data-stu-id="c6edc-117">A [**Win32\_PhysicalMemory**](win32-physicalmemory.md) that represents the physical memory containing the memory device.</span></span>

</dd> <dt>

<span data-ttu-id="c6edc-118">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="c6edc-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6edc-119">Tipo di dati: **Win32 \_ MemoryDevice**</span><span class="sxs-lookup"><span data-stu-id="c6edc-119">Data type: **Win32\_MemoryDevice**</span></span>
</dt> <dt>

<span data-ttu-id="c6edc-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c6edc-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6edc-121">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ MemoryDevice")</span><span class="sxs-lookup"><span data-stu-id="c6edc-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_MemoryDevice")</span></span>
</dt> </dl>

<span data-ttu-id="c6edc-122">**\_ MemoryDeviceLocation Win32** che rappresenta il dispositivo di memoria esistente nella memoria fisica.</span><span class="sxs-lookup"><span data-stu-id="c6edc-122">A **Win32\_MemoryDeviceLocation** that represents the memory device existing in the physical memory.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c6edc-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="c6edc-123">Remarks</span></span>

<span data-ttu-id="c6edc-124">La classe **Win32 \_ MemoryDeviceLocation** è derivata da [**CIM \_ realizzations**](cim-realizes.md).</span><span class="sxs-lookup"><span data-stu-id="c6edc-124">The **Win32\_MemoryDeviceLocation** class is derived from [**CIM\_Realizes**](cim-realizes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c6edc-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c6edc-125">Requirements</span></span>



| <span data-ttu-id="c6edc-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6edc-126">Requirement</span></span> | <span data-ttu-id="c6edc-127">Valore</span><span class="sxs-lookup"><span data-stu-id="c6edc-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c6edc-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c6edc-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c6edc-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c6edc-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c6edc-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c6edc-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c6edc-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c6edc-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c6edc-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c6edc-132">Namespace</span></span><br/>                | <span data-ttu-id="c6edc-133">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="c6edc-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c6edc-134">MOF</span><span class="sxs-lookup"><span data-stu-id="c6edc-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c6edc-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c6edc-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c6edc-136">DLL</span><span class="sxs-lookup"><span data-stu-id="c6edc-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c6edc-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c6edc-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6edc-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c6edc-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6edc-139">**CIM \_ realizza**</span><span class="sxs-lookup"><span data-stu-id="c6edc-139">**CIM\_Realizes**</span></span>](cim-realizes.md)
</dt> <dt>

[<span data-ttu-id="c6edc-140">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="c6edc-140">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

