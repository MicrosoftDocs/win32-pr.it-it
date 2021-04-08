---
title: Classe MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02
description: La \_ \_ \_ classe EnterpriseDataProtection01 RETRIEVEBYTIMERANGE02 di Reporting MDM viene usata per recuperare i log presenti all'interno di StartTime e StopTime.
ms.assetid: 6abec00e-901f-4f79-840d-a4ef3a4d392d
keywords:
- Classe MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02
- Classe MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02, descritta
topic_type:
- apiref
api_name:
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02.InstanceID
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec266e68bbaaafb1f1e3a78fba7ea6b91805096a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047895"
---
# <a name="mdm_reporting_enterprisedataprotection01_retrievebytimerange02-class"></a><span data-ttu-id="f0589-105">MDM \_ Reporting \_ EnterpriseDataProtection01 \_ classe RetrieveByTimeRange02</span><span class="sxs-lookup"><span data-stu-id="f0589-105">MDM\_Reporting\_EnterpriseDataProtection01\_RetrieveByTimeRange02 class</span></span>

<span data-ttu-id="f0589-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="f0589-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="f0589-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="f0589-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="f0589-108">La **classe \_ \_ EnterpriseDataProtection01 \_ RetrieveByTimeRange02 di Reporting MDM** viene usata per recuperare i log presenti all'interno di StartTime e StopTime.</span><span class="sxs-lookup"><span data-stu-id="f0589-108">The **MDM\_Reporting\_EnterpriseDataProtection01\_RetrieveByTimeRange02** class is used to retrieve the logs that exist within the StartTime and StopTime.</span></span> <span data-ttu-id="f0589-109">StartTime e StopTime sono espressi in formato ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="f0589-109">The StartTime and StopTime are expressed in ISO 8601 format.</span></span> <span data-ttu-id="f0589-110">Se i valori di StartTime e StopTime non sono specificati, i valori vengono interpretati come prima esistente o ultima ora esistente.</span><span class="sxs-lookup"><span data-stu-id="f0589-110">If the StartTime and StopTime are not specified, then the values are interpreted as either first existing or last existing time.</span></span>

<span data-ttu-id="f0589-111">Ecco gli altri scenari possibili:</span><span class="sxs-lookup"><span data-stu-id="f0589-111">Here are the other possible scenarios:</span></span>

-   <span data-ttu-id="f0589-112">Se StartTime e StopTime non sono specificati, vengono restituiti tutti i log esistenti.</span><span class="sxs-lookup"><span data-stu-id="f0589-112">If the StartTime and StopTime are not specified, then it returns all existing logs.</span></span>
-   <span data-ttu-id="f0589-113">Se il StopTime è specificato, ma il StartTime non è specificato, vengono restituiti tutti i log esistenti prima di StopTime.</span><span class="sxs-lookup"><span data-stu-id="f0589-113">If the StopTime is specified, but the StartTime is not specified, then all logs that exist before the StopTime are returned.</span></span>
-   <span data-ttu-id="f0589-114">Se viene specificato StartTime, ma StopTime non è specificato, vengono restituiti tutti i log esistenti dall'oggetto StartTime.</span><span class="sxs-lookup"><span data-stu-id="f0589-114">If the StartTime is specified, but the StopTime is not specified, then all that logs that exist from the StartTime are returned.</span></span>

<span data-ttu-id="f0589-115">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="f0589-115">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0589-116">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f0589-116">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02
{
  string InstanceID;
  string ParentID;
  string Logs;
  string StartTime;
  string StopTime;
  sint32 Type;
};
```

## <a name="members"></a><span data-ttu-id="f0589-117">Members</span><span class="sxs-lookup"><span data-stu-id="f0589-117">Members</span></span>

<span data-ttu-id="f0589-118">La **classe \_ \_ EnterpriseDataProtection01 \_ RetrieveByTimeRange02 di Reporting MDM** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f0589-118">The **MDM\_Reporting\_EnterpriseDataProtection01\_RetrieveByTimeRange02** class has these types of members:</span></span>

-   [<span data-ttu-id="f0589-119">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f0589-119">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f0589-120">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f0589-120">Properties</span></span>

<span data-ttu-id="f0589-121">La classe RetrieveByTimeRange02 per la **\_ creazione di report MDM \_ \_ EnterpriseDataProtection01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="f0589-121">The **MDM\_Reporting\_EnterpriseDataProtection01\_RetrieveByTimeRange02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f0589-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f0589-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0589-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f0589-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0589-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f0589-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f0589-125">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f0589-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f0589-126">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="f0589-126">Identifies the name of the parent node.</span></span> <span data-ttu-id="f0589-127">Per questa classe la stringa è "RetrieveByTimeRange".</span><span class="sxs-lookup"><span data-stu-id="f0589-127">For this class, the string is "RetrieveByTimeRange".</span></span>

</dd> <dt>

[<span data-ttu-id="f0589-128">Log</span><span class="sxs-lookup"><span data-stu-id="f0589-128">Logs</span></span>](/windows/client-management/mdm/reporting-csp#logs)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0589-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f0589-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0589-130">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f0589-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f0589-131">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="f0589-131">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0589-132">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f0589-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0589-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f0589-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f0589-134">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f0589-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f0589-135">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="f0589-135">Describes the full path to the parent node.</span></span> <span data-ttu-id="f0589-136">Per questa classe la stringa è "./Vendor/MSFT/EnterpriseDataProtection"</span><span class="sxs-lookup"><span data-stu-id="f0589-136">For this class, the string is "./Vendor/MSFT/EnterpriseDataProtection"</span></span>

</dd> <dt>

[<span data-ttu-id="f0589-137">StartTime</span><span class="sxs-lookup"><span data-stu-id="f0589-137">StartTime</span></span>](/windows/client-management/mdm/reporting-csp#starttime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0589-138">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f0589-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0589-139">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f0589-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f0589-140">StopTime</span><span class="sxs-lookup"><span data-stu-id="f0589-140">StopTime</span></span>](/windows/client-management/mdm/reporting-csp#stoptime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0589-141">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f0589-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0589-142">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f0589-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f0589-143">Tipo</span><span class="sxs-lookup"><span data-stu-id="f0589-143">Type</span></span>](/windows/client-management/mdm/reporting-csp#type)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0589-144">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f0589-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f0589-145">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f0589-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f0589-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f0589-146">Requirements</span></span>



| <span data-ttu-id="f0589-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0589-147">Requirement</span></span> | <span data-ttu-id="f0589-148">Valore</span><span class="sxs-lookup"><span data-stu-id="f0589-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0589-149">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f0589-149">Minimum supported client</span></span><br/> | <span data-ttu-id="f0589-150">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="f0589-150">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="f0589-151">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f0589-151">Minimum supported server</span></span><br/> | <span data-ttu-id="f0589-152">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="f0589-152">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="f0589-153">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f0589-153">Namespace</span></span><br/>                | <span data-ttu-id="f0589-154">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="f0589-154">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="f0589-155">MOF</span><span class="sxs-lookup"><span data-stu-id="f0589-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f0589-156"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f0589-156"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="f0589-157">DLL</span><span class="sxs-lookup"><span data-stu-id="f0589-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f0589-158"><dt>\\DMWmiBridgeProv.dllfile MOF</dt></span><span class="sxs-lookup"><span data-stu-id="f0589-158"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

