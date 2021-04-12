---
description: La \_ classe WMI dell'associazione SystemDriverPNPEntity Win32 mette in correlazione un dispositivo Plug and Play nel computer che esegue Windows e il driver che supporta il dispositivo Plug and Play.
ms.assetid: 2696c8e5-3bc3-42e3-807b-a387607c7c09
ms.tgt_platform: multiple
title: Classe Win32_SystemDriverPNPEntity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriverPNPEntity
- Win32_SystemDriverPNPEntity.Antecedent
- Win32_SystemDriverPNPEntity.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8b5a7eedfbd7a545e37cb9cda38c19cf61308761
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523682"
---
# <a name="win32_systemdriverpnpentity-class"></a><span data-ttu-id="0507a-103">Win32 \_ SystemDriverPNPEntity (classe)</span><span class="sxs-lookup"><span data-stu-id="0507a-103">Win32\_SystemDriverPNPEntity class</span></span>

<span data-ttu-id="0507a-104">La [classe WMI](../wmisdk/retrieving-a-class.md) dell'associazione **\_ SystemDriverPNPEntity Win32** mette in correlazione un dispositivo Plug and Play nel computer che esegue Windows e il driver che supporta il dispositivo Plug and Play.</span><span class="sxs-lookup"><span data-stu-id="0507a-104">The **Win32\_SystemDriverPNPEntity** association [WMI class](../wmisdk/retrieving-a-class.md) relates a Plug and Play device on the computer system running Windows and the driver that supports the Plug and Play device.</span></span>

<span data-ttu-id="0507a-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="0507a-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="0507a-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="0507a-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0507a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0507a-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{0800F074-CB98-11d2-B35D-00104BC97924}"), AMENDMENT]
class Win32_SystemDriverPNPEntity : CIM_Dependency
{
  Win32_PNPEntity    REF Antecedent;
  Win32_SystemDriver REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="0507a-108">Members</span><span class="sxs-lookup"><span data-stu-id="0507a-108">Members</span></span>

<span data-ttu-id="0507a-109">La classe **Win32 \_ SystemDriverPNPEntity** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="0507a-109">The **Win32\_SystemDriverPNPEntity** class has these types of members:</span></span>

-   [<span data-ttu-id="0507a-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0507a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0507a-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0507a-111">Properties</span></span>

<span data-ttu-id="0507a-112">La classe **Win32 \_ SystemDriverPNPEntity** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="0507a-112">The **Win32\_SystemDriverPNPEntity** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0507a-113">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="0507a-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0507a-114">Tipo di dati: **Win32 \_ PNPEntity**</span><span class="sxs-lookup"><span data-stu-id="0507a-114">Data type: **Win32\_PNPEntity**</span></span>
</dt> <dt>

<span data-ttu-id="0507a-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0507a-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0507a-116">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("antecedente"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| WMI \_ Win32 PNPEntity")</span><span class="sxs-lookup"><span data-stu-id="0507a-116">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_PNPEntity")</span></span>
</dt> </dl>

<span data-ttu-id="0507a-117">Rappresenta il dispositivo Plug and Play controllato dal driver.</span><span class="sxs-lookup"><span data-stu-id="0507a-117">Represents the Plug and Play device controlled by the driver.</span></span>

</dd> <dt>

<span data-ttu-id="0507a-118">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="0507a-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0507a-119">Tipo di dati: **Win32 \_ SystemDriver**</span><span class="sxs-lookup"><span data-stu-id="0507a-119">Data type: **Win32\_SystemDriver**</span></span>
</dt> <dt>

<span data-ttu-id="0507a-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0507a-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0507a-121">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("dipendente"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ SystemDriver")</span><span class="sxs-lookup"><span data-stu-id="0507a-121">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_SystemDriver")</span></span>
</dt> </dl>

<span data-ttu-id="0507a-122">[**\_ SystemDriver Win32**](win32-systemdriver.md) che rappresenta il driver che supporta il dispositivo Plug and Play.</span><span class="sxs-lookup"><span data-stu-id="0507a-122">A [**Win32\_SystemDriver**](win32-systemdriver.md) that represents the driver that supports the Plug and Play device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0507a-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="0507a-123">Remarks</span></span>

<span data-ttu-id="0507a-124">La classe **Win32 \_ SystemDriverPNPEntity** è derivata dalla [**\_ dipendenza CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="0507a-124">The **Win32\_SystemDriverPNPEntity** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0507a-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0507a-125">Requirements</span></span>



| <span data-ttu-id="0507a-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="0507a-126">Requirement</span></span> | <span data-ttu-id="0507a-127">Valore</span><span class="sxs-lookup"><span data-stu-id="0507a-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0507a-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0507a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="0507a-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0507a-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0507a-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0507a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="0507a-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0507a-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0507a-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0507a-132">Namespace</span></span><br/>                | <span data-ttu-id="0507a-133">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="0507a-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0507a-134">MOF</span><span class="sxs-lookup"><span data-stu-id="0507a-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0507a-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0507a-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0507a-136">DLL</span><span class="sxs-lookup"><span data-stu-id="0507a-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0507a-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0507a-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0507a-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0507a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0507a-139">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="0507a-139">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

[<span data-ttu-id="0507a-140">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="0507a-140">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
