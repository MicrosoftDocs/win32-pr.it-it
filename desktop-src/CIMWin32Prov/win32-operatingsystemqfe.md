---
description: La \_ classe WMI dell'associazione OperatingSystemQFE Win32 mette in correlazione un sistema operativo e gli aggiornamenti del prodotto applicati come rappresentati in Win32 \_ QuickFixEngineering.
ms.assetid: 71985759-7e45-44df-82a9-f9a93e3b923e
ms.tgt_platform: multiple
title: Classe Win32_OperatingSystemQFE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystemQFE
- Win32_OperatingSystemQFE.Antecedent
- Win32_OperatingSystemQFE.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a3b357e3c6efb62217c137bc6c785185154ed984
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966294"
---
# <a name="win32_operatingsystemqfe-class"></a><span data-ttu-id="3e8f6-103">Win32 \_ OperatingSystemQFE (classe)</span><span class="sxs-lookup"><span data-stu-id="3e8f6-103">Win32\_OperatingSystemQFE class</span></span>

<span data-ttu-id="3e8f6-104">La [classe WMI](../wmisdk/retrieving-a-class.md) dell'associazione **\_ OperatingSystemQFE Win32** mette in correlazione un sistema operativo e gli aggiornamenti del prodotto applicati come rappresentati in [**Win32 \_ QuickFixEngineering**](win32-quickfixengineering.md).</span><span class="sxs-lookup"><span data-stu-id="3e8f6-104">The **Win32\_OperatingSystemQFE** association [WMI class](../wmisdk/retrieving-a-class.md) relates an operating system and the product updates applied as represented in [**Win32\_QuickFixEngineering**](win32-quickfixengineering.md).</span></span>

<span data-ttu-id="3e8f6-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="3e8f6-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="3e8f6-106">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="3e8f6-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e8f6-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3e8f6-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{2CB2C452-C516-11D2-B364-00105A1F77A1}"), AMENDMENT]
class Win32_OperatingSystemQFE : CIM_Dependency
{
  Win32_OperatingSystem     REF Antecedent;
  Win32_QuickFixEngineering REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="3e8f6-108">Members</span><span class="sxs-lookup"><span data-stu-id="3e8f6-108">Members</span></span>

<span data-ttu-id="3e8f6-109">La classe **Win32 \_ OperatingSystemQFE** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="3e8f6-109">The **Win32\_OperatingSystemQFE** class has these types of members:</span></span>

-   [<span data-ttu-id="3e8f6-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3e8f6-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3e8f6-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3e8f6-111">Properties</span></span>

<span data-ttu-id="3e8f6-112">La classe **Win32 \_ OperatingSystemQFE** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="3e8f6-112">The **Win32\_OperatingSystemQFE** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3e8f6-113">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="3e8f6-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e8f6-114">Tipo di dati: **Win32 \_ OperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="3e8f6-114">Data type: **Win32\_OperatingSystem**</span></span>
</dt> <dt>

<span data-ttu-id="3e8f6-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3e8f6-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e8f6-116">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("antecedente"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| WMI \_ Win32 OperatingSystem")</span><span class="sxs-lookup"><span data-stu-id="3e8f6-116">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_OperatingSystem")</span></span>
</dt> </dl>

<span data-ttu-id="3e8f6-117">Riferimento all'istanza di che rappresenta il sistema interessato dall'aggiornamento del prodotto nell'associazione.</span><span class="sxs-lookup"><span data-stu-id="3e8f6-117">Reference to the instance representing the system affected by the product update in this association.</span></span>

</dd> <dt>

<span data-ttu-id="3e8f6-118">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="3e8f6-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e8f6-119">Tipo di dati: **Win32 \_ QuickFixEngineering**</span><span class="sxs-lookup"><span data-stu-id="3e8f6-119">Data type: **Win32\_QuickFixEngineering**</span></span>
</dt> <dt>

<span data-ttu-id="3e8f6-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3e8f6-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e8f6-121">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**debole**](../wmisdk/standard-qualifiers.md), [**override**](../wmisdk/standard-qualifiers.md) ("dipendente"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ QuickFixEngineering")</span><span class="sxs-lookup"><span data-stu-id="3e8f6-121">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Weak**](../wmisdk/standard-qualifiers.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_QuickFixEngineering")</span></span>
</dt> </dl>

<span data-ttu-id="3e8f6-122">Riferimento all'istanza di che rappresenta l'istanza dell'oggetto applicata al sistema operativo in questa associazione.</span><span class="sxs-lookup"><span data-stu-id="3e8f6-122">Reference to the instance representing the object instance applied to the operating system in this association.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3e8f6-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="3e8f6-123">Remarks</span></span>

<span data-ttu-id="3e8f6-124">La classe **Win32 \_ OperatingSystemQFE** è derivata dalla [**\_ dipendenza CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="3e8f6-124">The **Win32\_OperatingSystemQFE** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3e8f6-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3e8f6-125">Requirements</span></span>



| <span data-ttu-id="3e8f6-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e8f6-126">Requirement</span></span> | <span data-ttu-id="3e8f6-127">Valore</span><span class="sxs-lookup"><span data-stu-id="3e8f6-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3e8f6-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3e8f6-128">Minimum supported client</span></span><br/> | <span data-ttu-id="3e8f6-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3e8f6-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3e8f6-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3e8f6-130">Minimum supported server</span></span><br/> | <span data-ttu-id="3e8f6-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3e8f6-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3e8f6-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3e8f6-132">Namespace</span></span><br/>                | <span data-ttu-id="3e8f6-133">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="3e8f6-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3e8f6-134">MOF</span><span class="sxs-lookup"><span data-stu-id="3e8f6-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3e8f6-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3e8f6-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3e8f6-136">DLL</span><span class="sxs-lookup"><span data-stu-id="3e8f6-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e8f6-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e8f6-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e8f6-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3e8f6-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e8f6-139">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="3e8f6-139">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

[<span data-ttu-id="3e8f6-140">Classi del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="3e8f6-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
