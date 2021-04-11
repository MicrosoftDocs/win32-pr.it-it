---
description: La \_ classe WMI dell'associazione SystemOperatingSystem Win32 mette in correlazione un computer e il relativo sistema operativo.
ms.assetid: dc71f80b-6fbd-4bc8-8783-3922d8050518
ms.tgt_platform: multiple
title: Classe Win32_SystemOperatingSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemOperatingSystem
- Win32_SystemOperatingSystem.PrimaryOS
- Win32_SystemOperatingSystem.GroupComponent
- Win32_SystemOperatingSystem.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ba3f8ac94ec882ee1df96da51d93d2c24fde9b3f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127610"
---
# <a name="win32_systemoperatingsystem-class"></a><span data-ttu-id="a10db-103">Win32 \_ SystemOperatingSystem (classe)</span><span class="sxs-lookup"><span data-stu-id="a10db-103">Win32\_SystemOperatingSystem class</span></span>

<span data-ttu-id="a10db-104">La [classe WMI](../wmisdk/retrieving-a-class.md) dell'associazione **\_ SystemOperatingSystem Win32** mette in correlazione un computer e il relativo sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="a10db-104">The **Win32\_SystemOperatingSystem** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and its operating system.</span></span>

<span data-ttu-id="a10db-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="a10db-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="a10db-106">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="a10db-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a10db-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a10db-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F0-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemOperatingSystem : CIM_InstalledOS
{
  boolean                   PrimaryOS;
  Win32_ComputerSystem  REF GroupComponent;
  Win32_OperatingSystem REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="a10db-108">Members</span><span class="sxs-lookup"><span data-stu-id="a10db-108">Members</span></span>

<span data-ttu-id="a10db-109">La classe **Win32 \_ SystemOperatingSystem** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a10db-109">The **Win32\_SystemOperatingSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="a10db-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a10db-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a10db-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a10db-111">Properties</span></span>

<span data-ttu-id="a10db-112">La classe **Win32 \_ SystemOperatingSystem** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="a10db-112">The **Win32\_SystemOperatingSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a10db-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="a10db-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a10db-114">Tipo di dati: **Win32 \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="a10db-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="a10db-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a10db-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a10db-116">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")</span><span class="sxs-lookup"><span data-stu-id="a10db-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="a10db-117">[**\_ ComputerSystem Win32**](win32-computersystemprocessor.md) che descrive le proprietà del computer su cui è installato il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="a10db-117">A [**Win32\_ComputerSystem**](win32-computersystemprocessor.md) that describes the properties of the computer system upon which the operating system is installed.</span></span>

</dd> <dt>

<span data-ttu-id="a10db-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="a10db-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a10db-119">Tipo di dati: **Win32 \_ OperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="a10db-119">Data type: **Win32\_OperatingSystem**</span></span>
</dt> <dt>

<span data-ttu-id="a10db-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a10db-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a10db-121">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ OperatingSystem")</span><span class="sxs-lookup"><span data-stu-id="a10db-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_OperatingSystem")</span></span>
</dt> </dl>

<span data-ttu-id="a10db-122">[**\_ OperatingSystem Win32**](win32-operatingsystem.md) che descrive le proprietà del sistema operativo in esecuzione nel computer.</span><span class="sxs-lookup"><span data-stu-id="a10db-122">A [**Win32\_OperatingSystem**](win32-operatingsystem.md) that describes properties of the operating system running on this computer system.</span></span>

</dd> <dt>

<span data-ttu-id="a10db-123">**Primarie**</span><span class="sxs-lookup"><span data-stu-id="a10db-123">**PrimaryOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a10db-124">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="a10db-124">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a10db-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a10db-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a10db-126">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Sistema operativo DMTF \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="a10db-126">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operating System\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="a10db-127">Se **true**, il sistema operativo installato è il sistema operativo predefinito per il computer.</span><span class="sxs-lookup"><span data-stu-id="a10db-127">If **TRUE**, the installed operating system is the default operating system for the computer system.</span></span>

<span data-ttu-id="a10db-128">Questa proprietà viene ereditata da [**CIM \_ installato**](cim-installedos.md).</span><span class="sxs-lookup"><span data-stu-id="a10db-128">This property is inherited from [**CIM\_InstalledOS**](cim-installedos.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a10db-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="a10db-129">Remarks</span></span>

<span data-ttu-id="a10db-130">La classe **Win32 \_ SystemOperatingSystem** è derivata da [**CIM \_ installato**](cim-installedos.md).</span><span class="sxs-lookup"><span data-stu-id="a10db-130">The **Win32\_SystemOperatingSystem** class is derived from [**CIM\_InstalledOS**](cim-installedos.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a10db-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a10db-131">Requirements</span></span>



| <span data-ttu-id="a10db-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="a10db-132">Requirement</span></span> | <span data-ttu-id="a10db-133">Valore</span><span class="sxs-lookup"><span data-stu-id="a10db-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a10db-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a10db-134">Minimum supported client</span></span><br/> | <span data-ttu-id="a10db-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a10db-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a10db-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a10db-136">Minimum supported server</span></span><br/> | <span data-ttu-id="a10db-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a10db-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a10db-138">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a10db-138">Namespace</span></span><br/>                | <span data-ttu-id="a10db-139">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="a10db-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a10db-140">MOF</span><span class="sxs-lookup"><span data-stu-id="a10db-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a10db-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a10db-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a10db-142">DLL</span><span class="sxs-lookup"><span data-stu-id="a10db-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a10db-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a10db-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a10db-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a10db-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a10db-145">**CIM \_ installato**</span><span class="sxs-lookup"><span data-stu-id="a10db-145">**CIM\_InstalledOS**</span></span>](cim-installedos.md)
</dt> <dt>

[<span data-ttu-id="a10db-146">Classi del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="a10db-146">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
