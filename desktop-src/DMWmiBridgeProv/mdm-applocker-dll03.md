---
title: Classe MDM_AppLocker_DLL03
description: La \_ classe MDM AppLocker \_ DLL03 definisce le restrizioni dei criteri per l'elaborazione di file dll.
ms.assetid: 956b2ec0-f8a8-41d1-a571-01e73c4cebf9
keywords:
- Classe MDM_AppLocker_DLL03
- Classe MDM_AppLocker_DLL03, descritta
topic_type:
- apiref
api_name:
- MDM_AppLocker_DLL03
- MDM_AppLocker_DLL03.InstanceID
- MDM_AppLocker_DLL03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c332a7d606b21ed9641c3c25f10a011cf7bea6e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302586"
---
# <a name="mdm_applocker_dll03-class"></a><span data-ttu-id="7b553-105">MDM \_ AppLocker \_ DLL03 Class</span><span class="sxs-lookup"><span data-stu-id="7b553-105">MDM\_AppLocker\_DLL03 class</span></span>

<span data-ttu-id="7b553-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="7b553-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="7b553-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="7b553-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="7b553-108">La classe **MDM \_ AppLocker \_ DLL03** definisce le restrizioni dei criteri per l'elaborazione di file dll.</span><span class="sxs-lookup"><span data-stu-id="7b553-108">The **MDM\_AppLocker\_DLL03** class defines the policy restrictions for processing DLL files.</span></span>

<span data-ttu-id="7b553-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="7b553-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b553-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7b553-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_AppLocker_DLL03
{
  string InstanceID;
  string ParentID;
  string Policy;
  string EnforcementMode;
  string NonInteractiveProcessEnforcement;
};
```

## <a name="members"></a><span data-ttu-id="7b553-111">Members</span><span class="sxs-lookup"><span data-stu-id="7b553-111">Members</span></span>

<span data-ttu-id="7b553-112">I tipi di membri della classe **MDM \_ AppLocker \_ DLL03** sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="7b553-112">The **MDM\_AppLocker\_DLL03** class has these types of members:</span></span>

-   [<span data-ttu-id="7b553-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7b553-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7b553-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7b553-114">Properties</span></span>

<span data-ttu-id="7b553-115">La classe **MDM di \_ AppLocker \_ DLL03** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="7b553-115">The **MDM\_AppLocker\_DLL03** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="7b553-116">**EnforcementMode**</span><span class="sxs-lookup"><span data-stu-id="7b553-116">**EnforcementMode**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b553-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7b553-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b553-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="7b553-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7b553-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="7b553-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b553-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7b553-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b553-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7b553-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b553-122">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7b553-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="7b553-123">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="7b553-123">Identifies the name of the parent node.</span></span>

</dd> <dt>

[<span data-ttu-id="7b553-124">**NonInteractiveProcessEnforcement**</span><span class="sxs-lookup"><span data-stu-id="7b553-124">**NonInteractiveProcessEnforcement**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b553-125">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7b553-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b553-126">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="7b553-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7b553-127">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="7b553-127">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b553-128">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7b553-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b553-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7b553-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b553-130">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7b553-130">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="7b553-131">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="7b553-131">Describes the full path to the parent node.</span></span> <span data-ttu-id="7b553-132">Per questa classe la stringa è "./Vendor/MSFT/AppLocker/ApplicationLaunchRestrictions"</span><span class="sxs-lookup"><span data-stu-id="7b553-132">For this class, the string is "./Vendor/MSFT/AppLocker/ApplicationLaunchRestrictions"</span></span>

</dd> <dt>

[<span data-ttu-id="7b553-133">**Criteri**</span><span class="sxs-lookup"><span data-stu-id="7b553-133">**Policy**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b553-134">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7b553-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b553-135">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="7b553-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7b553-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7b553-136">Requirements</span></span>



| <span data-ttu-id="7b553-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b553-137">Requirement</span></span> | <span data-ttu-id="7b553-138">Valore</span><span class="sxs-lookup"><span data-stu-id="7b553-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b553-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7b553-139">Minimum supported client</span></span><br/> | <span data-ttu-id="7b553-140">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="7b553-140">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7b553-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7b553-141">Minimum supported server</span></span><br/> | <span data-ttu-id="7b553-142">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="7b553-142">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="7b553-143">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7b553-143">Namespace</span></span><br/>                | <span data-ttu-id="7b553-144">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="7b553-144">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="7b553-145">MOF</span><span class="sxs-lookup"><span data-stu-id="7b553-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7b553-146"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7b553-146"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="7b553-147">DLL</span><span class="sxs-lookup"><span data-stu-id="7b553-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b553-148"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b553-148"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b553-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7b553-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b553-150">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="7b553-150">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

