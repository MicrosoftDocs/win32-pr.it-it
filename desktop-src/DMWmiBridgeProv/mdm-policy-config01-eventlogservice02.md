---
title: Classe MDM_Policy_Config01_EventLogService02
description: La \_ \_ classe Config01 EventLogService02 di criteri MDM \_ Configura il comportamento del log eventi.
ms.assetid: 206934c4-6671-4f13-be79-22ff1fb7ce7e
keywords:
- Classe MDM_Policy_Config01_EventLogService02
- Classe MDM_Policy_Config01_EventLogService02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_EventLogService02
- MDM_Policy_Config01_EventLogService02.InstanceID
- MDM_Policy_Config01_EventLogService02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e39d3e78e686886e689ab2333b073108207446a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964023"
---
# <a name="mdm_policy_config01_eventlogservice02-class"></a><span data-ttu-id="5b248-105">\_ \_ Classe Config01 EventLogService02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="5b248-105">MDM\_Policy\_Config01\_EventLogService02 class</span></span>

<span data-ttu-id="5b248-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="5b248-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="5b248-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="5b248-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="5b248-108">La \_ \_ classe Config01 EventLogService02 di criteri MDM \_ Configura il comportamento del log eventi.</span><span class="sxs-lookup"><span data-stu-id="5b248-108">The MDM\_Policy\_Config01\_EventLogService02 class configures the event log behavior.</span></span>

<span data-ttu-id="5b248-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="5b248-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b248-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5b248-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_EventLogService02
{
  string InstanceID;
  string ParentID;
  string ControlEventLogBehavior;
  string SpecifyMaximumFileSizeApplicationLog;
  string SpecifyMaximumFileSizeSecurityLog;
  string SpecifyMaximumFileSizeSystemLog;
};
```

## <a name="members"></a><span data-ttu-id="5b248-111">Members</span><span class="sxs-lookup"><span data-stu-id="5b248-111">Members</span></span>

<span data-ttu-id="5b248-112">La **classe \_ \_ Config01 \_ EventLogService02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="5b248-112">The **MDM\_Policy\_Config01\_EventLogService02** class has these types of members:</span></span>

-   [<span data-ttu-id="5b248-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5b248-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5b248-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5b248-114">Properties</span></span>

<span data-ttu-id="5b248-115">La **classe \_ \_ \_ EventLogService02 dei criteri MDM Config01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="5b248-115">The **MDM\_Policy\_Config01\_EventLogService02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="5b248-116">ControlEventLogBehavior</span><span class="sxs-lookup"><span data-stu-id="5b248-116">ControlEventLogBehavior</span></span>](/windows/client-management/mdm/policy-csp-eventlogservice#eventlogservice-controleventlogbehavior)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b248-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5b248-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b248-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5b248-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5b248-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="5b248-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b248-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5b248-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b248-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5b248-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b248-122">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5b248-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5b248-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="5b248-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b248-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5b248-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b248-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5b248-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b248-126">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5b248-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5b248-127">SpecifyMaximumFileSizeApplicationLog</span><span class="sxs-lookup"><span data-stu-id="5b248-127">SpecifyMaximumFileSizeApplicationLog</span></span>](/windows/client-management/mdm/policy-csp-eventlogservice#eventlogservice-specifymaximumfilesizeapplicationlog)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b248-128">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5b248-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b248-129">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5b248-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5b248-130">SpecifyMaximumFileSizeSecurityLog</span><span class="sxs-lookup"><span data-stu-id="5b248-130">SpecifyMaximumFileSizeSecurityLog</span></span>](/windows/client-management/mdm/policy-csp-eventlogservice#eventlogservice-specifymaximumfilesizesecuritylog)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b248-131">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5b248-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b248-132">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5b248-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5b248-133">SpecifyMaximumFileSizeSystemLog</span><span class="sxs-lookup"><span data-stu-id="5b248-133">SpecifyMaximumFileSizeSystemLog</span></span>](/windows/client-management/mdm/policy-csp-eventlogservice#eventlogservice-specifymaximumfilesizesystemlog)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b248-134">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5b248-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b248-135">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5b248-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5b248-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5b248-136">Requirements</span></span>



| <span data-ttu-id="5b248-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b248-137">Requirement</span></span> | <span data-ttu-id="5b248-138">Valore</span><span class="sxs-lookup"><span data-stu-id="5b248-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b248-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5b248-139">Minimum supported client</span></span><br/> | <span data-ttu-id="5b248-140">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="5b248-140">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5b248-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5b248-141">Minimum supported server</span></span><br/> | <span data-ttu-id="5b248-142">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="5b248-142">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="5b248-143">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5b248-143">Namespace</span></span><br/>                | <span data-ttu-id="5b248-144">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="5b248-144">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="5b248-145">MOF</span><span class="sxs-lookup"><span data-stu-id="5b248-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5b248-146"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5b248-146"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="5b248-147">DLL</span><span class="sxs-lookup"><span data-stu-id="5b248-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5b248-148"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b248-148"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

