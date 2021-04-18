---
description: La \_ classe WMI dell'associazione SystemLoadOrderGroups Win32 mette in correlazione un computer e un gruppo di ordini di caricamento.
ms.assetid: fb637300-0f70-465a-a72b-f0ab3f246790
ms.tgt_platform: multiple
title: Classe Win32_SystemLoadOrderGroups
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemLoadOrderGroups
- Win32_SystemLoadOrderGroups.GroupComponent
- Win32_SystemLoadOrderGroups.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 510acfbde2f562493a454abe80a4f7788377e556
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305249"
---
# <a name="win32_systemloadordergroups-class"></a><span data-ttu-id="13ee6-103">Win32 \_ SystemLoadOrderGroups (classe)</span><span class="sxs-lookup"><span data-stu-id="13ee6-103">Win32\_SystemLoadOrderGroups class</span></span>

<span data-ttu-id="13ee6-104">La [classe WMI](../wmisdk/retrieving-a-class.md) dell'associazione **\_ SystemLoadOrderGroups Win32** mette in correlazione un computer e un gruppo di ordini di caricamento.</span><span class="sxs-lookup"><span data-stu-id="13ee6-104">The **Win32\_SystemLoadOrderGroups** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and a load order group.</span></span>

<span data-ttu-id="13ee6-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="13ee6-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="13ee6-106">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="13ee6-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="13ee6-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="13ee6-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C503-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemLoadOrderGroups : CIM_SystemComponent
{
  Win32_ComputerSystem REF GroupComponent;
  Win32_LoadOrderGroup REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="13ee6-108">Members</span><span class="sxs-lookup"><span data-stu-id="13ee6-108">Members</span></span>

<span data-ttu-id="13ee6-109">La classe **Win32 \_ SystemLoadOrderGroups** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="13ee6-109">The **Win32\_SystemLoadOrderGroups** class has these types of members:</span></span>

-   [<span data-ttu-id="13ee6-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="13ee6-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="13ee6-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="13ee6-111">Properties</span></span>

<span data-ttu-id="13ee6-112">La classe **Win32 \_ SystemLoadOrderGroups** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="13ee6-112">The **Win32\_SystemLoadOrderGroups** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="13ee6-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="13ee6-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13ee6-114">Tipo di dati: **Win32 \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="13ee6-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="13ee6-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="13ee6-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13ee6-116">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")</span><span class="sxs-lookup"><span data-stu-id="13ee6-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="13ee6-117">Riferimento all'istanza di che rappresenta il computer in cui è presente il gruppo dell'ordine di caricamento.</span><span class="sxs-lookup"><span data-stu-id="13ee6-117">Reference to the instance representing the computer system where the load order group exists.</span></span>

</dd> <dt>

<span data-ttu-id="13ee6-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="13ee6-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13ee6-119">Tipo di dati: **Win32 \_ LoadOrderGroup**</span><span class="sxs-lookup"><span data-stu-id="13ee6-119">Data type: **Win32\_LoadOrderGroup**</span></span>
</dt> <dt>

<span data-ttu-id="13ee6-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="13ee6-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13ee6-121">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ LoadOrderGroup")</span><span class="sxs-lookup"><span data-stu-id="13ee6-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_LoadOrderGroup")</span></span>
</dt> </dl>

<span data-ttu-id="13ee6-122">Riferimento all'istanza di che rappresenta il gruppo di ordini di caricamento esistente nel computer.</span><span class="sxs-lookup"><span data-stu-id="13ee6-122">Reference to the instance representing the load order group existing on the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="13ee6-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="13ee6-123">Remarks</span></span>

<span data-ttu-id="13ee6-124">La classe **Win32 \_ SystemLoadOrderGroups** è derivata da [**CIM \_ SystemComponent**](cim-systemcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="13ee6-124">The **Win32\_SystemLoadOrderGroups** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="13ee6-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="13ee6-125">Requirements</span></span>



| <span data-ttu-id="13ee6-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="13ee6-126">Requirement</span></span> | <span data-ttu-id="13ee6-127">Valore</span><span class="sxs-lookup"><span data-stu-id="13ee6-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="13ee6-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="13ee6-128">Minimum supported client</span></span><br/> | <span data-ttu-id="13ee6-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="13ee6-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="13ee6-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="13ee6-130">Minimum supported server</span></span><br/> | <span data-ttu-id="13ee6-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="13ee6-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="13ee6-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="13ee6-132">Namespace</span></span><br/>                | <span data-ttu-id="13ee6-133">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="13ee6-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="13ee6-134">MOF</span><span class="sxs-lookup"><span data-stu-id="13ee6-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="13ee6-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="13ee6-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="13ee6-136">DLL</span><span class="sxs-lookup"><span data-stu-id="13ee6-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13ee6-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13ee6-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13ee6-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="13ee6-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13ee6-139">**\_SYSTEMCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="13ee6-139">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> <dt>

[<span data-ttu-id="13ee6-140">Classi del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="13ee6-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
