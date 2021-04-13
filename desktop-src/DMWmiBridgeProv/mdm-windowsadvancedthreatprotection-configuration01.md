---
title: Classe MDM_WindowsAdvancedThreatProtection_Configuration01
description: La \_ classe MDM WindowsAdvancedThreatProtection \_ Configuration01 viene usata per determinare la configurazione degli endpoint di Windows Defender Advanced Threat Protection (WDATP).
ms.assetid: b4b2ff02-3836-4044-b8fa-d3405f433d8c
keywords:
- Classe MDM_WindowsAdvancedThreatProtection_Configuration01
- Classe MDM_WindowsAdvancedThreatProtection_Configuration01, descritta
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MDM_WindowsAdvancedThreatProtection_Configuration01
- MDM_WindowsAdvancedThreatProtection_Configuration01.InstanceID
- MDM_WindowsAdvancedThreatProtection_Configuration01.ParentID
- MDM_WindowsAdvancedThreatProtection_Configuration01.GroupIds
api_type:
- DllExport
api_location:
- Mofs\DMWmiBridgeProv.dll
ms.openlocfilehash: c6cd6689a66735790c381ac307a443c08464a379
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518424"
---
# <a name="mdm_windowsadvancedthreatprotection_configuration01-class"></a><span data-ttu-id="2704b-105">\_Classe MDM WindowsAdvancedThreatProtection \_ Configuration01</span><span class="sxs-lookup"><span data-stu-id="2704b-105">MDM\_WindowsAdvancedThreatProtection\_Configuration01 class</span></span>

<span data-ttu-id="2704b-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="2704b-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="2704b-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="2704b-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="2704b-108">La classe **MDM \_ WindowsAdvancedThreatProtection \_ Configuration01** viene usata per determinare la configurazione degli endpoint di Windows Defender Advanced Threat Protection (WDATP).</span><span class="sxs-lookup"><span data-stu-id="2704b-108">The **MDM\_WindowsAdvancedThreatProtection\_Configuration01** class is used to determine the configuration of Windows Defender Advanced Threat Protection (WDATP) endpoints.</span></span>

<span data-ttu-id="2704b-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="2704b-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2704b-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2704b-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_WindowsAdvancedThreatProtection_Configuration01
{
  string InstanceID;
  string ParentID;
  sint32 SampleSharing;
  string GroupIds;
  sint32 TelemetryReportingFrequency;
};
```

## <a name="members"></a><span data-ttu-id="2704b-111">Members</span><span class="sxs-lookup"><span data-stu-id="2704b-111">Members</span></span>

<span data-ttu-id="2704b-112">La classe **MDM \_ WindowsAdvancedThreatProtection \_ Configuration01** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="2704b-112">The **MDM\_WindowsAdvancedThreatProtection\_Configuration01** class has these types of members:</span></span>

-   [<span data-ttu-id="2704b-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2704b-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2704b-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2704b-114">Properties</span></span>

<span data-ttu-id="2704b-115">La classe **MDM \_ WindowsAdvancedThreatProtection \_ Configuration01** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="2704b-115">The **MDM\_WindowsAdvancedThreatProtection\_Configuration01** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2704b-116">**GroupID**</span><span class="sxs-lookup"><span data-stu-id="2704b-116">**GroupIds**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2704b-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2704b-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2704b-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="2704b-118">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2704b-119">TBD</span><span class="sxs-lookup"><span data-stu-id="2704b-119">TBD</span></span>

</dd> <dt>

<span data-ttu-id="2704b-120">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2704b-120">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2704b-121">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2704b-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2704b-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2704b-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2704b-123">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2704b-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2704b-124">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="2704b-124">Identifies the name of the parent node.</span></span> <span data-ttu-id="2704b-125">Per questa classe la stringa è "Configuration".</span><span class="sxs-lookup"><span data-stu-id="2704b-125">For this class, the string is "Configuration".</span></span>

</dd> <dt>

<span data-ttu-id="2704b-126">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="2704b-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2704b-127">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2704b-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2704b-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2704b-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2704b-129">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2704b-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2704b-130">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="2704b-130">Describes the full path to the parent node.</span></span> <span data-ttu-id="2704b-131">Per questa classe la stringa è "./Vendor/MSFT/WindowsAdvancedThreatProtection"</span><span class="sxs-lookup"><span data-stu-id="2704b-131">For this class, the string is "./Vendor/MSFT/WindowsAdvancedThreatProtection"</span></span>

</dd> <dt>

[<span data-ttu-id="2704b-132">SampleSharing</span><span class="sxs-lookup"><span data-stu-id="2704b-132">SampleSharing</span></span>](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#configuration-samplesharing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2704b-133">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="2704b-133">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2704b-134">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="2704b-134">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2704b-135">TelemetryReportingFrequency</span><span class="sxs-lookup"><span data-stu-id="2704b-135">TelemetryReportingFrequency</span></span>](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#configuration-telemetryreportingfrequency)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2704b-136">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="2704b-136">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2704b-137">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="2704b-137">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2704b-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2704b-138">Requirements</span></span>



| <span data-ttu-id="2704b-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="2704b-139">Requirement</span></span> | <span data-ttu-id="2704b-140">Valore</span><span class="sxs-lookup"><span data-stu-id="2704b-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2704b-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2704b-141">Minimum supported client</span></span><br/> | <span data-ttu-id="2704b-142">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="2704b-142">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="2704b-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2704b-143">Minimum supported server</span></span><br/> | <span data-ttu-id="2704b-144">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="2704b-144">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="2704b-145">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2704b-145">Namespace</span></span><br/>                | <span data-ttu-id="2704b-146">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="2704b-146">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="2704b-147">MOF</span><span class="sxs-lookup"><span data-stu-id="2704b-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2704b-148"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2704b-148"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="2704b-149">DLL</span><span class="sxs-lookup"><span data-stu-id="2704b-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2704b-150"><dt>\\DMWmiBridgeProv.dllfile MOF</dt></span><span class="sxs-lookup"><span data-stu-id="2704b-150"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2704b-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2704b-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2704b-152">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="2704b-152">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

