---
title: Classe MDM_AppLocker_ApplicationLaunchRestrictions01_EXE03
description: La \_ classe MDM AppLocker \_ ApplicationLaunchRestrictions01 \_ EXE03 consente di specificare quali applicazioni exe possono essere avviate.
ms.assetid: 27f10b5c-bc3b-4344-afcf-5718ea13e909
keywords:
- Classe MDM_AppLocker_ApplicationLaunchRestrictions01_EXE03
- Classe MDM_AppLocker_ApplicationLaunchRestrictions01_EXE03, descritta
topic_type:
- apiref
api_name:
- MDM_AppLocker_ApplicationLaunchRestrictions01_EXE03
- MDM_AppLocker_ApplicationLaunchRestrictions01_EXE03.InstanceID
- MDM_AppLocker_ApplicationLaunchRestrictions01_EXE03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58aeb86edc21fec974c099fd8d25bd2e3fb244ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873649"
---
# <a name="mdm_applocker_applicationlaunchrestrictions01_exe03-class"></a><span data-ttu-id="824d4-105">MDM \_ AppLocker \_ ApplicationLaunchRestrictions01 \_ classe EXE03</span><span class="sxs-lookup"><span data-stu-id="824d4-105">MDM\_AppLocker\_ApplicationLaunchRestrictions01\_EXE03 class</span></span>

<span data-ttu-id="824d4-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="824d4-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="824d4-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="824d4-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="824d4-108">La classe **MDM \_ AppLocker \_ ApplicationLaunchRestrictions01 \_ EXE03** consente di specificare quali applicazioni exe possono essere avviate.</span><span class="sxs-lookup"><span data-stu-id="824d4-108">The **MDM\_AppLocker\_ApplicationLaunchRestrictions01\_EXE03** class allows you to specify which EXE applications are allowed to launch.</span></span>

<span data-ttu-id="824d4-109">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="824d4-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="824d4-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="824d4-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_AppLocker_ApplicationLaunchRestrictions01_EXE03
{
  string InstanceID;
  string ParentID;
  string Policy;
  string EnforcementMode;
  string NonInteractiveProcessEnforcement;
};
```

## <a name="members"></a><span data-ttu-id="824d4-111">Members</span><span class="sxs-lookup"><span data-stu-id="824d4-111">Members</span></span>

<span data-ttu-id="824d4-112">La classe **MDM \_ AppLocker \_ ApplicationLaunchRestrictions01 \_ EXE03** include questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="824d4-112">The **MDM\_AppLocker\_ApplicationLaunchRestrictions01\_EXE03** class has these types of members:</span></span>

-   [<span data-ttu-id="824d4-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="824d4-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="824d4-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="824d4-114">Properties</span></span>

<span data-ttu-id="824d4-115">La classe **MDM \_ AppLocker \_ ApplicationLaunchRestrictions01 \_ EXE03** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="824d4-115">The **MDM\_AppLocker\_ApplicationLaunchRestrictions01\_EXE03** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="824d4-116">**EnforcementMode**</span><span class="sxs-lookup"><span data-stu-id="824d4-116">**EnforcementMode**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="824d4-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="824d4-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="824d4-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="824d4-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="824d4-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="824d4-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="824d4-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="824d4-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="824d4-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="824d4-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="824d4-122">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="824d4-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="824d4-123">Definisce le restrizioni per l'avvio di applicazioni eseguibili.</span><span class="sxs-lookup"><span data-stu-id="824d4-123">Defines restrictions for launching executable applications.</span></span>

</dd> <dt>

[<span data-ttu-id="824d4-124">**NonInteractiveProcessEnforcement**</span><span class="sxs-lookup"><span data-stu-id="824d4-124">**NonInteractiveProcessEnforcement**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="824d4-125">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="824d4-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="824d4-126">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="824d4-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="824d4-127">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="824d4-127">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="824d4-128">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="824d4-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="824d4-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="824d4-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="824d4-130">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="824d4-130">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="824d4-131">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="824d4-131">Describes the full path to the parent node.</span></span> <span data-ttu-id="824d4-132">Per questa classe la stringa è "*grouping*./Vendor/MSFT/AppLocker/ApplicationLaunchRestrictions/"</span><span class="sxs-lookup"><span data-stu-id="824d4-132">For this class, the string is "./Vendor/MSFT/AppLocker/ApplicationLaunchRestrictions/*Grouping*"</span></span>

</dd> <dt>

[<span data-ttu-id="824d4-133">**Criteri**</span><span class="sxs-lookup"><span data-stu-id="824d4-133">**Policy**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="824d4-134">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="824d4-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="824d4-135">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="824d4-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="824d4-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="824d4-136">Requirements</span></span>



| <span data-ttu-id="824d4-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="824d4-137">Requirement</span></span> | <span data-ttu-id="824d4-138">Valore</span><span class="sxs-lookup"><span data-stu-id="824d4-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="824d4-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="824d4-139">Minimum supported client</span></span><br/> | <span data-ttu-id="824d4-140">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="824d4-140">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="824d4-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="824d4-141">Minimum supported server</span></span><br/> | <span data-ttu-id="824d4-142">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="824d4-142">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="824d4-143">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="824d4-143">Namespace</span></span><br/>                | <span data-ttu-id="824d4-144">\\ \\ DMMap MDM CIMv2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="824d4-144">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="824d4-145">MOF</span><span class="sxs-lookup"><span data-stu-id="824d4-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="824d4-146"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="824d4-146"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="824d4-147">DLL</span><span class="sxs-lookup"><span data-stu-id="824d4-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="824d4-148"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="824d4-148"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="824d4-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="824d4-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="824d4-150">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="824d4-150">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

