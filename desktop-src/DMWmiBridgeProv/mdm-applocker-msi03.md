---
title: Classe MDM_AppLocker_MSI03
description: La \_ classe MDM AppLocker \_ MSI03 definisce le restrizioni dei criteri per l'elaborazione dei file MSI.
ms.assetid: b7b6602d-38b7-46f0-9542-71228ab0c303
keywords:
- Classe MDM_AppLocker_MSI03
- Classe MDM_AppLocker_MSI03, descritta
topic_type:
- apiref
api_name:
- MDM_AppLocker_MSI03
- MDM_AppLocker_MSI03.InstanceID
- MDM_AppLocker_MSI03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5bd17a979ac0e4a6dcbbc07a38ba72bfd50ede4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743567"
---
# <a name="mdm_applocker_msi03-class"></a><span data-ttu-id="4ca2f-105">MDM \_ AppLocker \_ MSI03 Class</span><span class="sxs-lookup"><span data-stu-id="4ca2f-105">MDM\_AppLocker\_MSI03 class</span></span>

<span data-ttu-id="4ca2f-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="4ca2f-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="4ca2f-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="4ca2f-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="4ca2f-108">La classe **MDM \_ AppLocker \_ MSI03** definisce le restrizioni dei criteri per l'elaborazione dei file MSI.</span><span class="sxs-lookup"><span data-stu-id="4ca2f-108">The **MDM\_AppLocker\_MSI03** class defines the policy restrictions for processing MSI files.</span></span>

<span data-ttu-id="4ca2f-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="4ca2f-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ca2f-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4ca2f-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_AppLocker_MSI03
{
  string InstanceID;
  string ParentID;
  string Policy;
  string EnforcementMode;
};
```

## <a name="members"></a><span data-ttu-id="4ca2f-111">Members</span><span class="sxs-lookup"><span data-stu-id="4ca2f-111">Members</span></span>

<span data-ttu-id="4ca2f-112">I tipi di membri della classe **MDM \_ AppLocker \_ MSI03** sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="4ca2f-112">The **MDM\_AppLocker\_MSI03** class has these types of members:</span></span>

-   [<span data-ttu-id="4ca2f-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4ca2f-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4ca2f-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4ca2f-114">Properties</span></span>

<span data-ttu-id="4ca2f-115">La classe **MDM di \_ AppLocker \_ MSI03** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="4ca2f-115">The **MDM\_AppLocker\_MSI03** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="4ca2f-116">**EnforcementMode**</span><span class="sxs-lookup"><span data-stu-id="4ca2f-116">**EnforcementMode**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ca2f-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4ca2f-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4ca2f-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4ca2f-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4ca2f-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="4ca2f-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ca2f-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4ca2f-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4ca2f-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4ca2f-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4ca2f-122">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4ca2f-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="4ca2f-123">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="4ca2f-123">Identifies the name of the parent node.</span></span>

</dd> <dt>

<span data-ttu-id="4ca2f-124">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="4ca2f-124">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ca2f-125">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4ca2f-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4ca2f-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4ca2f-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4ca2f-127">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4ca2f-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="4ca2f-128">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="4ca2f-128">Describes the full path to the parent node.</span></span> <span data-ttu-id="4ca2f-129">Per questa classe la stringa è "./Vendor/MSFT/AppLocker/ApplicationLaunchRestrictions"</span><span class="sxs-lookup"><span data-stu-id="4ca2f-129">For this class, the string is "./Vendor/MSFT/AppLocker/ApplicationLaunchRestrictions"</span></span>

</dd> <dt>

[<span data-ttu-id="4ca2f-130">**Criteri**</span><span class="sxs-lookup"><span data-stu-id="4ca2f-130">**Policy**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ca2f-131">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4ca2f-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4ca2f-132">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4ca2f-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4ca2f-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4ca2f-133">Requirements</span></span>



| <span data-ttu-id="4ca2f-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ca2f-134">Requirement</span></span> | <span data-ttu-id="4ca2f-135">Valore</span><span class="sxs-lookup"><span data-stu-id="4ca2f-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ca2f-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4ca2f-136">Minimum supported client</span></span><br/> | <span data-ttu-id="4ca2f-137">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="4ca2f-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4ca2f-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4ca2f-138">Minimum supported server</span></span><br/> | <span data-ttu-id="4ca2f-139">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="4ca2f-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="4ca2f-140">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4ca2f-140">Namespace</span></span><br/>                | <span data-ttu-id="4ca2f-141">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="4ca2f-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="4ca2f-142">MOF</span><span class="sxs-lookup"><span data-stu-id="4ca2f-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4ca2f-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4ca2f-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="4ca2f-144">DLL</span><span class="sxs-lookup"><span data-stu-id="4ca2f-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4ca2f-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4ca2f-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ca2f-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4ca2f-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ca2f-147">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="4ca2f-147">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

