---
title: Classe MDM_Policy_Result01_Authentication02
description: La \_ classe Authentication02 dei criteri MDM \_ Result01 \_ rappresenta i criteri di gestione dell'autenticazione disponibili.
ms.assetid: a67275dc-5f4d-4672-9a6e-84fa65cde3ad
keywords:
- Classe MDM_Policy_Result01_Authentication02
- Classe MDM_Policy_Result01_Authentication02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Authentication02
- MDM_Policy_Result01_Authentication02.InstanceID
- MDM_Policy_Result01_Authentication02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80d80979fe7b025ea7b0677436036c8760d4b0ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121407"
---
# <a name="mdm_policy_result01_authentication02-class"></a><span data-ttu-id="262db-105">\_ \_ Classe Result01 Authentication02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="262db-105">MDM\_Policy\_Result01\_Authentication02 class</span></span>

<span data-ttu-id="262db-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="262db-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="262db-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="262db-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="262db-108">La **classe \_ \_ \_ Authentication02 dei criteri MDM Result01** rappresenta i criteri di gestione dell'autenticazione disponibili.</span><span class="sxs-lookup"><span data-stu-id="262db-108">The **MDM\_Policy\_Result01\_Authentication02** class represents the authentication management policies available.</span></span>

<span data-ttu-id="262db-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="262db-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="262db-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="262db-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Authentication02
{
  string InstanceID;
  string ParentID;
  sint32 AllowAadPasswordReset;
  sint32 AllowFastReconnect;
  sint32 AllowFidoDeviceSignon;
  sint32 AllowSecondaryAuthenticationDevice;
};
```

## <a name="members"></a><span data-ttu-id="262db-111">Members</span><span class="sxs-lookup"><span data-stu-id="262db-111">Members</span></span>

<span data-ttu-id="262db-112">La **classe \_ \_ Result01 \_ Authentication02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="262db-112">The **MDM\_Policy\_Result01\_Authentication02** class has these types of members:</span></span>

-   [<span data-ttu-id="262db-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="262db-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="262db-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="262db-114">Properties</span></span>

<span data-ttu-id="262db-115">La **classe \_ \_ \_ Authentication02 dei criteri MDM Result01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="262db-115">The **MDM\_Policy\_Result01\_Authentication02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="262db-116">AllowAadPasswordReset</span><span class="sxs-lookup"><span data-stu-id="262db-116">AllowAadPasswordReset</span></span>](/windows/client-management/mdm/policy-csp-authentication#authentication-allowaadpasswordreset)
</dt> <dd> <dl> <dt>

<span data-ttu-id="262db-117">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="262db-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="262db-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="262db-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="262db-119">AllowFastReconnect</span><span class="sxs-lookup"><span data-stu-id="262db-119">AllowFastReconnect</span></span>](/windows/client-management/mdm/policy-csp-authentication#authentication-allowfastreconnect)
</dt> <dd> <dl> <dt>

<span data-ttu-id="262db-120">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="262db-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="262db-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="262db-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="262db-122">AllowFidoDeviceSignon</span><span class="sxs-lookup"><span data-stu-id="262db-122">AllowFidoDeviceSignon</span></span>](/windows/client-management/mdm/policy-csp-authentication#authentication-allowfidodevicesignon)
</dt> <dd> <dl> <dt>

<span data-ttu-id="262db-123">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="262db-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="262db-124">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="262db-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="262db-125">AllowSecondaryAuthenticationDevice</span><span class="sxs-lookup"><span data-stu-id="262db-125">AllowSecondaryAuthenticationDevice</span></span>](/windows/client-management/mdm/policy-csp-authentication#authentication-allowsecondaryauthenticationdevice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="262db-126">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="262db-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="262db-127">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="262db-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="262db-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="262db-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="262db-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="262db-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="262db-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="262db-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="262db-131">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="262db-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="262db-132">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="262db-132">Identifies the name of the parent node.</span></span> <span data-ttu-id="262db-133">Per questa classe la stringa è "Authentication".</span><span class="sxs-lookup"><span data-stu-id="262db-133">For this class, the string is "Authentication".</span></span>

</dd> <dt>

<span data-ttu-id="262db-134">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="262db-134">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="262db-135">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="262db-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="262db-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="262db-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="262db-137">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="262db-137">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="262db-138">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="262db-138">Describes the full path to the parent node.</span></span> <span data-ttu-id="262db-139">Per questa classe la stringa è "./Vendor/MSFT/Policy/Result"</span><span class="sxs-lookup"><span data-stu-id="262db-139">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="262db-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="262db-140">Requirements</span></span>



| <span data-ttu-id="262db-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="262db-141">Requirement</span></span> | <span data-ttu-id="262db-142">Valore</span><span class="sxs-lookup"><span data-stu-id="262db-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="262db-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="262db-143">Minimum supported client</span></span><br/> | <span data-ttu-id="262db-144">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="262db-144">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="262db-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="262db-145">Minimum supported server</span></span><br/> | <span data-ttu-id="262db-146">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="262db-146">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="262db-147">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="262db-147">Namespace</span></span><br/>                | <span data-ttu-id="262db-148">\\ \\ DMMap MDM CIMv2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="262db-148">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="262db-149">MOF</span><span class="sxs-lookup"><span data-stu-id="262db-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="262db-150"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="262db-150"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="262db-151">DLL</span><span class="sxs-lookup"><span data-stu-id="262db-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="262db-152"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="262db-152"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="262db-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="262db-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="262db-154">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="262db-154">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

