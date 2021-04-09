---
title: Classe MDM_AppLocker_CodeIntegrity03
description: La \_ classe MDM \_ di AppLocker CodeIntegrity03 definisce i criteri per l'integrità del codice.
ms.assetid: 8e7649b4-2e89-4d79-923e-3767e5b0ea52
keywords:
- Classe MDM_AppLocker_CodeIntegrity03
- Classe MDM_AppLocker_CodeIntegrity03, descritta
topic_type:
- apiref
api_name:
- MDM_AppLocker_CodeIntegrity03
- MDM_AppLocker_CodeIntegrity03.InstanceID
- MDM_AppLocker_CodeIntegrity03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff702f2887f47c1cc5fcebeb4b8ec9a08c450b8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741202"
---
# <a name="mdm_applocker_codeintegrity03-class"></a><span data-ttu-id="9d1ab-105">MDM \_ AppLocker \_ CodeIntegrity03 Class</span><span class="sxs-lookup"><span data-stu-id="9d1ab-105">MDM\_AppLocker\_CodeIntegrity03 class</span></span>

<span data-ttu-id="9d1ab-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="9d1ab-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="9d1ab-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="9d1ab-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="9d1ab-108">La classe **MDM di \_ AppLocker \_ CodeIntegrity03** definisce i criteri per l'integrità del codice.</span><span class="sxs-lookup"><span data-stu-id="9d1ab-108">The **MDM\_AppLocker\_CodeIntegrity03** class defines the policy for Code Integrity.</span></span>

<span data-ttu-id="9d1ab-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="9d1ab-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d1ab-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9d1ab-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_AppLocker_CodeIntegrity03
{
  string InstanceID;
  string ParentID;
  string Policy;
};
```

## <a name="members"></a><span data-ttu-id="9d1ab-111">Members</span><span class="sxs-lookup"><span data-stu-id="9d1ab-111">Members</span></span>

<span data-ttu-id="9d1ab-112">I tipi di membri della classe **MDM \_ AppLocker \_ CodeIntegrity03** sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="9d1ab-112">The **MDM\_AppLocker\_CodeIntegrity03** class has these types of members:</span></span>

-   [<span data-ttu-id="9d1ab-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9d1ab-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9d1ab-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9d1ab-114">Properties</span></span>

<span data-ttu-id="9d1ab-115">La classe **MDM di \_ AppLocker \_ CodeIntegrity03** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="9d1ab-115">The **MDM\_AppLocker\_CodeIntegrity03** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9d1ab-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="9d1ab-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d1ab-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9d1ab-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d1ab-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9d1ab-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d1ab-119">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9d1ab-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9d1ab-120">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="9d1ab-120">Identifies the name of the parent node.</span></span>

</dd> <dt>

<span data-ttu-id="9d1ab-121">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="9d1ab-121">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d1ab-122">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9d1ab-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d1ab-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9d1ab-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d1ab-124">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9d1ab-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9d1ab-125">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="9d1ab-125">Describes the full path to the parent node.</span></span> <span data-ttu-id="9d1ab-126">Per questa classe la stringa è "./Vendor/MSFT/AppLocker/ApplicationLaunchRestrictions"</span><span class="sxs-lookup"><span data-stu-id="9d1ab-126">For this class, the string is "./Vendor/MSFT/AppLocker/ApplicationLaunchRestrictions"</span></span>

</dd> <dt>

[<span data-ttu-id="9d1ab-127">**Criteri**</span><span class="sxs-lookup"><span data-stu-id="9d1ab-127">**Policy**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d1ab-128">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9d1ab-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d1ab-129">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9d1ab-129">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="9d1ab-130">Qualificatori: **OctetString**</span><span class="sxs-lookup"><span data-stu-id="9d1ab-130">Qualifiers: **Octetstring**</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9d1ab-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9d1ab-131">Requirements</span></span>



| <span data-ttu-id="9d1ab-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d1ab-132">Requirement</span></span> | <span data-ttu-id="9d1ab-133">Valore</span><span class="sxs-lookup"><span data-stu-id="9d1ab-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d1ab-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9d1ab-134">Minimum supported client</span></span><br/> | <span data-ttu-id="9d1ab-135">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="9d1ab-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9d1ab-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9d1ab-136">Minimum supported server</span></span><br/> | <span data-ttu-id="9d1ab-137">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="9d1ab-137">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="9d1ab-138">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9d1ab-138">Namespace</span></span><br/>                | <span data-ttu-id="9d1ab-139">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="9d1ab-139">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="9d1ab-140">MOF</span><span class="sxs-lookup"><span data-stu-id="9d1ab-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9d1ab-141"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9d1ab-141"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="9d1ab-142">DLL</span><span class="sxs-lookup"><span data-stu-id="9d1ab-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d1ab-143"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d1ab-143"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d1ab-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9d1ab-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d1ab-145">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="9d1ab-145">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

