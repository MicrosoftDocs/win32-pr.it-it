---
title: Classe MDM_Policy_Config01_CredentialProviders02
description: La \_ \_ classe Config01 CredentialProviders02 dei criteri MDM \_ Configura i criteri del provider di credenziali disponibili.
ms.assetid: 84a44fef-1481-4d1d-9531-f2ff6f3b36e6
keywords:
- Classe MDM_Policy_Config01_CredentialProviders02
- Classe MDM_Policy_Config01_CredentialProviders02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_CredentialProviders02
- MDM_Policy_Config01_CredentialProviders02.InstanceID
- MDM_Policy_Config01_CredentialProviders02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c22f77a4ec63a37c71353be43836dd307d5f5293
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476025"
---
# <a name="mdm_policy_config01_credentialproviders02-class"></a><span data-ttu-id="6acea-105">\_ \_ Classe Config01 CredentialProviders02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="6acea-105">MDM\_Policy\_Config01\_CredentialProviders02 class</span></span>

<span data-ttu-id="6acea-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="6acea-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="6acea-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="6acea-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="6acea-108">La \_ \_ classe Config01 CredentialProviders02 dei criteri MDM \_ Configura i criteri del provider di credenziali disponibili.</span><span class="sxs-lookup"><span data-stu-id="6acea-108">The MDM\_Policy\_Config01\_CredentialProviders02 class configures the available credential provider policies.</span></span>

<span data-ttu-id="6acea-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="6acea-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6acea-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6acea-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_CredentialProviders02
{
  string InstanceID;
  string ParentID;
  string AllowPINLogon;
  string BlockPicturePassword;
  sint32 DisableAutomaticReDeploymentCredentials;
};
```

## <a name="members"></a><span data-ttu-id="6acea-111">Members</span><span class="sxs-lookup"><span data-stu-id="6acea-111">Members</span></span>

<span data-ttu-id="6acea-112">La **classe \_ \_ Config01 \_ CredentialProviders02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="6acea-112">The **MDM\_Policy\_Config01\_CredentialProviders02** class has these types of members:</span></span>

-   [<span data-ttu-id="6acea-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6acea-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6acea-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6acea-114">Properties</span></span>

<span data-ttu-id="6acea-115">La **classe \_ \_ \_ CredentialProviders02 dei criteri MDM Config01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="6acea-115">The **MDM\_Policy\_Config01\_CredentialProviders02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="6acea-116">AllowPINLogon</span><span class="sxs-lookup"><span data-stu-id="6acea-116">AllowPINLogon</span></span>](/windows/client-management/mdm/policy-csp-credentialproviders#credentialproviders-allowpinlogon)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6acea-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6acea-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6acea-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="6acea-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6acea-119">BlockPicturePassword</span><span class="sxs-lookup"><span data-stu-id="6acea-119">BlockPicturePassword</span></span>](/windows/client-management/mdm/policy-csp-credentialproviders#credentialproviders-blockpicturepassword)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6acea-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6acea-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6acea-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="6acea-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6acea-122">DisableAutomaticReDeploymentCredentials</span><span class="sxs-lookup"><span data-stu-id="6acea-122">DisableAutomaticReDeploymentCredentials</span></span>](/windows/client-management/mdm/policy-csp-credentialproviders#credentialproviders-disableautomaticredeploymentcredentials)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6acea-123">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="6acea-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6acea-124">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="6acea-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6acea-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="6acea-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6acea-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6acea-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6acea-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6acea-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6acea-128">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6acea-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6acea-129">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="6acea-129">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6acea-130">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6acea-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6acea-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6acea-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6acea-132">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6acea-132">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6acea-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6acea-133">Requirements</span></span>



| <span data-ttu-id="6acea-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="6acea-134">Requirement</span></span> | <span data-ttu-id="6acea-135">Valore</span><span class="sxs-lookup"><span data-stu-id="6acea-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6acea-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6acea-136">Minimum supported client</span></span><br/> | <span data-ttu-id="6acea-137">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="6acea-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6acea-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6acea-138">Minimum supported server</span></span><br/> | <span data-ttu-id="6acea-139">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="6acea-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="6acea-140">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6acea-140">Namespace</span></span><br/>                | <span data-ttu-id="6acea-141">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="6acea-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="6acea-142">MOF</span><span class="sxs-lookup"><span data-stu-id="6acea-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6acea-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6acea-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="6acea-144">DLL</span><span class="sxs-lookup"><span data-stu-id="6acea-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6acea-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6acea-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

