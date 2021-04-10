---
title: Classe MDM_AppLocker_EnterpriseDataProtection01_StoreApps03
description: La \_ classe MDM AppLocker \_ EnterpriseDataProtection01 \_ StoreApps03 acquisisce l'elenco di app di Windows a cui è consentito gestire i dati aziendali. Deve essere usato in combinazione con le impostazioni in./Vendor/MSFT/Policy/ConfigSource/DataProtection.
ms.assetid: f37fe52d-dbe1-45b7-acd5-5047c46d9bd0
keywords:
- Classe MDM_AppLocker_EnterpriseDataProtection01_StoreApps03
- Classe MDM_AppLocker_EnterpriseDataProtection01_StoreApps03, descritta
topic_type:
- apiref
api_name:
- MDM_AppLocker_EnterpriseDataProtection01_StoreApps03
- MDM_AppLocker_EnterpriseDataProtection01_StoreApps03.InstanceID
- MDM_AppLocker_EnterpriseDataProtection01_StoreApps03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 240f641e542bbbe0c71fd686e2d9df3908b9bab3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964897"
---
# <a name="mdm_applocker_enterprisedataprotection01_storeapps03-class"></a><span data-ttu-id="9b3d9-106">MDM \_ AppLocker \_ EnterpriseDataProtection01 \_ classe StoreApps03</span><span class="sxs-lookup"><span data-stu-id="9b3d9-106">MDM\_AppLocker\_EnterpriseDataProtection01\_StoreApps03 class</span></span>

<span data-ttu-id="9b3d9-107">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="9b3d9-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="9b3d9-108">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="9b3d9-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="9b3d9-109">La classe **MDM \_ AppLocker \_ EnterpriseDataProtection01 \_ StoreApps03** acquisisce l'elenco di app di Windows a cui è consentito gestire i dati aziendali.</span><span class="sxs-lookup"><span data-stu-id="9b3d9-109">The **MDM\_AppLocker\_EnterpriseDataProtection01\_StoreApps03** class captures the list of Windows apps that are allowed to handle enterprise data.</span></span> <span data-ttu-id="9b3d9-110">Deve essere usato in combinazione con le impostazioni in./Vendor/MSFT/Policy/ConfigSource/DataProtection.</span><span class="sxs-lookup"><span data-stu-id="9b3d9-110">Should be used in conjunction with the settings in ./Vendor/MSFT/Policy/ConfigSource/DataProtection .</span></span>

<span data-ttu-id="9b3d9-111">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="9b3d9-111">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b3d9-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9b3d9-112">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_AppLocker_EnterpriseDataProtection01_StoreApps03
{
  string InstanceID;
  string ParentID;
  string Policy;
};
```

## <a name="members"></a><span data-ttu-id="9b3d9-113">Members</span><span class="sxs-lookup"><span data-stu-id="9b3d9-113">Members</span></span>

<span data-ttu-id="9b3d9-114">La classe **MDM \_ AppLocker \_ EnterpriseDataProtection01 \_ StoreApps03** include questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="9b3d9-114">The **MDM\_AppLocker\_EnterpriseDataProtection01\_StoreApps03** class has these types of members:</span></span>

-   [<span data-ttu-id="9b3d9-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9b3d9-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9b3d9-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9b3d9-116">Properties</span></span>

<span data-ttu-id="9b3d9-117">La classe **MDM \_ AppLocker \_ EnterpriseDataProtection01 \_ StoreApps03** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="9b3d9-117">The **MDM\_AppLocker\_EnterpriseDataProtection01\_StoreApps03** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9b3d9-118">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="9b3d9-118">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b3d9-119">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9b3d9-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b3d9-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9b3d9-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b3d9-121">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9b3d9-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9b3d9-122">Definisce le restrizioni per l'esecuzione di app da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="9b3d9-122">Defines restrictions for running apps from the Windows Store.</span></span>

</dd> <dt>

<span data-ttu-id="9b3d9-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="9b3d9-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b3d9-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9b3d9-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b3d9-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9b3d9-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b3d9-126">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9b3d9-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9b3d9-127">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="9b3d9-127">Describes the full path to the parent node.</span></span> <span data-ttu-id="9b3d9-128">Per questa classe la stringa è "*grouping*./Vendor/MSFT/AppLocker/EnterpriseDataProtection/"</span><span class="sxs-lookup"><span data-stu-id="9b3d9-128">For this class, the string is "./Vendor/MSFT/AppLocker/EnterpriseDataProtection/*Grouping*"</span></span>

</dd> <dt>

[<span data-ttu-id="9b3d9-129">**Criteri**</span><span class="sxs-lookup"><span data-stu-id="9b3d9-129">**Policy**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b3d9-130">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9b3d9-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b3d9-131">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9b3d9-131">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9b3d9-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9b3d9-132">Requirements</span></span>



| <span data-ttu-id="9b3d9-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b3d9-133">Requirement</span></span> | <span data-ttu-id="9b3d9-134">Valore</span><span class="sxs-lookup"><span data-stu-id="9b3d9-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b3d9-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9b3d9-135">Minimum supported client</span></span><br/> | <span data-ttu-id="9b3d9-136">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="9b3d9-136">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9b3d9-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9b3d9-137">Minimum supported server</span></span><br/> | <span data-ttu-id="9b3d9-138">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="9b3d9-138">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="9b3d9-139">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9b3d9-139">Namespace</span></span><br/>                | <span data-ttu-id="9b3d9-140">\\ \\ DMMap MDM CIMv2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="9b3d9-140">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="9b3d9-141">MOF</span><span class="sxs-lookup"><span data-stu-id="9b3d9-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9b3d9-142"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9b3d9-142"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="9b3d9-143">DLL</span><span class="sxs-lookup"><span data-stu-id="9b3d9-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b3d9-144"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b3d9-144"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b3d9-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9b3d9-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b3d9-146">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="9b3d9-146">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

