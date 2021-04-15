---
title: Classe MDM_Policy_Result01_Defender02
description: Il \_ criterio MDM \_ Result01 \_ Defender02class rappresenta i criteri correlati a Windows Defender.
ms.assetid: 82c8a7a2-8369-46c4-aa87-b44b742a274d
keywords:
- Classe MDM_Policy_Result01_Defender02
- Classe MDM_Policy_Result01_Defender02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Defender02
- MDM_Policy_Result01_Defender02.InstanceID
- MDM_Policy_Result01_Defender02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae898751a9f15af1c945efd3e6a473dfe07c7cd7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475892"
---
# <a name="mdm_policy_result01_defender02-class"></a><span data-ttu-id="966e8-105">\_ \_ Classe Result01 Defender02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="966e8-105">MDM\_Policy\_Result01\_Defender02 class</span></span>

<span data-ttu-id="966e8-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="966e8-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="966e8-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="966e8-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="966e8-108">La **classe \_ \_ Result01 \_ Defender02 dei criteri MDM** rappresenta i criteri correlati a Windows Defender</span><span class="sxs-lookup"><span data-stu-id="966e8-108">The **MDM\_Policy\_Result01\_Defender02** class represents policies related to Windows Defender</span></span>

<span data-ttu-id="966e8-109">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="966e8-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="966e8-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="966e8-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Defender02
{
  string InstanceID;
  string ParentID;
  sint32 AllowArchiveScanning;
  sint32 AllowBehaviorMonitoring;
  sint32 AllowCloudProtection;
  sint32 AllowEmailScanning;
  sint32 AllowFullScanOnMappedNetworkDrives;
  sint32 AllowFullScanRemovableDriveScanning;
  sint32 AllowIntrusionPreventionSystem;
  sint32 AllowIOAVProtection;
  sint32 AllowOnAccessProtection;
  sint32 AllowRealtimeMonitoring;
  sint32 AllowScanningNetworkFiles;
  sint32 AllowScriptScanning;
  sint32 AllowUserUIAccess;
  string AttackSurfaceReductionRules;
  string AttackSurfaceReductionOnlyExclusions;
  sint32 AVGCPULoadFactor;
  sint32 CloudExtendedTimeout;
  string ControlledFolderAccessProtectedFolders;
  string ControlledFolderAccessAllowedApplications;
  sint32 CloudBlockLevel;
  sint32 DaysToRetainCleanedMalware;
  sint32 EnableControlledFolderAccess;
  sint32 EnableNetworkProtection;
  sint32 PUAProtection;
  string ExcludedProcesses;
  string ExcludedPaths;
  string ExcludedExtensions;
  sint32 RealTimeScanDirection;
  sint32 ScheduleQuickScanTime;
  sint32 ScheduleScanDay;
  sint32 ScheduleScanTime;
  sint32 SignatureUpdateInterval;
  sint32 SubmitSamplesConsent;
  string ThreatSeverityDefaultAction;
  sint32 ScanParameter;
};
```

## <a name="members"></a><span data-ttu-id="966e8-111">Members</span><span class="sxs-lookup"><span data-stu-id="966e8-111">Members</span></span>

<span data-ttu-id="966e8-112">La **classe \_ \_ Result01 \_ Defender02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="966e8-112">The **MDM\_Policy\_Result01\_Defender02** class has these types of members:</span></span>

-   [<span data-ttu-id="966e8-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="966e8-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="966e8-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="966e8-114">Properties</span></span>

<span data-ttu-id="966e8-115">La **classe \_ \_ \_ Defender02 dei criteri MDM Result01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="966e8-115">The **MDM\_Policy\_Result01\_Defender02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="966e8-116">AllowArchiveScanning</span><span class="sxs-lookup"><span data-stu-id="966e8-116">AllowArchiveScanning</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowarchivescanning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="966e8-117">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="966e8-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="966e8-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="966e8-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="966e8-119">AllowBehaviorMonitoring</span><span class="sxs-lookup"><span data-stu-id="966e8-119">AllowBehaviorMonitoring</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowbehaviormonitoring)
</dt> <dd> <dl> <dt>

<span data-ttu-id="966e8-120">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="966e8-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="966e8-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="966e8-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="966e8-122">AllowCloudProtection</span><span class="sxs-lookup"><span data-stu-id="966e8-122">AllowCloudProtection</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowcloudprotection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="966e8-123">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="966e8-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="966e8-124">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="966e8-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="966e8-125">AllowEmailScanning</span><span class="sxs-lookup"><span data-stu-id="966e8-125">AllowEmailScanning</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowemailscanning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="966e8-126">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="966e8-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="966e8-127">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="966e8-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="966e8-128">AllowFullScanOnMappedNetworkDrives</span><span class="sxs-lookup"><span data-stu-id="966e8-128">AllowFullScanOnMappedNetworkDrives</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowfullscanonmappednetworkdrives)
</dt> <dd> <dl> <dt>

<span data-ttu-id="966e8-129">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="966e8-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="966e8-130">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="966e8-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="966e8-131">AllowFullScanRemovableDriveScanning</span><span class="sxs-lookup"><span data-stu-id="966e8-131">AllowFullScanRemovableDriveScanning</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowfullscanremovabledrivescanning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="966e8-132">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="966e8-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="966e8-133">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="966e8-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="966e8-134">AllowIntrusionPreventionSystem</span><span class="sxs-lookup"><span data-stu-id="966e8-134">AllowIntrusionPreventionSystem</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowintrusionpreventionsystem)
</dt> <dd> <dl> <dt>

<span data-ttu-id="966e8-135">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="966e8-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="966e8-136">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="966e8-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="966e8-137">AllowIOAVProtection</span><span class="sxs-lookup"><span data-stu-id="966e8-137">AllowIOAVProtection</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowioavprotection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="966e8-138">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="966e8-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="966e8-139">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="966e8-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="966e8-140">AllowOnAccessProtection</span><span class="sxs-lookup"><span data-stu-id="966e8-140">AllowOnAccessProtection</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowonaccessprotection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="966e8-141">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="966e8-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="966e8-142">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="966e8-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="966e8-143">AllowRealtimeMonitoring</span><span class="sxs-lookup"><span data-stu-id="966e8-143">AllowRealtimeMonitoring</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowrealtimemonitoring)
</dt> <dd> <dl> <dt>

<span data-ttu-id="966e8-144">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="966e8-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="966e8-145">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="966e8-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="966e8-146">AllowScanningNetworkFiles</span><span class="sxs-lookup"><span data-stu-id="966e8-146">AllowScanningNetworkFiles</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowscanningnetworkfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="966e8-147">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="966e8-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="966e8-148">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="966e8-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="966e8-149">AllowScriptScanning</span><span class="sxs-lookup"><span data-stu-id="966e8-149">AllowScriptScanning</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowscriptscanning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="966e8-150">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="966e8-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="966e8-151">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="966e8-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="966e8-152">AllowUserUIAccess</span><span class="sxs-lookup"><span data-stu-id="966e8-152">AllowUserUIAccess</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowuseruiaccess)
</dt> <dd> <dl> <dt>

<span data-ttu-id="966e8-153">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="966e8-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="966e8-154">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="966e8-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="966e8-155">AttackSurfaceReductionOnlyExclusions</span><span class="sxs-lookup"><span data-stu-id="966e8-155">AttackSurfaceReductionOnlyExclusions</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-attacksurfacereductiononlyexclusions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="966e8-156">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="966e8-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="966e8-157">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="966e8-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="966e8-158">AttackSurfaceReductionRules</span><span class="sxs-lookup"><span data-stu-id="966e8-158">AttackSurfaceReductionRules</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-attacksurfacereductionrules)
</dt> <dd> <dl> <dt>

<span data-ttu-id="966e8-159">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="966e8-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="966e8-160">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="966e8-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="966e8-161">AVGCPULoadFactor</span><span class="sxs-lookup"><span data-stu-id="966e8-161">AVGCPULoadFactor</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-avgcpuloadfactor)
</dt> <dd> <dl> <dt>

<span data-ttu-id="966e8-162">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="966e8-162">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="966e8-163">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="966e8-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="966e8-164">CloudBlockLevel</span><span class="sxs-lookup"><span data-stu-id="966e8-164">CloudBlockLevel</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-cloudblocklevel)
</dt> <dd> <dl> <dt>

<span data-ttu-id="966e8-165">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="966e8-165">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="966e8-166">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="966e8-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="966e8-167">CloudExtendedTimeout</span><span class="sxs-lookup"><span data-stu-id="966e8-167">CloudExtendedTimeout</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-cloudextendedtimeout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="966e8-168">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="966e8-168">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="966e8-169">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="966e8-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="966e8-170">ControlledFolderAccessAllowedApplications</span><span class="sxs-lookup"><span data-stu-id="966e8-170">ControlledFolderAccessAllowedApplications</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-controlledfolderaccessallowedapplications)
</dt> <dd> <dl> <dt>

<span data-ttu-id="966e8-171">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="966e8-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="966e8-172">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="966e8-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="966e8-173">ControlledFolderAccessProtectedFolders</span><span class="sxs-lookup"><span data-stu-id="966e8-173">ControlledFolderAccessProtectedFolders</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-controlledfolderaccessprotectedfolders)
</dt> <dd> <dl> <dt>

<span data-ttu-id="966e8-174">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="966e8-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="966e8-175">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="966e8-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="966e8-176">DaysToRetainCleanedMalware</span><span class="sxs-lookup"><span data-stu-id="966e8-176">DaysToRetainCleanedMalware</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-daystoretaincleanedmalware)
</dt> <dd> <dl> <dt>

<span data-ttu-id="966e8-177">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="966e8-177">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="966e8-178">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="966e8-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="966e8-179">EnableControlledFolderAccess</span><span class="sxs-lookup"><span data-stu-id="966e8-179">EnableControlledFolderAccess</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-enablecontrolledfolderaccess)
</dt> <dd> <dl> <dt>

<span data-ttu-id="966e8-180">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="966e8-180">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="966e8-181">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="966e8-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="966e8-182">EnableNetworkProtection</span><span class="sxs-lookup"><span data-stu-id="966e8-182">EnableNetworkProtection</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-enablenetworkprotection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="966e8-183">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="966e8-183">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="966e8-184">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="966e8-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="966e8-185">ExcludedExtensions</span><span class="sxs-lookup"><span data-stu-id="966e8-185">ExcludedExtensions</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-excludedextensions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="966e8-186">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="966e8-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="966e8-187">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="966e8-187">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="966e8-188">ExcludedPaths</span><span class="sxs-lookup"><span data-stu-id="966e8-188">ExcludedPaths</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-excludedpaths)
</dt> <dd> <dl> <dt>

<span data-ttu-id="966e8-189">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="966e8-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="966e8-190">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="966e8-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="966e8-191">ExcludedProcesses</span><span class="sxs-lookup"><span data-stu-id="966e8-191">ExcludedProcesses</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-excludedprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="966e8-192">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="966e8-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="966e8-193">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="966e8-193">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="966e8-194">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="966e8-194">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="966e8-195">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="966e8-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="966e8-196">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="966e8-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="966e8-197">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="966e8-197">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="966e8-198">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="966e8-198">Identifies the name of the parent node.</span></span> <span data-ttu-id="966e8-199">Per questa classe la stringa è "Defender".</span><span class="sxs-lookup"><span data-stu-id="966e8-199">For this class, the string is "Defender".</span></span>

</dd> <dt>

<span data-ttu-id="966e8-200">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="966e8-200">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="966e8-201">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="966e8-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="966e8-202">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="966e8-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="966e8-203">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="966e8-203">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="966e8-204">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="966e8-204">Describes the full path to the parent node.</span></span> <span data-ttu-id="966e8-205">Per questa classe la stringa è "./Vendor/MSFT/Policy/Result"</span><span class="sxs-lookup"><span data-stu-id="966e8-205">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="966e8-206">PUAProtection</span><span class="sxs-lookup"><span data-stu-id="966e8-206">PUAProtection</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-puaprotection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="966e8-207">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="966e8-207">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="966e8-208">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="966e8-208">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="966e8-209">RealTimeScanDirection</span><span class="sxs-lookup"><span data-stu-id="966e8-209">RealTimeScanDirection</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-realtimescandirection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="966e8-210">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="966e8-210">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="966e8-211">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="966e8-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="966e8-212">ScanParameter</span><span class="sxs-lookup"><span data-stu-id="966e8-212">ScanParameter</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-scanparameter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="966e8-213">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="966e8-213">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="966e8-214">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="966e8-214">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="966e8-215">ScheduleQuickScanTime</span><span class="sxs-lookup"><span data-stu-id="966e8-215">ScheduleQuickScanTime</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-schedulequickscantime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="966e8-216">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="966e8-216">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="966e8-217">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="966e8-217">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="966e8-218">ScheduleScanDay</span><span class="sxs-lookup"><span data-stu-id="966e8-218">ScheduleScanDay</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-schedulescanday)
</dt> <dd> <dl> <dt>

<span data-ttu-id="966e8-219">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="966e8-219">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="966e8-220">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="966e8-220">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="966e8-221">ScheduleScanTime</span><span class="sxs-lookup"><span data-stu-id="966e8-221">ScheduleScanTime</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-schedulescantime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="966e8-222">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="966e8-222">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="966e8-223">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="966e8-223">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="966e8-224">SignatureUpdateInterval</span><span class="sxs-lookup"><span data-stu-id="966e8-224">SignatureUpdateInterval</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-signatureupdateinterval)
</dt> <dd> <dl> <dt>

<span data-ttu-id="966e8-225">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="966e8-225">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="966e8-226">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="966e8-226">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="966e8-227">SubmitSamplesConsent</span><span class="sxs-lookup"><span data-stu-id="966e8-227">SubmitSamplesConsent</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-submitsamplesconsent)
</dt> <dd> <dl> <dt>

<span data-ttu-id="966e8-228">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="966e8-228">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="966e8-229">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="966e8-229">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="966e8-230">ThreatSeverityDefaultAction</span><span class="sxs-lookup"><span data-stu-id="966e8-230">ThreatSeverityDefaultAction</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-threatseveritydefaultaction)
</dt> <dd> <dl> <dt>

<span data-ttu-id="966e8-231">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="966e8-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="966e8-232">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="966e8-232">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="966e8-233">Requisiti</span><span class="sxs-lookup"><span data-stu-id="966e8-233">Requirements</span></span>



| <span data-ttu-id="966e8-234">Requisito</span><span class="sxs-lookup"><span data-stu-id="966e8-234">Requirement</span></span> | <span data-ttu-id="966e8-235">Valore</span><span class="sxs-lookup"><span data-stu-id="966e8-235">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="966e8-236">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="966e8-236">Minimum supported client</span></span><br/> | <span data-ttu-id="966e8-237">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="966e8-237">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="966e8-238">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="966e8-238">Minimum supported server</span></span><br/> | <span data-ttu-id="966e8-239">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="966e8-239">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="966e8-240">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="966e8-240">Namespace</span></span><br/>                | <span data-ttu-id="966e8-241">\\ \\ DMMap MDM CIMv2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="966e8-241">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="966e8-242">MOF</span><span class="sxs-lookup"><span data-stu-id="966e8-242">MOF</span></span><br/>                      | <dl> <span data-ttu-id="966e8-243"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="966e8-243"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="966e8-244">DLL</span><span class="sxs-lookup"><span data-stu-id="966e8-244">DLL</span></span><br/>                      | <dl> <span data-ttu-id="966e8-245"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="966e8-245"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="966e8-246">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="966e8-246">See also</span></span>

<dl> <dt>

[<span data-ttu-id="966e8-247">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="966e8-247">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

