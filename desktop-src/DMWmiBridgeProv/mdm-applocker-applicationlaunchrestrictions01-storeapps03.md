---
title: Classe MDM_AppLocker_ApplicationLaunchRestrictions01_StoreApps03
description: La \_ classe MDM AppLocker \_ ApplicationLaunchRestrictions01 \_ StoreApps03 consente di specificare quali applicazioni exe sono consentite o non consentite per la protezione dei dati aziendali.
ms.assetid: de5ceaea-589a-4ed7-8dd6-eb9477d68e0e
keywords:
- Classe MDM_AppLocker_ApplicationLaunchRestrictions01_StoreApps03
- Classe MDM_AppLocker_ApplicationLaunchRestrictions01_StoreApps03, descritta
topic_type:
- apiref
api_name:
- MDM_AppLocker_ApplicationLaunchRestrictions01_StoreApps03
- MDM_AppLocker_ApplicationLaunchRestrictions01_StoreApps03.InstanceID
- MDM_AppLocker_ApplicationLaunchRestrictions01_StoreApps03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54c58610c10e672a6fbc1406b2d022b8ce211871
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301472"
---
# <a name="mdm_applocker_applicationlaunchrestrictions01_storeapps03-class"></a><span data-ttu-id="5a6f6-105">MDM \_ AppLocker \_ ApplicationLaunchRestrictions01 \_ classe StoreApps03</span><span class="sxs-lookup"><span data-stu-id="5a6f6-105">MDM\_AppLocker\_ApplicationLaunchRestrictions01\_StoreApps03 class</span></span>

<span data-ttu-id="5a6f6-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="5a6f6-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="5a6f6-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="5a6f6-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="5a6f6-108">La classe **MDM \_ AppLocker \_ ApplicationLaunchRestrictions01 \_ StoreApps03** consente di specificare quali applicazioni exe sono consentite o non consentite per la protezione dei dati aziendali.</span><span class="sxs-lookup"><span data-stu-id="5a6f6-108">The **MDM\_AppLocker\_ApplicationLaunchRestrictions01\_StoreApps03** class allows you to specify which EXE applications are allowed or disallowed for Enterprise Data Protection.</span></span>

<span data-ttu-id="5a6f6-109">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="5a6f6-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a6f6-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5a6f6-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_AppLocker_ApplicationLaunchRestrictions01_StoreApps03
{
  string InstanceID;
  string ParentID;
  string Policy;
  string EnforcementMode;
};
```

## <a name="members"></a><span data-ttu-id="5a6f6-111">Members</span><span class="sxs-lookup"><span data-stu-id="5a6f6-111">Members</span></span>

<span data-ttu-id="5a6f6-112">La classe **MDM \_ AppLocker \_ ApplicationLaunchRestrictions01 \_ StoreApps03** include questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="5a6f6-112">The **MDM\_AppLocker\_ApplicationLaunchRestrictions01\_StoreApps03** class has these types of members:</span></span>

-   [<span data-ttu-id="5a6f6-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5a6f6-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5a6f6-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5a6f6-114">Properties</span></span>

<span data-ttu-id="5a6f6-115">La classe **MDM \_ AppLocker \_ ApplicationLaunchRestrictions01 \_ StoreApps03** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="5a6f6-115">The **MDM\_AppLocker\_ApplicationLaunchRestrictions01\_StoreApps03** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="5a6f6-116">**EnforcementMode**</span><span class="sxs-lookup"><span data-stu-id="5a6f6-116">**EnforcementMode**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a6f6-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5a6f6-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a6f6-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5a6f6-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5a6f6-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="5a6f6-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a6f6-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5a6f6-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a6f6-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5a6f6-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a6f6-122">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5a6f6-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5a6f6-123">Definisce le restrizioni per l'esecuzione di app da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="5a6f6-123">Defines restrictions for running apps from the Windows Store.</span></span>

</dd> <dt>

<span data-ttu-id="5a6f6-124">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="5a6f6-124">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a6f6-125">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5a6f6-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a6f6-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5a6f6-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a6f6-127">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5a6f6-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5a6f6-128">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="5a6f6-128">Describes the full path to the parent node.</span></span> <span data-ttu-id="5a6f6-129">Per questa classe la stringa è "*grouping*./Vendor/MSFT/AppLocker/ApplicationLaunchRestrictions/"</span><span class="sxs-lookup"><span data-stu-id="5a6f6-129">For this class, the string is "./Vendor/MSFT/AppLocker/ApplicationLaunchRestrictions/*Grouping*"</span></span>

</dd> <dt>

[<span data-ttu-id="5a6f6-130">**Criteri**</span><span class="sxs-lookup"><span data-stu-id="5a6f6-130">**Policy**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a6f6-131">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5a6f6-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a6f6-132">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5a6f6-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5a6f6-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5a6f6-133">Requirements</span></span>



| <span data-ttu-id="5a6f6-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a6f6-134">Requirement</span></span> | <span data-ttu-id="5a6f6-135">Valore</span><span class="sxs-lookup"><span data-stu-id="5a6f6-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a6f6-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5a6f6-136">Minimum supported client</span></span><br/> | <span data-ttu-id="5a6f6-137">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="5a6f6-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5a6f6-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5a6f6-138">Minimum supported server</span></span><br/> | <span data-ttu-id="5a6f6-139">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="5a6f6-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="5a6f6-140">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5a6f6-140">Namespace</span></span><br/>                | <span data-ttu-id="5a6f6-141">\\ \\ DMMap MDM CIMv2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="5a6f6-141">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="5a6f6-142">MOF</span><span class="sxs-lookup"><span data-stu-id="5a6f6-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5a6f6-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5a6f6-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="5a6f6-144">DLL</span><span class="sxs-lookup"><span data-stu-id="5a6f6-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a6f6-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a6f6-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a6f6-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5a6f6-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a6f6-147">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="5a6f6-147">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

