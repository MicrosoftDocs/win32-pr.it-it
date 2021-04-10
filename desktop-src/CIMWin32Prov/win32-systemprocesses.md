---
description: La \_ classe WMI dell'associazione SystemProcesses Win32 mette in relazione un computer e un processo in esecuzione nel sistema.
ms.assetid: 0d8c3ec6-265e-4486-8e94-f5acd2845cf5
ms.tgt_platform: multiple
title: Classe Win32_SystemProcesses
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemProcesses
- Win32_SystemProcesses.GroupComponent
- Win32_SystemProcesses.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1b963aea5d9c651e27dc4380200e40dd3dcb9a77
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049195"
---
# <a name="win32_systemprocesses-class"></a><span data-ttu-id="849e8-103">Win32 \_ SystemProcesses (classe)</span><span class="sxs-lookup"><span data-stu-id="849e8-103">Win32\_SystemProcesses class</span></span>

<span data-ttu-id="849e8-104">La [classe WMI](../wmisdk/retrieving-a-class.md) dell'associazione **\_ SystemProcesses Win32** mette in relazione un computer e un processo in esecuzione nel sistema.</span><span class="sxs-lookup"><span data-stu-id="849e8-104">The **Win32\_SystemProcesses** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and a process running on that system.</span></span>

<span data-ttu-id="849e8-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="849e8-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="849e8-106">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="849e8-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="849e8-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="849e8-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F3-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemProcesses : CIM_SystemComponent
{
  Win32_ComputerSystem REF GroupComponent;
  Win32_Process        REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="849e8-108">Members</span><span class="sxs-lookup"><span data-stu-id="849e8-108">Members</span></span>

<span data-ttu-id="849e8-109">La classe **Win32 \_ SystemProcesses** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="849e8-109">The **Win32\_SystemProcesses** class has these types of members:</span></span>

-   [<span data-ttu-id="849e8-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="849e8-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="849e8-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="849e8-111">Properties</span></span>

<span data-ttu-id="849e8-112">La classe **Win32 \_ SystemProcesses** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="849e8-112">The **Win32\_SystemProcesses** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="849e8-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="849e8-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="849e8-114">Tipo di dati: **Win32 \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="849e8-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="849e8-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="849e8-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="849e8-116">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")</span><span class="sxs-lookup"><span data-stu-id="849e8-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="849e8-117">Riferimento all'istanza di che rappresenta il computer su cui è in esecuzione il processo.</span><span class="sxs-lookup"><span data-stu-id="849e8-117">Reference to the instance representing the computer system upon which the process is running.</span></span>

</dd> <dt>

<span data-ttu-id="849e8-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="849e8-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="849e8-119">Tipo di dati **: \_ processo Win32**</span><span class="sxs-lookup"><span data-stu-id="849e8-119">Data type: **Win32\_Process**</span></span>
</dt> <dt>

<span data-ttu-id="849e8-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="849e8-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="849e8-121">Qualificatori: [**chiave**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| processo Win32 Win32 \_ ")</span><span class="sxs-lookup"><span data-stu-id="849e8-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_Process")</span></span>
</dt> </dl>

<span data-ttu-id="849e8-122">Riferimento all'istanza di che rappresenta il processo in esecuzione nel computer.</span><span class="sxs-lookup"><span data-stu-id="849e8-122">Reference to the instance representing the process running on the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="849e8-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="849e8-123">Remarks</span></span>

<span data-ttu-id="849e8-124">La classe **Win32 \_ SystemProcesses** è derivata da [**CIM \_ SystemComponent**](cim-systemcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="849e8-124">The **Win32\_SystemProcesses** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="849e8-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="849e8-125">Requirements</span></span>



| <span data-ttu-id="849e8-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="849e8-126">Requirement</span></span> | <span data-ttu-id="849e8-127">Valore</span><span class="sxs-lookup"><span data-stu-id="849e8-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="849e8-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="849e8-128">Minimum supported client</span></span><br/> | <span data-ttu-id="849e8-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="849e8-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="849e8-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="849e8-130">Minimum supported server</span></span><br/> | <span data-ttu-id="849e8-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="849e8-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="849e8-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="849e8-132">Namespace</span></span><br/>                | <span data-ttu-id="849e8-133">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="849e8-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="849e8-134">MOF</span><span class="sxs-lookup"><span data-stu-id="849e8-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="849e8-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="849e8-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="849e8-136">DLL</span><span class="sxs-lookup"><span data-stu-id="849e8-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="849e8-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="849e8-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="849e8-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="849e8-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="849e8-139">**\_SYSTEMCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="849e8-139">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> <dt>

[<span data-ttu-id="849e8-140">Classi del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="849e8-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
