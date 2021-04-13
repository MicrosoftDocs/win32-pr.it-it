---
title: Classe MDM_Policy_Result01_CredentialsUI02
description: La \_ classe CredentialsUI02 dei criteri MDM \_ Result01 \_ rappresenta i criteri di credenziali disponibili.
ms.assetid: d50a4cc5-e87f-44a5-9345-744126615d04
keywords:
- Classe MDM_Policy_Result01_CredentialsUI02
- Classe MDM_Policy_Result01_CredentialsUI02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_CredentialsUI02
- MDM_Policy_Result01_CredentialsUI02.InstanceID
- MDM_Policy_Result01_CredentialsUI02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e444e36f2602fa30ca51601e6cd08e7fa8e30c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475718"
---
# <a name="mdm_policy_result01_credentialsui02-class"></a><span data-ttu-id="55bfd-105">\_ \_ Classe Result01 CredentialsUI02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="55bfd-105">MDM\_Policy\_Result01\_CredentialsUI02 class</span></span>

<span data-ttu-id="55bfd-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="55bfd-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="55bfd-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="55bfd-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="55bfd-108">La \_ classe CredentialsUI02 dei criteri MDM \_ Result01 \_ rappresenta i criteri di credenziali disponibili.</span><span class="sxs-lookup"><span data-stu-id="55bfd-108">The MDM\_Policy\_Result01\_CredentialsUI02 class represents the available credentials policies.</span></span>

<span data-ttu-id="55bfd-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="55bfd-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="55bfd-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="55bfd-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_CredentialsUI02
{
  string InstanceID;
  string ParentID;
  string DisablePasswordReveal;
  string EnumerateAdministrators;
};
```

## <a name="members"></a><span data-ttu-id="55bfd-111">Members</span><span class="sxs-lookup"><span data-stu-id="55bfd-111">Members</span></span>

<span data-ttu-id="55bfd-112">La **classe \_ \_ Result01 \_ CredentialsUI02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="55bfd-112">The **MDM\_Policy\_Result01\_CredentialsUI02** class has these types of members:</span></span>

-   [<span data-ttu-id="55bfd-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="55bfd-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="55bfd-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="55bfd-114">Properties</span></span>

<span data-ttu-id="55bfd-115">La **classe \_ \_ \_ CredentialsUI02 dei criteri MDM Result01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="55bfd-115">The **MDM\_Policy\_Result01\_CredentialsUI02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="55bfd-116">DisablePasswordReveal</span><span class="sxs-lookup"><span data-stu-id="55bfd-116">DisablePasswordReveal</span></span>](/windows/client-management/mdm/policy-csp-credentialsui#credentialsui-disablepasswordreveal)
</dt> <dd> <dl> <dt>

<span data-ttu-id="55bfd-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="55bfd-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55bfd-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="55bfd-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="55bfd-119">EnumerateAdministrators</span><span class="sxs-lookup"><span data-stu-id="55bfd-119">EnumerateAdministrators</span></span>](/windows/client-management/mdm/policy-csp-credentialsui#credentialsui-enumerateadministrators)
</dt> <dd> <dl> <dt>

<span data-ttu-id="55bfd-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="55bfd-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55bfd-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="55bfd-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="55bfd-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="55bfd-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55bfd-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="55bfd-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55bfd-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="55bfd-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55bfd-125">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="55bfd-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="55bfd-126">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="55bfd-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55bfd-127">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="55bfd-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55bfd-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="55bfd-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55bfd-129">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="55bfd-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="55bfd-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="55bfd-130">Requirements</span></span>



| <span data-ttu-id="55bfd-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="55bfd-131">Requirement</span></span> | <span data-ttu-id="55bfd-132">Valore</span><span class="sxs-lookup"><span data-stu-id="55bfd-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55bfd-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="55bfd-133">Minimum supported client</span></span><br/> | <span data-ttu-id="55bfd-134">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="55bfd-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="55bfd-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="55bfd-135">Minimum supported server</span></span><br/> | <span data-ttu-id="55bfd-136">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="55bfd-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="55bfd-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="55bfd-137">Namespace</span></span><br/>                | <span data-ttu-id="55bfd-138">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="55bfd-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="55bfd-139">MOF</span><span class="sxs-lookup"><span data-stu-id="55bfd-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="55bfd-140"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="55bfd-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="55bfd-141">DLL</span><span class="sxs-lookup"><span data-stu-id="55bfd-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55bfd-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55bfd-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

