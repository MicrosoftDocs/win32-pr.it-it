---
description: La \_ classe WMI dell'associazione SystemServices Win32 mette in correlazione un sistema computer e un programma del servizio esistente nel sistema.
ms.assetid: b372e696-e1e0-4b1e-9fb8-83af8a75c405
ms.tgt_platform: multiple
title: Classe Win32_SystemServices
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemServices
- Win32_SystemServices.GroupComponent
- Win32_SystemServices.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d8e61469729f3753256bc7fcf5598265b5c1b7dc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748391"
---
# <a name="win32_systemservices-class"></a><span data-ttu-id="8d93d-103">Win32 \_ SystemServices (classe)</span><span class="sxs-lookup"><span data-stu-id="8d93d-103">Win32\_SystemServices class</span></span>

<span data-ttu-id="8d93d-104">La [classe WMI](../wmisdk/retrieving-a-class.md) dell'associazione **\_ SystemServices Win32** mette in correlazione un sistema computer e un programma del servizio esistente nel sistema.</span><span class="sxs-lookup"><span data-stu-id="8d93d-104">The **Win32\_SystemServices** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and a service program that exists on the system.</span></span>

<span data-ttu-id="8d93d-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="8d93d-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="8d93d-106">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="8d93d-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d93d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8d93d-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F6-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemServices : CIM_SystemComponent
{
  Win32_ComputerSystem REF GroupComponent;
  Win32_Service        REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="8d93d-108">Members</span><span class="sxs-lookup"><span data-stu-id="8d93d-108">Members</span></span>

<span data-ttu-id="8d93d-109">La classe **Win32 \_ SystemServices** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="8d93d-109">The **Win32\_SystemServices** class has these types of members:</span></span>

-   [<span data-ttu-id="8d93d-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8d93d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8d93d-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8d93d-111">Properties</span></span>

<span data-ttu-id="8d93d-112">La classe **Win32 \_ SystemServices** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="8d93d-112">The **Win32\_SystemServices** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8d93d-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="8d93d-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d93d-114">Tipo di dati: **Win32 \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="8d93d-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="8d93d-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8d93d-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d93d-116">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")</span><span class="sxs-lookup"><span data-stu-id="8d93d-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="8d93d-117">Riferimento all'istanza di che rappresenta le proprietà del computer in cui è presente il servizio.</span><span class="sxs-lookup"><span data-stu-id="8d93d-117">Reference to the instance representing the properties of the computer system on which the service exists.</span></span>

</dd> <dt>

<span data-ttu-id="8d93d-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="8d93d-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d93d-119">Tipo di dati **: \_ servizio Win32**</span><span class="sxs-lookup"><span data-stu-id="8d93d-119">Data type: **Win32\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="8d93d-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8d93d-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d93d-121">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| servizio WMI Win32 \_ ")</span><span class="sxs-lookup"><span data-stu-id="8d93d-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_Service")</span></span>
</dt> </dl>

<span data-ttu-id="8d93d-122">Riferimento all'istanza di che rappresenta il servizio esistente nel computer.</span><span class="sxs-lookup"><span data-stu-id="8d93d-122">Reference to the instance representing the service that exists on the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8d93d-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="8d93d-123">Remarks</span></span>

<span data-ttu-id="8d93d-124">La classe **Win32 \_ SystemServices** è derivata da [**CIM \_ SystemComponent**](cim-systemcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="8d93d-124">The **Win32\_SystemServices** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8d93d-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8d93d-125">Requirements</span></span>



| <span data-ttu-id="8d93d-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d93d-126">Requirement</span></span> | <span data-ttu-id="8d93d-127">Valore</span><span class="sxs-lookup"><span data-stu-id="8d93d-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8d93d-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8d93d-128">Minimum supported client</span></span><br/> | <span data-ttu-id="8d93d-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8d93d-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8d93d-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8d93d-130">Minimum supported server</span></span><br/> | <span data-ttu-id="8d93d-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8d93d-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8d93d-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8d93d-132">Namespace</span></span><br/>                | <span data-ttu-id="8d93d-133">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="8d93d-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8d93d-134">MOF</span><span class="sxs-lookup"><span data-stu-id="8d93d-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8d93d-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8d93d-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8d93d-136">DLL</span><span class="sxs-lookup"><span data-stu-id="8d93d-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8d93d-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d93d-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d93d-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8d93d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d93d-139">**\_SYSTEMCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="8d93d-139">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> <dt>

[<span data-ttu-id="8d93d-140">Classi del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="8d93d-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
