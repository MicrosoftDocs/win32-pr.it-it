---
title: Classe MDM_Policy_Config01_Cryptography02
description: La \_ \_ classe Config01 Cryptography02 dei criteri MDM rappresenta i \_ criteri correlati alla crittografia.
ms.assetid: e1e06dbd-507e-4da5-bcd5-4d551bd99302
keywords:
- Classe MDM_Policy_Config01_Cryptography02
- Classe MDM_Policy_Config01_Cryptography02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Cryptography02
- MDM_Policy_Config01_Cryptography02.InstanceID
- MDM_Policy_Config01_Cryptography02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92f13a5a04e3d312d8ba262359847719652ecc4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476019"
---
# <a name="mdm_policy_config01_cryptography02-class"></a><span data-ttu-id="f3824-105">\_ \_ Classe Config01 Cryptography02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="f3824-105">MDM\_Policy\_Config01\_Cryptography02 class</span></span>

<span data-ttu-id="f3824-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="f3824-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="f3824-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="f3824-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="f3824-108">La **classe \_ \_ Config01 \_ Cryptography02 dei criteri MDM** rappresenta i criteri correlati alla crittografia.</span><span class="sxs-lookup"><span data-stu-id="f3824-108">The **MDM\_Policy\_Config01\_Cryptography02** class represents policies related to cryptography.</span></span>

<span data-ttu-id="f3824-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="f3824-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3824-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f3824-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Cryptography02
{
  string InstanceID;
  string ParentID;
  sint32 AllowFipsAlgorithmPolicy;
  string TLSCipherSuites;
};
```

## <a name="members"></a><span data-ttu-id="f3824-111">Members</span><span class="sxs-lookup"><span data-stu-id="f3824-111">Members</span></span>

<span data-ttu-id="f3824-112">La **classe \_ \_ Config01 \_ Cryptography02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f3824-112">The **MDM\_Policy\_Config01\_Cryptography02** class has these types of members:</span></span>

-   [<span data-ttu-id="f3824-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f3824-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f3824-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f3824-114">Properties</span></span>

<span data-ttu-id="f3824-115">La **classe \_ \_ \_ Cryptography02 dei criteri MDM Config01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="f3824-115">The **MDM\_Policy\_Config01\_Cryptography02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="f3824-116">AllowFipsAlgorithmPolicy</span><span class="sxs-lookup"><span data-stu-id="f3824-116">AllowFipsAlgorithmPolicy</span></span>](/windows/client-management/mdm/policy-csp-cryptography#cryptography-allowfipsalgorithmpolicy)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3824-117">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f3824-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f3824-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f3824-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f3824-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f3824-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3824-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f3824-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3824-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3824-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3824-122">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f3824-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f3824-123">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="f3824-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="f3824-124">Per questa classe la stringa è "Cryptography".</span><span class="sxs-lookup"><span data-stu-id="f3824-124">For this class, the string is "Cryptography"</span></span>

</dd> <dt>

<span data-ttu-id="f3824-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="f3824-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3824-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f3824-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3824-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3824-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3824-128">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f3824-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f3824-129">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="f3824-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="f3824-130">Per questa classe la stringa è "./Vendor/MSFT/Policy/Config"</span><span class="sxs-lookup"><span data-stu-id="f3824-130">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="f3824-131">TLSCipherSuites</span><span class="sxs-lookup"><span data-stu-id="f3824-131">TLSCipherSuites</span></span>](/windows/client-management/mdm/policy-csp-cryptography#cryptography-tlsciphersuites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3824-132">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f3824-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3824-133">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f3824-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f3824-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f3824-134">Requirements</span></span>



| <span data-ttu-id="f3824-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3824-135">Requirement</span></span> | <span data-ttu-id="f3824-136">Valore</span><span class="sxs-lookup"><span data-stu-id="f3824-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3824-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f3824-137">Minimum supported client</span></span><br/> | <span data-ttu-id="f3824-138">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="f3824-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f3824-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f3824-139">Minimum supported server</span></span><br/> | <span data-ttu-id="f3824-140">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="f3824-140">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="f3824-141">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f3824-141">Namespace</span></span><br/>                | <span data-ttu-id="f3824-142">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="f3824-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="f3824-143">MOF</span><span class="sxs-lookup"><span data-stu-id="f3824-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f3824-144"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f3824-144"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="f3824-145">DLL</span><span class="sxs-lookup"><span data-stu-id="f3824-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3824-146"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3824-146"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3824-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f3824-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3824-148">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="f3824-148">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

