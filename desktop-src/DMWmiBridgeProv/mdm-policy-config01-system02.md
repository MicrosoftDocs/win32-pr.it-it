---
title: Classe MDM_Policy_Config01_System02
description: La \_ classe System02 dei criteri MDM \_ Config01 \_ rappresenta i criteri di sistema disponibili.
ms.assetid: 0C3E21DF-309C-4AF3-8682-E921BF45BDEF
keywords:
- Classe MDM_Policy_ConfigSource01_System02
- Classe MDM_Policy_ConfigSource01_System02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_ConfigSource01_System02
- MDM_Policy_ConfigSource01_System02.InstanceID
- MDM_Policy_ConfigSource01_System02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d45ae8061b3e383abdd075d461d5b6dc2c46a053
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741674"
---
# <a name="mdm_policy_config01_system02-class"></a><span data-ttu-id="13cd5-105">\_ \_ Classe Config01 System02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="13cd5-105">MDM\_Policy\_Config01\_System02 class</span></span>

<span data-ttu-id="13cd5-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="13cd5-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="13cd5-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="13cd5-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="13cd5-108">La **classe \_ \_ \_ System02 dei criteri MDM Config01** rappresenta i criteri di sistema disponibili.</span><span class="sxs-lookup"><span data-stu-id="13cd5-108">The **MDM\_Policy\_Config01\_System02** class represents the System policies available.</span></span> <span data-ttu-id="13cd5-109">Questi criteri determinano le configurazioni di sistema consentite.</span><span class="sxs-lookup"><span data-stu-id="13cd5-109">These policies determine System configurations that are allowed.</span></span>

<span data-ttu-id="13cd5-110">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="13cd5-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="13cd5-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="13cd5-111">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_System02
{
  string InstanceID = "System";
  string ParentID;
  sint32 AllowBuildPreview;
  sint32 AllowEmbeddedMode;
  sint32 AllowExperimentation;
  sint32 AllowFontProviders;
  sint32 AllowLocation;
  sint32 AllowStorageCard;
  sint32 AllowTelemetry;
  string TelemetryProxy;
  sint32 AllowUserToResetPhone;
  string BootStartDriverInitialization;
  sint32 DisableEnterpriseAuthProxy;
  sint32 DisableOneDriveFileSync;
  string DisableSystemRestore;
  sint32 LimitEnhancedDiagnosticDataWindowsAnalytics;
  sint32 FeedbackHubAlwaysSaveDiagnosticsLocally;
};
```

## <a name="members"></a><span data-ttu-id="13cd5-112">Members</span><span class="sxs-lookup"><span data-stu-id="13cd5-112">Members</span></span>

<span data-ttu-id="13cd5-113">La **classe \_ \_ ConfigSource01 \_ System02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="13cd5-113">The **MDM\_Policy\_ConfigSource01\_System02** class has these types of members:</span></span>

-   [<span data-ttu-id="13cd5-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="13cd5-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="13cd5-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="13cd5-115">Properties</span></span>

<span data-ttu-id="13cd5-116">La **classe \_ \_ \_ System02 dei criteri MDM ConfigSource01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="13cd5-116">The **MDM\_Policy\_ConfigSource01\_System02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="13cd5-117">AllowBuildPreview</span><span class="sxs-lookup"><span data-stu-id="13cd5-117">AllowBuildPreview</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowbuildpreview)
</dt> <dd> <dl> <dt>

<span data-ttu-id="13cd5-118">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="13cd5-118">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="13cd5-119">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="13cd5-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="13cd5-120">AllowEmbeddedMode</span><span class="sxs-lookup"><span data-stu-id="13cd5-120">AllowEmbeddedMode</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowembeddedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="13cd5-121">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="13cd5-121">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="13cd5-122">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="13cd5-122">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="13cd5-123">AllowExperimentation</span><span class="sxs-lookup"><span data-stu-id="13cd5-123">AllowExperimentation</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowexperimentation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="13cd5-124">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="13cd5-124">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="13cd5-125">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="13cd5-125">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="13cd5-126">AllowFontProviders</span><span class="sxs-lookup"><span data-stu-id="13cd5-126">AllowFontProviders</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowfontproviders)
</dt> <dd> <dl> <dt>

<span data-ttu-id="13cd5-127">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="13cd5-127">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="13cd5-128">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="13cd5-128">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="13cd5-129">AllowLocation</span><span class="sxs-lookup"><span data-stu-id="13cd5-129">AllowLocation</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowlocation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="13cd5-130">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="13cd5-130">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="13cd5-131">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="13cd5-131">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="13cd5-132">AllowStorageCard</span><span class="sxs-lookup"><span data-stu-id="13cd5-132">AllowStorageCard</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowstoragecard)
</dt> <dd> <dl> <dt>

<span data-ttu-id="13cd5-133">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="13cd5-133">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="13cd5-134">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="13cd5-134">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="13cd5-135">AllowTelemetry</span><span class="sxs-lookup"><span data-stu-id="13cd5-135">AllowTelemetry</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowtelemetry)
</dt> <dd> <dl> <dt>

<span data-ttu-id="13cd5-136">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="13cd5-136">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="13cd5-137">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="13cd5-137">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="13cd5-138">AllowUserToResetPhone</span><span class="sxs-lookup"><span data-stu-id="13cd5-138">AllowUserToResetPhone</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowusertoresetphone)
</dt> <dd> <dl> <dt>

<span data-ttu-id="13cd5-139">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="13cd5-139">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="13cd5-140">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="13cd5-140">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="13cd5-141">BootStartDriverInitialization</span><span class="sxs-lookup"><span data-stu-id="13cd5-141">BootStartDriverInitialization</span></span>](/windows/client-management/mdm/policy-csp-system#system-bootstartdriverinitialization)
</dt> <dd> <dl> <dt>

<span data-ttu-id="13cd5-142">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="13cd5-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13cd5-143">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="13cd5-143">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="13cd5-144">DisableEnterpriseAuthProxy</span><span class="sxs-lookup"><span data-stu-id="13cd5-144">DisableEnterpriseAuthProxy</span></span>](/windows/client-management/mdm/policy-csp-system#system-disableenterpriseauthproxy)
</dt> <dd> <dl> <dt>

<span data-ttu-id="13cd5-145">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="13cd5-145">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="13cd5-146">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="13cd5-146">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="13cd5-147">DisableOneDriveFileSync</span><span class="sxs-lookup"><span data-stu-id="13cd5-147">DisableOneDriveFileSync</span></span>](/windows/client-management/mdm/policy-csp-system#system-disableonedrivefilesync)
</dt> <dd> <dl> <dt>

<span data-ttu-id="13cd5-148">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="13cd5-148">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="13cd5-149">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="13cd5-149">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="13cd5-150">DisableSystemRestore</span><span class="sxs-lookup"><span data-stu-id="13cd5-150">DisableSystemRestore</span></span>](/windows/client-management/mdm/policy-csp-system#system-disablesystemrestore)
</dt> <dd> <dl> <dt>

<span data-ttu-id="13cd5-151">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="13cd5-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13cd5-152">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="13cd5-152">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="13cd5-153">FeedbackHubAlwaysSaveDiagnosticsLocally</span><span class="sxs-lookup"><span data-stu-id="13cd5-153">FeedbackHubAlwaysSaveDiagnosticsLocally</span></span>](/windows/client-management/mdm/policy-csp-system#system-feedbackhubalwayssavediagnosticslocally)
</dt> <dd> <dl> <dt>

<span data-ttu-id="13cd5-154">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="13cd5-154">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="13cd5-155">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="13cd5-155">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="13cd5-156">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="13cd5-156">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13cd5-157">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="13cd5-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13cd5-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="13cd5-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13cd5-159">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="13cd5-159">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="13cd5-160">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="13cd5-160">Identifies the name of the parent node.</span></span> <span data-ttu-id="13cd5-161">Per questa classe la stringa è "System".</span><span class="sxs-lookup"><span data-stu-id="13cd5-161">For this class, the string is "System".</span></span>

</dd> <dt>

[<span data-ttu-id="13cd5-162">LimitEnhancedDiagnosticDataWindowsAnalytics</span><span class="sxs-lookup"><span data-stu-id="13cd5-162">LimitEnhancedDiagnosticDataWindowsAnalytics</span></span>](/windows/client-management/mdm/policy-csp-system#system-limitenhanceddiagnosticdatawindowsanalytics)
</dt> <dd> <dl> <dt>

<span data-ttu-id="13cd5-163">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="13cd5-163">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="13cd5-164">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="13cd5-164">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="13cd5-165">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="13cd5-165">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13cd5-166">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="13cd5-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13cd5-167">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="13cd5-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13cd5-168">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="13cd5-168">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="13cd5-169">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="13cd5-169">Describes the full path to the parent node.</span></span> <span data-ttu-id="13cd5-170">Per questa classe la stringa è "./Vendor/MSFT/Policy/Config"</span><span class="sxs-lookup"><span data-stu-id="13cd5-170">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

<span data-ttu-id="13cd5-171">"./Vendor/MSFT/Policy/Config"</span><span class="sxs-lookup"><span data-stu-id="13cd5-171">"./Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="13cd5-172">TelemetryProxy</span><span class="sxs-lookup"><span data-stu-id="13cd5-172">TelemetryProxy</span></span>](/windows/client-management/mdm/policy-csp-system#system-telemetryproxy)
</dt> <dd> <dl> <dt>

<span data-ttu-id="13cd5-173">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="13cd5-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13cd5-174">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="13cd5-174">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="13cd5-175">Requisiti</span><span class="sxs-lookup"><span data-stu-id="13cd5-175">Requirements</span></span>



| <span data-ttu-id="13cd5-176">Requisito</span><span class="sxs-lookup"><span data-stu-id="13cd5-176">Requirement</span></span> | <span data-ttu-id="13cd5-177">Valore</span><span class="sxs-lookup"><span data-stu-id="13cd5-177">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13cd5-178">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="13cd5-178">Minimum supported client</span></span><br/> | <span data-ttu-id="13cd5-179">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="13cd5-179">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="13cd5-180">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="13cd5-180">Minimum supported server</span></span><br/> | <span data-ttu-id="13cd5-181">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="13cd5-181">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="13cd5-182">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="13cd5-182">Namespace</span></span><br/>                | <span data-ttu-id="13cd5-183">\\ \\ DMMap MDM CIMv2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="13cd5-183">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="13cd5-184">MOF</span><span class="sxs-lookup"><span data-stu-id="13cd5-184">MOF</span></span><br/>                      | <dl> <span data-ttu-id="13cd5-185"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="13cd5-185"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="13cd5-186">DLL</span><span class="sxs-lookup"><span data-stu-id="13cd5-186">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13cd5-187"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13cd5-187"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13cd5-188">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="13cd5-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13cd5-189">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="13cd5-189">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

