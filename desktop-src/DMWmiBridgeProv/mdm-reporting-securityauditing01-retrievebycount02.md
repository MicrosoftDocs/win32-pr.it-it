---
title: Classe MDM_Reporting_SecurityAuditing01_RetrieveByCount02
description: La \_ \_ \_ classe SecurityAuditing01 RETRIEVEBYCOUNT02 di Reporting MDM viene utilizzata per recuperare un numero specificato di log da StartTime.
ms.assetid: dfa50c04-99d6-4f6a-90ff-70a829bd317d
keywords:
- Classe MDM_Reporting_SecurityAuditing01_RetrieveByCount02
- Classe MDM_Reporting_SecurityAuditing01_RetrieveByCount02, descritta
topic_type:
- apiref
api_name:
- MDM_Reporting_SecurityAuditing01_RetrieveByCount02
- MDM_Reporting_SecurityAuditing01_RetrieveByCount02.InstanceID
- MDM_Reporting_SecurityAuditing01_RetrieveByCount02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c979d25cdc9887a500307494218a6fc11f98bf86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740066"
---
# <a name="mdm_reporting_securityauditing01_retrievebycount02-class"></a><span data-ttu-id="489b7-105">MDM \_ Reporting \_ SecurityAuditing01 \_ classe RetrieveByCount02</span><span class="sxs-lookup"><span data-stu-id="489b7-105">MDM\_Reporting\_SecurityAuditing01\_RetrieveByCount02 class</span></span>

<span data-ttu-id="489b7-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="489b7-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="489b7-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="489b7-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="489b7-108">La [**classe \_ \_ SecurityAuditing01 \_ RetrieveByCount02 di Reporting MDM**](mdm-reporting-enterprisedataprotection01-retrievebycount02.md) viene utilizzata per recuperare un numero specificato di log da StartTime.</span><span class="sxs-lookup"><span data-stu-id="489b7-108">The [**MDM\_Reporting\_SecurityAuditing01\_RetrieveByCount02**](mdm-reporting-enterprisedataprotection01-retrievebycount02.md) class is used to retrieve a specified number of logs from the StartTime.</span></span> <span data-ttu-id="489b7-109">Il StartTime è espresso nel formato ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="489b7-109">The StartTime is expressed in ISO 8601 format.</span></span> <span data-ttu-id="489b7-110">È possibile impostare il numero di log necessari impostando LogCount e StartTime.</span><span class="sxs-lookup"><span data-stu-id="489b7-110">You can set the number of logs required by setting LogCount and StartTime.</span></span> <span data-ttu-id="489b7-111">Restituisce il numero specificato di log o meno, se il numero totale di log è inferiore a LogCount.</span><span class="sxs-lookup"><span data-stu-id="489b7-111">It returns the specified number of log or less, if the total number logs is less than LogCount.</span></span>

<span data-ttu-id="489b7-112">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="489b7-112">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="489b7-113">Sintassi</span><span class="sxs-lookup"><span data-stu-id="489b7-113">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Reporting_SecurityAuditing01_RetrieveByCount02
{
  string InstanceID;
  string ParentID;
  string Logs;
  sint32 LogCount;
  string StartTime;
};
```

## <a name="members"></a><span data-ttu-id="489b7-114">Members</span><span class="sxs-lookup"><span data-stu-id="489b7-114">Members</span></span>

<span data-ttu-id="489b7-115">La **classe \_ \_ SecurityAuditing01 \_ RetrieveByCount02 di Reporting MDM** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="489b7-115">The **MDM\_Reporting\_SecurityAuditing01\_RetrieveByCount02** class has these types of members:</span></span>

-   [<span data-ttu-id="489b7-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="489b7-116">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="489b7-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="489b7-117">Properties</span></span>

<span data-ttu-id="489b7-118">La classe RetrieveByCount02 per la **\_ creazione di report MDM \_ \_ SecurityAuditing01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="489b7-118">The **MDM\_Reporting\_SecurityAuditing01\_RetrieveByCount02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="489b7-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="489b7-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="489b7-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="489b7-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="489b7-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="489b7-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="489b7-122">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="489b7-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="489b7-123">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="489b7-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="489b7-124">Per questa classe la stringa è "RetrieveByCount".</span><span class="sxs-lookup"><span data-stu-id="489b7-124">For this class, the string is "RetrieveByCount".</span></span>

</dd> <dt>

[<span data-ttu-id="489b7-125">LogCount</span><span class="sxs-lookup"><span data-stu-id="489b7-125">LogCount</span></span>](/windows/client-management/mdm/reporting-csp#logcount)
</dt> <dd> <dl> <dt>

<span data-ttu-id="489b7-126">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="489b7-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="489b7-127">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="489b7-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="489b7-128">Log</span><span class="sxs-lookup"><span data-stu-id="489b7-128">Logs</span></span>](/windows/client-management/mdm/reporting-csp#logs)
</dt> <dd> <dl> <dt>

<span data-ttu-id="489b7-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="489b7-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="489b7-130">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="489b7-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="489b7-131">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="489b7-131">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="489b7-132">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="489b7-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="489b7-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="489b7-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="489b7-134">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="489b7-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="489b7-135">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="489b7-135">Describes the full path to the parent node.</span></span> <span data-ttu-id="489b7-136">Per questa classe la stringa è "./Vendor/MSFT/SecurityAuditing"</span><span class="sxs-lookup"><span data-stu-id="489b7-136">For this class, the string is "./Vendor/MSFT/SecurityAuditing"</span></span>

</dd> <dt>

[<span data-ttu-id="489b7-137">StartTime</span><span class="sxs-lookup"><span data-stu-id="489b7-137">StartTime</span></span>](/windows/client-management/mdm/reporting-csp#starttime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="489b7-138">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="489b7-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="489b7-139">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="489b7-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="489b7-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="489b7-140">Requirements</span></span>



| <span data-ttu-id="489b7-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="489b7-141">Requirement</span></span> | <span data-ttu-id="489b7-142">Valore</span><span class="sxs-lookup"><span data-stu-id="489b7-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="489b7-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="489b7-143">Minimum supported client</span></span><br/> | <span data-ttu-id="489b7-144">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="489b7-144">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="489b7-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="489b7-145">Minimum supported server</span></span><br/> | <span data-ttu-id="489b7-146">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="489b7-146">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="489b7-147">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="489b7-147">Namespace</span></span><br/>                | <span data-ttu-id="489b7-148">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="489b7-148">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="489b7-149">MOF</span><span class="sxs-lookup"><span data-stu-id="489b7-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="489b7-150"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="489b7-150"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="489b7-151">DLL</span><span class="sxs-lookup"><span data-stu-id="489b7-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="489b7-152"><dt>\\DMWmiBridgeProv.dllfile MOF</dt></span><span class="sxs-lookup"><span data-stu-id="489b7-152"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

