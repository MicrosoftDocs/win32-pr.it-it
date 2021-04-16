---
description: La \_ classe WMI dell'associazione MemoryArrayLocation Win32 mette in correlazione una matrice di memoria logica e la matrice di memoria fisica in cui è presente.
ms.assetid: 455daeee-ad67-4599-84d6-fa3f4ac593aa
ms.tgt_platform: multiple
title: Classe Win32_MemoryArrayLocation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_MemoryArrayLocation
- Win32_MemoryArrayLocation.Dependent
- Win32_MemoryArrayLocation.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 62aae3bf672b12bdb947ff8ce6b76f919eaa11b7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524105"
---
# <a name="win32_memoryarraylocation-class"></a><span data-ttu-id="fc02d-103">Win32 \_ MemoryArrayLocation (classe)</span><span class="sxs-lookup"><span data-stu-id="fc02d-103">Win32\_MemoryArrayLocation class</span></span>

<span data-ttu-id="fc02d-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) dell'associazione **\_ MemoryArrayLocation Win32** mette in correlazione una matrice di memoria logica e la matrice di memoria fisica in cui è presente.</span><span class="sxs-lookup"><span data-stu-id="fc02d-104">The **Win32\_MemoryArrayLocation** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a logical memory array and the physical memory array on which it exists.</span></span>

<span data-ttu-id="fc02d-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="fc02d-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="fc02d-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="fc02d-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc02d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fc02d-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{B24EF561-BBBE-11d2-ABFB-00805F538618}"), AMENDMENT]
class Win32_MemoryArrayLocation : CIM_Realizes
{
  Win32_MemoryArray         REF Dependent;
  Win32_PhysicalMemoryArray REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="fc02d-108">Members</span><span class="sxs-lookup"><span data-stu-id="fc02d-108">Members</span></span>

<span data-ttu-id="fc02d-109">La classe **Win32 \_ MemoryArrayLocation** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="fc02d-109">The **Win32\_MemoryArrayLocation** class has these types of members:</span></span>

-   [<span data-ttu-id="fc02d-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="fc02d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fc02d-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="fc02d-111">Properties</span></span>

<span data-ttu-id="fc02d-112">La classe **Win32 \_ MemoryArrayLocation** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="fc02d-112">The **Win32\_MemoryArrayLocation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fc02d-113">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="fc02d-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc02d-114">Tipo di dati: **Win32 \_ PhysicalMemoryArray**</span><span class="sxs-lookup"><span data-stu-id="fc02d-114">Data type: **Win32\_PhysicalMemoryArray**</span></span>
</dt> <dt>

<span data-ttu-id="fc02d-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fc02d-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc02d-116">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| WMI \_ Win32 PhysicalMemoryArray")</span><span class="sxs-lookup"><span data-stu-id="fc02d-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_PhysicalMemoryArray")</span></span>
</dt> </dl>

<span data-ttu-id="fc02d-117">[**\_ PhysicalMemoryArray Win32**](win32-physicalmemoryarray.md) che descrive la matrice di memoria fisica che implementa la matrice di memoria logica.</span><span class="sxs-lookup"><span data-stu-id="fc02d-117">A [**Win32\_PhysicalMemoryArray**](win32-physicalmemoryarray.md) that describes the physical memory array that implements the logical memory array.</span></span>

</dd> <dt>

<span data-ttu-id="fc02d-118">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="fc02d-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc02d-119">Tipo di dati: **Win32 \_ MemoryArray**</span><span class="sxs-lookup"><span data-stu-id="fc02d-119">Data type: **Win32\_MemoryArray**</span></span>
</dt> <dt>

<span data-ttu-id="fc02d-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fc02d-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc02d-121">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ MemoryArray")</span><span class="sxs-lookup"><span data-stu-id="fc02d-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_MemoryArray")</span></span>
</dt> </dl>

<span data-ttu-id="fc02d-122">[**\_ MemoryArray Win32**](win32-memoryarray.md) che descrive la matrice di memoria logica implementata dalla matrice di memoria fisica.</span><span class="sxs-lookup"><span data-stu-id="fc02d-122">A [**Win32\_MemoryArray**](win32-memoryarray.md) that describes the logical memory array implemented by the physical memory array.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fc02d-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="fc02d-123">Remarks</span></span>

<span data-ttu-id="fc02d-124">La classe **Win32 \_ MemoryArrayLocation** è derivata da [**CIM \_ realizzations**](cim-realizes.md).</span><span class="sxs-lookup"><span data-stu-id="fc02d-124">The **Win32\_MemoryArrayLocation** class is derived from [**CIM\_Realizes**](cim-realizes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fc02d-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fc02d-125">Requirements</span></span>



| <span data-ttu-id="fc02d-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc02d-126">Requirement</span></span> | <span data-ttu-id="fc02d-127">Valore</span><span class="sxs-lookup"><span data-stu-id="fc02d-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fc02d-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fc02d-128">Minimum supported client</span></span><br/> | <span data-ttu-id="fc02d-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fc02d-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fc02d-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fc02d-130">Minimum supported server</span></span><br/> | <span data-ttu-id="fc02d-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fc02d-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fc02d-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="fc02d-132">Namespace</span></span><br/>                | <span data-ttu-id="fc02d-133">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="fc02d-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fc02d-134">MOF</span><span class="sxs-lookup"><span data-stu-id="fc02d-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fc02d-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fc02d-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fc02d-136">DLL</span><span class="sxs-lookup"><span data-stu-id="fc02d-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fc02d-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fc02d-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc02d-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fc02d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc02d-139">**CIM \_ realizza**</span><span class="sxs-lookup"><span data-stu-id="fc02d-139">**CIM\_Realizes**</span></span>](cim-realizes.md)
</dt> <dt>

[<span data-ttu-id="fc02d-140">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="fc02d-140">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

