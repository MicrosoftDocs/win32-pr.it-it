---
description: La \_ classe CIM Statistics rappresenta un'associazione che mette in correlazione gli elementi di sistema gestiti ai gruppi statistici che vi si applicano.
ms.assetid: fc75991b-adcd-4e47-b610-7503f6bb7c03
ms.tgt_platform: multiple
title: Classe CIM_Statistics
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Statistics
- CIM_Statistics.Element
- CIM_Statistics.Stats
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b35299a52c771ee3bcb76673ef1e2164af3b3180
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103965959"
---
# <a name="cim_statistics-class"></a><span data-ttu-id="304e5-103">CIM \_ Statistics (classe)</span><span class="sxs-lookup"><span data-stu-id="304e5-103">CIM\_Statistics class</span></span>

<span data-ttu-id="304e5-104">La classe **CIM \_ Statistics** rappresenta un'associazione che mette in correlazione gli elementi di sistema gestiti ai gruppi statistici che vi si applicano.</span><span class="sxs-lookup"><span data-stu-id="304e5-104">The **CIM\_Statistics** class represents an association that relates managed system elements to the statistical groups that apply to them.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="304e5-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="304e5-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="304e5-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="304e5-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="304e5-107">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="304e5-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="304e5-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="304e5-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="304e5-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="304e5-109">Syntax</span></span>

``` syntax
[Abstract, Association, UUID("{956597A3-7D80-11D2-AAD3-006008C78BC7}"), AMENDMENT]
class CIM_Statistics
{
  CIM_ManagedSystemElement   REF Element;
  CIM_StatisticalInformation REF Stats;
};
```

## <a name="members"></a><span data-ttu-id="304e5-110">Members</span><span class="sxs-lookup"><span data-stu-id="304e5-110">Members</span></span>

<span data-ttu-id="304e5-111">La classe **CIM \_ Statistics** include questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="304e5-111">The **CIM\_Statistics** class has these types of members:</span></span>

-   [<span data-ttu-id="304e5-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="304e5-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="304e5-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="304e5-113">Properties</span></span>

<span data-ttu-id="304e5-114">La classe **CIM \_ Statistics** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="304e5-114">The **CIM\_Statistics** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="304e5-115">**elemento**</span><span class="sxs-lookup"><span data-stu-id="304e5-115">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="304e5-116">Tipo di dati: **CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="304e5-116">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="304e5-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="304e5-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="304e5-118">Riferimento alla classe [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) per la quale vengono definiti i dati statistici o della metrica.</span><span class="sxs-lookup"><span data-stu-id="304e5-118">Reference to the [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) class for which statistical or metric data is defined.</span></span>

</dd> <dt>

<span data-ttu-id="304e5-119">**Statistiche**</span><span class="sxs-lookup"><span data-stu-id="304e5-119">**Stats**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="304e5-120">Tipo di dati: **CIM \_ StatisticalInformation**</span><span class="sxs-lookup"><span data-stu-id="304e5-120">Data type: **CIM\_StatisticalInformation**</span></span>
</dt> <dt>

<span data-ttu-id="304e5-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="304e5-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="304e5-122">Riferimento all'oggetto o alle informazioni statistiche.</span><span class="sxs-lookup"><span data-stu-id="304e5-122">Reference to the statistical information or object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="304e5-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="304e5-123">Remarks</span></span>

<span data-ttu-id="304e5-124">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="304e5-124">WMI does not implement this class.</span></span>

<span data-ttu-id="304e5-125">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="304e5-125">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="304e5-126">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="304e5-126">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="304e5-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="304e5-127">Requirements</span></span>



| <span data-ttu-id="304e5-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="304e5-128">Requirement</span></span> | <span data-ttu-id="304e5-129">Valore</span><span class="sxs-lookup"><span data-stu-id="304e5-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="304e5-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="304e5-130">Minimum supported client</span></span><br/> | <span data-ttu-id="304e5-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="304e5-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="304e5-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="304e5-132">Minimum supported server</span></span><br/> | <span data-ttu-id="304e5-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="304e5-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="304e5-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="304e5-134">Namespace</span></span><br/>                | <span data-ttu-id="304e5-135">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="304e5-135">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="304e5-136">MOF</span><span class="sxs-lookup"><span data-stu-id="304e5-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="304e5-137"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="304e5-137"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="304e5-138">DLL</span><span class="sxs-lookup"><span data-stu-id="304e5-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="304e5-139"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="304e5-139"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




