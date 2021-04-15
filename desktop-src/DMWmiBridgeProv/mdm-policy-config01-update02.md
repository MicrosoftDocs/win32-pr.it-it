---
title: Classe MDM_Policy_Config01_Privacy02
description: La \_ classe Update02 dei criteri MDM \_ Config01 \_ rappresenta i criteri di aggiornamento disponibili.
ms.assetid: 7324912c-7ac5-42fd-baee-f7e2d81de023
keywords:
- Classe MDM_Policy_Config01_Privacy02
- Classe MDM_Policy_Config01_Update02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Update02
- MDM_Policy_Config01_Update02.InstanceID
- MDM_Policy_Config01_Update02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3044fc527fd23d49fac383dc25778d3a978b2788
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476918"
---
# <a name="mdm_policy_config01_update02-class"></a><span data-ttu-id="4a00a-105">\_ \_ Classe Config01 Update02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="4a00a-105">MDM\_Policy\_Config01\_Update02 class</span></span>

<span data-ttu-id="4a00a-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="4a00a-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="4a00a-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="4a00a-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="4a00a-108">La **classe \_ \_ \_ Update02 dei criteri MDM Config01** rappresenta i criteri di aggiornamento disponibili.</span><span class="sxs-lookup"><span data-stu-id="4a00a-108">The **MDM\_Policy\_Config01\_Update02** class represents the update policies available.</span></span>

<span data-ttu-id="4a00a-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="4a00a-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a00a-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4a00a-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Update02
{
  string InstanceID;
  string ParentID;
  sint32 RequireUpdateApproval;
  sint32 AllowAutoUpdate;
  sint32 AllowAutoWindowsUpdateDownloadOverMeteredNetwork;
  sint32 AllowMUUpdateService;
  sint32 ScheduledInstallDay;
  sint32 ScheduledInstallThirdWeek;
  sint32 ScheduledInstallSecondWeek;
  sint32 ScheduledInstallFourthWeek;
  sint32 ScheduledInstallFirstWeek;
  sint32 ScheduledInstallEveryWeek;
  sint32 ScheduledInstallTime;
  sint32 AllowUpdateService;
  sint32 DeferQualityUpdatesPeriodInDays;
  sint32 DeferFeatureUpdatesPeriodInDays;
  sint32 BranchReadinessLevel;
  string UpdateServiceUrl;
  sint32 SetEDURestart;
  sint32 AutoRestartDeadlinePeriodInDays;
  string UpdateServiceUrlAlternate;
  sint32 FillEmptyContentUrls;
  sint32 AllowNonMicrosoftSignedUpdate;
  sint32 RequireDeferUpgrade;
  sint32 PauseDeferrals;
  sint32 PauseQualityUpdates;
  sint32 PhoneUpdateRestrictions;
  string PauseQualityUpdatesStartTime;
  sint32 PauseFeatureUpdates;
  string PauseFeatureUpdatesStartTime;
  sint32 DeferUpgradePeriod;
  sint32 ExcludeWUDriversInQualityUpdate;
  sint32 IgnoreMOUpdateDownloadLimit;
  sint32 ManagePreviewBuilds;
  sint32 IgnoreMOAppDownloadLimit;
  sint32 DeferUpdatePeriod;
  sint32 ActiveHoursEnd;
  sint32 ActiveHoursStart;
  sint32 DetectionFrequency;
  sint32 DisableDualScan;
  sint32 EngagedRestartDeadline;
  sint32 EngagedRestartSnoozeSchedule;
  sint32 EngagedRestartTransitionSchedule;
  sint32 ScheduleImminentRestartWarning;
  sint32 ScheduleRestartWarning;
  sint32 SetAutoRestartNotificationDisable;
  sint32 AutoRestartNotificationSchedule;
  sint32 AutoRestartRequiredNotificationDismissal;
  sint32 ActiveHoursMaxRange;
};
```

## <a name="members"></a><span data-ttu-id="4a00a-111">Members</span><span class="sxs-lookup"><span data-stu-id="4a00a-111">Members</span></span>

<span data-ttu-id="4a00a-112">La **classe \_ \_ Config01 \_ Update02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="4a00a-112">The **MDM\_Policy\_Config01\_Update02** class has these types of members:</span></span>

-   [<span data-ttu-id="4a00a-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4a00a-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4a00a-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4a00a-114">Properties</span></span>

<span data-ttu-id="4a00a-115">La **classe \_ \_ \_ Update02 dei criteri MDM Config01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="4a00a-115">The **MDM\_Policy\_Config01\_Update02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="4a00a-116">ActiveHoursEnd</span><span class="sxs-lookup"><span data-stu-id="4a00a-116">ActiveHoursEnd</span></span>](/windows/client-management/mdm/policy-csp-update#update-activehoursend)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a00a-117">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="4a00a-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4a00a-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4a00a-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4a00a-119">ActiveHoursMaxRange</span><span class="sxs-lookup"><span data-stu-id="4a00a-119">ActiveHoursMaxRange</span></span>](/windows/client-management/mdm/policy-csp-update#update-activehoursmaxrange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a00a-120">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="4a00a-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4a00a-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4a00a-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4a00a-122">ActiveHoursStart</span><span class="sxs-lookup"><span data-stu-id="4a00a-122">ActiveHoursStart</span></span>](/windows/client-management/mdm/policy-csp-update#update-activehoursstart)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a00a-123">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="4a00a-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4a00a-124">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4a00a-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4a00a-125">AllowAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="4a00a-125">AllowAutoUpdate</span></span>](/windows/client-management/mdm/policy-csp-update#update-allowautoupdate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a00a-126">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="4a00a-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4a00a-127">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4a00a-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4a00a-128">AllowAutoWindowsUpdateDownloadOverMeteredNetwork</span><span class="sxs-lookup"><span data-stu-id="4a00a-128">AllowAutoWindowsUpdateDownloadOverMeteredNetwork</span></span>](/windows/client-management/mdm/policy-csp-update#update-allowautowindowsupdatedownloadovermeterednetwork)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a00a-129">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="4a00a-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4a00a-130">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4a00a-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4a00a-131">AllowMUUpdateService</span><span class="sxs-lookup"><span data-stu-id="4a00a-131">AllowMUUpdateService</span></span>](/windows/client-management/mdm/policy-csp-update#update-allowmuupdateservice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a00a-132">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="4a00a-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4a00a-133">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4a00a-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4a00a-134">AllowNonMicrosoftSignedUpdate</span><span class="sxs-lookup"><span data-stu-id="4a00a-134">AllowNonMicrosoftSignedUpdate</span></span>](/windows/client-management/mdm/policy-csp-update#update-allownonmicrosoftsignedupdate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a00a-135">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="4a00a-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4a00a-136">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4a00a-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4a00a-137">AllowUpdateService</span><span class="sxs-lookup"><span data-stu-id="4a00a-137">AllowUpdateService</span></span>](/windows/client-management/mdm/policy-csp-update#update-allowupdateservice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a00a-138">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="4a00a-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4a00a-139">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4a00a-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4a00a-140">AutoRestartDeadlinePeriodInDays</span><span class="sxs-lookup"><span data-stu-id="4a00a-140">AutoRestartDeadlinePeriodInDays</span></span>](/windows/client-management/mdm/policy-csp-update#update-autorestartdeadlineperiodindays)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a00a-141">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="4a00a-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4a00a-142">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4a00a-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4a00a-143">AutoRestartNotificationSchedule</span><span class="sxs-lookup"><span data-stu-id="4a00a-143">AutoRestartNotificationSchedule</span></span>](/windows/client-management/mdm/policy-csp-update#update-autorestartnotificationschedule)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a00a-144">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="4a00a-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4a00a-145">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4a00a-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4a00a-146">AutoRestartRequiredNotificationDismissal</span><span class="sxs-lookup"><span data-stu-id="4a00a-146">AutoRestartRequiredNotificationDismissal</span></span>](/windows/client-management/mdm/policy-csp-update#update-autorestartrequirednotificationdismissal)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a00a-147">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="4a00a-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4a00a-148">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4a00a-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4a00a-149">BranchReadinessLevel</span><span class="sxs-lookup"><span data-stu-id="4a00a-149">BranchReadinessLevel</span></span>](/windows/client-management/mdm/policy-csp-update#update-branchreadinesslevel)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a00a-150">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="4a00a-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4a00a-151">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4a00a-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4a00a-152">DeferFeatureUpdatesPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="4a00a-152">DeferFeatureUpdatesPeriodInDays</span></span>](/windows/client-management/mdm/policy-csp-update#update-deferfeatureupdatesperiodindays)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a00a-153">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="4a00a-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4a00a-154">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4a00a-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4a00a-155">DeferQualityUpdatesPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="4a00a-155">DeferQualityUpdatesPeriodInDays</span></span>](/windows/client-management/mdm/policy-csp-update#update-deferqualityupdatesperiodindays)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a00a-156">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="4a00a-156">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4a00a-157">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4a00a-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4a00a-158">DeferUpdatePeriod</span><span class="sxs-lookup"><span data-stu-id="4a00a-158">DeferUpdatePeriod</span></span>](/windows/client-management/mdm/policy-csp-update#update-deferupdateperiod)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a00a-159">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="4a00a-159">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4a00a-160">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4a00a-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4a00a-161">DeferUpgradePeriod</span><span class="sxs-lookup"><span data-stu-id="4a00a-161">DeferUpgradePeriod</span></span>](/windows/client-management/mdm/policy-csp-update#update-deferupgradeperiod)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a00a-162">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="4a00a-162">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4a00a-163">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4a00a-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4a00a-164">DetectionFrequency</span><span class="sxs-lookup"><span data-stu-id="4a00a-164">DetectionFrequency</span></span>](/windows/client-management/mdm/policy-csp-update#update-detectionfrequency)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a00a-165">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="4a00a-165">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4a00a-166">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4a00a-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4a00a-167">DisableDualScan</span><span class="sxs-lookup"><span data-stu-id="4a00a-167">DisableDualScan</span></span>](/windows/client-management/mdm/policy-csp-update#update-disabledualscan)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a00a-168">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="4a00a-168">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4a00a-169">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4a00a-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4a00a-170">EngagedRestartDeadline</span><span class="sxs-lookup"><span data-stu-id="4a00a-170">EngagedRestartDeadline</span></span>](/windows/client-management/mdm/policy-csp-update#update-engagedrestartdeadline)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a00a-171">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="4a00a-171">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4a00a-172">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4a00a-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4a00a-173">EngagedRestartSnoozeSchedule</span><span class="sxs-lookup"><span data-stu-id="4a00a-173">EngagedRestartSnoozeSchedule</span></span>](/windows/client-management/mdm/policy-csp-update#update-engagedrestartsnoozeschedule)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a00a-174">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="4a00a-174">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4a00a-175">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4a00a-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4a00a-176">EngagedRestartTransitionSchedule</span><span class="sxs-lookup"><span data-stu-id="4a00a-176">EngagedRestartTransitionSchedule</span></span>](/windows/client-management/mdm/policy-csp-update#update-engagedrestarttransitionschedule)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a00a-177">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="4a00a-177">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4a00a-178">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4a00a-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4a00a-179">ExcludeWUDriversInQualityUpdate</span><span class="sxs-lookup"><span data-stu-id="4a00a-179">ExcludeWUDriversInQualityUpdate</span></span>](/windows/client-management/mdm/policy-csp-update#update-excludewudriversinqualityupdate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a00a-180">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="4a00a-180">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4a00a-181">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4a00a-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4a00a-182">FillEmptyContentUrls</span><span class="sxs-lookup"><span data-stu-id="4a00a-182">FillEmptyContentUrls</span></span>](/windows/client-management/mdm/policy-csp-update#update-fillemptycontenturls)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a00a-183">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="4a00a-183">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4a00a-184">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4a00a-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4a00a-185">IgnoreMOAppDownloadLimit</span><span class="sxs-lookup"><span data-stu-id="4a00a-185">IgnoreMOAppDownloadLimit</span></span>](/windows/client-management/mdm/policy-csp-update#update-ignoremoappdownloadlimit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a00a-186">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="4a00a-186">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4a00a-187">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4a00a-187">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4a00a-188">IgnoreMOUpdateDownloadLimit</span><span class="sxs-lookup"><span data-stu-id="4a00a-188">IgnoreMOUpdateDownloadLimit</span></span>](/windows/client-management/mdm/policy-csp-update#update-ignoremoupdatedownloadlimit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a00a-189">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="4a00a-189">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4a00a-190">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4a00a-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4a00a-191">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="4a00a-191">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a00a-192">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4a00a-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4a00a-193">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4a00a-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4a00a-194">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4a00a-194">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="4a00a-195">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="4a00a-195">Identifies the name of the parent node.</span></span> <span data-ttu-id="4a00a-196">Per questa classe la stringa è "Update".</span><span class="sxs-lookup"><span data-stu-id="4a00a-196">For this class, the string is "Update"</span></span>

</dd> <dt>

[<span data-ttu-id="4a00a-197">ManagePreviewBuilds</span><span class="sxs-lookup"><span data-stu-id="4a00a-197">ManagePreviewBuilds</span></span>](/windows/client-management/mdm/policy-csp-update#update-managepreviewbuilds)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a00a-198">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="4a00a-198">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4a00a-199">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4a00a-199">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4a00a-200">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="4a00a-200">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a00a-201">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4a00a-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4a00a-202">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4a00a-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4a00a-203">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4a00a-203">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="4a00a-204">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="4a00a-204">Describes the full path to the parent node.</span></span> <span data-ttu-id="4a00a-205">Per questa classe la stringa è "./Vendor/MSFT/Policy/Config"</span><span class="sxs-lookup"><span data-stu-id="4a00a-205">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="4a00a-206">PauseDeferrals</span><span class="sxs-lookup"><span data-stu-id="4a00a-206">PauseDeferrals</span></span>](/windows/client-management/mdm/policy-csp-update#update-pausedeferrals)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a00a-207">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="4a00a-207">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4a00a-208">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4a00a-208">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4a00a-209">PauseFeatureUpdates</span><span class="sxs-lookup"><span data-stu-id="4a00a-209">PauseFeatureUpdates</span></span>](/windows/client-management/mdm/policy-csp-update#update-pausefeatureupdates)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a00a-210">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="4a00a-210">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4a00a-211">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4a00a-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4a00a-212">PauseFeatureUpdatesStartTime</span><span class="sxs-lookup"><span data-stu-id="4a00a-212">PauseFeatureUpdatesStartTime</span></span>](/windows/client-management/mdm/policy-csp-update#update-pausefeatureupdatesstarttime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a00a-213">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4a00a-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4a00a-214">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4a00a-214">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4a00a-215">PauseQualityUpdates</span><span class="sxs-lookup"><span data-stu-id="4a00a-215">PauseQualityUpdates</span></span>](/windows/client-management/mdm/policy-csp-update#update-pausequalityupdates)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a00a-216">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="4a00a-216">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4a00a-217">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4a00a-217">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4a00a-218">PauseQualityUpdatesStartTime</span><span class="sxs-lookup"><span data-stu-id="4a00a-218">PauseQualityUpdatesStartTime</span></span>](/windows/client-management/mdm/policy-csp-update#update-pausequalityupdatesstarttime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a00a-219">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4a00a-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4a00a-220">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4a00a-220">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4a00a-221">PhoneUpdateRestrictions</span><span class="sxs-lookup"><span data-stu-id="4a00a-221">PhoneUpdateRestrictions</span></span>](/windows/client-management/mdm/policy-csp-update#update-phoneupdaterestrictions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a00a-222">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="4a00a-222">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4a00a-223">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4a00a-223">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4a00a-224">RequireDeferUpgrade</span><span class="sxs-lookup"><span data-stu-id="4a00a-224">RequireDeferUpgrade</span></span>](/windows/client-management/mdm/policy-csp-update#update-requiredeferupgrade)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a00a-225">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="4a00a-225">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4a00a-226">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4a00a-226">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4a00a-227">RequireUpdateApproval</span><span class="sxs-lookup"><span data-stu-id="4a00a-227">RequireUpdateApproval</span></span>](/windows/client-management/mdm/policy-csp-update#update-requireupdateapproval)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a00a-228">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="4a00a-228">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4a00a-229">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4a00a-229">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4a00a-230">ScheduledInstallDay</span><span class="sxs-lookup"><span data-stu-id="4a00a-230">ScheduledInstallDay</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstallday)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a00a-231">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="4a00a-231">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4a00a-232">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4a00a-232">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4a00a-233">ScheduledInstallEveryWeek</span><span class="sxs-lookup"><span data-stu-id="4a00a-233">ScheduledInstallEveryWeek</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstalleveryweek)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a00a-234">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="4a00a-234">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4a00a-235">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4a00a-235">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4a00a-236">ScheduledInstallFirstWeek</span><span class="sxs-lookup"><span data-stu-id="4a00a-236">ScheduledInstallFirstWeek</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstallfirstweek)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a00a-237">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="4a00a-237">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4a00a-238">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4a00a-238">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4a00a-239">ScheduledInstallFourthWeek</span><span class="sxs-lookup"><span data-stu-id="4a00a-239">ScheduledInstallFourthWeek</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstallfourthweek)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a00a-240">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="4a00a-240">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4a00a-241">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4a00a-241">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4a00a-242">ScheduledInstallSecondWeek</span><span class="sxs-lookup"><span data-stu-id="4a00a-242">ScheduledInstallSecondWeek</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstallsecondweek)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a00a-243">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="4a00a-243">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4a00a-244">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4a00a-244">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4a00a-245">ScheduledInstallThirdWeek</span><span class="sxs-lookup"><span data-stu-id="4a00a-245">ScheduledInstallThirdWeek</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstallthirdweek)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a00a-246">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="4a00a-246">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4a00a-247">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4a00a-247">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4a00a-248">ScheduledInstallTime</span><span class="sxs-lookup"><span data-stu-id="4a00a-248">ScheduledInstallTime</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstalltime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a00a-249">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="4a00a-249">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4a00a-250">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4a00a-250">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4a00a-251">ScheduleImminentRestartWarning</span><span class="sxs-lookup"><span data-stu-id="4a00a-251">ScheduleImminentRestartWarning</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduleimminentrestartwarning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a00a-252">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="4a00a-252">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4a00a-253">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4a00a-253">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4a00a-254">ScheduleRestartWarning</span><span class="sxs-lookup"><span data-stu-id="4a00a-254">ScheduleRestartWarning</span></span>](/windows/client-management/mdm/policy-csp-update#update-schedulerestartwarning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a00a-255">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="4a00a-255">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4a00a-256">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4a00a-256">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4a00a-257">SetAutoRestartNotificationDisable</span><span class="sxs-lookup"><span data-stu-id="4a00a-257">SetAutoRestartNotificationDisable</span></span>](/windows/client-management/mdm/policy-csp-update#update-setautorestartnotificationdisable)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a00a-258">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="4a00a-258">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4a00a-259">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4a00a-259">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4a00a-260">SetEDURestart</span><span class="sxs-lookup"><span data-stu-id="4a00a-260">SetEDURestart</span></span>](/windows/client-management/mdm/policy-csp-update#update-setedurestart)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a00a-261">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="4a00a-261">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4a00a-262">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4a00a-262">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4a00a-263">UpdateServiceUrl</span><span class="sxs-lookup"><span data-stu-id="4a00a-263">UpdateServiceUrl</span></span>](/windows/client-management/mdm/policy-csp-update#update-updateserviceurl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a00a-264">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4a00a-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4a00a-265">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4a00a-265">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4a00a-266">UpdateServiceUrlAlternate</span><span class="sxs-lookup"><span data-stu-id="4a00a-266">UpdateServiceUrlAlternate</span></span>](/windows/client-management/mdm/policy-csp-update#update-updateserviceurlalternate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a00a-267">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4a00a-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4a00a-268">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4a00a-268">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4a00a-269">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4a00a-269">Requirements</span></span>



| <span data-ttu-id="4a00a-270">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a00a-270">Requirement</span></span> | <span data-ttu-id="4a00a-271">Valore</span><span class="sxs-lookup"><span data-stu-id="4a00a-271">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a00a-272">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4a00a-272">Minimum supported client</span></span><br/> | <span data-ttu-id="4a00a-273">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="4a00a-273">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4a00a-274">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4a00a-274">Minimum supported server</span></span><br/> | <span data-ttu-id="4a00a-275">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="4a00a-275">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="4a00a-276">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4a00a-276">Namespace</span></span><br/>                | <span data-ttu-id="4a00a-277">\\ \\ DMMap MDM CIMv2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="4a00a-277">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="4a00a-278">MOF</span><span class="sxs-lookup"><span data-stu-id="4a00a-278">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4a00a-279"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4a00a-279"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="4a00a-280">DLL</span><span class="sxs-lookup"><span data-stu-id="4a00a-280">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4a00a-281"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a00a-281"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a00a-282">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4a00a-282">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a00a-283">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="4a00a-283">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

