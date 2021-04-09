---
title: Classe MDM_AppLocker_EnterpriseDataProtection01_EXE03
description: La \_ classe MDM AppLocker \_ EnterpriseDataProtection01 \_ EXE03 acquisisce l'elenco di applicazioni eseguibili a cui è consentito gestire i dati aziendali.
ms.assetid: 43f253d4-3f9d-4651-91b4-b7460706e8b4
keywords:
- Classe MDM_AppLocker_EnterpriseDataProtection01_EXE03
- Classe MDM_AppLocker_EnterpriseDataProtection01_EXE03, descritta
topic_type:
- apiref
api_name:
- MDM_AppLocker_EnterpriseDataProtection01_EXE03
- MDM_AppLocker_EnterpriseDataProtection01_EXE03.InstanceID
- MDM_AppLocker_EnterpriseDataProtection01_EXE03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5b6cbaba46034c26524ca7e12aaa93b588708f2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121418"
---
# <a name="mdm_applocker_enterprisedataprotection01_exe03-class"></a><span data-ttu-id="6f87f-105">MDM \_ AppLocker \_ EnterpriseDataProtection01 \_ classe EXE03</span><span class="sxs-lookup"><span data-stu-id="6f87f-105">MDM\_AppLocker\_EnterpriseDataProtection01\_EXE03 class</span></span>

<span data-ttu-id="6f87f-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="6f87f-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="6f87f-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="6f87f-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="6f87f-108">La classe **MDM \_ AppLocker \_ EnterpriseDataProtection01 \_ EXE03** acquisisce l'elenco di applicazioni eseguibili a cui è consentito gestire i dati aziendali.</span><span class="sxs-lookup"><span data-stu-id="6f87f-108">The **MDM\_AppLocker\_EnterpriseDataProtection01\_EXE03** class captures the list of executable applications that are allowed to handle enterprise data.</span></span> <span data-ttu-id="6f87f-109">Deve essere usato in combinazione con le impostazioni in./Vendor/MSFT/Policy/ConfigSource/DataProtection.</span><span class="sxs-lookup"><span data-stu-id="6f87f-109">Should be used in conjunction with the settings in ./Vendor/MSFT/Policy/ConfigSource/DataProtection .</span></span>

<span data-ttu-id="6f87f-110">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="6f87f-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f87f-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6f87f-111">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_AppLocker_EnterpriseDataProtection01_EXE03
{
  string InstanceID;
  string ParentID;
  string Policy;
};
```

## <a name="members"></a><span data-ttu-id="6f87f-112">Members</span><span class="sxs-lookup"><span data-stu-id="6f87f-112">Members</span></span>

<span data-ttu-id="6f87f-113">La classe **MDM \_ AppLocker \_ EnterpriseDataProtection01 \_ EXE03** include questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="6f87f-113">The **MDM\_AppLocker\_EnterpriseDataProtection01\_EXE03** class has these types of members:</span></span>

-   [<span data-ttu-id="6f87f-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6f87f-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6f87f-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6f87f-115">Properties</span></span>

<span data-ttu-id="6f87f-116">La classe **MDM \_ AppLocker \_ EnterpriseDataProtection01 \_ EXE03** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="6f87f-116">The **MDM\_AppLocker\_EnterpriseDataProtection01\_EXE03** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6f87f-117">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="6f87f-117">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f87f-118">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6f87f-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f87f-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6f87f-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f87f-120">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6f87f-120">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="6f87f-121">Definisce le restrizioni per l'avvio di applicazioni eseguibili.</span><span class="sxs-lookup"><span data-stu-id="6f87f-121">Defines restrictions for launching executable applications.</span></span>

</dd> <dt>

<span data-ttu-id="6f87f-122">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="6f87f-122">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f87f-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6f87f-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f87f-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6f87f-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f87f-125">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6f87f-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="6f87f-126">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="6f87f-126">Describes the full path to the parent node.</span></span> <span data-ttu-id="6f87f-127">Per questa classe la stringa è "*grouping*./Vendor/MSFT/AppLocker/EnterpriseDataProtection/"</span><span class="sxs-lookup"><span data-stu-id="6f87f-127">For this class, the string is "./Vendor/MSFT/AppLocker/EnterpriseDataProtection/*Grouping*"</span></span>

</dd> <dt>

[<span data-ttu-id="6f87f-128">**Criteri**</span><span class="sxs-lookup"><span data-stu-id="6f87f-128">**Policy**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f87f-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6f87f-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f87f-130">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="6f87f-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6f87f-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6f87f-131">Requirements</span></span>



| <span data-ttu-id="6f87f-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f87f-132">Requirement</span></span> | <span data-ttu-id="6f87f-133">Valore</span><span class="sxs-lookup"><span data-stu-id="6f87f-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f87f-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6f87f-134">Minimum supported client</span></span><br/> | <span data-ttu-id="6f87f-135">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="6f87f-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6f87f-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6f87f-136">Minimum supported server</span></span><br/> | <span data-ttu-id="6f87f-137">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="6f87f-137">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="6f87f-138">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6f87f-138">Namespace</span></span><br/>                | <span data-ttu-id="6f87f-139">\\ \\ DMMap MDM CIMv2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="6f87f-139">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="6f87f-140">MOF</span><span class="sxs-lookup"><span data-stu-id="6f87f-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6f87f-141"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6f87f-141"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="6f87f-142">DLL</span><span class="sxs-lookup"><span data-stu-id="6f87f-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f87f-143"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f87f-143"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f87f-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6f87f-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f87f-145">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="6f87f-145">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

