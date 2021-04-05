---
title: Classe MDM_Policy_Config01_BitLocker02
description: La \_ \_ classe Config01 Bitlocker02 dei criteri MDM \_ rappresenta i criteri di BitLocker disponibili.
ms.assetid: 885df93f-41f5-4cf7-8bce-9b253b190e17
keywords:
- Classe MDM_Policy_Config01_BitLocker02
- Classe MDM_Policy_Config01_BitLocker02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_BitLocker02
- MDM_Policy_Config01_BitLocker02.InstanceID
- MDM_Policy_Config01_BitLocker02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 005c16365dfc227aff4c854e77b2a733a3c4ac70
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048173"
---
# <a name="mdm_policy_config01_bitlocker02-class"></a><span data-ttu-id="f1df4-105">\_ \_ Classe Config01 BitLocker02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="f1df4-105">MDM\_Policy\_Config01\_BitLocker02 class</span></span>

<span data-ttu-id="f1df4-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="f1df4-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="f1df4-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="f1df4-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="f1df4-108">La **classe \_ \_ Config01 \_ Bitlocker02 dei criteri MDM** rappresenta i criteri di BitLocker disponibili.</span><span class="sxs-lookup"><span data-stu-id="f1df4-108">The **MDM\_Policy\_Config01\_Bitlocker02** class represents the BitLocker policies available.</span></span>

<span data-ttu-id="f1df4-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="f1df4-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1df4-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f1df4-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_BitLocker02
{
  string InstanceID;
  string ParentID;
  sint32 EncryptionMethod;
};
```

## <a name="members"></a><span data-ttu-id="f1df4-111">Members</span><span class="sxs-lookup"><span data-stu-id="f1df4-111">Members</span></span>

<span data-ttu-id="f1df4-112">La **classe \_ \_ Config01 \_ BitLocker02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f1df4-112">The **MDM\_Policy\_Config01\_BitLocker02** class has these types of members:</span></span>

-   [<span data-ttu-id="f1df4-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f1df4-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f1df4-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f1df4-114">Properties</span></span>

<span data-ttu-id="f1df4-115">La **classe \_ \_ \_ BitLocker02 dei criteri MDM Config01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="f1df4-115">The **MDM\_Policy\_Config01\_BitLocker02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="f1df4-116">EncryptionMethod</span><span class="sxs-lookup"><span data-stu-id="f1df4-116">EncryptionMethod</span></span>](/windows/client-management/mdm/policy-csp-bitlocker#bitlocker-encryptionmethod)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1df4-117">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f1df4-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f1df4-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f1df4-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f1df4-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f1df4-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1df4-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f1df4-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1df4-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1df4-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1df4-122">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f1df4-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f1df4-123">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="f1df4-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="f1df4-124">Per questa classe la stringa è "BitLocker"</span><span class="sxs-lookup"><span data-stu-id="f1df4-124">For this class, the string is "BitLocker"</span></span>

</dd> <dt>

<span data-ttu-id="f1df4-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="f1df4-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1df4-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f1df4-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1df4-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1df4-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1df4-128">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f1df4-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f1df4-129">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="f1df4-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="f1df4-130">Per questa classe la stringa è "./Vendor/MSFT/Policy/Config"</span><span class="sxs-lookup"><span data-stu-id="f1df4-130">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f1df4-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f1df4-131">Requirements</span></span>



| <span data-ttu-id="f1df4-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1df4-132">Requirement</span></span> | <span data-ttu-id="f1df4-133">Valore</span><span class="sxs-lookup"><span data-stu-id="f1df4-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1df4-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f1df4-134">Minimum supported client</span></span><br/> | <span data-ttu-id="f1df4-135">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="f1df4-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f1df4-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f1df4-136">Minimum supported server</span></span><br/> | <span data-ttu-id="f1df4-137">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="f1df4-137">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="f1df4-138">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f1df4-138">Namespace</span></span><br/>                | <span data-ttu-id="f1df4-139">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="f1df4-139">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="f1df4-140">MOF</span><span class="sxs-lookup"><span data-stu-id="f1df4-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f1df4-141"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f1df4-141"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="f1df4-142">DLL</span><span class="sxs-lookup"><span data-stu-id="f1df4-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1df4-143"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f1df4-143"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1df4-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f1df4-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1df4-145">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="f1df4-145">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

