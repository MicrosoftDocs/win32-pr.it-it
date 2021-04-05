---
title: Classe MDM_Policy_Result01_System02
description: La \_ classe System02 dei criteri MDM \_ Result01 \_ rappresenta i criteri di sistema disponibili.
ms.assetid: 9A0D9688-9062-429F-897F-75705DC8FD79
keywords:
- Classe MDM_Policy_Result01_System02
- Classe MDM_Policy_Result01_System02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_System02
- MDM_Policy_Result01_System02.InstanceID
- MDM_Policy_Result01_System02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffedc3c4e0eda857c071a3174690ad9677fd97da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741194"
---
# <a name="mdm_policy_result01_system02-class"></a><span data-ttu-id="5fac2-105">\_ \_ Classe Result01 System02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="5fac2-105">MDM\_Policy\_Result01\_System02 class</span></span>

<span data-ttu-id="5fac2-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="5fac2-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="5fac2-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="5fac2-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="5fac2-108">La **classe \_ \_ \_ System02 dei criteri MDM Result01** rappresenta i criteri di sistema disponibili.</span><span class="sxs-lookup"><span data-stu-id="5fac2-108">The **MDM\_Policy\_Result01\_System02** class represents the System policies available.</span></span> <span data-ttu-id="5fac2-109">Questi criteri determinano le configurazioni di sistema consentite.</span><span class="sxs-lookup"><span data-stu-id="5fac2-109">These policies determine System configurations that are allowed.</span></span>

<span data-ttu-id="5fac2-110">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="5fac2-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fac2-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5fac2-111">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_System02
{
  string InstanceID;
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

## <a name="members"></a><span data-ttu-id="5fac2-112">Members</span><span class="sxs-lookup"><span data-stu-id="5fac2-112">Members</span></span>

<span data-ttu-id="5fac2-113">La **classe \_ \_ Result01 \_ System02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="5fac2-113">The **MDM\_Policy\_Result01\_System02** class has these types of members:</span></span>

-   [<span data-ttu-id="5fac2-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5fac2-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5fac2-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5fac2-115">Properties</span></span>

<span data-ttu-id="5fac2-116">La **classe \_ \_ \_ System02 dei criteri MDM Result01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="5fac2-116">The **MDM\_Policy\_Result01\_System02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="5fac2-117">AllowBuildPreview</span><span class="sxs-lookup"><span data-stu-id="5fac2-117">AllowBuildPreview</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowbuildpreview)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fac2-118">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5fac2-118">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5fac2-119">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5fac2-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5fac2-120">AllowEmbeddedMode</span><span class="sxs-lookup"><span data-stu-id="5fac2-120">AllowEmbeddedMode</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowembeddedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fac2-121">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5fac2-121">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5fac2-122">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5fac2-122">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5fac2-123">AllowExperimentation</span><span class="sxs-lookup"><span data-stu-id="5fac2-123">AllowExperimentation</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowexperimentation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fac2-124">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5fac2-124">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5fac2-125">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5fac2-125">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5fac2-126">AllowFontProviders</span><span class="sxs-lookup"><span data-stu-id="5fac2-126">AllowFontProviders</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowfontproviders)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fac2-127">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5fac2-127">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5fac2-128">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5fac2-128">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5fac2-129">AllowLocation</span><span class="sxs-lookup"><span data-stu-id="5fac2-129">AllowLocation</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowlocation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fac2-130">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5fac2-130">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5fac2-131">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5fac2-131">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5fac2-132">AllowStorageCard</span><span class="sxs-lookup"><span data-stu-id="5fac2-132">AllowStorageCard</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowstoragecard)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fac2-133">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5fac2-133">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5fac2-134">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5fac2-134">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5fac2-135">AllowTelemetry</span><span class="sxs-lookup"><span data-stu-id="5fac2-135">AllowTelemetry</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowtelemetry)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fac2-136">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5fac2-136">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5fac2-137">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5fac2-137">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5fac2-138">AllowUserToResetPhone</span><span class="sxs-lookup"><span data-stu-id="5fac2-138">AllowUserToResetPhone</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowusertoresetphone)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fac2-139">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5fac2-139">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5fac2-140">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5fac2-140">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5fac2-141">BootStartDriverInitialization</span><span class="sxs-lookup"><span data-stu-id="5fac2-141">BootStartDriverInitialization</span></span>](/windows/client-management/mdm/policy-csp-system#system-bootstartdriverinitialization)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fac2-142">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5fac2-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5fac2-143">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5fac2-143">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5fac2-144">DisableEnterpriseAuthProxy</span><span class="sxs-lookup"><span data-stu-id="5fac2-144">DisableEnterpriseAuthProxy</span></span>](/windows/client-management/mdm/policy-csp-system#system-disableenterpriseauthproxy)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fac2-145">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5fac2-145">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5fac2-146">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5fac2-146">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5fac2-147">DisableOneDriveFileSync</span><span class="sxs-lookup"><span data-stu-id="5fac2-147">DisableOneDriveFileSync</span></span>](/windows/client-management/mdm/policy-csp-system#system-disableonedrivefilesync)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fac2-148">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5fac2-148">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5fac2-149">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5fac2-149">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5fac2-150">DisableSystemRestore</span><span class="sxs-lookup"><span data-stu-id="5fac2-150">DisableSystemRestore</span></span>](/windows/client-management/mdm/policy-csp-system#system-disablesystemrestore)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fac2-151">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5fac2-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5fac2-152">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5fac2-152">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5fac2-153">FeedbackHubAlwaysSaveDiagnosticsLocally</span><span class="sxs-lookup"><span data-stu-id="5fac2-153">FeedbackHubAlwaysSaveDiagnosticsLocally</span></span>](/windows/client-management/mdm/policy-csp-system#system-feedbackhubalwayssavediagnosticslocally)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fac2-154">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5fac2-154">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5fac2-155">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5fac2-155">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5fac2-156">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="5fac2-156">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fac2-157">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5fac2-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5fac2-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5fac2-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5fac2-159">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5fac2-159">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5fac2-160">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="5fac2-160">Identifies the name of the parent node.</span></span> <span data-ttu-id="5fac2-161">Per questa classe la stringa è "System".</span><span class="sxs-lookup"><span data-stu-id="5fac2-161">For this class, the string is "System".</span></span>

</dd> <dt>

[<span data-ttu-id="5fac2-162">LimitEnhancedDiagnosticDataWindowsAnalytics</span><span class="sxs-lookup"><span data-stu-id="5fac2-162">LimitEnhancedDiagnosticDataWindowsAnalytics</span></span>](/windows/client-management/mdm/policy-csp-system#system-limitenhanceddiagnosticdatawindowsanalytics)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fac2-163">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5fac2-163">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5fac2-164">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5fac2-164">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5fac2-165">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="5fac2-165">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fac2-166">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5fac2-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5fac2-167">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5fac2-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5fac2-168">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5fac2-168">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5fac2-169">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="5fac2-169">Describes the full path to the parent node.</span></span> <span data-ttu-id="5fac2-170">Per questa classe la stringa è "./Vendor/MSFT/Policy/Result"</span><span class="sxs-lookup"><span data-stu-id="5fac2-170">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="5fac2-171">TelemetryProxy</span><span class="sxs-lookup"><span data-stu-id="5fac2-171">TelemetryProxy</span></span>](/windows/client-management/mdm/policy-csp-system#system-telemetryproxy)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fac2-172">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5fac2-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5fac2-173">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5fac2-173">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5fac2-174">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5fac2-174">Requirements</span></span>



| <span data-ttu-id="5fac2-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="5fac2-175">Requirement</span></span> | <span data-ttu-id="5fac2-176">Valore</span><span class="sxs-lookup"><span data-stu-id="5fac2-176">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fac2-177">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5fac2-177">Minimum supported client</span></span><br/> | <span data-ttu-id="5fac2-178">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="5fac2-178">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5fac2-179">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5fac2-179">Minimum supported server</span></span><br/> | <span data-ttu-id="5fac2-180">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="5fac2-180">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="5fac2-181">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5fac2-181">Namespace</span></span><br/>                | <span data-ttu-id="5fac2-182">\\ \\ DMMap MDM CIMv2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="5fac2-182">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="5fac2-183">MOF</span><span class="sxs-lookup"><span data-stu-id="5fac2-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5fac2-184"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5fac2-184"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="5fac2-185">DLL</span><span class="sxs-lookup"><span data-stu-id="5fac2-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5fac2-186"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5fac2-186"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5fac2-187">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5fac2-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fac2-188">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="5fac2-188">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

