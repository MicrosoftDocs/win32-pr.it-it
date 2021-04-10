---
description: L' \_ aggregazione CIM StorageDefect raccoglie gli errori di archiviazione per un extent di archiviazione.
ms.assetid: 7acd3d25-4691-43cb-badc-662684989345
ms.tgt_platform: multiple
title: Classe CIM_StorageDefect
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_StorageDefect
- CIM_StorageDefect.Error
- CIM_StorageDefect.Extent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8e6c2be45fe2f44afa407dc72e3ae90c486593ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966312"
---
# <a name="cim_storagedefect-class"></a><span data-ttu-id="4e166-103">CIM \_ StorageDefect (classe)</span><span class="sxs-lookup"><span data-stu-id="4e166-103">CIM\_StorageDefect class</span></span>

<span data-ttu-id="4e166-104">L'aggregazione **CIM \_ StorageDefect** raccoglie gli errori di archiviazione per un extent di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="4e166-104">The **CIM\_StorageDefect** aggregation collects the storage errors for a storage extent.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4e166-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="4e166-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4e166-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="4e166-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="4e166-107">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="4e166-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="4e166-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="4e166-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e166-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4e166-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{5CC70817-DB31-11d2-85FC-0000F8102E5F}"), Aggregation, Association, AMENDMENT]
class CIM_StorageDefect
{
  CIM_StorageError  REF Error;
  CIM_StorageExtent REF Extent;
};
```

## <a name="members"></a><span data-ttu-id="4e166-110">Members</span><span class="sxs-lookup"><span data-stu-id="4e166-110">Members</span></span>

<span data-ttu-id="4e166-111">La classe **CIM \_ StorageDefect** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="4e166-111">The **CIM\_StorageDefect** class has these types of members:</span></span>

-   [<span data-ttu-id="4e166-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4e166-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4e166-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4e166-113">Properties</span></span>

<span data-ttu-id="4e166-114">La classe **CIM \_ StorageDefect** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="4e166-114">The **CIM\_StorageDefect** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4e166-115">**Error (Errore) (Error (Errore)e)**</span><span class="sxs-lookup"><span data-stu-id="4e166-115">**Error**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e166-116">Tipo di dati: **CIM \_ StorageError**</span><span class="sxs-lookup"><span data-stu-id="4e166-116">Data type: **CIM\_StorageError**</span></span>
</dt> <dt>

<span data-ttu-id="4e166-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4e166-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e166-118">Qualificatori: [ **debole**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="4e166-118">Qualifiers: [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="4e166-119">Riferimento all'oggetto Error, che definisce gli indirizzi iniziale e finale di cui è stato eseguito il mapping dall'extent di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="4e166-119">Reference to the error object, which defines the starting and ending addresses that are mapped out of the storage extent.</span></span>

</dd> <dt>

<span data-ttu-id="4e166-120">**Extent**</span><span class="sxs-lookup"><span data-stu-id="4e166-120">**Extent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e166-121">Tipo di dati: **CIM \_ StorageExtent**</span><span class="sxs-lookup"><span data-stu-id="4e166-121">Data type: **CIM\_StorageExtent**</span></span>
</dt> <dt>

<span data-ttu-id="4e166-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4e166-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e166-123">Qualificatori: [**aggregato**](/windows/desktop/WmiSdk/standard-qualifiers), [**massimo**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="4e166-123">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="4e166-124">Riferimento all'extent di archiviazione in cui si sono verificati gli errori.</span><span class="sxs-lookup"><span data-stu-id="4e166-124">Reference to the storage extent on which the errors occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4e166-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="4e166-125">Remarks</span></span>

<span data-ttu-id="4e166-126">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="4e166-126">WMI does not implement this class.</span></span>

<span data-ttu-id="4e166-127">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="4e166-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4e166-128">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="4e166-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e166-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4e166-129">Requirements</span></span>



| <span data-ttu-id="4e166-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e166-130">Requirement</span></span> | <span data-ttu-id="4e166-131">Valore</span><span class="sxs-lookup"><span data-stu-id="4e166-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e166-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4e166-132">Minimum supported client</span></span><br/> | <span data-ttu-id="4e166-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4e166-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4e166-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4e166-134">Minimum supported server</span></span><br/> | <span data-ttu-id="4e166-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4e166-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4e166-136">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4e166-136">Namespace</span></span><br/>                | <span data-ttu-id="4e166-137">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="4e166-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4e166-138">MOF</span><span class="sxs-lookup"><span data-stu-id="4e166-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4e166-139"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4e166-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4e166-140">DLL</span><span class="sxs-lookup"><span data-stu-id="4e166-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e166-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e166-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

