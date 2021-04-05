---
title: Classe MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02
description: La \_ \_ \_ classe SecurityAuditing01 RETRIEVEBYTIMERANGE02 di Reporting MDM viene usata per recuperare i log presenti all'interno di StartTime e StopTime.
ms.assetid: e360bc76-f006-45e1-b78a-29125fbcd5ae
keywords:
- Classe MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02
- Classe MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02, descritta
topic_type:
- apiref
api_name:
- MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02
- MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02.InstanceID
- MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abbbe47dfb3ff23c1d1bd891053375e19d6e503e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740063"
---
# <a name="mdm_reporting_securityauditing01_retrievebytimerange02-class"></a><span data-ttu-id="ac350-105">MDM \_ Reporting \_ SecurityAuditing01 \_ classe RetrieveByTimeRange02</span><span class="sxs-lookup"><span data-stu-id="ac350-105">MDM\_Reporting\_SecurityAuditing01\_RetrieveByTimeRange02 class</span></span>

<span data-ttu-id="ac350-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="ac350-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="ac350-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="ac350-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="ac350-108">La **classe \_ \_ SecurityAuditing01 \_ RetrieveByTimeRange02 di Reporting MDM** viene utilizzata per recuperare i log presenti all'interno di StartTime e StopTime. i StartTime e StopTime sono espressi in formato ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="ac350-108">The **MDM\_Reporting\_SecurityAuditing01\_RetrieveByTimeRange02** class is used to retrieve the logs that exist within the StartTime and StopTime.The StartTime and StopTime are expressed in ISO 8601 format.</span></span> <span data-ttu-id="ac350-109">Se i valori di StartTime e StopTime non sono specificati, i valori vengono interpretati come prima esistente o ultima ora esistente.</span><span class="sxs-lookup"><span data-stu-id="ac350-109">If the StartTime and StopTime are not specified, then the values are interpreted as either first existing or last existing time.</span></span>

<span data-ttu-id="ac350-110">Ecco gli altri scenari possibili:</span><span class="sxs-lookup"><span data-stu-id="ac350-110">Here are the other possible scenarios:</span></span>

-   <span data-ttu-id="ac350-111">Se StartTime e StopTime non sono specificati, vengono restituiti tutti i log esistenti.</span><span class="sxs-lookup"><span data-stu-id="ac350-111">If the StartTime and StopTime are not specified, then it returns all existing logs.</span></span>
-   <span data-ttu-id="ac350-112">Se il StopTime è specificato, ma il StartTime non è specificato, vengono restituiti tutti i log esistenti prima di StopTime.</span><span class="sxs-lookup"><span data-stu-id="ac350-112">If the StopTime is specified, but the StartTime is not specified, then all logs that exist before the StopTime are returned.</span></span>
-   <span data-ttu-id="ac350-113">Se viene specificato StartTime, ma StopTime non è specificato, vengono restituiti tutti i log esistenti dall'oggetto StartTime.</span><span class="sxs-lookup"><span data-stu-id="ac350-113">If the StartTime is specified, but the StopTime is not specified, then all that logs that exist from the StartTime are returned.</span></span>

<span data-ttu-id="ac350-114">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="ac350-114">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac350-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ac350-115">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02
{
  string InstanceID;
  string ParentID;
  string Logs;
  string StartTime;
  string StopTime;
};
```

## <a name="members"></a><span data-ttu-id="ac350-116">Members</span><span class="sxs-lookup"><span data-stu-id="ac350-116">Members</span></span>

<span data-ttu-id="ac350-117">La **classe \_ \_ SecurityAuditing01 \_ RetrieveByTimeRange02 di Reporting MDM** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ac350-117">The **MDM\_Reporting\_SecurityAuditing01\_RetrieveByTimeRange02** class has these types of members:</span></span>

-   [<span data-ttu-id="ac350-118">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ac350-118">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ac350-119">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ac350-119">Properties</span></span>

<span data-ttu-id="ac350-120">La classe RetrieveByTimeRange02 per la **\_ creazione di report MDM \_ \_ SecurityAuditing01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="ac350-120">The **MDM\_Reporting\_SecurityAuditing01\_RetrieveByTimeRange02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ac350-121">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ac350-121">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac350-122">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ac350-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac350-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ac350-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac350-124">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ac350-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ac350-125">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="ac350-125">Identifies the name of the parent node.</span></span> <span data-ttu-id="ac350-126">Per questa classe la stringa è "RetrieveByTimeRange".</span><span class="sxs-lookup"><span data-stu-id="ac350-126">For this class, the string is "RetrieveByTimeRange".</span></span>

</dd> <dt>

[<span data-ttu-id="ac350-127">Log</span><span class="sxs-lookup"><span data-stu-id="ac350-127">Logs</span></span>](/windows/client-management/mdm/reporting-csp#logs)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac350-128">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ac350-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac350-129">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ac350-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ac350-130">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="ac350-130">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac350-131">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ac350-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac350-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ac350-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac350-133">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ac350-133">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ac350-134">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="ac350-134">Describes the full path to the parent node.</span></span> <span data-ttu-id="ac350-135">Per questa classe la stringa è "./Vendor/MSFT/SecurityAuditing"</span><span class="sxs-lookup"><span data-stu-id="ac350-135">For this class, the string is "./Vendor/MSFT/SecurityAuditing"</span></span>

</dd> <dt>

[<span data-ttu-id="ac350-136">StartTime</span><span class="sxs-lookup"><span data-stu-id="ac350-136">StartTime</span></span>](/windows/client-management/mdm/reporting-csp#starttime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac350-137">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ac350-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac350-138">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ac350-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac350-139">StopTime</span><span class="sxs-lookup"><span data-stu-id="ac350-139">StopTime</span></span>](/windows/client-management/mdm/reporting-csp#stoptime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac350-140">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ac350-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac350-141">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ac350-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ac350-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ac350-142">Requirements</span></span>



| <span data-ttu-id="ac350-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac350-143">Requirement</span></span> | <span data-ttu-id="ac350-144">Valore</span><span class="sxs-lookup"><span data-stu-id="ac350-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac350-145">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ac350-145">Minimum supported client</span></span><br/> | <span data-ttu-id="ac350-146">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="ac350-146">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="ac350-147">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ac350-147">Minimum supported server</span></span><br/> | <span data-ttu-id="ac350-148">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="ac350-148">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="ac350-149">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ac350-149">Namespace</span></span><br/>                | <span data-ttu-id="ac350-150">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="ac350-150">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="ac350-151">MOF</span><span class="sxs-lookup"><span data-stu-id="ac350-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ac350-152"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ac350-152"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="ac350-153">DLL</span><span class="sxs-lookup"><span data-stu-id="ac350-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac350-154"><dt>\\DMWmiBridgeProv.dllfile MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ac350-154"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

