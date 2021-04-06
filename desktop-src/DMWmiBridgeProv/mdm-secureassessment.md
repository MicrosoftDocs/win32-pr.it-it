---
title: Classe MDM_SecureAssessment
description: Il \_ SECUREASSESSMENTCLASS MDM viene usato per fornire informazioni di configurazione per il browser di valutazione sicura.
ms.assetid: ad456f01-c77d-428b-a8bf-03e9ae106e60
keywords:
- Classe MDM_SecureAssessment
- Classe MDM_SecureAssessment, descritta
topic_type:
- apiref
api_name:
- MDM_SecureAssessment
- MDM_SecureAssessment.InstanceID
- MDM_SecureAssessment.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: deef2c8ee832a54775ae9dd51d85414a607ca8b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963789"
---
# <a name="mdm_secureassessment-class"></a><span data-ttu-id="c596b-105">MDM \_ SecureAssessment (classe)</span><span class="sxs-lookup"><span data-stu-id="c596b-105">MDM\_SecureAssessment class</span></span>

<span data-ttu-id="c596b-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="c596b-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="c596b-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="c596b-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="c596b-108">La classe **MDM \_ SecureAssessment** viene utilizzata per fornire informazioni di configurazione per il browser Secure assessment.</span><span class="sxs-lookup"><span data-stu-id="c596b-108">The **MDM\_SecureAssessment** class is used to provide configuration information for the secure assessment browser.</span></span>

<span data-ttu-id="c596b-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="c596b-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c596b-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c596b-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_SecureAssessment
{
  string  InstanceID;
  string  ParentID;
  string  LaunchURI;
  string  TesterAccount;
  boolean AllowTextSuggestions;
  boolean RequirePrinting;
  boolean AllowScreenMonitoring;
};
```

## <a name="members"></a><span data-ttu-id="c596b-111">Members</span><span class="sxs-lookup"><span data-stu-id="c596b-111">Members</span></span>

<span data-ttu-id="c596b-112">La classe **MDM \_ SecureAssessment** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="c596b-112">The **MDM\_SecureAssessment** class has these types of members:</span></span>

-   [<span data-ttu-id="c596b-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c596b-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c596b-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c596b-114">Properties</span></span>

<span data-ttu-id="c596b-115">La classe **MDM \_ SecureAssessment** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="c596b-115">The **MDM\_SecureAssessment** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="c596b-116">AllowScreenMonitoring</span><span class="sxs-lookup"><span data-stu-id="c596b-116">AllowScreenMonitoring</span></span>](/windows/client-management/mdm/secureassessment-csp#allowscreenmonitoring)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c596b-117">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="c596b-117">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c596b-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="c596b-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c596b-119">AllowTextSuggestions</span><span class="sxs-lookup"><span data-stu-id="c596b-119">AllowTextSuggestions</span></span>](/windows/client-management/mdm/secureassessment-csp#AllowTextSuggestions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c596b-120">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="c596b-120">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c596b-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="c596b-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c596b-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c596b-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c596b-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c596b-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c596b-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c596b-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c596b-125">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c596b-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c596b-126">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="c596b-126">Identifies the name of the parent node.</span></span> <span data-ttu-id="c596b-127">Per questa classe la stringa è "SecureAssessment".</span><span class="sxs-lookup"><span data-stu-id="c596b-127">For this class, the string is "SecureAssessment".</span></span>

</dd> <dt>

[<span data-ttu-id="c596b-128">LaunchURI</span><span class="sxs-lookup"><span data-stu-id="c596b-128">LaunchURI</span></span>](/windows/client-management/mdm/secureassessment-csp#launchuri)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c596b-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c596b-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c596b-130">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="c596b-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c596b-131">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="c596b-131">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c596b-132">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c596b-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c596b-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c596b-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c596b-134">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c596b-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c596b-135">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="c596b-135">Describes the full path to the parent node.</span></span> <span data-ttu-id="c596b-136">Per questa classe la stringa è "./Vendor/MSFT/"</span><span class="sxs-lookup"><span data-stu-id="c596b-136">For this class, the string is "./Vendor/MSFT/"</span></span>

</dd> <dt>

[<span data-ttu-id="c596b-137">RequirePrinting</span><span class="sxs-lookup"><span data-stu-id="c596b-137">RequirePrinting</span></span>](/windows/client-management/mdm/secureassessment-csp#requireprinting)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c596b-138">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="c596b-138">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c596b-139">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="c596b-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c596b-140">TesterAccount</span><span class="sxs-lookup"><span data-stu-id="c596b-140">TesterAccount</span></span>](/windows/client-management/mdm/secureassessment-csp#testeraccount)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c596b-141">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c596b-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c596b-142">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="c596b-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c596b-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c596b-143">Requirements</span></span>



| <span data-ttu-id="c596b-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="c596b-144">Requirement</span></span> | <span data-ttu-id="c596b-145">Valore</span><span class="sxs-lookup"><span data-stu-id="c596b-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c596b-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c596b-146">Minimum supported client</span></span><br/> | <span data-ttu-id="c596b-147">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="c596b-147">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="c596b-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c596b-148">Minimum supported server</span></span><br/> | <span data-ttu-id="c596b-149">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="c596b-149">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="c596b-150">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c596b-150">Namespace</span></span><br/>                | <span data-ttu-id="c596b-151">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="c596b-151">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="c596b-152">MOF</span><span class="sxs-lookup"><span data-stu-id="c596b-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c596b-153"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c596b-153"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="c596b-154">DLL</span><span class="sxs-lookup"><span data-stu-id="c596b-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c596b-155"><dt>\\DMWmiBridgeProv.dllfile MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c596b-155"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

