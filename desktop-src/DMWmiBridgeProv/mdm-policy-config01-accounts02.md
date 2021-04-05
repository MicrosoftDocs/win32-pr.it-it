---
title: Classe MDM_Policy_Config01_Accounts02
description: La \_ \_ classe Config01 Accounts02 dei criteri MDM rappresenta i \_ criteri correlati agli account.
ms.assetid: 628a0745-0ac5-4038-8ea8-04344098682d
keywords:
- Classe MDM_Policy_Config01_Accounts02
- Classe MDM_Policy_Config01_Accounts02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Accounts02
- MDM_Policy_Config01_Accounts02.InstanceID
- MDM_Policy_Config01_Accounts02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8833f1477014f3c7c2200e07c242549f5235fbdc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048177"
---
# <a name="mdm_policy_config01_accounts02-class"></a><span data-ttu-id="6202d-105">\_ \_ Classe Config01 Accounts02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="6202d-105">MDM\_Policy\_Config01\_Accounts02 class</span></span>

<span data-ttu-id="6202d-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="6202d-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="6202d-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="6202d-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="6202d-108">La **classe \_ \_ Config01 \_ Accounts02 dei criteri MDM** rappresenta i criteri correlati agli account.</span><span class="sxs-lookup"><span data-stu-id="6202d-108">The **MDM\_Policy\_Config01\_Accounts02** class represents policies related to accounts.</span></span>

<span data-ttu-id="6202d-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="6202d-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6202d-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6202d-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Accounts02
{
  string InstanceID;
  string ParentID;
  sint32 AllowMicrosoftAccountConnection;
  sint32 AllowMicrosoftAccountSignInAssistant;
  sint32 AllowAddingNonMicrosoftAccountsManually;
  string DomainNamesForEmailSync;
};
```

## <a name="members"></a><span data-ttu-id="6202d-111">Members</span><span class="sxs-lookup"><span data-stu-id="6202d-111">Members</span></span>

<span data-ttu-id="6202d-112">La **classe \_ \_ Config01 \_ Accounts02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="6202d-112">The **MDM\_Policy\_Config01\_Accounts02** class has these types of members:</span></span>

-   [<span data-ttu-id="6202d-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6202d-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6202d-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6202d-114">Properties</span></span>

<span data-ttu-id="6202d-115">La **classe \_ \_ \_ Accounts02 dei criteri MDM Config01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="6202d-115">The **MDM\_Policy\_Config01\_Accounts02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="6202d-116">AllowAddingNonMicrosoftAccountsManually</span><span class="sxs-lookup"><span data-stu-id="6202d-116">AllowAddingNonMicrosoftAccountsManually</span></span>](/windows/client-management/mdm/policy-csp-accounts#accounts-allowaddingnonmicrosoftaccountsmanually)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6202d-117">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="6202d-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6202d-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="6202d-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6202d-119">AllowMicrosoftAccountConnection</span><span class="sxs-lookup"><span data-stu-id="6202d-119">AllowMicrosoftAccountConnection</span></span>](/windows/client-management/mdm/policy-csp-accounts#accounts-allowmicrosoftaccountconnection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6202d-120">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="6202d-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6202d-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="6202d-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6202d-122">AllowMicrosoftAccountSignInAssistant</span><span class="sxs-lookup"><span data-stu-id="6202d-122">AllowMicrosoftAccountSignInAssistant</span></span>](/windows/client-management/mdm/policy-csp-accounts#accounts-allowmicrosoftaccountsigninassistant)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6202d-123">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="6202d-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6202d-124">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="6202d-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6202d-125">DomainNamesForEmailSync</span><span class="sxs-lookup"><span data-stu-id="6202d-125">DomainNamesForEmailSync</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6202d-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6202d-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6202d-127">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="6202d-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6202d-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="6202d-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6202d-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6202d-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6202d-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6202d-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6202d-131">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6202d-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="6202d-132">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="6202d-132">Identifies the name of the parent node.</span></span> <span data-ttu-id="6202d-133">Per questa classe la stringa è "Accounts".</span><span class="sxs-lookup"><span data-stu-id="6202d-133">For this class, the string is "Accounts".</span></span>

</dd> <dt>

<span data-ttu-id="6202d-134">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="6202d-134">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6202d-135">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6202d-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6202d-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6202d-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6202d-137">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6202d-137">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="6202d-138">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="6202d-138">Describes the full path to the parent node.</span></span> <span data-ttu-id="6202d-139">Per questa classe la stringa è "./Vendor/MSFT/Policy/Config"</span><span class="sxs-lookup"><span data-stu-id="6202d-139">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6202d-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6202d-140">Requirements</span></span>



| <span data-ttu-id="6202d-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="6202d-141">Requirement</span></span> | <span data-ttu-id="6202d-142">Valore</span><span class="sxs-lookup"><span data-stu-id="6202d-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6202d-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6202d-143">Minimum supported client</span></span><br/> | <span data-ttu-id="6202d-144">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="6202d-144">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6202d-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6202d-145">Minimum supported server</span></span><br/> | <span data-ttu-id="6202d-146">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="6202d-146">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="6202d-147">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6202d-147">Namespace</span></span><br/>                | <span data-ttu-id="6202d-148">\\ \\ DMMap MDM CIMv2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="6202d-148">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="6202d-149">MOF</span><span class="sxs-lookup"><span data-stu-id="6202d-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6202d-150"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6202d-150"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="6202d-151">DLL</span><span class="sxs-lookup"><span data-stu-id="6202d-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6202d-152"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6202d-152"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6202d-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6202d-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6202d-154">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="6202d-154">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

