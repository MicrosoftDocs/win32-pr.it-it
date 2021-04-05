---
title: Classe MDM_Policy_Config01_RemoteAssistance02
description: La \_ \_ classe Config01 RemoteAssistance02 dei criteri MDM \_ Configura i criteri di assistenza remota.
ms.assetid: bcc6c570-66d9-4dcd-b7f2-2d03733c0bcb
keywords:
- Classe MDM_Policy_Config01_RemoteAssistance02
- Classe MDM_Policy_Config01_RemoteAssistance02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_RemoteAssistance02
- MDM_Policy_Config01_RemoteAssistance02.InstanceID
- MDM_Policy_Config01_RemoteAssistance02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aceadb2eb784e72e4e332cdd34df44d779c99e97
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873769"
---
# <a name="mdm_policy_config01_remoteassistance02-class"></a><span data-ttu-id="0013c-105">\_ \_ Classe Config01 RemoteAssistance02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="0013c-105">MDM\_Policy\_Config01\_RemoteAssistance02 class</span></span>

<span data-ttu-id="0013c-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="0013c-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="0013c-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="0013c-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="0013c-108">La \_ \_ classe Config01 RemoteAssistance02 dei criteri MDM \_ Configura i criteri di assistenza remota.</span><span class="sxs-lookup"><span data-stu-id="0013c-108">The MDM\_Policy\_Config01\_RemoteAssistance02 class configures the remote assistance policies.</span></span>

<span data-ttu-id="0013c-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="0013c-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0013c-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0013c-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_RemoteAssistance02
{
  string InstanceID;
  string ParentID;
  string CustomizeWarningMessages;
  string SessionLogging;
  string SolicitedRemoteAssistance;
  string UnsolicitedRemoteAssistance;
};
```

## <a name="members"></a><span data-ttu-id="0013c-111">Members</span><span class="sxs-lookup"><span data-stu-id="0013c-111">Members</span></span>

<span data-ttu-id="0013c-112">La **classe \_ \_ Config01 \_ RemoteAssistance02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="0013c-112">The **MDM\_Policy\_Config01\_RemoteAssistance02** class has these types of members:</span></span>

-   [<span data-ttu-id="0013c-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0013c-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0013c-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0013c-114">Properties</span></span>

<span data-ttu-id="0013c-115">La **classe \_ \_ \_ RemoteAssistance02 dei criteri MDM Config01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="0013c-115">The **MDM\_Policy\_Config01\_RemoteAssistance02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="0013c-116">CustomizeWarningMessages</span><span class="sxs-lookup"><span data-stu-id="0013c-116">CustomizeWarningMessages</span></span>](/windows/client-management/mdm/policy-csp-remoteassistance#remoteassistance-customizewarningmessages)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0013c-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0013c-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0013c-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="0013c-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0013c-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="0013c-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0013c-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0013c-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0013c-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0013c-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0013c-122">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0013c-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0013c-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="0013c-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0013c-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0013c-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0013c-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0013c-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0013c-126">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0013c-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0013c-127">SessionLogging</span><span class="sxs-lookup"><span data-stu-id="0013c-127">SessionLogging</span></span>](/windows/client-management/mdm/policy-csp-remoteassistance#remoteassistance-sessionlogging)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0013c-128">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0013c-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0013c-129">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="0013c-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0013c-130">SolicitedRemoteAssistance</span><span class="sxs-lookup"><span data-stu-id="0013c-130">SolicitedRemoteAssistance</span></span>](/windows/client-management/mdm/policy-csp-remoteassistance#remoteassistance-solicitedremoteassistance)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0013c-131">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0013c-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0013c-132">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="0013c-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0013c-133">UnsolicitedRemoteAssistance</span><span class="sxs-lookup"><span data-stu-id="0013c-133">UnsolicitedRemoteAssistance</span></span>](/windows/client-management/mdm/policy-csp-remoteassistance#remoteassistance-unsolicitedremoteassistance)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0013c-134">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0013c-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0013c-135">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="0013c-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0013c-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0013c-136">Requirements</span></span>



| <span data-ttu-id="0013c-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="0013c-137">Requirement</span></span> | <span data-ttu-id="0013c-138">Valore</span><span class="sxs-lookup"><span data-stu-id="0013c-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0013c-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0013c-139">Minimum supported client</span></span><br/> | <span data-ttu-id="0013c-140">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="0013c-140">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0013c-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0013c-141">Minimum supported server</span></span><br/> | <span data-ttu-id="0013c-142">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="0013c-142">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="0013c-143">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0013c-143">Namespace</span></span><br/>                | <span data-ttu-id="0013c-144">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="0013c-144">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="0013c-145">MOF</span><span class="sxs-lookup"><span data-stu-id="0013c-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0013c-146"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0013c-146"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="0013c-147">DLL</span><span class="sxs-lookup"><span data-stu-id="0013c-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0013c-148"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0013c-148"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

