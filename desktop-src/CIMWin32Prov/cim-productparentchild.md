---
description: L' \_ associazione CIM ProductParentChild definisce una gerarchia padre-figlio tra i prodotti. Ad esempio, un prodotto può essere fornito con altri prodotti.
ms.assetid: 244576fd-8dae-4554-b80b-0cac58c93037
ms.tgt_platform: multiple
title: Classe CIM_ProductParentChild
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProductParentChild
- CIM_ProductParentChild.Child
- CIM_ProductParentChild.Parent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3a5fd34cc3dffc6d5c8df7f7a76d9cada7856d57
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523210"
---
# <a name="cim_productparentchild-class"></a><span data-ttu-id="a7329-104">CIM \_ ProductParentChild (classe)</span><span class="sxs-lookup"><span data-stu-id="a7329-104">CIM\_ProductParentChild class</span></span>

<span data-ttu-id="a7329-105">L'associazione **CIM \_ ProductParentChild** definisce una gerarchia padre-figlio tra i prodotti.</span><span class="sxs-lookup"><span data-stu-id="a7329-105">The **CIM\_ProductParentChild** association defines a parent-child hierarchy among products.</span></span> <span data-ttu-id="a7329-106">Ad esempio, un prodotto può essere fornito con altri prodotti.</span><span class="sxs-lookup"><span data-stu-id="a7329-106">For example, a product can come bundled with other products.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a7329-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="a7329-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a7329-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="a7329-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a7329-109">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="a7329-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="a7329-110">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="a7329-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7329-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a7329-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{3E24D5A6-DB2B-11d2-85FC-0000F8102E5F}"), Aggregation, Association, AMENDMENT]
class CIM_ProductParentChild
{
  CIM_Product REF Child;
  CIM_Product REF Parent;
};
```

## <a name="members"></a><span data-ttu-id="a7329-112">Members</span><span class="sxs-lookup"><span data-stu-id="a7329-112">Members</span></span>

<span data-ttu-id="a7329-113">La classe **CIM \_ ProductParentChild** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a7329-113">The **CIM\_ProductParentChild** class has these types of members:</span></span>

-   [<span data-ttu-id="a7329-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a7329-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a7329-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a7329-115">Properties</span></span>

<span data-ttu-id="a7329-116">La classe **CIM \_ ProductParentChild** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="a7329-116">The **CIM\_ProductParentChild** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a7329-117">**Figlio**</span><span class="sxs-lookup"><span data-stu-id="a7329-117">**Child**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7329-118">Tipo di dati **: \_ prodotto CIM**</span><span class="sxs-lookup"><span data-stu-id="a7329-118">Data type: **CIM\_Product**</span></span>
</dt> <dt>

<span data-ttu-id="a7329-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a7329-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7329-120">Riferimento al prodotto figlio nell'associazione.</span><span class="sxs-lookup"><span data-stu-id="a7329-120">Reference to the child product in the association.</span></span>

</dd> <dt>

<span data-ttu-id="a7329-121">**Parent**</span><span class="sxs-lookup"><span data-stu-id="a7329-121">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7329-122">Tipo di dati **: \_ prodotto CIM**</span><span class="sxs-lookup"><span data-stu-id="a7329-122">Data type: **CIM\_Product**</span></span>
</dt> <dt>

<span data-ttu-id="a7329-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a7329-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7329-124">Qualificatori: [ **Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a7329-124">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a7329-125">Riferimento al prodotto padre nell'associazione.</span><span class="sxs-lookup"><span data-stu-id="a7329-125">Reference to the parent product in the association.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a7329-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="a7329-126">Remarks</span></span>

<span data-ttu-id="a7329-127">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="a7329-127">WMI does not implement this class.</span></span>

<span data-ttu-id="a7329-128">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="a7329-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a7329-129">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="a7329-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7329-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a7329-130">Requirements</span></span>



| <span data-ttu-id="a7329-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7329-131">Requirement</span></span> | <span data-ttu-id="a7329-132">Valore</span><span class="sxs-lookup"><span data-stu-id="a7329-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a7329-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a7329-133">Minimum supported client</span></span><br/> | <span data-ttu-id="a7329-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a7329-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a7329-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a7329-135">Minimum supported server</span></span><br/> | <span data-ttu-id="a7329-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a7329-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a7329-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a7329-137">Namespace</span></span><br/>                | <span data-ttu-id="a7329-138">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="a7329-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a7329-139">MOF</span><span class="sxs-lookup"><span data-stu-id="a7329-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a7329-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a7329-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a7329-141">DLL</span><span class="sxs-lookup"><span data-stu-id="a7329-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7329-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7329-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

