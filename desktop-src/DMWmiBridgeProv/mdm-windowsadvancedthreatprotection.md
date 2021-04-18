---
title: Classe MDM_WindowsAdvancedThreatProtection
description: La \_ classe MDM WindowsAdvancedThreatProtection viene utilizzata per caricare gli endpoint offboard per Windows Defender Advanced Threat Protection (WDATP).
ms.assetid: 7a95253e-6d13-4c1b-b78d-c56c6378f7c3
keywords:
- Classe MDM_WindowsAdvancedThreatProtection
- Classe MDM_WindowsAdvancedThreatProtection, descritta
topic_type:
- apiref
api_name:
- MDM_WindowsAdvancedThreatProtection
- MDM_WindowsAdvancedThreatProtection.InstanceID
- MDM_WindowsAdvancedThreatProtection.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c369406a3c8bcf982aeb18b4bbb53c1af4983e84
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302110"
---
# <a name="mdm_windowsadvancedthreatprotection-class"></a><span data-ttu-id="05ae4-105">MDM \_ WindowsAdvancedThreatProtection (classe)</span><span class="sxs-lookup"><span data-stu-id="05ae4-105">MDM\_WindowsAdvancedThreatProtection class</span></span>

<span data-ttu-id="05ae4-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="05ae4-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="05ae4-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="05ae4-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="05ae4-108">La classe **MDM \_ WindowsAdvancedThreatProtection** viene utilizzata per caricare gli endpoint offboard per Windows Defender Advanced Threat Protection (WDATP).</span><span class="sxs-lookup"><span data-stu-id="05ae4-108">The **MDM\_WindowsAdvancedThreatProtection** class is used to onboard and offboard endpoints for Windows Defender Advanced Threat Protection (WDATP).</span></span>

<span data-ttu-id="05ae4-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="05ae4-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="05ae4-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="05ae4-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_WindowsAdvancedThreatProtection
{
  string InstanceID;
  string ParentID;
  string Onboarding;
  string Offboarding;
};
```

## <a name="members"></a><span data-ttu-id="05ae4-111">Members</span><span class="sxs-lookup"><span data-stu-id="05ae4-111">Members</span></span>

<span data-ttu-id="05ae4-112">La classe **MDM \_ WindowsAdvancedThreatProtection** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="05ae4-112">The **MDM\_WindowsAdvancedThreatProtection** class has these types of members:</span></span>

-   [<span data-ttu-id="05ae4-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="05ae4-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="05ae4-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="05ae4-114">Properties</span></span>

<span data-ttu-id="05ae4-115">La classe **MDM \_ WindowsAdvancedThreatProtection** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="05ae4-115">The **MDM\_WindowsAdvancedThreatProtection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="05ae4-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="05ae4-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05ae4-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="05ae4-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05ae4-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="05ae4-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05ae4-119">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="05ae4-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="05ae4-120">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="05ae4-120">Identifies the name of the parent node.</span></span> <span data-ttu-id="05ae4-121">Per questa classe la stringa è "WindowsAdvancedThreatProtection".</span><span class="sxs-lookup"><span data-stu-id="05ae4-121">For this class, the string is "WindowsAdvancedThreatProtection".</span></span>

</dd> <dt>

[<span data-ttu-id="05ae4-122">Offboarding</span><span class="sxs-lookup"><span data-stu-id="05ae4-122">Offboarding</span></span>](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#offboarding)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05ae4-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="05ae4-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05ae4-124">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="05ae4-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05ae4-125">Onboarding</span><span class="sxs-lookup"><span data-stu-id="05ae4-125">Onboarding</span></span>](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#onboarding)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05ae4-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="05ae4-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05ae4-127">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="05ae4-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="05ae4-128">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="05ae4-128">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05ae4-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="05ae4-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05ae4-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="05ae4-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05ae4-131">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="05ae4-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="05ae4-132">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="05ae4-132">Describes the full path to the parent node.</span></span> <span data-ttu-id="05ae4-133">Per questa classe la stringa è "./Vendor/MSFT/"</span><span class="sxs-lookup"><span data-stu-id="05ae4-133">For this class, the string is "./Vendor/MSFT/"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="05ae4-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="05ae4-134">Requirements</span></span>



| <span data-ttu-id="05ae4-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="05ae4-135">Requirement</span></span> | <span data-ttu-id="05ae4-136">Valore</span><span class="sxs-lookup"><span data-stu-id="05ae4-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05ae4-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="05ae4-137">Minimum supported client</span></span><br/> | <span data-ttu-id="05ae4-138">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="05ae4-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="05ae4-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="05ae4-139">Minimum supported server</span></span><br/> | <span data-ttu-id="05ae4-140">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="05ae4-140">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="05ae4-141">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="05ae4-141">Namespace</span></span><br/>                | <span data-ttu-id="05ae4-142">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="05ae4-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="05ae4-143">MOF</span><span class="sxs-lookup"><span data-stu-id="05ae4-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="05ae4-144"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="05ae4-144"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="05ae4-145">DLL</span><span class="sxs-lookup"><span data-stu-id="05ae4-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="05ae4-146"><dt>\\DMWmiBridgeProv.dllfile MOF</dt></span><span class="sxs-lookup"><span data-stu-id="05ae4-146"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05ae4-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="05ae4-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05ae4-148">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="05ae4-148">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

