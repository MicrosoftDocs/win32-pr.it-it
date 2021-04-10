---
title: Classe MDM_AppLocker_Script03
description: La \_ classe MDM AppLocker \_ Script03 definisce le restrizioni dei criteri per l'elaborazione di file dll.
ms.assetid: 61fada02-7245-4825-945c-b41e9eff8e74
keywords:
- Classe MDM_AppLocker_Script03
- Classe MDM_AppLocker_Script03, descritta
topic_type:
- apiref
api_name:
- MDM_AppLocker_Script03
- MDM_AppLocker_Script03.InstanceID
- MDM_AppLocker_Script03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 402efedb1e15a0ea0df3dea654328de4ba0ddd86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048734"
---
# <a name="mdm_applocker_script03-class"></a><span data-ttu-id="b33c5-105">MDM \_ AppLocker \_ Script03 Class</span><span class="sxs-lookup"><span data-stu-id="b33c5-105">MDM\_AppLocker\_Script03 class</span></span>

<span data-ttu-id="b33c5-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="b33c5-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b33c5-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="b33c5-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b33c5-108">La classe **MDM \_ AppLocker \_ Script03** definisce le restrizioni dei criteri per l'elaborazione di file dll.</span><span class="sxs-lookup"><span data-stu-id="b33c5-108">The **MDM\_AppLocker\_Script03** class defines the policy restrictions for processing DLL files.</span></span>

<span data-ttu-id="b33c5-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="b33c5-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b33c5-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b33c5-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_AppLocker_Script03
{
  string InstanceID;
  string ParentID;
  string Policy;
  string EnforcementMode;
};
```

## <a name="members"></a><span data-ttu-id="b33c5-111">Members</span><span class="sxs-lookup"><span data-stu-id="b33c5-111">Members</span></span>

<span data-ttu-id="b33c5-112">I tipi di membri della classe **MDM \_ AppLocker \_ Script03** sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="b33c5-112">The **MDM\_AppLocker\_Script03** class has these types of members:</span></span>

-   [<span data-ttu-id="b33c5-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b33c5-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b33c5-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b33c5-114">Properties</span></span>

<span data-ttu-id="b33c5-115">La classe **MDM di \_ AppLocker \_ Script03** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="b33c5-115">The **MDM\_AppLocker\_Script03** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="b33c5-116">**EnforcementMode**</span><span class="sxs-lookup"><span data-stu-id="b33c5-116">**EnforcementMode**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b33c5-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b33c5-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b33c5-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b33c5-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b33c5-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b33c5-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b33c5-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b33c5-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b33c5-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b33c5-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b33c5-122">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b33c5-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b33c5-123">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="b33c5-123">Identifies the name of the parent node.</span></span>

</dd> <dt>

<span data-ttu-id="b33c5-124">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="b33c5-124">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b33c5-125">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b33c5-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b33c5-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b33c5-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b33c5-127">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b33c5-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b33c5-128">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="b33c5-128">Describes the full path to the parent node.</span></span> <span data-ttu-id="b33c5-129">Per questa classe la stringa è "./Vendor/MSFT/AppLocker/ApplicationLaunchRestrictions"</span><span class="sxs-lookup"><span data-stu-id="b33c5-129">For this class, the string is "./Vendor/MSFT/AppLocker/ApplicationLaunchRestrictions"</span></span>

</dd> <dt>

[<span data-ttu-id="b33c5-130">**Criteri**</span><span class="sxs-lookup"><span data-stu-id="b33c5-130">**Policy**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b33c5-131">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b33c5-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b33c5-132">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b33c5-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b33c5-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b33c5-133">Requirements</span></span>



| <span data-ttu-id="b33c5-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="b33c5-134">Requirement</span></span> | <span data-ttu-id="b33c5-135">Valore</span><span class="sxs-lookup"><span data-stu-id="b33c5-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b33c5-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b33c5-136">Minimum supported client</span></span><br/> | <span data-ttu-id="b33c5-137">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="b33c5-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b33c5-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b33c5-138">Minimum supported server</span></span><br/> | <span data-ttu-id="b33c5-139">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="b33c5-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="b33c5-140">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b33c5-140">Namespace</span></span><br/>                | <span data-ttu-id="b33c5-141">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="b33c5-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="b33c5-142">MOF</span><span class="sxs-lookup"><span data-stu-id="b33c5-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b33c5-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b33c5-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="b33c5-144">DLL</span><span class="sxs-lookup"><span data-stu-id="b33c5-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b33c5-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b33c5-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b33c5-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b33c5-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b33c5-147">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="b33c5-147">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

