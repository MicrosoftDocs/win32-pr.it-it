---
description: La \_ classe WMI dell'associazione SystemBIOS Win32 mette in relazione un computer (inclusi dati quali le proprietà di avvio, i fusi orari, le configurazioni di avvio o le password amministrative) e un BIOS di sistema (servizi, lingue e proprietà di gestione del sistema).
ms.assetid: 92747b1b-ef28-40ab-868a-6755aee8c723
ms.tgt_platform: multiple
title: Classe Win32_SystemBIOS
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemBIOS
- Win32_SystemBIOS.PartComponent
- Win32_SystemBIOS.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: bc8ec1f3526e2faefe0e63c9dea357accd025c13
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878218"
---
# <a name="win32_systembios-class"></a><span data-ttu-id="7bd92-103">Win32 \_ SystemBIOS (classe)</span><span class="sxs-lookup"><span data-stu-id="7bd92-103">Win32\_SystemBIOS class</span></span>

<span data-ttu-id="7bd92-104">La [classe WMI](../wmisdk/retrieving-a-class.md) dell'associazione **\_ SystemBIOS Win32** mette in relazione un computer (inclusi dati quali le proprietà di avvio, i fusi orari, le configurazioni di avvio o le password amministrative) e un BIOS di sistema (servizi, lingue e proprietà di gestione del sistema).</span><span class="sxs-lookup"><span data-stu-id="7bd92-104">The **Win32\_SystemBIOS** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system (including data such as startup properties, time zones, boot configurations, or administrative passwords), and a system BIOS (services, languages, and system management properties).</span></span>

<span data-ttu-id="7bd92-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="7bd92-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="7bd92-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="7bd92-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7bd92-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7bd92-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4EE-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemBIOS : CIM_SystemComponent
{
  Win32_BIOS           REF PartComponent;
  Win32_ComputerSystem REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="7bd92-108">Members</span><span class="sxs-lookup"><span data-stu-id="7bd92-108">Members</span></span>

<span data-ttu-id="7bd92-109">La classe **Win32 \_ SystemBIOS** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="7bd92-109">The **Win32\_SystemBIOS** class has these types of members:</span></span>

-   [<span data-ttu-id="7bd92-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7bd92-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7bd92-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7bd92-111">Properties</span></span>

<span data-ttu-id="7bd92-112">La classe **Win32 \_ SystemBIOS** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="7bd92-112">The **Win32\_SystemBIOS** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7bd92-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="7bd92-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bd92-114">Tipo di dati: **Win32 \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="7bd92-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="7bd92-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7bd92-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7bd92-116">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")</span><span class="sxs-lookup"><span data-stu-id="7bd92-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="7bd92-117">[**\_ ComputerSystem Win32**](win32-computersystemprocessor.md) che contiene il BIOS dell'associazione.</span><span class="sxs-lookup"><span data-stu-id="7bd92-117">The [**Win32\_ComputerSystem**](win32-computersystemprocessor.md) containing the BIOS of the association.</span></span>

</dd> <dt>

<span data-ttu-id="7bd92-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="7bd92-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bd92-119">Tipo di dati **: \_ BIOS Win32**</span><span class="sxs-lookup"><span data-stu-id="7bd92-119">Data type: **Win32\_BIOS**</span></span>
</dt> <dt>

<span data-ttu-id="7bd92-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7bd92-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7bd92-121">Qualificatori: [**chiave**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| BIOS Win32 Win32 \_ ")</span><span class="sxs-lookup"><span data-stu-id="7bd92-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_BIOS")</span></span>
</dt> </dl>

<span data-ttu-id="7bd92-122">Un [**\_ BIOS Win32**](win32-bios.md) contenuto nel computer del sistema di questa associazione.</span><span class="sxs-lookup"><span data-stu-id="7bd92-122">A [**Win32\_BIOS**](win32-bios.md) contained in the computer system of this association.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7bd92-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="7bd92-123">Remarks</span></span>

<span data-ttu-id="7bd92-124">La classe **Win32 \_ SystemBIOS** è derivata da [**CIM \_ SystemComponent**](cim-systemcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="7bd92-124">The **Win32\_SystemBIOS** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7bd92-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7bd92-125">Requirements</span></span>



| <span data-ttu-id="7bd92-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="7bd92-126">Requirement</span></span> | <span data-ttu-id="7bd92-127">Valore</span><span class="sxs-lookup"><span data-stu-id="7bd92-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7bd92-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7bd92-128">Minimum supported client</span></span><br/> | <span data-ttu-id="7bd92-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7bd92-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7bd92-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7bd92-130">Minimum supported server</span></span><br/> | <span data-ttu-id="7bd92-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7bd92-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7bd92-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7bd92-132">Namespace</span></span><br/>                | <span data-ttu-id="7bd92-133">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="7bd92-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7bd92-134">MOF</span><span class="sxs-lookup"><span data-stu-id="7bd92-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7bd92-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7bd92-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7bd92-136">DLL</span><span class="sxs-lookup"><span data-stu-id="7bd92-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7bd92-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7bd92-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7bd92-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7bd92-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bd92-139">**\_SYSTEMCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="7bd92-139">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> <dt>

[<span data-ttu-id="7bd92-140">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="7bd92-140">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
