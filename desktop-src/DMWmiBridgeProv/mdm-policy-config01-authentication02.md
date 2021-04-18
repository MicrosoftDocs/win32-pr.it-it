---
title: Classe MDM_Policy_Config01_Authentication02
description: La \_ classe Authentication02 dei criteri MDM \_ Config01 \_ rappresenta i criteri di gestione dell'autenticazione disponibili.
ms.assetid: 928e0b60-5533-45dc-90e6-be7d70210138
keywords:
- Classe MDM_Policy_Config01_Authentication02
- Classe MDM_Policy_Config01_Authentication02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Authentication02
- MDM_Policy_Config01_Authentication02.InstanceID
- MDM_Policy_Config01_Authentication02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfab66a548f4a92c445f748aca1bb15758ac48c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301382"
---
# <a name="mdm_policy_config01_authentication02-class"></a><span data-ttu-id="82078-105">\_ \_ Classe Config01 Authentication02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="82078-105">MDM\_Policy\_Config01\_Authentication02 class</span></span>

<span data-ttu-id="82078-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="82078-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="82078-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="82078-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="82078-108">La **classe \_ \_ \_ Authentication02 dei criteri MDM Config01** rappresenta i criteri di gestione dell'autenticazione disponibili.</span><span class="sxs-lookup"><span data-stu-id="82078-108">The **MDM\_Policy\_Config01\_Authentication02** class represents the authentication management policies available.</span></span>

<span data-ttu-id="82078-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="82078-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="82078-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="82078-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Authentication02
{
  string InstanceID;
  string ParentID;
  sint32 AllowAadPasswordReset;
  sint32 AllowFastReconnect;
  sint32 AllowFidoDeviceSignon;
  sint32 AllowSecondaryAuthenticationDevice;
};
```

## <a name="members"></a><span data-ttu-id="82078-111">Members</span><span class="sxs-lookup"><span data-stu-id="82078-111">Members</span></span>

<span data-ttu-id="82078-112">La **classe \_ \_ Config01 \_ Authentication02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="82078-112">The **MDM\_Policy\_Config01\_Authentication02** class has these types of members:</span></span>

-   [<span data-ttu-id="82078-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="82078-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="82078-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="82078-114">Properties</span></span>

<span data-ttu-id="82078-115">La **classe \_ \_ \_ Authentication02 dei criteri MDM Config01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="82078-115">The **MDM\_Policy\_Config01\_Authentication02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="82078-116">AllowAadPasswordReset</span><span class="sxs-lookup"><span data-stu-id="82078-116">AllowAadPasswordReset</span></span>](/windows/client-management/mdm/policy-csp-authentication#authentication-allowaadpasswordreset)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82078-117">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="82078-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="82078-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82078-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82078-119">AllowFastReconnect</span><span class="sxs-lookup"><span data-stu-id="82078-119">AllowFastReconnect</span></span>](/windows/client-management/mdm/policy-csp-authentication#authentication-allowfastreconnect)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82078-120">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="82078-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="82078-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82078-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82078-122">AllowFidoDeviceSignon</span><span class="sxs-lookup"><span data-stu-id="82078-122">AllowFidoDeviceSignon</span></span>](/windows/client-management/mdm/policy-csp-authentication#authentication-allowfidodevicesignon)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82078-123">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="82078-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="82078-124">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82078-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82078-125">AllowSecondaryAuthenticationDevice</span><span class="sxs-lookup"><span data-stu-id="82078-125">AllowSecondaryAuthenticationDevice</span></span>](/windows/client-management/mdm/policy-csp-authentication#authentication-allowsecondaryauthenticationdevice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82078-126">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="82078-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="82078-127">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82078-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="82078-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="82078-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82078-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82078-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82078-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="82078-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="82078-131">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="82078-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="82078-132">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="82078-132">Identifies the name of the parent node.</span></span> <span data-ttu-id="82078-133">Per questa classe la stringa è "Authentication".</span><span class="sxs-lookup"><span data-stu-id="82078-133">For this class, the string is "Authentication".</span></span>

</dd> <dt>

<span data-ttu-id="82078-134">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="82078-134">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82078-135">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82078-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82078-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="82078-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="82078-137">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="82078-137">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="82078-138">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="82078-138">Describes the full path to the parent node.</span></span> <span data-ttu-id="82078-139">Per questa classe la stringa è "./Vendor/MSFT/Policy/Config"</span><span class="sxs-lookup"><span data-stu-id="82078-139">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="82078-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="82078-140">Requirements</span></span>



| <span data-ttu-id="82078-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="82078-141">Requirement</span></span> | <span data-ttu-id="82078-142">Valore</span><span class="sxs-lookup"><span data-stu-id="82078-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82078-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="82078-143">Minimum supported client</span></span><br/> | <span data-ttu-id="82078-144">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="82078-144">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="82078-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="82078-145">Minimum supported server</span></span><br/> | <span data-ttu-id="82078-146">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="82078-146">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="82078-147">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="82078-147">Namespace</span></span><br/>                | <span data-ttu-id="82078-148">\\ \\ DMMap MDM CIMv2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="82078-148">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="82078-149">MOF</span><span class="sxs-lookup"><span data-stu-id="82078-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="82078-150"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="82078-150"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="82078-151">DLL</span><span class="sxs-lookup"><span data-stu-id="82078-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="82078-152"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82078-152"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82078-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="82078-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82078-154">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="82078-154">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

