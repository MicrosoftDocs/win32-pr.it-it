---
description: La \_ classe CIM FRUPhysicalElements rappresenta gli elementi fisici che costituiscono un'unità sostituibile sul campo (FRU).
ms.assetid: ecdb19a8-5169-4370-8d2d-a21a0021ea5b
ms.tgt_platform: multiple
title: Classe CIM_FRUPhysicalElements
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FRUPhysicalElements
- CIM_FRUPhysicalElements.Component
- CIM_FRUPhysicalElements.FRU
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5c47160b9053a323f693d76f5b84d922c5120992
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966156"
---
# <a name="cim_fruphysicalelements-class"></a><span data-ttu-id="f40f8-103">CIM \_ FRUPhysicalElements (classe)</span><span class="sxs-lookup"><span data-stu-id="f40f8-103">CIM\_FRUPhysicalElements class</span></span>

<span data-ttu-id="f40f8-104">La classe **CIM \_ FRUPhysicalElements** rappresenta gli elementi fisici che costituiscono un'unità sostituibile sul campo (FRU).</span><span class="sxs-lookup"><span data-stu-id="f40f8-104">The **CIM\_FRUPhysicalElements** class represents the physical elements that make up a field replaceable unit (FRU).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f40f8-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="f40f8-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f40f8-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="f40f8-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f40f8-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="f40f8-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="f40f8-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="f40f8-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f40f8-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f40f8-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{977E36CA-DB2A-11d2-85FC-0000F8102E5F}"), Aggregation, Association, AMENDMENT]
class CIM_FRUPhysicalElements
{
  CIM_PhysicalElement REF Component;
  CIM_FRU             REF FRU;
};
```

## <a name="members"></a><span data-ttu-id="f40f8-110">Members</span><span class="sxs-lookup"><span data-stu-id="f40f8-110">Members</span></span>

<span data-ttu-id="f40f8-111">La classe **CIM \_ FRUPhysicalElements** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f40f8-111">The **CIM\_FRUPhysicalElements** class has these types of members:</span></span>

-   [<span data-ttu-id="f40f8-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f40f8-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f40f8-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f40f8-113">Properties</span></span>

<span data-ttu-id="f40f8-114">La classe **CIM \_ FRUPhysicalElements** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="f40f8-114">The **CIM\_FRUPhysicalElements** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f40f8-115">**Componente**</span><span class="sxs-lookup"><span data-stu-id="f40f8-115">**Component**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f40f8-116">Tipo di dati **: \_ fisico CIM**</span><span class="sxs-lookup"><span data-stu-id="f40f8-116">Data type: **CIM\_PhysicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="f40f8-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f40f8-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f40f8-118">Riferimento a un elemento fisico che fa parte della FRU.</span><span class="sxs-lookup"><span data-stu-id="f40f8-118">Reference to a physical element that is a part of the FRU.</span></span>

</dd> <dt>

<span data-ttu-id="f40f8-119">**FRU**</span><span class="sxs-lookup"><span data-stu-id="f40f8-119">**FRU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f40f8-120">Tipo di dati **: \_ FRU CIM**</span><span class="sxs-lookup"><span data-stu-id="f40f8-120">Data type: **CIM\_FRU**</span></span>
</dt> <dt>

<span data-ttu-id="f40f8-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f40f8-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f40f8-122">Qualificatori: [**aggregato**](/windows/desktop/WmiSdk/standard-qualifiers), [**massimo**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="f40f8-122">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="f40f8-123">Riferimento alla FRU.</span><span class="sxs-lookup"><span data-stu-id="f40f8-123">Reference to the FRU.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f40f8-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="f40f8-124">Remarks</span></span>

<span data-ttu-id="f40f8-125">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="f40f8-125">WMI does not implement this class.</span></span>

<span data-ttu-id="f40f8-126">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="f40f8-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f40f8-127">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="f40f8-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f40f8-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f40f8-128">Requirements</span></span>



| <span data-ttu-id="f40f8-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="f40f8-129">Requirement</span></span> | <span data-ttu-id="f40f8-130">Valore</span><span class="sxs-lookup"><span data-stu-id="f40f8-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f40f8-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f40f8-131">Minimum supported client</span></span><br/> | <span data-ttu-id="f40f8-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f40f8-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f40f8-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f40f8-133">Minimum supported server</span></span><br/> | <span data-ttu-id="f40f8-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f40f8-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f40f8-135">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f40f8-135">Namespace</span></span><br/>                | <span data-ttu-id="f40f8-136">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="f40f8-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f40f8-137">MOF</span><span class="sxs-lookup"><span data-stu-id="f40f8-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f40f8-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f40f8-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f40f8-139">DLL</span><span class="sxs-lookup"><span data-stu-id="f40f8-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f40f8-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f40f8-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

