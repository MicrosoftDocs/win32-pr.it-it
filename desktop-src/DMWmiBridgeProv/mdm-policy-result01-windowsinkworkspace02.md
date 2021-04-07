---
title: Classe MDM_Policy_Result01_WindowsInkWorkspace02
description: La \_ \_ classe Result01 WindowsInkWorkspace02 dei criteri MDM \_ rappresenta i criteri dell'area di lavoro input penna disponibili.
ms.assetid: a3bb85e5-554f-4f41-8e65-e221f8adc947
keywords:
- Classe MDM_Policy_Result01_WindowsInkWorkspace02
- Classe MDM_Policy_Result01_WindowsInkWorkspace02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_WindowsInkWorkspace02
- MDM_Policy_Result01_WindowsInkWorkspace02.InstanceID
- MDM_Policy_Result01_WindowsInkWorkspace02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d64100ec0566b7cd996840d012d018b8dbc75aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873357"
---
# <a name="mdm_policy_result01_windowsinkworkspace02-class"></a><span data-ttu-id="19b03-105">\_ \_ Classe Result01 WindowsInkWorkspace02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="19b03-105">MDM\_Policy\_Result01\_WindowsInkWorkspace02 class</span></span>

<span data-ttu-id="19b03-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="19b03-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="19b03-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="19b03-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="19b03-108">La [**classe \_ \_ Result01 \_ WindowsInkWorkspace02 dei criteri MDM**](mdm-policy-config01-windowsinkworkspace02.md) rappresenta i criteri dell'area di lavoro input penna disponibili.</span><span class="sxs-lookup"><span data-stu-id="19b03-108">The [**MDM\_Policy\_Result01\_WindowsInkWorkspace02**](mdm-policy-config01-windowsinkworkspace02.md) class represents the ink workspace policies available.</span></span>

<span data-ttu-id="19b03-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="19b03-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="19b03-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="19b03-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_WindowsInkWorkspace02
{
  string InstanceID;
  string ParentID;
  sint32 AllowWindowsInkWorkspace;
  sint32 AllowSuggestedAppsInWindowsInkWorkspace;
};
```

## <a name="members"></a><span data-ttu-id="19b03-111">Members</span><span class="sxs-lookup"><span data-stu-id="19b03-111">Members</span></span>

<span data-ttu-id="19b03-112">La **classe \_ \_ Result01 \_ WindowsInkWorkspace02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="19b03-112">The **MDM\_Policy\_Result01\_WindowsInkWorkspace02** class has these types of members:</span></span>

-   [<span data-ttu-id="19b03-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="19b03-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="19b03-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="19b03-114">Properties</span></span>

<span data-ttu-id="19b03-115">La **classe \_ \_ \_ WindowsInkWorkspace02 dei criteri MDM Result01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="19b03-115">The **MDM\_Policy\_Result01\_WindowsInkWorkspace02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="19b03-116">AllowSuggestedAppsInWindowsInkWorkspace</span><span class="sxs-lookup"><span data-stu-id="19b03-116">AllowSuggestedAppsInWindowsInkWorkspace</span></span>](/windows/client-management/mdm/policy-csp-windowsinkworkspace#windowsinkworkspace-allowsuggestedappsinwindowsinkworkspace)
</dt> <dd> <dl> <dt>

<span data-ttu-id="19b03-117">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="19b03-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="19b03-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="19b03-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="19b03-119">AllowWindowsInkWorkspace</span><span class="sxs-lookup"><span data-stu-id="19b03-119">AllowWindowsInkWorkspace</span></span>](/windows/client-management/mdm/policy-csp-windowsinkworkspace#windowsinkworkspace-allowwindowsinkworkspace)
</dt> <dd> <dl> <dt>

<span data-ttu-id="19b03-120">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="19b03-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="19b03-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="19b03-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="19b03-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="19b03-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19b03-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="19b03-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19b03-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="19b03-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19b03-125">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="19b03-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="19b03-126">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="19b03-126">Identifies the name of the parent node.</span></span> <span data-ttu-id="19b03-127">Per questa classe la stringa è "WindowsInkWorkspace".</span><span class="sxs-lookup"><span data-stu-id="19b03-127">For this class, the string is "WindowsInkWorkspace".</span></span>

</dd> <dt>

<span data-ttu-id="19b03-128">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="19b03-128">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19b03-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="19b03-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19b03-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="19b03-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19b03-131">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="19b03-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="19b03-132">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="19b03-132">Describes the full path to the parent node.</span></span> <span data-ttu-id="19b03-133">Per questa classe la stringa è "./Vendor/MSFT/Policy/Result"</span><span class="sxs-lookup"><span data-stu-id="19b03-133">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="19b03-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="19b03-134">Requirements</span></span>



| <span data-ttu-id="19b03-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="19b03-135">Requirement</span></span> | <span data-ttu-id="19b03-136">Valore</span><span class="sxs-lookup"><span data-stu-id="19b03-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19b03-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="19b03-137">Minimum supported client</span></span><br/> | <span data-ttu-id="19b03-138">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="19b03-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="19b03-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="19b03-139">Minimum supported server</span></span><br/> | <span data-ttu-id="19b03-140">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="19b03-140">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="19b03-141">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="19b03-141">Namespace</span></span><br/>                | <span data-ttu-id="19b03-142">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="19b03-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="19b03-143">MOF</span><span class="sxs-lookup"><span data-stu-id="19b03-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="19b03-144"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="19b03-144"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl>       |
| <span data-ttu-id="19b03-145">DLL</span><span class="sxs-lookup"><span data-stu-id="19b03-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19b03-146"><dt>\\DMWmiBridgeProv.dllfile MOF</dt></span><span class="sxs-lookup"><span data-stu-id="19b03-146"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

