---
title: Classe MDM_Policy_Config01_RemoteShell02
description: La \_ \_ classe Config01 RemoteShell02 dei criteri MDM \_ Configura i criteri della shell remota.
ms.assetid: 7026fadb-ec6a-4696-a24c-1b1e071b94b0
keywords:
- Classe MDM_Policy_Config01_RemoteShell02
- Classe MDM_Policy_Config01_RemoteShell02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_RemoteShell02
- MDM_Policy_Config01_RemoteShell02.InstanceID
- MDM_Policy_Config01_RemoteShell02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c318b0c6f23e92d90091495fdc25993d6958ca56
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476936"
---
# <a name="mdm_policy_config01_remoteshell02-class"></a><span data-ttu-id="29ee6-105">\_ \_ Classe Config01 RemoteShell02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="29ee6-105">MDM\_Policy\_Config01\_RemoteShell02 class</span></span>

<span data-ttu-id="29ee6-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="29ee6-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="29ee6-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="29ee6-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="29ee6-108">La \_ \_ classe Config01 RemoteShell02 dei criteri MDM \_ Configura i criteri della shell remota.</span><span class="sxs-lookup"><span data-stu-id="29ee6-108">The MDM\_Policy\_Config01\_RemoteShell02 class configures the remote shell policies.</span></span>

<span data-ttu-id="29ee6-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="29ee6-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="29ee6-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="29ee6-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_RemoteShell02
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

## <a name="members"></a><span data-ttu-id="29ee6-111">Members</span><span class="sxs-lookup"><span data-stu-id="29ee6-111">Members</span></span>

<span data-ttu-id="29ee6-112">La **classe \_ \_ Config01 \_ RemoteShell02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="29ee6-112">The **MDM\_Policy\_Config01\_RemoteShell02** class has these types of members:</span></span>

-   [<span data-ttu-id="29ee6-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="29ee6-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="29ee6-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="29ee6-114">Properties</span></span>

<span data-ttu-id="29ee6-115">La **classe \_ \_ \_ RemoteShell02 dei criteri MDM Config01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="29ee6-115">The **MDM\_Policy\_Config01\_RemoteShell02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="29ee6-116">AllowRemoteShellAccess</span><span class="sxs-lookup"><span data-stu-id="29ee6-116">AllowRemoteShellAccess</span></span>](/windows/client-management/mdm/policy-csp-remoteshell#remoteshell-allowremoteshellaccess)
</dt> <dd> <dl> <dt>

<span data-ttu-id="29ee6-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="29ee6-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="29ee6-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="29ee6-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="29ee6-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="29ee6-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29ee6-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="29ee6-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="29ee6-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="29ee6-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="29ee6-122">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="29ee6-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="29ee6-123">MaxConcurrentUsers</span><span class="sxs-lookup"><span data-stu-id="29ee6-123">MaxConcurrentUsers</span></span>](/windows/client-management/mdm/policy-csp-remoteshell#remoteshell-maxconcurrentusers)
</dt> <dd> <dl> <dt>

<span data-ttu-id="29ee6-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="29ee6-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="29ee6-125">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="29ee6-125">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="29ee6-126">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="29ee6-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29ee6-127">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="29ee6-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="29ee6-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="29ee6-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="29ee6-129">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="29ee6-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="29ee6-130">SpecifyIdleTimeout</span><span class="sxs-lookup"><span data-stu-id="29ee6-130">SpecifyIdleTimeout</span></span>](/windows/client-management/mdm/policy-csp-remoteshell#remoteshell-specifyidletimeout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="29ee6-131">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="29ee6-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="29ee6-132">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="29ee6-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="29ee6-133">SpecifyMaxMemory</span><span class="sxs-lookup"><span data-stu-id="29ee6-133">SpecifyMaxMemory</span></span>](/windows/client-management/mdm/policy-csp-remoteshell#remoteshell-specifymaxmemory)
</dt> <dd> <dl> <dt>

<span data-ttu-id="29ee6-134">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="29ee6-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="29ee6-135">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="29ee6-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="29ee6-136">SpecifyMaxProcesses</span><span class="sxs-lookup"><span data-stu-id="29ee6-136">SpecifyMaxProcesses</span></span>](/windows/client-management/mdm/policy-csp-remoteshell#remoteshell-specifymaxprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="29ee6-137">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="29ee6-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="29ee6-138">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="29ee6-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="29ee6-139">SpecifyMaxRemoteShells</span><span class="sxs-lookup"><span data-stu-id="29ee6-139">SpecifyMaxRemoteShells</span></span>](/windows/client-management/mdm/policy-csp-remoteshell#remoteshell-specifymaxremoteshells)
</dt> <dd> <dl> <dt>

<span data-ttu-id="29ee6-140">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="29ee6-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="29ee6-141">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="29ee6-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="29ee6-142">SpecifyShellTimeout</span><span class="sxs-lookup"><span data-stu-id="29ee6-142">SpecifyShellTimeout</span></span>](/windows/client-management/mdm/policy-csp-remoteshell#remoteshell-specifyshelltimeout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="29ee6-143">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="29ee6-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="29ee6-144">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="29ee6-144">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="29ee6-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="29ee6-145">Requirements</span></span>



| <span data-ttu-id="29ee6-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="29ee6-146">Requirement</span></span> | <span data-ttu-id="29ee6-147">Valore</span><span class="sxs-lookup"><span data-stu-id="29ee6-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29ee6-148">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="29ee6-148">Minimum supported client</span></span><br/> | <span data-ttu-id="29ee6-149">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="29ee6-149">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="29ee6-150">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="29ee6-150">Minimum supported server</span></span><br/> | <span data-ttu-id="29ee6-151">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="29ee6-151">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="29ee6-152">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="29ee6-152">Namespace</span></span><br/>                | <span data-ttu-id="29ee6-153">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="29ee6-153">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="29ee6-154">MOF</span><span class="sxs-lookup"><span data-stu-id="29ee6-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="29ee6-155"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="29ee6-155"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="29ee6-156">DLL</span><span class="sxs-lookup"><span data-stu-id="29ee6-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="29ee6-157"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29ee6-157"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

