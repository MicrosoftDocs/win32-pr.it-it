---
description: La \_ classe WMI dell'associazione SystemResources Win32 mette in relazione una risorsa di sistema e il sistema del computer in cui risiede.
ms.assetid: 90bff0b0-7c1d-44bf-b67e-aefeaa4b4a83
ms.tgt_platform: multiple
title: Classe Win32_SystemResources
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemResources
- Win32_SystemResources.GroupComponent
- Win32_SystemResources.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fe96467e4bc609fa9426edd3c977b5596ea95fe7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966128"
---
# <a name="win32_systemresources-class"></a><span data-ttu-id="56415-103">Win32 \_ SystemResources (classe)</span><span class="sxs-lookup"><span data-stu-id="56415-103">Win32\_SystemResources class</span></span>

<span data-ttu-id="56415-104">La [classe WMI](../wmisdk/retrieving-a-class.md) dell'associazione **\_ SystemResources Win32** mette in relazione una risorsa di sistema e il sistema del computer in cui risiede.</span><span class="sxs-lookup"><span data-stu-id="56415-104">The **Win32\_SystemResources** association [WMI class](../wmisdk/retrieving-a-class.md) relates a system resource and the computer system it resides on.</span></span>

<span data-ttu-id="56415-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="56415-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="56415-106">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="56415-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="56415-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="56415-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F8-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemResources : CIM_ComputerSystemResource
{
  Win32_ComputerSystem REF GroupComponent;
  CIM_SystemResource   REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="56415-108">Members</span><span class="sxs-lookup"><span data-stu-id="56415-108">Members</span></span>

<span data-ttu-id="56415-109">La classe **Win32 \_ SystemResources** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="56415-109">The **Win32\_SystemResources** class has these types of members:</span></span>

-   [<span data-ttu-id="56415-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="56415-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="56415-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="56415-111">Properties</span></span>

<span data-ttu-id="56415-112">La classe **Win32 \_ SystemResources** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="56415-112">The **Win32\_SystemResources** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="56415-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="56415-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56415-114">Tipo di dati: **Win32 \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="56415-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="56415-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="56415-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56415-116">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")</span><span class="sxs-lookup"><span data-stu-id="56415-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="56415-117">Riferimento all'istanza di che rappresenta il computer in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="56415-117">Reference to the instance representing the computer system where the resource is located.</span></span>

</dd> <dt>

<span data-ttu-id="56415-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="56415-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56415-119">Tipo di dati: **CIM \_ SystemResource**</span><span class="sxs-lookup"><span data-stu-id="56415-119">Data type: **CIM\_SystemResource**</span></span>
</dt> <dt>

<span data-ttu-id="56415-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="56415-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56415-121">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ SystemResource")</span><span class="sxs-lookup"><span data-stu-id="56415-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_SystemResource")</span></span>
</dt> </dl>

<span data-ttu-id="56415-122">Riferimento all'istanza di che rappresenta la risorsa, ad esempio servizi di I/O e risorse di memoria, disponibile nel computer.</span><span class="sxs-lookup"><span data-stu-id="56415-122">Reference to the instance representing the resource (such as I/O services and memory resources) available on the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="56415-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="56415-123">Remarks</span></span>

<span data-ttu-id="56415-124">La classe **Win32 \_ SystemResources** è derivata da [**CIM \_ ComputerSystemResource**](cim-computersystemresource.md).</span><span class="sxs-lookup"><span data-stu-id="56415-124">The **Win32\_SystemResources** class is derived from [**CIM\_ComputerSystemResource**](cim-computersystemresource.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="56415-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="56415-125">Requirements</span></span>



| <span data-ttu-id="56415-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="56415-126">Requirement</span></span> | <span data-ttu-id="56415-127">Valore</span><span class="sxs-lookup"><span data-stu-id="56415-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="56415-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="56415-128">Minimum supported client</span></span><br/> | <span data-ttu-id="56415-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="56415-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="56415-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="56415-130">Minimum supported server</span></span><br/> | <span data-ttu-id="56415-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="56415-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="56415-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="56415-132">Namespace</span></span><br/>                | <span data-ttu-id="56415-133">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="56415-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="56415-134">MOF</span><span class="sxs-lookup"><span data-stu-id="56415-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="56415-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="56415-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="56415-136">DLL</span><span class="sxs-lookup"><span data-stu-id="56415-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="56415-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56415-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56415-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="56415-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56415-139">**\_COMPUTERSYSTEMRESOURCE CIM**</span><span class="sxs-lookup"><span data-stu-id="56415-139">**CIM\_ComputerSystemResource**</span></span>](cim-computersystemresource.md)
</dt> <dt>

[<span data-ttu-id="56415-140">Classi del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="56415-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
