---
title: Classe MDM_Policy_Result01_RemoteShell02
description: La \_ classe RemoteShell02 dei criteri MDM \_ Result01 \_ rappresenta i criteri della shell remota.
ms.assetid: d005b2e6-e838-4bda-9ba4-bd49c092f951
keywords:
- Classe MDM_Policy_Result01_RemoteShell02
- Classe MDM_Policy_Result01_RemoteShell02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_RemoteShell02
- MDM_Policy_Result01_RemoteShell02.InstanceID
- MDM_Policy_Result01_RemoteShell02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: babd602823d0cc2e98a6855c3803aea240627e37
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873465"
---
# <a name="mdm_policy_result01_remoteshell02-class"></a><span data-ttu-id="b710c-105">\_ \_ Classe Result01 RemoteShell02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="b710c-105">MDM\_Policy\_Result01\_RemoteShell02 class</span></span>

<span data-ttu-id="b710c-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="b710c-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b710c-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="b710c-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b710c-108">La \_ classe RemoteShell02 dei criteri MDM \_ Result01 \_ rappresenta i criteri della shell remota.</span><span class="sxs-lookup"><span data-stu-id="b710c-108">The MDM\_Policy\_Result01\_RemoteShell02 class represents the remote shell policies.</span></span>

<span data-ttu-id="b710c-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="b710c-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b710c-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b710c-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_RemoteShell02
{
  string InstanceID;
  string ParentID;
  string AllowRemoteShellAccess;
  string MaxConcurrentUsers;
  string SpecifyIdleTimeout;
  string SpecifyMaxMemory;
  string SpecifyMaxProcesses;
  string SpecifyMaxRemoteShells;
  string SpecifyShellTimeout;
};
```

## <a name="members"></a><span data-ttu-id="b710c-111">Members</span><span class="sxs-lookup"><span data-stu-id="b710c-111">Members</span></span>

<span data-ttu-id="b710c-112">La **classe \_ \_ Result01 \_ RemoteShell02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b710c-112">The **MDM\_Policy\_Result01\_RemoteShell02** class has these types of members:</span></span>

-   [<span data-ttu-id="b710c-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b710c-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b710c-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b710c-114">Properties</span></span>

<span data-ttu-id="b710c-115">La **classe \_ \_ \_ RemoteShell02 dei criteri MDM Result01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="b710c-115">The **MDM\_Policy\_Result01\_RemoteShell02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="b710c-116">AllowRemoteShellAccess</span><span class="sxs-lookup"><span data-stu-id="b710c-116">AllowRemoteShellAccess</span></span>](/windows/client-management/mdm/policy-csp-remoteshell#remoteshell-allowremoteshellaccess)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b710c-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b710c-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b710c-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b710c-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b710c-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b710c-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b710c-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b710c-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b710c-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b710c-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b710c-122">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b710c-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b710c-123">MaxConcurrentUsers</span><span class="sxs-lookup"><span data-stu-id="b710c-123">MaxConcurrentUsers</span></span>](/windows/client-management/mdm/policy-csp-remoteshell#remoteshell-maxconcurrentusers)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b710c-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b710c-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b710c-125">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b710c-125">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b710c-126">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="b710c-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b710c-127">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b710c-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b710c-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b710c-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b710c-129">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b710c-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b710c-130">SpecifyIdleTimeout</span><span class="sxs-lookup"><span data-stu-id="b710c-130">SpecifyIdleTimeout</span></span>](/windows/client-management/mdm/policy-csp-remoteshell#remoteshell-specifyidletimeout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b710c-131">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b710c-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b710c-132">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b710c-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b710c-133">SpecifyMaxMemory</span><span class="sxs-lookup"><span data-stu-id="b710c-133">SpecifyMaxMemory</span></span>](/windows/client-management/mdm/policy-csp-remoteshell#remoteshell-specifymaxmemory)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b710c-134">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b710c-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b710c-135">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b710c-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b710c-136">SpecifyMaxProcesses</span><span class="sxs-lookup"><span data-stu-id="b710c-136">SpecifyMaxProcesses</span></span>](/windows/client-management/mdm/policy-csp-remoteshell#remoteshell-specifymaxprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b710c-137">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b710c-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b710c-138">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b710c-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b710c-139">SpecifyMaxRemoteShells</span><span class="sxs-lookup"><span data-stu-id="b710c-139">SpecifyMaxRemoteShells</span></span>](/windows/client-management/mdm/policy-csp-remoteshell#remoteshell-specifymaxremoteshells)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b710c-140">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b710c-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b710c-141">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b710c-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b710c-142">SpecifyShellTimeout</span><span class="sxs-lookup"><span data-stu-id="b710c-142">SpecifyShellTimeout</span></span>](/windows/client-management/mdm/policy-csp-remoteshell#remoteshell-specifyshelltimeout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b710c-143">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b710c-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b710c-144">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b710c-144">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b710c-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b710c-145">Requirements</span></span>



| <span data-ttu-id="b710c-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="b710c-146">Requirement</span></span> | <span data-ttu-id="b710c-147">Valore</span><span class="sxs-lookup"><span data-stu-id="b710c-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b710c-148">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b710c-148">Minimum supported client</span></span><br/> | <span data-ttu-id="b710c-149">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="b710c-149">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b710c-150">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b710c-150">Minimum supported server</span></span><br/> | <span data-ttu-id="b710c-151">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="b710c-151">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="b710c-152">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b710c-152">Namespace</span></span><br/>                | <span data-ttu-id="b710c-153">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="b710c-153">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="b710c-154">MOF</span><span class="sxs-lookup"><span data-stu-id="b710c-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b710c-155"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b710c-155"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="b710c-156">DLL</span><span class="sxs-lookup"><span data-stu-id="b710c-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b710c-157"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b710c-157"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

