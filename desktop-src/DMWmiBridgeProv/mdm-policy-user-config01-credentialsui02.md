---
title: Classe MDM_Policy_User_Config01_CredentialsUI02
description: La \_ classe del criterio MDM \_ utente \_ Config01 \_ CredentialsUI02 rappresenta i criteri di credenziali disponibili.
ms.assetid: b0a45070-c25b-4a4d-9fbc-cd107fd0fa2f
keywords:
- Classe MDM_Policy_User_Config01_CredentialsUI02
- Classe MDM_Policy_User_Config01_CredentialsUI02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_User_Config01_CredentialsUI02
- MDM_Policy_User_Config01_CredentialsUI02.InstanceID
- MDM_Policy_User_Config01_CredentialsUI02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 230d0286ac36540b4d0b8506a72a9b4389d37e6e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048584"
---
# <a name="mdm_policy_user_config01_credentialsui02-class"></a><span data-ttu-id="37717-105">\_Utente criteri \_ MDM \_ Config01 \_ classe CredentialsUI02</span><span class="sxs-lookup"><span data-stu-id="37717-105">MDM\_Policy\_User\_Config01\_CredentialsUI02 class</span></span>

<span data-ttu-id="37717-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="37717-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="37717-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="37717-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="37717-108">La \_ classe del criterio MDM \_ utente \_ Config01 \_ CredentialsUI02 rappresenta i criteri di credenziali disponibili.</span><span class="sxs-lookup"><span data-stu-id="37717-108">The MDM\_Policy\_User\_Config01\_CredentialsUI02 class represents the available credentials policies.</span></span>

<span data-ttu-id="37717-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="37717-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="37717-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="37717-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Config01_CredentialsUI02
{
  string InstanceID;
  string ParentID;
  string DisablePasswordReveal;
};
```

## <a name="members"></a><span data-ttu-id="37717-111">Members</span><span class="sxs-lookup"><span data-stu-id="37717-111">Members</span></span>

<span data-ttu-id="37717-112">La **classe \_ \_ \_ Config01 \_ CredentialsUI02 dell'utente dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="37717-112">The **MDM\_Policy\_User\_Config01\_CredentialsUI02** class has these types of members:</span></span>

-   [<span data-ttu-id="37717-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="37717-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="37717-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="37717-114">Properties</span></span>

<span data-ttu-id="37717-115">La **classe \_ \_ \_ Config01 \_ CredentialsUI02 dell'utente dei criteri MDM** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="37717-115">The **MDM\_Policy\_User\_Config01\_CredentialsUI02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="37717-116">DisablePasswordReveal</span><span class="sxs-lookup"><span data-stu-id="37717-116">DisablePasswordReveal</span></span>](/windows/client-management/mdm/policy-csp-credentialsui#credentialsui-disablepasswordreveal)
</dt> <dd> <dl> <dt>

<span data-ttu-id="37717-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="37717-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37717-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="37717-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="37717-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="37717-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37717-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="37717-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37717-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="37717-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37717-122">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="37717-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="37717-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="37717-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37717-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="37717-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37717-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="37717-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37717-126">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="37717-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="37717-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="37717-127">Requirements</span></span>



| <span data-ttu-id="37717-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="37717-128">Requirement</span></span> | <span data-ttu-id="37717-129">Valore</span><span class="sxs-lookup"><span data-stu-id="37717-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37717-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="37717-130">Minimum supported client</span></span><br/> | <span data-ttu-id="37717-131">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="37717-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="37717-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="37717-132">Minimum supported server</span></span><br/> | <span data-ttu-id="37717-133">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="37717-133">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="37717-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="37717-134">Namespace</span></span><br/>                | <span data-ttu-id="37717-135">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="37717-135">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="37717-136">MOF</span><span class="sxs-lookup"><span data-stu-id="37717-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="37717-137"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="37717-137"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="37717-138">DLL</span><span class="sxs-lookup"><span data-stu-id="37717-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37717-139"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37717-139"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

