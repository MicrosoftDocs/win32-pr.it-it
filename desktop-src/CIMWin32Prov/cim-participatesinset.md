---
description: La \_ classe CIM ParticipatesInSet identifica gli elementi fisici che devono essere sostituiti insieme.
ms.assetid: 417607a3-6682-4745-a5ca-0538a0d4853d
ms.tgt_platform: multiple
title: Classe CIM_ParticipatesInSet
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ParticipatesInSet
- CIM_ParticipatesInSet.Element
- CIM_ParticipatesInSet.Set
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e1a581452ad6ce032dcb8d3ec5c6c0caa505f7bf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878037"
---
# <a name="cim_participatesinset-class"></a><span data-ttu-id="2ae63-103">CIM \_ ParticipatesInSet (classe)</span><span class="sxs-lookup"><span data-stu-id="2ae63-103">CIM\_ParticipatesInSet class</span></span>

<span data-ttu-id="2ae63-104">La classe **CIM \_ ParticipatesInSet** identifica gli elementi fisici che devono essere sostituiti insieme.</span><span class="sxs-lookup"><span data-stu-id="2ae63-104">The **CIM\_ParticipatesInSet** class identifies physical elements that should be replaced together.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2ae63-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="2ae63-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="2ae63-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="2ae63-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="2ae63-107">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="2ae63-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="2ae63-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="2ae63-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ae63-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2ae63-109">Syntax</span></span>

``` syntax
[Abstract, Association, Aggregation, UUID("{FAF76B6D-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_ParticipatesInSet
{
  CIM_PhysicalElement REF Element;
  CIM_ReplacementSet  REF Set;
};
```

## <a name="members"></a><span data-ttu-id="2ae63-110">Members</span><span class="sxs-lookup"><span data-stu-id="2ae63-110">Members</span></span>

<span data-ttu-id="2ae63-111">La classe **CIM \_ ParticipatesInSet** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="2ae63-111">The **CIM\_ParticipatesInSet** class has these types of members:</span></span>

-   [<span data-ttu-id="2ae63-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2ae63-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2ae63-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2ae63-113">Properties</span></span>

<span data-ttu-id="2ae63-114">La classe **CIM \_ ParticipatesInSet** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="2ae63-114">The **CIM\_ParticipatesInSet** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2ae63-115">**elemento**</span><span class="sxs-lookup"><span data-stu-id="2ae63-115">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ae63-116">Tipo di dati **: \_ fisico CIM**</span><span class="sxs-lookup"><span data-stu-id="2ae63-116">Data type: **CIM\_PhysicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="2ae63-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2ae63-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2ae63-118">Riferimento all'elemento fisico che deve essere sostituito con altri elementi, come un set.</span><span class="sxs-lookup"><span data-stu-id="2ae63-118">Reference to the physical element that should be replaced with other elements, as a set.</span></span>

</dd> <dt>

<span data-ttu-id="2ae63-119">**Set**</span><span class="sxs-lookup"><span data-stu-id="2ae63-119">**Set**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ae63-120">Tipo di dati: **CIM \_ ReplacementSet**</span><span class="sxs-lookup"><span data-stu-id="2ae63-120">Data type: **CIM\_ReplacementSet**</span></span>
</dt> <dt>

<span data-ttu-id="2ae63-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2ae63-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2ae63-122">Qualificatori: [ **Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2ae63-122">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2ae63-123">Riferimento al set di elementi sostitutivi.</span><span class="sxs-lookup"><span data-stu-id="2ae63-123">Reference to the replacement set of elements.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2ae63-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="2ae63-124">Remarks</span></span>

<span data-ttu-id="2ae63-125">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="2ae63-125">WMI does not implement this class.</span></span>

<span data-ttu-id="2ae63-126">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="2ae63-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="2ae63-127">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="2ae63-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ae63-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2ae63-128">Requirements</span></span>



| <span data-ttu-id="2ae63-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ae63-129">Requirement</span></span> | <span data-ttu-id="2ae63-130">Valore</span><span class="sxs-lookup"><span data-stu-id="2ae63-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2ae63-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2ae63-131">Minimum supported client</span></span><br/> | <span data-ttu-id="2ae63-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2ae63-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2ae63-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2ae63-133">Minimum supported server</span></span><br/> | <span data-ttu-id="2ae63-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2ae63-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2ae63-135">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2ae63-135">Namespace</span></span><br/>                | <span data-ttu-id="2ae63-136">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="2ae63-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2ae63-137">MOF</span><span class="sxs-lookup"><span data-stu-id="2ae63-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2ae63-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2ae63-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2ae63-139">DLL</span><span class="sxs-lookup"><span data-stu-id="2ae63-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2ae63-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2ae63-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

