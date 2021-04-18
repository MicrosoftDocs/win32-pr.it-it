---
description: L' \_ associazione CIM ElementsLinked rappresenta elementi fisici collegati da un collegamento fisico.
ms.assetid: b9e1d11e-6f89-4d7a-9b5c-01161e7c1bdf
ms.tgt_platform: multiple
title: Classe CIM_ElementsLinked
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementsLinked
- CIM_ElementsLinked.Dependent
- CIM_ElementsLinked.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 353809056d1ca3bae710272b02c2636a3f02eef1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304919"
---
# <a name="cim_elementslinked-class"></a><span data-ttu-id="fb72b-103">CIM \_ ElementsLinked (classe)</span><span class="sxs-lookup"><span data-stu-id="fb72b-103">CIM\_ElementsLinked class</span></span>

<span data-ttu-id="fb72b-104">L'associazione **CIM \_ ElementsLinked** rappresenta elementi fisici collegati da un collegamento fisico.</span><span class="sxs-lookup"><span data-stu-id="fb72b-104">The **CIM\_ElementsLinked** association represents physical elements that are cabled together by a physical link.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fb72b-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="fb72b-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="fb72b-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="fb72b-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="fb72b-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="fb72b-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="fb72b-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="fb72b-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb72b-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fb72b-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B83-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_ElementsLinked : CIM_Dependency
{
  CIM_PhysicalElement REF Dependent;
  CIM_PhysicalLink    REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="fb72b-110">Members</span><span class="sxs-lookup"><span data-stu-id="fb72b-110">Members</span></span>

<span data-ttu-id="fb72b-111">La classe **CIM \_ ElementsLinked** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="fb72b-111">The **CIM\_ElementsLinked** class has these types of members:</span></span>

-   [<span data-ttu-id="fb72b-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="fb72b-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fb72b-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="fb72b-113">Properties</span></span>

<span data-ttu-id="fb72b-114">La classe **CIM \_ ElementsLinked** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="fb72b-114">The **CIM\_ElementsLinked** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fb72b-115">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="fb72b-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb72b-116">Tipo di dati: **CIM \_ PhysicalLink**</span><span class="sxs-lookup"><span data-stu-id="fb72b-116">Data type: **CIM\_PhysicalLink**</span></span>
</dt> <dt>

<span data-ttu-id="fb72b-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fb72b-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fb72b-118">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="fb72b-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="fb72b-119">Un [**\_ PhysicalLink CIM**](cim-physicallink.md) che descrive il collegamento fisico.</span><span class="sxs-lookup"><span data-stu-id="fb72b-119">A [**CIM\_PhysicalLink**](cim-physicallink.md) that describes the physical link.</span></span>

</dd> <dt>

<span data-ttu-id="fb72b-120">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="fb72b-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb72b-121">Tipo di dati **: \_ fisico CIM**</span><span class="sxs-lookup"><span data-stu-id="fb72b-121">Data type: **CIM\_PhysicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="fb72b-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fb72b-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fb72b-123">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="fb72b-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="fb72b-124">Oggetto [**\_ fisico CIM**](cim-physicalelement.md) che descrive l'elemento fisico collegato.</span><span class="sxs-lookup"><span data-stu-id="fb72b-124">A [**CIM\_PhysicalElement**](cim-physicalelement.md) that describes the physical element that is linked.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fb72b-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="fb72b-125">Remarks</span></span>

<span data-ttu-id="fb72b-126">La classe **CIM \_ ElementsLinked** è derivata dalla [**\_ dipendenza CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="fb72b-126">The **CIM\_ElementsLinked** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="fb72b-127">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="fb72b-127">WMI does not implement this class.</span></span>

<span data-ttu-id="fb72b-128">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="fb72b-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="fb72b-129">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="fb72b-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb72b-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fb72b-130">Requirements</span></span>



| <span data-ttu-id="fb72b-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb72b-131">Requirement</span></span> | <span data-ttu-id="fb72b-132">Valore</span><span class="sxs-lookup"><span data-stu-id="fb72b-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fb72b-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fb72b-133">Minimum supported client</span></span><br/> | <span data-ttu-id="fb72b-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fb72b-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fb72b-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fb72b-135">Minimum supported server</span></span><br/> | <span data-ttu-id="fb72b-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fb72b-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fb72b-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="fb72b-137">Namespace</span></span><br/>                | <span data-ttu-id="fb72b-138">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="fb72b-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fb72b-139">MOF</span><span class="sxs-lookup"><span data-stu-id="fb72b-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fb72b-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fb72b-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fb72b-141">DLL</span><span class="sxs-lookup"><span data-stu-id="fb72b-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb72b-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb72b-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb72b-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fb72b-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb72b-144">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="fb72b-144">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

