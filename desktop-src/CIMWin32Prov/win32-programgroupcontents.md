---
description: La \_ classe WMI dell'associazione ProgramGroupContents Win32 mette in correlazione un ordine del gruppo di programmi e un singolo gruppo o elemento del programma contenuto.
ms.assetid: 687794d1-acc1-498a-9886-0c9ac762ebf4
ms.tgt_platform: multiple
title: Classe Win32_ProgramGroupContents
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ProgramGroupContents
- Win32_ProgramGroupContents.GroupComponent
- Win32_ProgramGroupContents.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5f77a61052357f7c67009ee7a89da018abeadda8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049118"
---
# <a name="win32_programgroupcontents-class"></a><span data-ttu-id="624d5-103">Win32 \_ ProgramGroupContents (classe)</span><span class="sxs-lookup"><span data-stu-id="624d5-103">Win32\_ProgramGroupContents class</span></span>

<span data-ttu-id="624d5-104">La [classe WMI](../wmisdk/retrieving-a-class.md) dell'associazione **\_ ProgramGroupContents Win32** mette in correlazione un ordine del gruppo di programmi e un singolo gruppo o elemento del programma contenuto.</span><span class="sxs-lookup"><span data-stu-id="624d5-104">The **Win32\_ProgramGroupContents** association [WMI class](../wmisdk/retrieving-a-class.md) relates a program group order and an individual program group or item contained in it.</span></span>

<span data-ttu-id="624d5-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="624d5-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="624d5-106">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="624d5-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="624d5-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="624d5-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{86E30E83-7DB2-11d2-90CB-0060081A46FD}"), AMENDMENT]
class Win32_ProgramGroupContents : CIM_Component
{
  Win32_LogicalProgramGroup REF GroupComponent;
  Win32_ProgramGroupOrItem  REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="624d5-108">Members</span><span class="sxs-lookup"><span data-stu-id="624d5-108">Members</span></span>

<span data-ttu-id="624d5-109">La classe **Win32 \_ ProgramGroupContents** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="624d5-109">The **Win32\_ProgramGroupContents** class has these types of members:</span></span>

-   [<span data-ttu-id="624d5-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="624d5-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="624d5-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="624d5-111">Properties</span></span>

<span data-ttu-id="624d5-112">La classe **Win32 \_ ProgramGroupContents** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="624d5-112">The **Win32\_ProgramGroupContents** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="624d5-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="624d5-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="624d5-114">Tipo di dati: **Win32 \_ LogicalProgramGroup**</span><span class="sxs-lookup"><span data-stu-id="624d5-114">Data type: **Win32\_LogicalProgramGroup**</span></span>
</dt> <dt>

<span data-ttu-id="624d5-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="624d5-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="624d5-116">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ LogicalProgramGroup")</span><span class="sxs-lookup"><span data-stu-id="624d5-116">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_LogicalProgramGroup")</span></span>
</dt> </dl>

<span data-ttu-id="624d5-117">Riferimento all'istanza di che rappresenta il gruppo di programmi logici per questa associazione.</span><span class="sxs-lookup"><span data-stu-id="624d5-117">Reference to the instance representing the logical program group for this association.</span></span>

</dd> <dt>

<span data-ttu-id="624d5-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="624d5-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="624d5-119">Tipo di dati: **Win32 \_ ProgramGroupOrItem**</span><span class="sxs-lookup"><span data-stu-id="624d5-119">Data type: **Win32\_ProgramGroupOrItem**</span></span>
</dt> <dt>

<span data-ttu-id="624d5-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="624d5-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="624d5-121">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ProgramGroupOrItem")</span><span class="sxs-lookup"><span data-stu-id="624d5-121">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ProgramGroupOrItem")</span></span>
</dt> </dl>

<span data-ttu-id="624d5-122">Riferimento all'istanza di che rappresenta il gruppo o l'elemento del menu **Start** per questa associazione.</span><span class="sxs-lookup"><span data-stu-id="624d5-122">Reference to the instance representing the **Start** menu group or item for this association.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="624d5-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="624d5-123">Remarks</span></span>

<span data-ttu-id="624d5-124">La classe **Win32 \_ ProgramGroupContents** è derivata dal [**\_ componente CIM**](cim-component.md).</span><span class="sxs-lookup"><span data-stu-id="624d5-124">The **Win32\_ProgramGroupContents** class is derived from [**CIM\_Component**](cim-component.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="624d5-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="624d5-125">Requirements</span></span>



| <span data-ttu-id="624d5-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="624d5-126">Requirement</span></span> | <span data-ttu-id="624d5-127">Valore</span><span class="sxs-lookup"><span data-stu-id="624d5-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="624d5-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="624d5-128">Minimum supported client</span></span><br/> | <span data-ttu-id="624d5-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="624d5-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="624d5-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="624d5-130">Minimum supported server</span></span><br/> | <span data-ttu-id="624d5-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="624d5-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="624d5-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="624d5-132">Namespace</span></span><br/>                | <span data-ttu-id="624d5-133">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="624d5-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="624d5-134">MOF</span><span class="sxs-lookup"><span data-stu-id="624d5-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="624d5-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="624d5-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="624d5-136">DLL</span><span class="sxs-lookup"><span data-stu-id="624d5-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="624d5-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="624d5-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="624d5-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="624d5-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="624d5-139">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="624d5-139">**CIM\_Component**</span></span>](cim-component.md)
</dt> <dt>

[<span data-ttu-id="624d5-140">Classi del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="624d5-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
