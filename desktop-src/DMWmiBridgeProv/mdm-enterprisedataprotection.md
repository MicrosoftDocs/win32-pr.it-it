---
title: Classe MDM_EnterpriseDataProtection
description: La \_ classe MDM EnterpriseDataProtection viene utilizzata per determinare lo stato corrente delle impostazioni specifiche di Windows Information Protection (WIP) (precedentemente note come protezione dei dati aziendali).
ms.assetid: 2b97de12-76d1-4b74-a979-f0484807b840
keywords:
- Classe MDM_EnterpriseDataProtection
- Classe MDM_EnterpriseDataProtection, descritta
topic_type:
- apiref
api_name:
- MDM_EnterpriseDataProtection
- MDM_EnterpriseDataProtection.InstanceID
- MDM_EnterpriseDataProtection.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00b4a3a1d9d491b6970ee95a081de8bb240d54d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478064"
---
# <a name="mdm_enterprisedataprotection-class"></a><span data-ttu-id="56440-105">MDM \_ EnterpriseDataProtection (classe)</span><span class="sxs-lookup"><span data-stu-id="56440-105">MDM\_EnterpriseDataProtection class</span></span>

<span data-ttu-id="56440-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="56440-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="56440-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="56440-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="56440-108">La classe **MDM \_ EnterpriseDataProtection** viene utilizzata per determinare lo stato corrente delle impostazioni specifiche di Windows Information Protection (WIP) (precedentemente note come protezione dei dati aziendali).</span><span class="sxs-lookup"><span data-stu-id="56440-108">The **MDM\_EnterpriseDataProtection** class is used to determine the current status of Windows Information Protection (WIP) (formerly known as Enterprise Data Protection) specific settings.</span></span>

<span data-ttu-id="56440-109">Per altre informazioni su WIP, vedere [proteggere i dati aziendali mediante EDP (Enterprise Data Protection)](/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip).</span><span class="sxs-lookup"><span data-stu-id="56440-109">For more information about WIP, see [Protect your enterprise data using enterprise data protection (EDP)](/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip).</span></span>

<span data-ttu-id="56440-110">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="56440-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="56440-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="56440-111">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_EnterpriseDataProtection
{
  string InstanceID;
  string ParentID;
  sint32 Status;
};
```

## <a name="members"></a><span data-ttu-id="56440-112">Members</span><span class="sxs-lookup"><span data-stu-id="56440-112">Members</span></span>

<span data-ttu-id="56440-113">La classe **MDM \_ EnterpriseDataProtection** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="56440-113">The **MDM\_EnterpriseDataProtection** class has these types of members:</span></span>

-   [<span data-ttu-id="56440-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="56440-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="56440-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="56440-115">Properties</span></span>

<span data-ttu-id="56440-116">La classe **MDM \_ EnterpriseDataProtection** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="56440-116">The **MDM\_EnterpriseDataProtection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="56440-117">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="56440-117">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56440-118">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="56440-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56440-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="56440-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56440-120">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="56440-120">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="56440-121">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="56440-121">Identifies the name of the parent node.</span></span> <span data-ttu-id="56440-122">Per questa classe la stringa è "EnterpriseDataProtection".</span><span class="sxs-lookup"><span data-stu-id="56440-122">For this class, the string is "EnterpriseDataProtection".</span></span>

</dd> <dt>

<span data-ttu-id="56440-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="56440-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56440-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="56440-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56440-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="56440-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56440-126">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="56440-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="56440-127">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="56440-127">Describes the full path to the parent node.</span></span> <span data-ttu-id="56440-128">Per questa classe la stringa è "./Vendor/MSFT/"</span><span class="sxs-lookup"><span data-stu-id="56440-128">For this class, the string is "./Vendor/MSFT/"</span></span>

</dd> <dt>

[<span data-ttu-id="56440-129">Status</span><span class="sxs-lookup"><span data-stu-id="56440-129">Status</span></span>](/windows/client-management/mdm/enterprisedataprotection-csp#status)
</dt> <dd> <dl> <dt>

<span data-ttu-id="56440-130">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="56440-130">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="56440-131">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="56440-131">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="56440-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="56440-132">Requirements</span></span>



| <span data-ttu-id="56440-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="56440-133">Requirement</span></span> | <span data-ttu-id="56440-134">Valore</span><span class="sxs-lookup"><span data-stu-id="56440-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56440-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="56440-135">Minimum supported client</span></span><br/> | <span data-ttu-id="56440-136">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="56440-136">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="56440-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="56440-137">Minimum supported server</span></span><br/> | <span data-ttu-id="56440-138">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="56440-138">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="56440-139">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="56440-139">Namespace</span></span><br/>                | <span data-ttu-id="56440-140">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="56440-140">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="56440-141">MOF</span><span class="sxs-lookup"><span data-stu-id="56440-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="56440-142"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="56440-142"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="56440-143">DLL</span><span class="sxs-lookup"><span data-stu-id="56440-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="56440-144"><dt>\\DMWmiBridgeProv.dllfile MOF</dt></span><span class="sxs-lookup"><span data-stu-id="56440-144"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

