---
description: La \_ classe WMI dell'associazione MemoryDeviceArray Win32 mette in correlazione un dispositivo di memoria e la matrice di memoria in cui risiede.
ms.assetid: 39ea6333-2352-488b-99e4-97594bea7dcd
ms.tgt_platform: multiple
title: Classe Win32_MemoryDeviceArray
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_MemoryDeviceArray
- Win32_MemoryDeviceArray.GroupComponent
- Win32_MemoryDeviceArray.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1e527f77183c3bdc09d464f6fed4808e45adefa5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877341"
---
# <a name="win32_memorydevicearray-class"></a><span data-ttu-id="d5c74-103">Win32 \_ MemoryDeviceArray (classe)</span><span class="sxs-lookup"><span data-stu-id="d5c74-103">Win32\_MemoryDeviceArray class</span></span>

<span data-ttu-id="d5c74-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) dell'associazione **\_ MemoryDeviceArray Win32** mette in correlazione un dispositivo di memoria e la matrice di memoria in cui risiede.</span><span class="sxs-lookup"><span data-stu-id="d5c74-104">The **Win32\_MemoryDeviceArray** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a memory device and the memory array in which it resides.</span></span>

<span data-ttu-id="d5c74-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="d5c74-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="d5c74-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="d5c74-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5c74-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d5c74-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{B24EF563-BBBE-11d2-ABFB-00805F538618}"), AMENDMENT]
class Win32_MemoryDeviceArray : CIM_Component
{
  Win32_MemoryArray  REF GroupComponent;
  Win32_MemoryDevice REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="d5c74-108">Members</span><span class="sxs-lookup"><span data-stu-id="d5c74-108">Members</span></span>

<span data-ttu-id="d5c74-109">La classe **Win32 \_ MemoryDeviceArray** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="d5c74-109">The **Win32\_MemoryDeviceArray** class has these types of members:</span></span>

-   [<span data-ttu-id="d5c74-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d5c74-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d5c74-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d5c74-111">Properties</span></span>

<span data-ttu-id="d5c74-112">La classe **Win32 \_ MemoryDeviceArray** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="d5c74-112">The **Win32\_MemoryDeviceArray** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d5c74-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="d5c74-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5c74-114">Tipo di dati: **Win32 \_ MemoryArray**</span><span class="sxs-lookup"><span data-stu-id="d5c74-114">Data type: **Win32\_MemoryArray**</span></span>
</dt> <dt>

<span data-ttu-id="d5c74-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d5c74-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d5c74-116">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ MemoryArray")</span><span class="sxs-lookup"><span data-stu-id="d5c74-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_MemoryArray")</span></span>
</dt> </dl>

<span data-ttu-id="d5c74-117">[**\_ MemoryArray Win32**](win32-memoryarray.md) che rappresenta la parte della matrice di memoria dell' \_ associazione MemoryDeviceArray Win32.</span><span class="sxs-lookup"><span data-stu-id="d5c74-117">A [**Win32\_MemoryArray**](win32-memoryarray.md) that represents the memory array part of the Win32\_MemoryDeviceArray association.</span></span>

</dd> <dt>

<span data-ttu-id="d5c74-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="d5c74-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5c74-119">Tipo di dati: **Win32 \_ MemoryDevice**</span><span class="sxs-lookup"><span data-stu-id="d5c74-119">Data type: **Win32\_MemoryDevice**</span></span>
</dt> <dt>

<span data-ttu-id="d5c74-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d5c74-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d5c74-121">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ MemoryDevice")</span><span class="sxs-lookup"><span data-stu-id="d5c74-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_MemoryDevice")</span></span>
</dt> </dl>

<span data-ttu-id="d5c74-122">[**\_ MemoryDevice Win32**](win32-memorydevice.md) che rappresenta una parte del dispositivo di memoria dell' \_ associazione MemoryDeviceArray Win32.</span><span class="sxs-lookup"><span data-stu-id="d5c74-122">A [**Win32\_MemoryDevice**](win32-memorydevice.md) that represents a memory device part of the Win32\_MemoryDeviceArray association.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d5c74-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="d5c74-123">Remarks</span></span>

<span data-ttu-id="d5c74-124">La classe **Win32 \_ MemoryDeviceArray** è derivata dal [**\_ componente CIM**](cim-component.md).</span><span class="sxs-lookup"><span data-stu-id="d5c74-124">The **Win32\_MemoryDeviceArray** class is derived from [**CIM\_Component**](cim-component.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d5c74-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d5c74-125">Requirements</span></span>



| <span data-ttu-id="d5c74-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5c74-126">Requirement</span></span> | <span data-ttu-id="d5c74-127">Valore</span><span class="sxs-lookup"><span data-stu-id="d5c74-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d5c74-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d5c74-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d5c74-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d5c74-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d5c74-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d5c74-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d5c74-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d5c74-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d5c74-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d5c74-132">Namespace</span></span><br/>                | <span data-ttu-id="d5c74-133">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="d5c74-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d5c74-134">MOF</span><span class="sxs-lookup"><span data-stu-id="d5c74-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d5c74-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d5c74-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d5c74-136">DLL</span><span class="sxs-lookup"><span data-stu-id="d5c74-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d5c74-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d5c74-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5c74-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d5c74-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5c74-139">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="d5c74-139">**CIM\_Component**</span></span>](cim-component.md)
</dt> <dt>

[<span data-ttu-id="d5c74-140">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="d5c74-140">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

