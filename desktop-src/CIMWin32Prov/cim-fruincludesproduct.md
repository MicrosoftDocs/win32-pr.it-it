---
description: La \_ classe CIM FRUIncludesProduct indica che un'unità sostituibile sul campo (FRU) può essere costituita da altri prodotti.
ms.assetid: e57dc7f5-4c5b-4ec4-9300-e080053955cb
ms.tgt_platform: multiple
title: Classe CIM_FRUIncludesProduct
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FRUIncludesProduct
- CIM_FRUIncludesProduct.Component
- CIM_FRUIncludesProduct.FRU
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 196f0cc1f2e81312e5e695c34e0a492ac7c05389
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104234503"
---
# <a name="cim_fruincludesproduct-class"></a><span data-ttu-id="b19d6-103">CIM \_ FRUIncludesProduct (classe)</span><span class="sxs-lookup"><span data-stu-id="b19d6-103">CIM\_FRUIncludesProduct class</span></span>

<span data-ttu-id="b19d6-104">La classe **CIM \_ FRUIncludesProduct** indica che un'unità sostituibile sul campo (FRU) può essere costituita da altri prodotti.</span><span class="sxs-lookup"><span data-stu-id="b19d6-104">The **CIM\_FRUIncludesProduct** class indicates that a field replaceable unit (FRU) may be composed of other products.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b19d6-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="b19d6-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b19d6-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b19d6-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b19d6-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="b19d6-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="b19d6-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="b19d6-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b19d6-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b19d6-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{87FEEDCA-DB2A-11d2-85FC-0000F8102E5F}"), Aggregation, Association, AMENDMENT]
class CIM_FRUIncludesProduct
{
  CIM_Product REF Component;
  CIM_FRU     REF FRU;
};
```

## <a name="members"></a><span data-ttu-id="b19d6-110">Members</span><span class="sxs-lookup"><span data-stu-id="b19d6-110">Members</span></span>

<span data-ttu-id="b19d6-111">La classe **CIM \_ FRUIncludesProduct** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b19d6-111">The **CIM\_FRUIncludesProduct** class has these types of members:</span></span>

-   [<span data-ttu-id="b19d6-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b19d6-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b19d6-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b19d6-113">Properties</span></span>

<span data-ttu-id="b19d6-114">La classe **CIM \_ FRUIncludesProduct** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="b19d6-114">The **CIM\_FRUIncludesProduct** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b19d6-115">**Componente**</span><span class="sxs-lookup"><span data-stu-id="b19d6-115">**Component**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b19d6-116">Tipo di dati **: \_ prodotto CIM**</span><span class="sxs-lookup"><span data-stu-id="b19d6-116">Data type: **CIM\_Product**</span></span>
</dt> <dt>

<span data-ttu-id="b19d6-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b19d6-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b19d6-118">Riferimento al prodotto che fa parte della FRU.</span><span class="sxs-lookup"><span data-stu-id="b19d6-118">Reference to the product that is a part of the FRU.</span></span>

</dd> <dt>

<span data-ttu-id="b19d6-119">**FRU**</span><span class="sxs-lookup"><span data-stu-id="b19d6-119">**FRU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b19d6-120">Tipo di dati **: \_ FRU CIM**</span><span class="sxs-lookup"><span data-stu-id="b19d6-120">Data type: **CIM\_FRU**</span></span>
</dt> <dt>

<span data-ttu-id="b19d6-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b19d6-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b19d6-122">Qualificatori: [**aggregato**](/windows/desktop/WmiSdk/standard-qualifiers), [**massimo**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="b19d6-122">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="b19d6-123">Riferimento alla FRU.</span><span class="sxs-lookup"><span data-stu-id="b19d6-123">Reference to the FRU.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b19d6-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="b19d6-124">Remarks</span></span>

<span data-ttu-id="b19d6-125">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="b19d6-125">WMI does not implement this class.</span></span>

<span data-ttu-id="b19d6-126">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="b19d6-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b19d6-127">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="b19d6-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b19d6-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b19d6-128">Requirements</span></span>



| <span data-ttu-id="b19d6-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="b19d6-129">Requirement</span></span> | <span data-ttu-id="b19d6-130">Valore</span><span class="sxs-lookup"><span data-stu-id="b19d6-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b19d6-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b19d6-131">Minimum supported client</span></span><br/> | <span data-ttu-id="b19d6-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b19d6-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b19d6-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b19d6-133">Minimum supported server</span></span><br/> | <span data-ttu-id="b19d6-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b19d6-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b19d6-135">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b19d6-135">Namespace</span></span><br/>                | <span data-ttu-id="b19d6-136">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="b19d6-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b19d6-137">MOF</span><span class="sxs-lookup"><span data-stu-id="b19d6-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b19d6-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b19d6-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b19d6-139">DLL</span><span class="sxs-lookup"><span data-stu-id="b19d6-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b19d6-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b19d6-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

