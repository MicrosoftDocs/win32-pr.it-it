---
title: Classe MDM_Policy_Result01_EventLogService02
description: La \_ \_ classe Result01 EventLogService02 dei criteri MDM \_ rappresenta il comportamento del log eventi.
ms.assetid: 6d4908e9-d283-486a-8309-57d5c5ec83d0
keywords:
- Classe MDM_Policy_Result01_EventLogService02
- Classe MDM_Policy_Result01_EventLogService02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_EventLogService02
- MDM_Policy_Result01_EventLogService02.InstanceID
- MDM_Policy_Result01_EventLogService02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 914a00c3646490e5d4679579aab7a38474a34f00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476906"
---
# <a name="mdm_policy_result01_eventlogservice02-class"></a><span data-ttu-id="2134b-105">\_ \_ Classe Result01 EventLogService02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="2134b-105">MDM\_Policy\_Result01\_EventLogService02 class</span></span>

<span data-ttu-id="2134b-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="2134b-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="2134b-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="2134b-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="2134b-108">La \_ \_ classe Result01 EventLogService02 dei criteri MDM \_ rappresenta il comportamento del log eventi.</span><span class="sxs-lookup"><span data-stu-id="2134b-108">The MDM\_Policy\_Result01\_EventLogService02 class represents the event log behavior.</span></span>

<span data-ttu-id="2134b-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="2134b-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2134b-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2134b-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_EventLogService02
{
  string InstanceID;
  string ParentID;
  string ControlEventLogBehavior;
  string SpecifyMaximumFileSizeApplicationLog;
  string SpecifyMaximumFileSizeSecurityLog;
  string SpecifyMaximumFileSizeSystemLog;
};
```

## <a name="members"></a><span data-ttu-id="2134b-111">Members</span><span class="sxs-lookup"><span data-stu-id="2134b-111">Members</span></span>

<span data-ttu-id="2134b-112">La **classe \_ \_ Result01 \_ EventLogService02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="2134b-112">The **MDM\_Policy\_Result01\_EventLogService02** class has these types of members:</span></span>

-   [<span data-ttu-id="2134b-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2134b-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2134b-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2134b-114">Properties</span></span>

<span data-ttu-id="2134b-115">La **classe \_ \_ \_ EventLogService02 dei criteri MDM Result01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="2134b-115">The **MDM\_Policy\_Result01\_EventLogService02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="2134b-116">ControlEventLogBehavior</span><span class="sxs-lookup"><span data-stu-id="2134b-116">ControlEventLogBehavior</span></span>](/windows/client-management/mdm/policy-csp-eventlogservice#eventlogservice-controleventlogbehavior)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2134b-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2134b-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2134b-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="2134b-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2134b-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2134b-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2134b-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2134b-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2134b-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2134b-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2134b-122">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2134b-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2134b-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="2134b-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2134b-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2134b-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2134b-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2134b-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2134b-126">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2134b-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2134b-127">SpecifyMaximumFileSizeApplicationLog</span><span class="sxs-lookup"><span data-stu-id="2134b-127">SpecifyMaximumFileSizeApplicationLog</span></span>](/windows/client-management/mdm/policy-csp-eventlogservice#eventlogservice-specifymaximumfilesizeapplicationlog)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2134b-128">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2134b-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2134b-129">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="2134b-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2134b-130">SpecifyMaximumFileSizeSecurityLog</span><span class="sxs-lookup"><span data-stu-id="2134b-130">SpecifyMaximumFileSizeSecurityLog</span></span>](/windows/client-management/mdm/policy-csp-eventlogservice#eventlogservice-specifymaximumfilesizesecuritylog)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2134b-131">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2134b-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2134b-132">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="2134b-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2134b-133">SpecifyMaximumFileSizeSystemLog</span><span class="sxs-lookup"><span data-stu-id="2134b-133">SpecifyMaximumFileSizeSystemLog</span></span>](/windows/client-management/mdm/policy-csp-eventlogservice#eventlogservice-specifymaximumfilesizesystemlog)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2134b-134">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2134b-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2134b-135">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="2134b-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2134b-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2134b-136">Requirements</span></span>



| <span data-ttu-id="2134b-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="2134b-137">Requirement</span></span> | <span data-ttu-id="2134b-138">Valore</span><span class="sxs-lookup"><span data-stu-id="2134b-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2134b-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2134b-139">Minimum supported client</span></span><br/> | <span data-ttu-id="2134b-140">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="2134b-140">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2134b-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2134b-141">Minimum supported server</span></span><br/> | <span data-ttu-id="2134b-142">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="2134b-142">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="2134b-143">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2134b-143">Namespace</span></span><br/>                | <span data-ttu-id="2134b-144">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="2134b-144">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="2134b-145">MOF</span><span class="sxs-lookup"><span data-stu-id="2134b-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2134b-146"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2134b-146"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="2134b-147">DLL</span><span class="sxs-lookup"><span data-stu-id="2134b-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2134b-148"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2134b-148"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

