---
description: L' \_ associazione CIM JobDestinationJobs descrive la posizione di invio di un processo per l'elaborazione, ovvero la destinazione del processo.
ms.assetid: 6f732d34-2284-4909-a966-6b4066780cb0
ms.tgt_platform: multiple
title: Classe CIM_JobDestinationJobs
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_JobDestinationJobs
- CIM_JobDestinationJobs.Dependent
- CIM_JobDestinationJobs.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4e59e20f776c410db53294b6f6e98a1b13aef0de
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225679"
---
# <a name="cim_jobdestinationjobs-class"></a><span data-ttu-id="5d2cd-103">CIM \_ JobDestinationJobs (classe)</span><span class="sxs-lookup"><span data-stu-id="5d2cd-103">CIM\_JobDestinationJobs class</span></span>

<span data-ttu-id="5d2cd-104">L'associazione **CIM \_ JobDestinationJobs** descrive la posizione di invio di un processo per l'elaborazione, ovvero la destinazione del processo.</span><span class="sxs-lookup"><span data-stu-id="5d2cd-104">The **CIM\_JobDestinationJobs** association describes where a job is submitted for processing (that is, to which job destination).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5d2cd-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="5d2cd-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="5d2cd-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="5d2cd-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="5d2cd-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="5d2cd-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="5d2cd-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="5d2cd-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d2cd-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5d2cd-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8D079BEE-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_JobDestinationJobs : CIM_Dependency
{
  CIM_Job            REF Dependent;
  CIM_JobDestination REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="5d2cd-110">Members</span><span class="sxs-lookup"><span data-stu-id="5d2cd-110">Members</span></span>

<span data-ttu-id="5d2cd-111">La classe **CIM \_ JobDestinationJobs** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="5d2cd-111">The **CIM\_JobDestinationJobs** class has these types of members:</span></span>

-   [<span data-ttu-id="5d2cd-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5d2cd-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5d2cd-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5d2cd-113">Properties</span></span>

<span data-ttu-id="5d2cd-114">La classe **CIM \_ JobDestinationJobs** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="5d2cd-114">The **CIM\_JobDestinationJobs** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5d2cd-115">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="5d2cd-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d2cd-116">Tipo di dati: **CIM \_ JobDestination**</span><span class="sxs-lookup"><span data-stu-id="5d2cd-116">Data type: **CIM\_JobDestination**</span></span>
</dt> <dt>

<span data-ttu-id="5d2cd-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5d2cd-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d2cd-118">Qualificatori: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="5d2cd-118">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="5d2cd-119">Un [**\_ JobDestination CIM**](cim-jobdestination.md) che descrive la destinazione del processo, possibilmente una coda.</span><span class="sxs-lookup"><span data-stu-id="5d2cd-119">A [**CIM\_JobDestination**](cim-jobdestination.md) describing the job destination, possibly a queue.</span></span>

</dd> <dt>

<span data-ttu-id="5d2cd-120">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="5d2cd-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d2cd-121">Tipo di dati **: \_ processo CIM**</span><span class="sxs-lookup"><span data-stu-id="5d2cd-121">Data type: **CIM\_Job**</span></span>
</dt> <dt>

<span data-ttu-id="5d2cd-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5d2cd-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d2cd-123">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="5d2cd-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="5d2cd-124">Un [**\_ processo CIM**](cim-job.md) che descrive il processo che si trova nella coda dei processi o nella destinazione.</span><span class="sxs-lookup"><span data-stu-id="5d2cd-124">A [**CIM\_Job**](cim-job.md) describing the job that is in the job queue/Destination.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5d2cd-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="5d2cd-125">Remarks</span></span>

<span data-ttu-id="5d2cd-126">**CIM \_ JobDestinationJobs** è derivato dalla [**\_ dipendenza CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="5d2cd-126">**CIM\_JobDestinationJobs** is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="5d2cd-127">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="5d2cd-127">WMI does not implement this class.</span></span>

<span data-ttu-id="5d2cd-128">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="5d2cd-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="5d2cd-129">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="5d2cd-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d2cd-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5d2cd-130">Requirements</span></span>



| <span data-ttu-id="5d2cd-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d2cd-131">Requirement</span></span> | <span data-ttu-id="5d2cd-132">Valore</span><span class="sxs-lookup"><span data-stu-id="5d2cd-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5d2cd-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5d2cd-133">Minimum supported client</span></span><br/> | <span data-ttu-id="5d2cd-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5d2cd-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5d2cd-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5d2cd-135">Minimum supported server</span></span><br/> | <span data-ttu-id="5d2cd-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5d2cd-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5d2cd-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5d2cd-137">Namespace</span></span><br/>                | <span data-ttu-id="5d2cd-138">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="5d2cd-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5d2cd-139">MOF</span><span class="sxs-lookup"><span data-stu-id="5d2cd-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5d2cd-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5d2cd-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5d2cd-141">DLL</span><span class="sxs-lookup"><span data-stu-id="5d2cd-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5d2cd-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d2cd-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d2cd-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5d2cd-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d2cd-144">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="5d2cd-144">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

