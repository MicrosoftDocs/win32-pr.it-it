---
title: Classe MDM_Policy_Config01_WindowsInkWorkspace02
description: La \_ \_ classe Config01 WindowsInkWorkspace02 dei criteri MDM \_ rappresenta i criteri dell'area di lavoro input penna disponibili.
ms.assetid: 676a459f-25b0-4cf7-bf64-635ac4a93f59
keywords:
- Classe MDM_Policy_Config01_WindowsInkWorkspace02
- Classe MDM_Policy_Config01_WindowsInkWorkspace02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_WindowsInkWorkspace02
- MDM_Policy_Config01_WindowsInkWorkspace02.InstanceID
- MDM_Policy_Config01_WindowsInkWorkspace02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f654326b0a44ed40faa06dfe80d933dc2c52c4f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964283"
---
# <a name="mdm_policy_config01_windowsinkworkspace02-class"></a><span data-ttu-id="e5996-105">\_ \_ Classe Config01 WindowsInkWorkspace02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="e5996-105">MDM\_Policy\_Config01\_WindowsInkWorkspace02 class</span></span>

<span data-ttu-id="e5996-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="e5996-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="e5996-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="e5996-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="e5996-108">La **classe \_ \_ Config01 \_ WindowsInkWorkspace02 dei criteri MDM** rappresenta i criteri dell'area di lavoro input penna disponibili.</span><span class="sxs-lookup"><span data-stu-id="e5996-108">The **MDM\_Policy\_Config01\_WindowsInkWorkspace02** class represents the ink workspace policies available.</span></span>

<span data-ttu-id="e5996-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="e5996-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5996-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e5996-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_WindowsInkWorkspace02
{
  string InstanceID;
  string ParentID;
  sint32 AllowWindowsInkWorkspace;
  sint32 AllowSuggestedAppsInWindowsInkWorkspace;
};
```

## <a name="members"></a><span data-ttu-id="e5996-111">Members</span><span class="sxs-lookup"><span data-stu-id="e5996-111">Members</span></span>

<span data-ttu-id="e5996-112">La **classe \_ \_ Config01 \_ WindowsInkWorkspace02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e5996-112">The **MDM\_Policy\_Config01\_WindowsInkWorkspace02** class has these types of members:</span></span>

-   [<span data-ttu-id="e5996-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e5996-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e5996-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e5996-114">Properties</span></span>

<span data-ttu-id="e5996-115">La **classe \_ \_ \_ WindowsInkWorkspace02 dei criteri MDM Config01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="e5996-115">The **MDM\_Policy\_Config01\_WindowsInkWorkspace02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="e5996-116">AllowSuggestedAppsInWindowsInkWorkspace</span><span class="sxs-lookup"><span data-stu-id="e5996-116">AllowSuggestedAppsInWindowsInkWorkspace</span></span>](/windows/client-management/mdm/policy-csp-windowsinkworkspace#windowsinkworkspace-allowsuggestedappsinwindowsinkworkspace)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5996-117">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e5996-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e5996-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="e5996-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e5996-119">AllowWindowsInkWorkspace</span><span class="sxs-lookup"><span data-stu-id="e5996-119">AllowWindowsInkWorkspace</span></span>](/windows/client-management/mdm/policy-csp-windowsinkworkspace#windowsinkworkspace-allowwindowsinkworkspace)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5996-120">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e5996-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e5996-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="e5996-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e5996-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e5996-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5996-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e5996-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5996-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e5996-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5996-125">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e5996-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e5996-126">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="e5996-126">Identifies the name of the parent node.</span></span> <span data-ttu-id="e5996-127">Per questa classe la stringa è "WindowsInkWorkspace".</span><span class="sxs-lookup"><span data-stu-id="e5996-127">For this class, the string is "WindowsInkWorkspace".</span></span>

</dd> <dt>

<span data-ttu-id="e5996-128">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="e5996-128">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5996-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e5996-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5996-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e5996-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5996-131">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e5996-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e5996-132">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="e5996-132">Describes the full path to the parent node.</span></span> <span data-ttu-id="e5996-133">Per questa classe la stringa è "./Vendor/MSFT/Policy/Config"</span><span class="sxs-lookup"><span data-stu-id="e5996-133">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e5996-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e5996-134">Requirements</span></span>



| <span data-ttu-id="e5996-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5996-135">Requirement</span></span> | <span data-ttu-id="e5996-136">Valore</span><span class="sxs-lookup"><span data-stu-id="e5996-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5996-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e5996-137">Minimum supported client</span></span><br/> | <span data-ttu-id="e5996-138">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="e5996-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="e5996-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e5996-139">Minimum supported server</span></span><br/> | <span data-ttu-id="e5996-140">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="e5996-140">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="e5996-141">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e5996-141">Namespace</span></span><br/>                | <span data-ttu-id="e5996-142">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="e5996-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="e5996-143">MOF</span><span class="sxs-lookup"><span data-stu-id="e5996-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e5996-144"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e5996-144"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl>       |
| <span data-ttu-id="e5996-145">DLL</span><span class="sxs-lookup"><span data-stu-id="e5996-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5996-146"><dt>\\DMWmiBridgeProv.dllfile MOF</dt></span><span class="sxs-lookup"><span data-stu-id="e5996-146"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

