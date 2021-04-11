---
title: Classe MDM_Policy_Config01_Privacy02
description: La \_ \_ classe Config01 Privacy02 dei criteri MDM \_ rappresenta i criteri di ricerca disponibili.
ms.assetid: 202213b9-5301-4c55-bbc6-6ce3daf705ad
keywords:
- Classe MDM_Policy_Config01_Privacy02
- Classe MDM_Policy_Config01_Privacy02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Privacy02
- MDM_Policy_Config01_Privacy02.InstanceID
- MDM_Policy_Config01_Privacy02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca714dc17db60982e5ba047690886bc88aa79853
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964199"
---
# <a name="mdm_policy_config01_privacy02-class"></a><span data-ttu-id="b2812-105">\_ \_ Classe Config01 Privacy02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="b2812-105">MDM\_Policy\_Config01\_Privacy02 class</span></span>

<span data-ttu-id="b2812-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="b2812-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b2812-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="b2812-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b2812-108">La **classe \_ \_ Config01 \_ Privacy02 dei criteri MDM** rappresenta i criteri di ricerca disponibili.</span><span class="sxs-lookup"><span data-stu-id="b2812-108">The **MDM\_Policy\_Config01\_Privacy02** class represents the search policies available.</span></span>

<span data-ttu-id="b2812-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="b2812-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2812-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b2812-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Privacy02
{
  string InstanceID;
  string ParentID;
  sint32 AllowAutoAcceptPairingAndPrivacyConsentPrompts;
  sint32 AllowInputPersonalization;
  string LetAppsSyncWithDevices_UserInControlOfTheseApps;
  sint32 PublishUserActivities;
  string LetAppsSyncWithDevices_ForceDenyTheseApps;
  string LetAppsSyncWithDevices_ForceAllowTheseApps;
  sint32 LetAppsSyncWithDevices;
  string LetAppsAccessTrustedDevices_UserInControlOfTheseApps;
  string LetAppsRunInBackground_UserInControlOfTheseApps;
  string LetAppsRunInBackground_ForceDenyTheseApps;
  string LetAppsRunInBackground_ForceAllowTheseApps;
  sint32 LetAppsRunInBackground;
  string LetAppsGetDiagnosticInfo_UserInControlOfTheseApps;
  string LetAppsGetDiagnosticInfo_ForceDenyTheseApps;
  string LetAppsGetDiagnosticInfo_ForceAllowTheseApps;
  sint32 LetAppsGetDiagnosticInfo;
  string LetAppsAccessTrustedDevices_ForceDenyTheseApps;
  string LetAppsAccessTrustedDevices_ForceAllowTheseApps;
  sint32 LetAppsAccessTrustedDevices;
  string LetAppsAccessRadios_UserInControlOfTheseApps;
  string LetAppsAccessTasks_UserInControlOfTheseApps;
  string LetAppsAccessTasks_ForceDenyTheseApps;
  string LetAppsAccessTasks_ForceAllowTheseApps;
  sint32 LetAppsAccessTasks;
  string LetAppsAccessRadios_ForceDenyTheseApps;
  string LetAppsAccessRadios_ForceAllowTheseApps;
  sint32 LetAppsAccessRadios;
  string LetAppsAccessPhone_UserInControlOfTheseApps;
  string LetAppsAccessPhone_ForceDenyTheseApps;
  string LetAppsAccessPhone_ForceAllowTheseApps;
  sint32 LetAppsAccessPhone;
  string LetAppsAccessMotion_UserInControlOfTheseApps;
  string LetAppsAccessNotifications_UserInControlOfTheseApps;
  string LetAppsAccessNotifications_ForceDenyTheseApps;
  string LetAppsAccessNotifications_ForceAllowTheseApps;
  sint32 LetAppsAccessNotifications;
  string LetAppsAccessMotion_ForceDenyTheseApps;
  string LetAppsAccessMotion_ForceAllowTheseApps;
  sint32 LetAppsAccessMotion;
  string LetAppsAccessMicrophone_UserInControlOfTheseApps;
  string LetAppsAccessMicrophone_ForceDenyTheseApps;
  string LetAppsAccessMicrophone_ForceAllowTheseApps;
  sint32 LetAppsAccessMicrophone;
  string LetAppsAccessMessaging_UserInControlOfTheseApps;
  string LetAppsAccessMessaging_ForceDenyTheseApps;
  string LetAppsAccessMessaging_ForceAllowTheseApps;
  sint32 LetAppsAccessMessaging;
  string LetAppsAccessLocation_UserInControlOfTheseApps;
  string LetAppsAccessLocation_ForceDenyTheseApps;
  string LetAppsAccessLocation_ForceAllowTheseApps;
  sint32 LetAppsAccessLocation;
  string LetAppsAccessEmail_UserInControlOfTheseApps;
  string LetAppsAccessEmail_ForceDenyTheseApps;
  string LetAppsAccessEmail_ForceAllowTheseApps;
  sint32 LetAppsAccessEmail;
  string LetAppsAccessContacts_UserInControlOfTheseApps;
  string LetAppsAccessContacts_ForceDenyTheseApps;
  string LetAppsAccessContacts_ForceAllowTheseApps;
  sint32 LetAppsAccessContacts;
  string LetAppsAccessCamera_UserInControlOfTheseApps;
  string LetAppsAccessCamera_ForceDenyTheseApps;
  string LetAppsAccessCamera_ForceAllowTheseApps;
  sint32 LetAppsAccessCamera;
  string LetAppsAccessCallHistory_UserInControlOfTheseApps;
  string LetAppsAccessCallHistory_ForceDenyTheseApps;
  string LetAppsAccessCallHistory_ForceAllowTheseApps;
  sint32 LetAppsAccessCallHistory;
  string LetAppsAccessCalendar_UserInControlOfTheseApps;
  string LetAppsAccessCalendar_ForceDenyTheseApps;
  string LetAppsAccessCalendar_ForceAllowTheseApps;
  sint32 LetAppsAccessCalendar;
  string LetAppsAccessAccountInfo_UserInControlOfTheseApps;
  string LetAppsAccessAccountInfo_ForceDenyTheseApps;
  string LetAppsAccessAccountInfo_ForceAllowTheseApps;
  sint32 LetAppsAccessAccountInfo;
  sint32 DisableAdvertisingId;
  sint32 EnableActivityFeed;
};
```

## <a name="members"></a><span data-ttu-id="b2812-111">Members</span><span class="sxs-lookup"><span data-stu-id="b2812-111">Members</span></span>

<span data-ttu-id="b2812-112">La **classe \_ \_ Config01 \_ Privacy02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b2812-112">The **MDM\_Policy\_Config01\_Privacy02** class has these types of members:</span></span>

-   [<span data-ttu-id="b2812-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b2812-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b2812-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b2812-114">Properties</span></span>

<span data-ttu-id="b2812-115">La **classe \_ \_ \_ Privacy02 dei criteri MDM Config01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="b2812-115">The **MDM\_Policy\_Config01\_Privacy02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="b2812-116">AllowAutoAcceptPairingAndPrivacyConsentPrompts</span><span class="sxs-lookup"><span data-stu-id="b2812-116">AllowAutoAcceptPairingAndPrivacyConsentPrompts</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-allowautoacceptpairingandprivacyconsentprompts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-117">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b2812-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2812-119">AllowInputPersonalization</span><span class="sxs-lookup"><span data-stu-id="b2812-119">AllowInputPersonalization</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-allowinputpersonalization)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-120">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b2812-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2812-122">DisableAdvertisingId</span><span class="sxs-lookup"><span data-stu-id="b2812-122">DisableAdvertisingId</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-disableadvertisingid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-123">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b2812-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-124">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2812-125">EnableActivityFeed</span><span class="sxs-lookup"><span data-stu-id="b2812-125">EnableActivityFeed</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-enableactivityfeed)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-126">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b2812-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-127">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b2812-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b2812-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2812-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2812-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2812-131">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b2812-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b2812-132">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="b2812-132">Identifies the name of the parent node.</span></span> <span data-ttu-id="b2812-133">Per questa classe la stringa è "privacy".</span><span class="sxs-lookup"><span data-stu-id="b2812-133">For this class, the string is "Privacy".</span></span>

</dd> <dt>

[<span data-ttu-id="b2812-134">LetAppsAccessAccountInfo</span><span class="sxs-lookup"><span data-stu-id="b2812-134">LetAppsAccessAccountInfo</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessaccountinfo)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-135">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b2812-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-136">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2812-137">\_ForceAllowTheseApps LetAppsAccessAccountInfo</span><span class="sxs-lookup"><span data-stu-id="b2812-137">LetAppsAccessAccountInfo\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessaccountinfo-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-138">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2812-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-139">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2812-140">\_ForceDenyTheseApps LetAppsAccessAccountInfo</span><span class="sxs-lookup"><span data-stu-id="b2812-140">LetAppsAccessAccountInfo\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessaccountinfo-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-141">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2812-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-142">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2812-143">\_UserInControlOfTheseApps LetAppsAccessAccountInfo</span><span class="sxs-lookup"><span data-stu-id="b2812-143">LetAppsAccessAccountInfo\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessaccountinfo-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-144">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2812-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-145">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2812-146">LetAppsAccessCalendar</span><span class="sxs-lookup"><span data-stu-id="b2812-146">LetAppsAccessCalendar</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscalendar)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-147">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b2812-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-148">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2812-149">\_ForceAllowTheseApps LetAppsAccessCalendar</span><span class="sxs-lookup"><span data-stu-id="b2812-149">LetAppsAccessCalendar\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscalendar-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-150">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2812-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-151">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2812-152">\_ForceDenyTheseApps LetAppsAccessCalendar</span><span class="sxs-lookup"><span data-stu-id="b2812-152">LetAppsAccessCalendar\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscalendar-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-153">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2812-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-154">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2812-155">\_UserInControlOfTheseApps LetAppsAccessCalendar</span><span class="sxs-lookup"><span data-stu-id="b2812-155">LetAppsAccessCalendar\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscalendar-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-156">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2812-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-157">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2812-158">LetAppsAccessCallHistory</span><span class="sxs-lookup"><span data-stu-id="b2812-158">LetAppsAccessCallHistory</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscallhistory)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-159">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b2812-159">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-160">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2812-161">\_ForceAllowTheseApps LetAppsAccessCallHistory</span><span class="sxs-lookup"><span data-stu-id="b2812-161">LetAppsAccessCallHistory\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscallhistory-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-162">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2812-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-163">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2812-164">\_ForceDenyTheseApps LetAppsAccessCallHistory</span><span class="sxs-lookup"><span data-stu-id="b2812-164">LetAppsAccessCallHistory\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscallhistory-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-165">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2812-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-166">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2812-167">\_UserInControlOfTheseApps LetAppsAccessCallHistory</span><span class="sxs-lookup"><span data-stu-id="b2812-167">LetAppsAccessCallHistory\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscallhistory-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-168">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2812-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-169">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2812-170">LetAppsAccessCamera</span><span class="sxs-lookup"><span data-stu-id="b2812-170">LetAppsAccessCamera</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscamera)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-171">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b2812-171">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-172">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2812-173">\_ForceAllowTheseApps LetAppsAccessCamera</span><span class="sxs-lookup"><span data-stu-id="b2812-173">LetAppsAccessCamera\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscamera-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-174">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2812-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-175">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2812-176">\_ForceDenyTheseApps LetAppsAccessCamera</span><span class="sxs-lookup"><span data-stu-id="b2812-176">LetAppsAccessCamera\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscamera-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-177">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2812-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-178">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2812-179">\_UserInControlOfTheseApps LetAppsAccessCamera</span><span class="sxs-lookup"><span data-stu-id="b2812-179">LetAppsAccessCamera\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscamera-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-180">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2812-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-181">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2812-182">LetAppsAccessContacts</span><span class="sxs-lookup"><span data-stu-id="b2812-182">LetAppsAccessContacts</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscontacts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-183">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b2812-183">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-184">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2812-185">\_ForceAllowTheseApps LetAppsAccessContacts</span><span class="sxs-lookup"><span data-stu-id="b2812-185">LetAppsAccessContacts\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscontacts-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-186">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2812-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-187">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-187">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2812-188">\_ForceDenyTheseApps LetAppsAccessContacts</span><span class="sxs-lookup"><span data-stu-id="b2812-188">LetAppsAccessContacts\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscontacts-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-189">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2812-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-190">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2812-191">\_UserInControlOfTheseApps LetAppsAccessContacts</span><span class="sxs-lookup"><span data-stu-id="b2812-191">LetAppsAccessContacts\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscontacts-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-192">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2812-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-193">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-193">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2812-194">LetAppsAccessEmail</span><span class="sxs-lookup"><span data-stu-id="b2812-194">LetAppsAccessEmail</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessemail)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-195">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b2812-195">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-196">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-196">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2812-197">\_ForceAllowTheseApps LetAppsAccessEmail</span><span class="sxs-lookup"><span data-stu-id="b2812-197">LetAppsAccessEmail\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessemail-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-198">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2812-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-199">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-199">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2812-200">\_ForceDenyTheseApps LetAppsAccessEmail</span><span class="sxs-lookup"><span data-stu-id="b2812-200">LetAppsAccessEmail\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessemail-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-201">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2812-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-202">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-202">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2812-203">\_UserInControlOfTheseApps LetAppsAccessEmail</span><span class="sxs-lookup"><span data-stu-id="b2812-203">LetAppsAccessEmail\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessemail-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-204">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2812-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-205">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-205">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2812-206">LetAppsAccessLocation</span><span class="sxs-lookup"><span data-stu-id="b2812-206">LetAppsAccessLocation</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesslocation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-207">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b2812-207">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-208">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-208">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2812-209">\_ForceAllowTheseApps LetAppsAccessLocation</span><span class="sxs-lookup"><span data-stu-id="b2812-209">LetAppsAccessLocation\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesslocation-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-210">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2812-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-211">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2812-212">\_ForceDenyTheseApps LetAppsAccessLocation</span><span class="sxs-lookup"><span data-stu-id="b2812-212">LetAppsAccessLocation\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesslocation-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-213">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2812-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-214">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-214">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2812-215">\_UserInControlOfTheseApps LetAppsAccessLocation</span><span class="sxs-lookup"><span data-stu-id="b2812-215">LetAppsAccessLocation\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesslocation-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-216">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2812-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-217">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-217">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2812-218">LetAppsAccessMessaging</span><span class="sxs-lookup"><span data-stu-id="b2812-218">LetAppsAccessMessaging</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmessaging)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-219">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b2812-219">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-220">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-220">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2812-221">\_ForceAllowTheseApps LetAppsAccessMessaging</span><span class="sxs-lookup"><span data-stu-id="b2812-221">LetAppsAccessMessaging\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmessaging-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-222">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2812-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-223">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-223">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2812-224">\_ForceDenyTheseApps LetAppsAccessMessaging</span><span class="sxs-lookup"><span data-stu-id="b2812-224">LetAppsAccessMessaging\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmessaging-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-225">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2812-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-226">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-226">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2812-227">\_UserInControlOfTheseApps LetAppsAccessMessaging</span><span class="sxs-lookup"><span data-stu-id="b2812-227">LetAppsAccessMessaging\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmessaging-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-228">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2812-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-229">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-229">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2812-230">LetAppsAccessMicrophone</span><span class="sxs-lookup"><span data-stu-id="b2812-230">LetAppsAccessMicrophone</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmicrophone)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-231">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b2812-231">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-232">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-232">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2812-233">\_ForceAllowTheseApps LetAppsAccessMicrophone</span><span class="sxs-lookup"><span data-stu-id="b2812-233">LetAppsAccessMicrophone\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmicrophone-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-234">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2812-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-235">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-235">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2812-236">\_ForceDenyTheseApps LetAppsAccessMicrophone</span><span class="sxs-lookup"><span data-stu-id="b2812-236">LetAppsAccessMicrophone\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmicrophone-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-237">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2812-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-238">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-238">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2812-239">\_UserInControlOfTheseApps LetAppsAccessMicrophone</span><span class="sxs-lookup"><span data-stu-id="b2812-239">LetAppsAccessMicrophone\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmicrophone-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-240">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2812-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-241">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-241">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2812-242">LetAppsAccessMotion</span><span class="sxs-lookup"><span data-stu-id="b2812-242">LetAppsAccessMotion</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmotion)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-243">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b2812-243">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-244">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-244">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2812-245">\_ForceAllowTheseApps LetAppsAccessMotion</span><span class="sxs-lookup"><span data-stu-id="b2812-245">LetAppsAccessMotion\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmotion-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-246">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2812-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-247">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-247">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2812-248">\_ForceDenyTheseApps LetAppsAccessMotion</span><span class="sxs-lookup"><span data-stu-id="b2812-248">LetAppsAccessMotion\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmotion-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-249">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2812-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-250">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-250">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2812-251">\_UserInControlOfTheseApps LetAppsAccessMotion</span><span class="sxs-lookup"><span data-stu-id="b2812-251">LetAppsAccessMotion\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmotion-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-252">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2812-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-253">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-253">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2812-254">LetAppsAccessNotifications</span><span class="sxs-lookup"><span data-stu-id="b2812-254">LetAppsAccessNotifications</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessnotifications)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-255">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b2812-255">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-256">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-256">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2812-257">\_ForceAllowTheseApps LetAppsAccessNotifications</span><span class="sxs-lookup"><span data-stu-id="b2812-257">LetAppsAccessNotifications\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessnotifications-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-258">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2812-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-259">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-259">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2812-260">\_ForceDenyTheseApps LetAppsAccessNotifications</span><span class="sxs-lookup"><span data-stu-id="b2812-260">LetAppsAccessNotifications\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessnotifications-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-261">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2812-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-262">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-262">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2812-263">\_UserInControlOfTheseApps LetAppsAccessNotifications</span><span class="sxs-lookup"><span data-stu-id="b2812-263">LetAppsAccessNotifications\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessnotifications-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-264">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2812-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-265">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-265">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2812-266">LetAppsAccessPhone</span><span class="sxs-lookup"><span data-stu-id="b2812-266">LetAppsAccessPhone</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessphone)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-267">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b2812-267">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-268">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-268">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2812-269">\_ForceAllowTheseApps LetAppsAccessPhone</span><span class="sxs-lookup"><span data-stu-id="b2812-269">LetAppsAccessPhone\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessphone-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-270">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2812-270">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-271">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-271">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2812-272">\_ForceDenyTheseApps LetAppsAccessPhone</span><span class="sxs-lookup"><span data-stu-id="b2812-272">LetAppsAccessPhone\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessphone-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-273">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2812-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-274">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-274">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2812-275">\_UserInControlOfTheseApps LetAppsAccessPhone</span><span class="sxs-lookup"><span data-stu-id="b2812-275">LetAppsAccessPhone\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessphone-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-276">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2812-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-277">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-277">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2812-278">LetAppsAccessRadios</span><span class="sxs-lookup"><span data-stu-id="b2812-278">LetAppsAccessRadios</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessradios)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-279">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b2812-279">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-280">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-280">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2812-281">\_ForceAllowTheseApps LetAppsAccessRadios</span><span class="sxs-lookup"><span data-stu-id="b2812-281">LetAppsAccessRadios\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessradios-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-282">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2812-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-283">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-283">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2812-284">\_ForceDenyTheseApps LetAppsAccessRadios</span><span class="sxs-lookup"><span data-stu-id="b2812-284">LetAppsAccessRadios\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessradios-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-285">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2812-285">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-286">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-286">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2812-287">\_UserInControlOfTheseApps LetAppsAccessRadios</span><span class="sxs-lookup"><span data-stu-id="b2812-287">LetAppsAccessRadios\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessradios-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-288">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2812-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-289">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-289">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2812-290">LetAppsAccessTasks</span><span class="sxs-lookup"><span data-stu-id="b2812-290">LetAppsAccessTasks</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstasks)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-291">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b2812-291">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-292">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-292">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2812-293">\_ForceAllowTheseApps LetAppsAccessTasks</span><span class="sxs-lookup"><span data-stu-id="b2812-293">LetAppsAccessTasks\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstasks-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-294">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2812-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-295">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-295">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2812-296">\_ForceDenyTheseApps LetAppsAccessTasks</span><span class="sxs-lookup"><span data-stu-id="b2812-296">LetAppsAccessTasks\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstasks-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-297">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2812-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-298">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-298">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2812-299">\_UserInControlOfTheseApps LetAppsAccessTasks</span><span class="sxs-lookup"><span data-stu-id="b2812-299">LetAppsAccessTasks\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstasks-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-300">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2812-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-301">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-301">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2812-302">LetAppsAccessTrustedDevices</span><span class="sxs-lookup"><span data-stu-id="b2812-302">LetAppsAccessTrustedDevices</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstrusteddevices)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-303">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b2812-303">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-304">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-304">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2812-305">\_ForceAllowTheseApps LetAppsAccessTrustedDevices</span><span class="sxs-lookup"><span data-stu-id="b2812-305">LetAppsAccessTrustedDevices\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstrusteddevices-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-306">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2812-306">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-307">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-307">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2812-308">\_ForceDenyTheseApps LetAppsAccessTrustedDevices</span><span class="sxs-lookup"><span data-stu-id="b2812-308">LetAppsAccessTrustedDevices\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstrusteddevices-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-309">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2812-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-310">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-310">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2812-311">\_UserInControlOfTheseApps LetAppsAccessTrustedDevices</span><span class="sxs-lookup"><span data-stu-id="b2812-311">LetAppsAccessTrustedDevices\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstrusteddevices-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-312">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2812-312">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-313">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-313">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2812-314">LetAppsGetDiagnosticInfo</span><span class="sxs-lookup"><span data-stu-id="b2812-314">LetAppsGetDiagnosticInfo</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsgetdiagnosticinfo)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-315">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b2812-315">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-316">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-316">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2812-317">\_ForceAllowTheseApps LetAppsGetDiagnosticInfo</span><span class="sxs-lookup"><span data-stu-id="b2812-317">LetAppsGetDiagnosticInfo\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsgetdiagnosticinfo-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-318">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2812-318">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-319">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-319">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2812-320">\_ForceDenyTheseApps LetAppsGetDiagnosticInfo</span><span class="sxs-lookup"><span data-stu-id="b2812-320">LetAppsGetDiagnosticInfo\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsgetdiagnosticinfo-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-321">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2812-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-322">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-322">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2812-323">\_UserInControlOfTheseApps LetAppsGetDiagnosticInfo</span><span class="sxs-lookup"><span data-stu-id="b2812-323">LetAppsGetDiagnosticInfo\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsgetdiagnosticinfo-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-324">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2812-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-325">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-325">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2812-326">LetAppsRunInBackground</span><span class="sxs-lookup"><span data-stu-id="b2812-326">LetAppsRunInBackground</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsruninbackground)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-327">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b2812-327">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-328">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-328">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2812-329">\_ForceAllowTheseApps LetAppsRunInBackground</span><span class="sxs-lookup"><span data-stu-id="b2812-329">LetAppsRunInBackground\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsruninbackground-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-330">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2812-330">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-331">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-331">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2812-332">\_ForceDenyTheseApps LetAppsRunInBackground</span><span class="sxs-lookup"><span data-stu-id="b2812-332">LetAppsRunInBackground\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsruninbackground-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-333">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2812-333">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-334">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-334">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2812-335">\_UserInControlOfTheseApps LetAppsRunInBackground</span><span class="sxs-lookup"><span data-stu-id="b2812-335">LetAppsRunInBackground\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsruninbackground-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-336">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2812-336">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-337">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-337">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2812-338">LetAppsSyncWithDevices</span><span class="sxs-lookup"><span data-stu-id="b2812-338">LetAppsSyncWithDevices</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappssyncwithdevices)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-339">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b2812-339">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-340">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-340">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2812-341">\_ForceAllowTheseApps LetAppsSyncWithDevices</span><span class="sxs-lookup"><span data-stu-id="b2812-341">LetAppsSyncWithDevices\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappssyncwithdevices-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-342">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2812-342">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-343">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-343">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2812-344">\_ForceDenyTheseApps LetAppsSyncWithDevices</span><span class="sxs-lookup"><span data-stu-id="b2812-344">LetAppsSyncWithDevices\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappssyncwithdevices-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-345">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2812-345">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-346">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-346">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2812-347">\_UserInControlOfTheseApps LetAppsSyncWithDevices</span><span class="sxs-lookup"><span data-stu-id="b2812-347">LetAppsSyncWithDevices\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappssyncwithdevices-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-348">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2812-348">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-349">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-349">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b2812-350">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="b2812-350">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-351">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2812-351">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-352">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2812-352">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2812-353">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b2812-353">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b2812-354">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="b2812-354">Describes the full path to the parent node.</span></span> <span data-ttu-id="b2812-355">Per questa classe la stringa è "./Vendor/MSFT/Policy/Config"</span><span class="sxs-lookup"><span data-stu-id="b2812-355">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="b2812-356">PublishUserActivities</span><span class="sxs-lookup"><span data-stu-id="b2812-356">PublishUserActivities</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-publishuseractivities)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2812-357">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b2812-357">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2812-358">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2812-358">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b2812-359">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b2812-359">Requirements</span></span>



| <span data-ttu-id="b2812-360">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2812-360">Requirement</span></span> | <span data-ttu-id="b2812-361">Valore</span><span class="sxs-lookup"><span data-stu-id="b2812-361">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2812-362">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b2812-362">Minimum supported client</span></span><br/> | <span data-ttu-id="b2812-363">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="b2812-363">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b2812-364">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b2812-364">Minimum supported server</span></span><br/> | <span data-ttu-id="b2812-365">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="b2812-365">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="b2812-366">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b2812-366">Namespace</span></span><br/>                | <span data-ttu-id="b2812-367">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="b2812-367">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="b2812-368">MOF</span><span class="sxs-lookup"><span data-stu-id="b2812-368">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b2812-369"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b2812-369"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="b2812-370">DLL</span><span class="sxs-lookup"><span data-stu-id="b2812-370">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2812-371"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b2812-371"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2812-372">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b2812-372">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2812-373">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="b2812-373">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

