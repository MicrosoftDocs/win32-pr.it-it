---
description: La \_ classe WMI dell'associazione SystemProgramGroups Win32 mette in correlazione un sistema di computer e un gruppo di programmi logici.
ms.assetid: cbf810c8-a967-4d60-889c-e47c43b039ea
ms.tgt_platform: multiple
title: Classe Win32_SystemProgramGroups
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemProgramGroups
- Win32_SystemProgramGroups.Element
- Win32_SystemProgramGroups.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1a8ca556c24295e2c4b04ab851610ef35ec9b715
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127595"
---
# <a name="win32_systemprogramgroups-class"></a><span data-ttu-id="3d3f5-103">Win32 \_ SystemProgramGroups (classe)</span><span class="sxs-lookup"><span data-stu-id="3d3f5-103">Win32\_SystemProgramGroups class</span></span>

<span data-ttu-id="3d3f5-104">La [classe WMI](../wmisdk/retrieving-a-class.md) dell'associazione **\_ SystemProgramGroups Win32** mette in correlazione un sistema di computer e un gruppo di programmi logici.</span><span class="sxs-lookup"><span data-stu-id="3d3f5-104">The **Win32\_SystemProgramGroups** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and a logical program group.</span></span>

<span data-ttu-id="3d3f5-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="3d3f5-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="3d3f5-106">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="3d3f5-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d3f5-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3d3f5-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C505-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemProgramGroups : Win32_SystemSetting
{
  Win32_ComputerSystem      REF Element;
  Win32_LogicalProgramGroup REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="3d3f5-108">Members</span><span class="sxs-lookup"><span data-stu-id="3d3f5-108">Members</span></span>

<span data-ttu-id="3d3f5-109">La classe **Win32 \_ SystemProgramGroups** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="3d3f5-109">The **Win32\_SystemProgramGroups** class has these types of members:</span></span>

-   [<span data-ttu-id="3d3f5-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3d3f5-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3d3f5-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3d3f5-111">Properties</span></span>

<span data-ttu-id="3d3f5-112">La classe **Win32 \_ SystemProgramGroups** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="3d3f5-112">The **Win32\_SystemProgramGroups** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3d3f5-113">**elemento**</span><span class="sxs-lookup"><span data-stu-id="3d3f5-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d3f5-114">Tipo di dati: **Win32 \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="3d3f5-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="3d3f5-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3d3f5-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d3f5-116">Qualificatori: [**override**](../wmisdk/standard-qualifiers.md) ("element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")</span><span class="sxs-lookup"><span data-stu-id="3d3f5-116">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="3d3f5-117">Riferimento all'istanza di che rappresenta il computer che contiene il gruppo di programmi logici.</span><span class="sxs-lookup"><span data-stu-id="3d3f5-117">Reference to the instance representing the computer system containing the logical program group.</span></span>

</dd> <dt>

<span data-ttu-id="3d3f5-118">**Impostazione**</span><span class="sxs-lookup"><span data-stu-id="3d3f5-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d3f5-119">Tipo di dati: **Win32 \_ LogicalProgramGroup**</span><span class="sxs-lookup"><span data-stu-id="3d3f5-119">Data type: **Win32\_LogicalProgramGroup**</span></span>
</dt> <dt>

<span data-ttu-id="3d3f5-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3d3f5-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d3f5-121">Qualificatori: [**override**](../wmisdk/standard-qualifiers.md) ("setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ LogicalProgramGroup")</span><span class="sxs-lookup"><span data-stu-id="3d3f5-121">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_LogicalProgramGroup")</span></span>
</dt> </dl>

<span data-ttu-id="3d3f5-122">Riferimento all'istanza che rappresenta il gruppo di programmi logici nel computer.</span><span class="sxs-lookup"><span data-stu-id="3d3f5-122">Reference to the instance representing the logical program group on the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3d3f5-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="3d3f5-123">Remarks</span></span>

<span data-ttu-id="3d3f5-124">La classe **Win32 \_ SystemProgramGroups** è derivata da [**Win32 \_ SystemSetting**](win32-systemsetting.md).</span><span class="sxs-lookup"><span data-stu-id="3d3f5-124">The **Win32\_SystemProgramGroups** class is derived from [**Win32\_SystemSetting**](win32-systemsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3d3f5-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3d3f5-125">Requirements</span></span>



| <span data-ttu-id="3d3f5-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d3f5-126">Requirement</span></span> | <span data-ttu-id="3d3f5-127">Valore</span><span class="sxs-lookup"><span data-stu-id="3d3f5-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3d3f5-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3d3f5-128">Minimum supported client</span></span><br/> | <span data-ttu-id="3d3f5-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3d3f5-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3d3f5-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3d3f5-130">Minimum supported server</span></span><br/> | <span data-ttu-id="3d3f5-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3d3f5-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3d3f5-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3d3f5-132">Namespace</span></span><br/>                | <span data-ttu-id="3d3f5-133">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="3d3f5-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3d3f5-134">MOF</span><span class="sxs-lookup"><span data-stu-id="3d3f5-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3d3f5-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3d3f5-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3d3f5-136">DLL</span><span class="sxs-lookup"><span data-stu-id="3d3f5-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d3f5-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d3f5-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d3f5-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3d3f5-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d3f5-139">**\_SystemSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="3d3f5-139">**Win32\_SystemSetting**</span></span>](win32-systemsetting.md)
</dt> <dt>

[<span data-ttu-id="3d3f5-140">Classi del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="3d3f5-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
