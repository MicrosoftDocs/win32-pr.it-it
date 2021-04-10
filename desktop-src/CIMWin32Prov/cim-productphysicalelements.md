---
description: La \_ classe CIM ProductPhysicalElements rappresenta gli elementi fisici che costituiscono un prodotto.
ms.assetid: cf23098a-f61e-4778-883e-1a5138af3da0
ms.tgt_platform: multiple
title: Classe CIM_ProductPhysicalElements
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProductPhysicalElements
- CIM_ProductPhysicalElements.Component
- CIM_ProductPhysicalElements.Product
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a581293426c421de0dd76636a9f446f245f6ab32
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126303"
---
# <a name="cim_productphysicalelements-class"></a><span data-ttu-id="ef5eb-103">CIM \_ ProductPhysicalElements (classe)</span><span class="sxs-lookup"><span data-stu-id="ef5eb-103">CIM\_ProductPhysicalElements class</span></span>

<span data-ttu-id="ef5eb-104">La classe **CIM \_ ProductPhysicalElements** rappresenta gli elementi fisici che costituiscono un prodotto.</span><span class="sxs-lookup"><span data-stu-id="ef5eb-104">The **CIM\_ProductPhysicalElements** class represents the physical elements that make up a product.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ef5eb-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="ef5eb-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ef5eb-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="ef5eb-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="ef5eb-107">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="ef5eb-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="ef5eb-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="ef5eb-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef5eb-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ef5eb-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{502F00A0-DB2B-11d2-85FC-0000F8102E5F}"), Aggregation, Association, AMENDMENT]
class CIM_ProductPhysicalElements
{
  CIM_PhysicalElement REF Component;
  CIM_Product         REF Product;
};
```

## <a name="members"></a><span data-ttu-id="ef5eb-110">Members</span><span class="sxs-lookup"><span data-stu-id="ef5eb-110">Members</span></span>

<span data-ttu-id="ef5eb-111">La classe **CIM \_ ProductPhysicalElements** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ef5eb-111">The **CIM\_ProductPhysicalElements** class has these types of members:</span></span>

-   [<span data-ttu-id="ef5eb-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ef5eb-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ef5eb-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ef5eb-113">Properties</span></span>

<span data-ttu-id="ef5eb-114">La classe **CIM \_ ProductPhysicalElements** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="ef5eb-114">The **CIM\_ProductPhysicalElements** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ef5eb-115">**Componente**</span><span class="sxs-lookup"><span data-stu-id="ef5eb-115">**Component**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef5eb-116">Tipo di dati **: \_ fisico CIM**</span><span class="sxs-lookup"><span data-stu-id="ef5eb-116">Data type: **CIM\_PhysicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="ef5eb-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ef5eb-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef5eb-118">Riferimento all'elemento fisico che fa parte del prodotto.</span><span class="sxs-lookup"><span data-stu-id="ef5eb-118">Reference to the physical element that is part of the product.</span></span>

</dd> <dt>

<span data-ttu-id="ef5eb-119">**Prodotto**</span><span class="sxs-lookup"><span data-stu-id="ef5eb-119">**Product**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef5eb-120">Tipo di dati **: \_ prodotto CIM**</span><span class="sxs-lookup"><span data-stu-id="ef5eb-120">Data type: **CIM\_Product**</span></span>
</dt> <dt>

<span data-ttu-id="ef5eb-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ef5eb-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef5eb-122">Qualificatori: [**aggregato**](/windows/desktop/WmiSdk/standard-qualifiers), [**massimo**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="ef5eb-122">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="ef5eb-123">Riferimento al prodotto.</span><span class="sxs-lookup"><span data-stu-id="ef5eb-123">Reference to the product.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ef5eb-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="ef5eb-124">Remarks</span></span>

<span data-ttu-id="ef5eb-125">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="ef5eb-125">WMI does not implement this class.</span></span>

<span data-ttu-id="ef5eb-126">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="ef5eb-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ef5eb-127">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="ef5eb-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef5eb-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ef5eb-128">Requirements</span></span>



| <span data-ttu-id="ef5eb-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef5eb-129">Requirement</span></span> | <span data-ttu-id="ef5eb-130">Valore</span><span class="sxs-lookup"><span data-stu-id="ef5eb-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ef5eb-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ef5eb-131">Minimum supported client</span></span><br/> | <span data-ttu-id="ef5eb-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ef5eb-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ef5eb-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ef5eb-133">Minimum supported server</span></span><br/> | <span data-ttu-id="ef5eb-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ef5eb-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ef5eb-135">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ef5eb-135">Namespace</span></span><br/>                | <span data-ttu-id="ef5eb-136">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="ef5eb-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ef5eb-137">MOF</span><span class="sxs-lookup"><span data-stu-id="ef5eb-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ef5eb-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ef5eb-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ef5eb-139">DLL</span><span class="sxs-lookup"><span data-stu-id="ef5eb-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef5eb-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef5eb-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

