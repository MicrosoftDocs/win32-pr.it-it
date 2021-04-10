---
title: Classe MDM_WindowsAdvancedThreatProtection_HealthState01
description: La \_ classe MDM WindowsAdvancedThreatProtection \_ HealthState01 viene usata per determinare lo stato di integrità degli endpoint di Windows Defender Advanced Threat Protection (WDATP).
ms.assetid: 8d630b95-9895-4cb8-99f2-8f869c4dfd18
keywords:
- Classe MDM_WindowsAdvancedThreatProtection_HealthState01
- Classe MDM_WindowsAdvancedThreatProtection_HealthState01, descritta
topic_type:
- apiref
api_name:
- MDM_WindowsAdvancedThreatProtection_HealthState01
- MDM_WindowsAdvancedThreatProtection_HealthState01.InstanceID
- MDM_WindowsAdvancedThreatProtection_HealthState01.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5519b731cf54a633a659ec865e7a1f0e12deda75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964609"
---
# <a name="mdm_windowsadvancedthreatprotection_healthstate01-class"></a><span data-ttu-id="9bcf2-105">\_Classe MDM WindowsAdvancedThreatProtection \_ HealthState01</span><span class="sxs-lookup"><span data-stu-id="9bcf2-105">MDM\_WindowsAdvancedThreatProtection\_HealthState01 class</span></span>

<span data-ttu-id="9bcf2-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="9bcf2-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="9bcf2-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="9bcf2-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="9bcf2-108">La classe **MDM \_ WindowsAdvancedThreatProtection \_ HealthState01** viene usata per determinare lo stato di integrità degli endpoint di Windows Defender Advanced Threat Protection (WDATP).</span><span class="sxs-lookup"><span data-stu-id="9bcf2-108">The **MDM\_WindowsAdvancedThreatProtection\_HealthState01** class is used to determine the health status of Windows Defender Advanced Threat Protection (WDATP) endpoints.</span></span>

<span data-ttu-id="9bcf2-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="9bcf2-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9bcf2-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9bcf2-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_WindowsAdvancedThreatProtection_HealthState01
{
  string   InstanceID;
  string   ParentID;
  datetime LastConnected;
  boolean  SenseIsRunning;
  sint32   OnboardingState;
  string   OrgId;
};
```

## <a name="members"></a><span data-ttu-id="9bcf2-111">Members</span><span class="sxs-lookup"><span data-stu-id="9bcf2-111">Members</span></span>

<span data-ttu-id="9bcf2-112">La classe **MDM \_ WindowsAdvancedThreatProtection \_ HealthState01** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="9bcf2-112">The **MDM\_WindowsAdvancedThreatProtection\_HealthState01** class has these types of members:</span></span>

-   [<span data-ttu-id="9bcf2-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9bcf2-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9bcf2-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9bcf2-114">Properties</span></span>

<span data-ttu-id="9bcf2-115">La classe **MDM \_ WindowsAdvancedThreatProtection \_ HealthState01** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="9bcf2-115">The **MDM\_WindowsAdvancedThreatProtection\_HealthState01** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9bcf2-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="9bcf2-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bcf2-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9bcf2-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9bcf2-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9bcf2-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9bcf2-119">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9bcf2-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9bcf2-120">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="9bcf2-120">Identifies the name of the parent node.</span></span> <span data-ttu-id="9bcf2-121">Per questa classe la stringa è "HealthState".</span><span class="sxs-lookup"><span data-stu-id="9bcf2-121">For this class, the string is "HealthState".</span></span>

</dd> <dt>

[<span data-ttu-id="9bcf2-122">LastConnected</span><span class="sxs-lookup"><span data-stu-id="9bcf2-122">LastConnected</span></span>](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#healthstate-lastconnected)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bcf2-123">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9bcf2-123">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9bcf2-124">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9bcf2-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9bcf2-125">OnboardingState</span><span class="sxs-lookup"><span data-stu-id="9bcf2-125">OnboardingState</span></span>](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#healthstate-onboardingstate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bcf2-126">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9bcf2-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9bcf2-127">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9bcf2-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9bcf2-128">OrgId</span><span class="sxs-lookup"><span data-stu-id="9bcf2-128">OrgId</span></span>](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#healthstate-orgid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bcf2-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9bcf2-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9bcf2-130">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9bcf2-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9bcf2-131">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="9bcf2-131">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bcf2-132">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9bcf2-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9bcf2-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9bcf2-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9bcf2-134">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9bcf2-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9bcf2-135">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="9bcf2-135">Describes the full path to the parent node.</span></span> <span data-ttu-id="9bcf2-136">Per questa classe la stringa è "./Vendor/MSFT/WindowsAdvancedThreatProtection"</span><span class="sxs-lookup"><span data-stu-id="9bcf2-136">For this class, the string is "./Vendor/MSFT/WindowsAdvancedThreatProtection"</span></span>

</dd> <dt>

[<span data-ttu-id="9bcf2-137">SenseIsRunning</span><span class="sxs-lookup"><span data-stu-id="9bcf2-137">SenseIsRunning</span></span>](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#healthstate-senseisrunning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bcf2-138">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="9bcf2-138">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9bcf2-139">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9bcf2-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9bcf2-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9bcf2-140">Requirements</span></span>



| <span data-ttu-id="9bcf2-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="9bcf2-141">Requirement</span></span> | <span data-ttu-id="9bcf2-142">Valore</span><span class="sxs-lookup"><span data-stu-id="9bcf2-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9bcf2-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9bcf2-143">Minimum supported client</span></span><br/> | <span data-ttu-id="9bcf2-144">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="9bcf2-144">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="9bcf2-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9bcf2-145">Minimum supported server</span></span><br/> | <span data-ttu-id="9bcf2-146">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="9bcf2-146">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="9bcf2-147">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9bcf2-147">Namespace</span></span><br/>                | <span data-ttu-id="9bcf2-148">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="9bcf2-148">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="9bcf2-149">MOF</span><span class="sxs-lookup"><span data-stu-id="9bcf2-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9bcf2-150"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9bcf2-150"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="9bcf2-151">DLL</span><span class="sxs-lookup"><span data-stu-id="9bcf2-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9bcf2-152"><dt>\\DMWmiBridgeProv.dllfile MOF</dt></span><span class="sxs-lookup"><span data-stu-id="9bcf2-152"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9bcf2-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9bcf2-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bcf2-154">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="9bcf2-154">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

