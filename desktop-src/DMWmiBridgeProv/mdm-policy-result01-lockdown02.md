---
title: Classe MDM_Policy_Result01_LockDown02
description: La \_ classe Lockdown02 dei criteri MDM \_ Result01 \_ rappresenta i criteri di blocco disponibili.
ms.assetid: 78eab50e-b1a7-4b96-a848-b8a86a3b82c3
keywords:
- Classe MDM_Policy_Result01_LockDown02
- Classe MDM_Policy_Result01_LockDown02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_LockDown02
- MDM_Policy_Result01_LockDown02.InstanceID
- MDM_Policy_Result01_LockDown02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 159e2178e3e5600bef4fc366a0cf49b7856ce886
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476271"
---
# <a name="mdm_policy_result01_lockdown02-class"></a><span data-ttu-id="46531-105">\_ \_ Classe Result01 LockDown02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="46531-105">MDM\_Policy\_Result01\_LockDown02 class</span></span>

<span data-ttu-id="46531-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="46531-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="46531-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="46531-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="46531-108">La **classe \_ \_ \_ Lockdown02 dei criteri MDM Result01** rappresenta i criteri di blocco disponibili.</span><span class="sxs-lookup"><span data-stu-id="46531-108">The **MDM\_Policy\_Result01\_Lockdown02** class represents the lockdown policies available.</span></span>

<span data-ttu-id="46531-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="46531-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="46531-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="46531-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_LockDown02
{
  string InstanceID;
  string ParentID;
  sint32 AllowEdgeSwipe;
};
```

## <a name="members"></a><span data-ttu-id="46531-111">Members</span><span class="sxs-lookup"><span data-stu-id="46531-111">Members</span></span>

<span data-ttu-id="46531-112">La **classe \_ \_ Result01 \_ LockDown02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="46531-112">The **MDM\_Policy\_Result01\_LockDown02** class has these types of members:</span></span>

-   [<span data-ttu-id="46531-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="46531-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="46531-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="46531-114">Properties</span></span>

<span data-ttu-id="46531-115">La **classe \_ \_ \_ LockDown02 dei criteri MDM Result01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="46531-115">The **MDM\_Policy\_Result01\_LockDown02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="46531-116">AllowEdgeSwipe</span><span class="sxs-lookup"><span data-stu-id="46531-116">AllowEdgeSwipe</span></span>](/windows/client-management/mdm/policy-csp-lockdown#lockdown-allowedgeswipe)
</dt> <dd> <dl> <dt>

<span data-ttu-id="46531-117">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="46531-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="46531-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="46531-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="46531-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="46531-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46531-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="46531-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46531-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="46531-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46531-122">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="46531-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="46531-123">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="46531-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="46531-124">Per questa classe la stringa è "Lockdown".</span><span class="sxs-lookup"><span data-stu-id="46531-124">For this class, the string is "Lockdown".</span></span>

</dd> <dt>

<span data-ttu-id="46531-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="46531-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46531-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="46531-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46531-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="46531-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46531-128">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="46531-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="46531-129">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="46531-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="46531-130">Per questa classe la stringa è "./Vendor/MSFT/Policy/Result"</span><span class="sxs-lookup"><span data-stu-id="46531-130">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="46531-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="46531-131">Requirements</span></span>



| <span data-ttu-id="46531-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="46531-132">Requirement</span></span> | <span data-ttu-id="46531-133">Valore</span><span class="sxs-lookup"><span data-stu-id="46531-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46531-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="46531-134">Minimum supported client</span></span><br/> | <span data-ttu-id="46531-135">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="46531-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="46531-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="46531-136">Minimum supported server</span></span><br/> | <span data-ttu-id="46531-137">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="46531-137">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="46531-138">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="46531-138">Namespace</span></span><br/>                | <span data-ttu-id="46531-139">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="46531-139">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="46531-140">MOF</span><span class="sxs-lookup"><span data-stu-id="46531-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="46531-141"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="46531-141"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl>       |
| <span data-ttu-id="46531-142">DLL</span><span class="sxs-lookup"><span data-stu-id="46531-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46531-143"><dt>\\DMWmiBridgeProv.dllfile MOF</dt></span><span class="sxs-lookup"><span data-stu-id="46531-143"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

