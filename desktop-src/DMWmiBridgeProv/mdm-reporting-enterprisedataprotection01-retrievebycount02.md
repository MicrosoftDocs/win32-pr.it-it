---
title: Classe MDM_Reporting_EnterpriseDataProtection01_RetrieveByCount02
description: La \_ \_ \_ classe EnterpriseDataProtection01 RETRIEVEBYCOUNT02 di Reporting MDM viene utilizzata per recuperare un numero specificato di log da StartTime.
ms.assetid: 0a581d5a-129b-48c3-a7a1-3947cc1e2ee9
keywords:
- Classe MDM_Reporting_EnterpriseDataProtection01_RetrieveByCount02
- Classe MDM_Reporting_EnterpriseDataProtection01_RetrieveByCount02, descritta
topic_type:
- apiref
api_name:
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByCount02
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByCount02.InstanceID
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByCount02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80fcc6e7ed3ccb630b500179d7273bdd09a21477
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475275"
---
# <a name="mdm_reporting_enterprisedataprotection01_retrievebycount02-class"></a><span data-ttu-id="4669a-105">MDM \_ Reporting \_ EnterpriseDataProtection01 \_ classe RetrieveByCount02</span><span class="sxs-lookup"><span data-stu-id="4669a-105">MDM\_Reporting\_EnterpriseDataProtection01\_RetrieveByCount02 class</span></span>

<span data-ttu-id="4669a-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="4669a-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="4669a-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="4669a-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="4669a-108">La **classe \_ \_ EnterpriseDataProtection01 \_ RetrieveByCount02 di Reporting MDM** viene utilizzata per recuperare un numero specificato di log da StartTime.</span><span class="sxs-lookup"><span data-stu-id="4669a-108">The **MDM\_Reporting\_EnterpriseDataProtection01\_RetrieveByCount02** class is used to retrieve a specified number of logs from the StartTime.</span></span> <span data-ttu-id="4669a-109">Il StartTime è espresso nel formato ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="4669a-109">The StartTime is expressed in ISO 8601 format.</span></span> <span data-ttu-id="4669a-110">È possibile impostare il numero di log necessari impostando LogCount e StartTime.</span><span class="sxs-lookup"><span data-stu-id="4669a-110">You can set the number of logs required by setting LogCount and StartTime.</span></span> <span data-ttu-id="4669a-111">Restituisce il numero specificato di log o meno, se il numero totale di log è inferiore a LogCount.</span><span class="sxs-lookup"><span data-stu-id="4669a-111">It returns the specified number of log or less, if the total number logs is less than LogCount.</span></span>

<span data-ttu-id="4669a-112">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="4669a-112">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4669a-113">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4669a-113">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Reporting_EnterpriseDataProtection01_RetrieveByCount02
{
  string InstanceID;
  string ParentID;
  string Logs;
  sint32 LogCount;
  string StartTime;
  sint32 Type;
};
```

## <a name="members"></a><span data-ttu-id="4669a-114">Members</span><span class="sxs-lookup"><span data-stu-id="4669a-114">Members</span></span>

<span data-ttu-id="4669a-115">La **classe \_ \_ EnterpriseDataProtection01 \_ RetrieveByCount02 di Reporting MDM** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="4669a-115">The **MDM\_Reporting\_EnterpriseDataProtection01\_RetrieveByCount02** class has these types of members:</span></span>

-   [<span data-ttu-id="4669a-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4669a-116">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4669a-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4669a-117">Properties</span></span>

<span data-ttu-id="4669a-118">La classe RetrieveByCount02 per la **\_ creazione di report MDM \_ \_ EnterpriseDataProtection01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="4669a-118">The **MDM\_Reporting\_EnterpriseDataProtection01\_RetrieveByCount02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4669a-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="4669a-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4669a-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4669a-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4669a-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4669a-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4669a-122">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4669a-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="4669a-123">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="4669a-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="4669a-124">Per questa classe la stringa è "RetrieveByCount".</span><span class="sxs-lookup"><span data-stu-id="4669a-124">For this class, the string is "RetrieveByCount".</span></span>

</dd> <dt>

[<span data-ttu-id="4669a-125">LogCount</span><span class="sxs-lookup"><span data-stu-id="4669a-125">LogCount</span></span>](/windows/client-management/mdm/reporting-csp#logcount)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4669a-126">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="4669a-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4669a-127">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4669a-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4669a-128">Log</span><span class="sxs-lookup"><span data-stu-id="4669a-128">Logs</span></span>](/windows/client-management/mdm/reporting-csp#logs)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4669a-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4669a-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4669a-130">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4669a-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4669a-131">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="4669a-131">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4669a-132">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4669a-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4669a-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4669a-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4669a-134">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4669a-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="4669a-135">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="4669a-135">Describes the full path to the parent node.</span></span> <span data-ttu-id="4669a-136">Per questa classe la stringa è "./Vendor/MSFT/EnterpriseDataProtection"</span><span class="sxs-lookup"><span data-stu-id="4669a-136">For this class, the string is "./Vendor/MSFT/EnterpriseDataProtection"</span></span>

</dd> <dt>

[<span data-ttu-id="4669a-137">StartTime</span><span class="sxs-lookup"><span data-stu-id="4669a-137">StartTime</span></span>](/windows/client-management/mdm/reporting-csp#starttime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4669a-138">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4669a-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4669a-139">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4669a-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4669a-140">Tipo</span><span class="sxs-lookup"><span data-stu-id="4669a-140">Type</span></span>](/windows/client-management/mdm/reporting-csp#type)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4669a-141">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="4669a-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4669a-142">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4669a-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4669a-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4669a-143">Requirements</span></span>



| <span data-ttu-id="4669a-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="4669a-144">Requirement</span></span> | <span data-ttu-id="4669a-145">Valore</span><span class="sxs-lookup"><span data-stu-id="4669a-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4669a-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4669a-146">Minimum supported client</span></span><br/> | <span data-ttu-id="4669a-147">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="4669a-147">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="4669a-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4669a-148">Minimum supported server</span></span><br/> | <span data-ttu-id="4669a-149">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="4669a-149">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="4669a-150">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4669a-150">Namespace</span></span><br/>                | <span data-ttu-id="4669a-151">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="4669a-151">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="4669a-152">MOF</span><span class="sxs-lookup"><span data-stu-id="4669a-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4669a-153"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4669a-153"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="4669a-154">DLL</span><span class="sxs-lookup"><span data-stu-id="4669a-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4669a-155"><dt>\\DMWmiBridgeProv.dllfile MOF</dt></span><span class="sxs-lookup"><span data-stu-id="4669a-155"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

