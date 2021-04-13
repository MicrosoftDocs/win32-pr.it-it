---
title: Classe MDM_Policy_Result01_Privacy02
description: La \_ \_ classe Result01 Privacy02 dei criteri MDM \_ rappresenta i criteri di ricerca disponibili.
ms.assetid: 40aa1b74-bdec-471d-a7d4-89e59bf8637c
keywords:
- Classe MDM_Policy_Result01_Privacy02
- Classe MDM_Policy_Result01_Privacy02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Privacy02
- MDM_Policy_Result01_Privacy02.InstanceID
- MDM_Policy_Result01_Privacy02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80bbe28d1c0bc1258ec3c9fb57fd592a97c96026
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475323"
---
# <a name="mdm_policy_result01_privacy02-class"></a><span data-ttu-id="94193-105">\_ \_ Classe Result01 Privacy02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="94193-105">MDM\_Policy\_Result01\_Privacy02 class</span></span>

<span data-ttu-id="94193-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="94193-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="94193-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="94193-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="94193-108">La **classe \_ \_ Result01 \_ Privacy02 dei criteri MDM** rappresenta i criteri di ricerca disponibili.</span><span class="sxs-lookup"><span data-stu-id="94193-108">The **MDM\_Policy\_Result01\_Privacy02** class represents the search policies available.</span></span>

<span data-ttu-id="94193-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="94193-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="94193-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="94193-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Privacy02
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

## <a name="members"></a><span data-ttu-id="94193-111">Members</span><span class="sxs-lookup"><span data-stu-id="94193-111">Members</span></span>

<span data-ttu-id="94193-112">La **classe \_ \_ Result01 \_ Privacy02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="94193-112">The **MDM\_Policy\_Result01\_Privacy02** class has these types of members:</span></span>

-   [<span data-ttu-id="94193-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="94193-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="94193-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="94193-114">Properties</span></span>

<span data-ttu-id="94193-115">La **classe \_ \_ \_ Privacy02 dei criteri MDM Result01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="94193-115">The **MDM\_Policy\_Result01\_Privacy02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="94193-116">AllowAutoAcceptPairingAndPrivacyConsentPrompts</span><span class="sxs-lookup"><span data-stu-id="94193-116">AllowAutoAcceptPairingAndPrivacyConsentPrompts</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-allowautoacceptpairingandprivacyconsentprompts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-117">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="94193-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="94193-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94193-119">AllowInputPersonalization</span><span class="sxs-lookup"><span data-stu-id="94193-119">AllowInputPersonalization</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-allowinputpersonalization)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-120">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="94193-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="94193-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94193-122">DisableAdvertisingId</span><span class="sxs-lookup"><span data-stu-id="94193-122">DisableAdvertisingId</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-disableadvertisingid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-123">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="94193-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="94193-124">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94193-125">EnableActivityFeed</span><span class="sxs-lookup"><span data-stu-id="94193-125">EnableActivityFeed</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-enableactivityfeed)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-126">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="94193-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="94193-127">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="94193-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="94193-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94193-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94193-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="94193-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94193-131">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="94193-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="94193-132">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="94193-132">Identifies the name of the parent node.</span></span> <span data-ttu-id="94193-133">Per questa classe la stringa è "privacy".</span><span class="sxs-lookup"><span data-stu-id="94193-133">For this class, the string is "Privacy".</span></span>

</dd> <dt>

[<span data-ttu-id="94193-134">LetAppsAccessAccountInfo</span><span class="sxs-lookup"><span data-stu-id="94193-134">LetAppsAccessAccountInfo</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessaccountinfo)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-135">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="94193-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="94193-136">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94193-137">\_ForceAllowTheseApps LetAppsAccessAccountInfo</span><span class="sxs-lookup"><span data-stu-id="94193-137">LetAppsAccessAccountInfo\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessaccountinfo-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-138">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94193-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94193-139">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94193-140">\_ForceDenyTheseApps LetAppsAccessAccountInfo</span><span class="sxs-lookup"><span data-stu-id="94193-140">LetAppsAccessAccountInfo\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessaccountinfo-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-141">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94193-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94193-142">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94193-143">\_UserInControlOfTheseApps LetAppsAccessAccountInfo</span><span class="sxs-lookup"><span data-stu-id="94193-143">LetAppsAccessAccountInfo\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessaccountinfo-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-144">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94193-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94193-145">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94193-146">LetAppsAccessCalendar</span><span class="sxs-lookup"><span data-stu-id="94193-146">LetAppsAccessCalendar</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscalendar)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-147">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="94193-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="94193-148">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94193-149">\_ForceAllowTheseApps LetAppsAccessCalendar</span><span class="sxs-lookup"><span data-stu-id="94193-149">LetAppsAccessCalendar\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscalendar-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-150">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94193-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94193-151">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94193-152">\_ForceDenyTheseApps LetAppsAccessCalendar</span><span class="sxs-lookup"><span data-stu-id="94193-152">LetAppsAccessCalendar\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscalendar-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-153">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94193-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94193-154">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94193-155">\_UserInControlOfTheseApps LetAppsAccessCalendar</span><span class="sxs-lookup"><span data-stu-id="94193-155">LetAppsAccessCalendar\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscalendar-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-156">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94193-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94193-157">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94193-158">LetAppsAccessCallHistory</span><span class="sxs-lookup"><span data-stu-id="94193-158">LetAppsAccessCallHistory</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscallhistory)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-159">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="94193-159">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="94193-160">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94193-161">\_ForceAllowTheseApps LetAppsAccessCallHistory</span><span class="sxs-lookup"><span data-stu-id="94193-161">LetAppsAccessCallHistory\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscallhistory-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-162">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94193-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94193-163">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94193-164">\_ForceDenyTheseApps LetAppsAccessCallHistory</span><span class="sxs-lookup"><span data-stu-id="94193-164">LetAppsAccessCallHistory\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscallhistory-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-165">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94193-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94193-166">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94193-167">\_UserInControlOfTheseApps LetAppsAccessCallHistory</span><span class="sxs-lookup"><span data-stu-id="94193-167">LetAppsAccessCallHistory\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscallhistory-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-168">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94193-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94193-169">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94193-170">LetAppsAccessCamera</span><span class="sxs-lookup"><span data-stu-id="94193-170">LetAppsAccessCamera</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscamera)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-171">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="94193-171">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="94193-172">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94193-173">\_ForceAllowTheseApps LetAppsAccessCamera</span><span class="sxs-lookup"><span data-stu-id="94193-173">LetAppsAccessCamera\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscamera-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-174">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94193-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94193-175">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94193-176">\_ForceDenyTheseApps LetAppsAccessCamera</span><span class="sxs-lookup"><span data-stu-id="94193-176">LetAppsAccessCamera\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscamera-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-177">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94193-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94193-178">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94193-179">\_UserInControlOfTheseApps LetAppsAccessCamera</span><span class="sxs-lookup"><span data-stu-id="94193-179">LetAppsAccessCamera\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscamera-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-180">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94193-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94193-181">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94193-182">LetAppsAccessContacts</span><span class="sxs-lookup"><span data-stu-id="94193-182">LetAppsAccessContacts</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscontacts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-183">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="94193-183">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="94193-184">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94193-185">\_ForceAllowTheseApps LetAppsAccessContacts</span><span class="sxs-lookup"><span data-stu-id="94193-185">LetAppsAccessContacts\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscontacts-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-186">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94193-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94193-187">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-187">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94193-188">\_ForceDenyTheseApps LetAppsAccessContacts</span><span class="sxs-lookup"><span data-stu-id="94193-188">LetAppsAccessContacts\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscontacts-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-189">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94193-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94193-190">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94193-191">\_UserInControlOfTheseApps LetAppsAccessContacts</span><span class="sxs-lookup"><span data-stu-id="94193-191">LetAppsAccessContacts\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscontacts-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-192">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94193-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94193-193">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-193">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94193-194">LetAppsAccessEmail</span><span class="sxs-lookup"><span data-stu-id="94193-194">LetAppsAccessEmail</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessemail)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-195">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="94193-195">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="94193-196">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-196">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94193-197">\_ForceAllowTheseApps LetAppsAccessEmail</span><span class="sxs-lookup"><span data-stu-id="94193-197">LetAppsAccessEmail\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessemail-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-198">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94193-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94193-199">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-199">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94193-200">\_ForceDenyTheseApps LetAppsAccessEmail</span><span class="sxs-lookup"><span data-stu-id="94193-200">LetAppsAccessEmail\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessemail-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-201">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94193-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94193-202">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-202">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94193-203">\_UserInControlOfTheseApps LetAppsAccessEmail</span><span class="sxs-lookup"><span data-stu-id="94193-203">LetAppsAccessEmail\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessemail-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-204">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94193-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94193-205">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-205">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94193-206">LetAppsAccessLocation</span><span class="sxs-lookup"><span data-stu-id="94193-206">LetAppsAccessLocation</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesslocation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-207">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="94193-207">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="94193-208">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-208">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94193-209">\_ForceAllowTheseApps LetAppsAccessLocation</span><span class="sxs-lookup"><span data-stu-id="94193-209">LetAppsAccessLocation\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesslocation-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-210">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94193-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94193-211">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94193-212">\_ForceDenyTheseApps LetAppsAccessLocation</span><span class="sxs-lookup"><span data-stu-id="94193-212">LetAppsAccessLocation\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesslocation-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-213">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94193-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94193-214">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-214">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94193-215">\_UserInControlOfTheseApps LetAppsAccessLocation</span><span class="sxs-lookup"><span data-stu-id="94193-215">LetAppsAccessLocation\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesslocation-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-216">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94193-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94193-217">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-217">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94193-218">LetAppsAccessMessaging</span><span class="sxs-lookup"><span data-stu-id="94193-218">LetAppsAccessMessaging</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmessaging)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-219">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="94193-219">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="94193-220">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-220">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94193-221">\_ForceAllowTheseApps LetAppsAccessMessaging</span><span class="sxs-lookup"><span data-stu-id="94193-221">LetAppsAccessMessaging\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmessaging-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-222">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94193-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94193-223">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-223">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94193-224">\_ForceDenyTheseApps LetAppsAccessMessaging</span><span class="sxs-lookup"><span data-stu-id="94193-224">LetAppsAccessMessaging\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmessaging-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-225">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94193-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94193-226">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-226">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94193-227">\_UserInControlOfTheseApps LetAppsAccessMessaging</span><span class="sxs-lookup"><span data-stu-id="94193-227">LetAppsAccessMessaging\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmessaging-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-228">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94193-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94193-229">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-229">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94193-230">LetAppsAccessMicrophone</span><span class="sxs-lookup"><span data-stu-id="94193-230">LetAppsAccessMicrophone</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmicrophone)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-231">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="94193-231">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="94193-232">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-232">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94193-233">\_ForceAllowTheseApps LetAppsAccessMicrophone</span><span class="sxs-lookup"><span data-stu-id="94193-233">LetAppsAccessMicrophone\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmicrophone-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-234">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94193-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94193-235">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-235">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94193-236">\_ForceDenyTheseApps LetAppsAccessMicrophone</span><span class="sxs-lookup"><span data-stu-id="94193-236">LetAppsAccessMicrophone\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmicrophone-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-237">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94193-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94193-238">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-238">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94193-239">\_UserInControlOfTheseApps LetAppsAccessMicrophone</span><span class="sxs-lookup"><span data-stu-id="94193-239">LetAppsAccessMicrophone\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmicrophone-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-240">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94193-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94193-241">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-241">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94193-242">LetAppsAccessMotion</span><span class="sxs-lookup"><span data-stu-id="94193-242">LetAppsAccessMotion</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmotion)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-243">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="94193-243">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="94193-244">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-244">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94193-245">\_ForceAllowTheseApps LetAppsAccessMotion</span><span class="sxs-lookup"><span data-stu-id="94193-245">LetAppsAccessMotion\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmotion-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-246">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94193-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94193-247">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-247">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94193-248">\_ForceDenyTheseApps LetAppsAccessMotion</span><span class="sxs-lookup"><span data-stu-id="94193-248">LetAppsAccessMotion\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmotion-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-249">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94193-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94193-250">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-250">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94193-251">\_UserInControlOfTheseApps LetAppsAccessMotion</span><span class="sxs-lookup"><span data-stu-id="94193-251">LetAppsAccessMotion\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmotion-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-252">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94193-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94193-253">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-253">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94193-254">LetAppsAccessNotifications</span><span class="sxs-lookup"><span data-stu-id="94193-254">LetAppsAccessNotifications</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessnotifications)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-255">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="94193-255">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="94193-256">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-256">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94193-257">\_ForceAllowTheseApps LetAppsAccessNotifications</span><span class="sxs-lookup"><span data-stu-id="94193-257">LetAppsAccessNotifications\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessnotifications-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-258">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94193-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94193-259">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-259">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94193-260">\_ForceDenyTheseApps LetAppsAccessNotifications</span><span class="sxs-lookup"><span data-stu-id="94193-260">LetAppsAccessNotifications\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessnotifications-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-261">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94193-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94193-262">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-262">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94193-263">\_UserInControlOfTheseApps LetAppsAccessNotifications</span><span class="sxs-lookup"><span data-stu-id="94193-263">LetAppsAccessNotifications\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessnotifications-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-264">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94193-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94193-265">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-265">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94193-266">LetAppsAccessPhone</span><span class="sxs-lookup"><span data-stu-id="94193-266">LetAppsAccessPhone</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessphone)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-267">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="94193-267">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="94193-268">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-268">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94193-269">\_ForceAllowTheseApps LetAppsAccessPhone</span><span class="sxs-lookup"><span data-stu-id="94193-269">LetAppsAccessPhone\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessphone-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-270">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94193-270">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94193-271">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-271">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94193-272">\_ForceDenyTheseApps LetAppsAccessPhone</span><span class="sxs-lookup"><span data-stu-id="94193-272">LetAppsAccessPhone\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessphone-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-273">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94193-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94193-274">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-274">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94193-275">\_UserInControlOfTheseApps LetAppsAccessPhone</span><span class="sxs-lookup"><span data-stu-id="94193-275">LetAppsAccessPhone\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessphone-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-276">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94193-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94193-277">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-277">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94193-278">LetAppsAccessRadios</span><span class="sxs-lookup"><span data-stu-id="94193-278">LetAppsAccessRadios</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessradios)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-279">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="94193-279">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="94193-280">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-280">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94193-281">\_ForceAllowTheseApps LetAppsAccessRadios</span><span class="sxs-lookup"><span data-stu-id="94193-281">LetAppsAccessRadios\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessradios-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-282">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94193-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94193-283">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-283">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94193-284">\_ForceDenyTheseApps LetAppsAccessRadios</span><span class="sxs-lookup"><span data-stu-id="94193-284">LetAppsAccessRadios\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessradios-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-285">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94193-285">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94193-286">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-286">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94193-287">\_UserInControlOfTheseApps LetAppsAccessRadios</span><span class="sxs-lookup"><span data-stu-id="94193-287">LetAppsAccessRadios\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessradios-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-288">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94193-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94193-289">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-289">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94193-290">LetAppsAccessTasks</span><span class="sxs-lookup"><span data-stu-id="94193-290">LetAppsAccessTasks</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstasks)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-291">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="94193-291">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="94193-292">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-292">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94193-293">\_ForceAllowTheseApps LetAppsAccessTasks</span><span class="sxs-lookup"><span data-stu-id="94193-293">LetAppsAccessTasks\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstasks-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-294">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94193-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94193-295">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-295">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94193-296">\_ForceDenyTheseApps LetAppsAccessTasks</span><span class="sxs-lookup"><span data-stu-id="94193-296">LetAppsAccessTasks\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstasks-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-297">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94193-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94193-298">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-298">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94193-299">\_UserInControlOfTheseApps LetAppsAccessTasks</span><span class="sxs-lookup"><span data-stu-id="94193-299">LetAppsAccessTasks\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstasks-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-300">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94193-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94193-301">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-301">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94193-302">LetAppsAccessTrustedDevices</span><span class="sxs-lookup"><span data-stu-id="94193-302">LetAppsAccessTrustedDevices</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstrusteddevices)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-303">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="94193-303">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="94193-304">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-304">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94193-305">\_ForceAllowTheseApps LetAppsAccessTrustedDevices</span><span class="sxs-lookup"><span data-stu-id="94193-305">LetAppsAccessTrustedDevices\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstrusteddevices-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-306">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94193-306">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94193-307">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-307">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94193-308">\_ForceDenyTheseApps LetAppsAccessTrustedDevices</span><span class="sxs-lookup"><span data-stu-id="94193-308">LetAppsAccessTrustedDevices\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstrusteddevices-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-309">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94193-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94193-310">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-310">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94193-311">\_UserInControlOfTheseApps LetAppsAccessTrustedDevices</span><span class="sxs-lookup"><span data-stu-id="94193-311">LetAppsAccessTrustedDevices\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstrusteddevices-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-312">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94193-312">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94193-313">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-313">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94193-314">LetAppsGetDiagnosticInfo</span><span class="sxs-lookup"><span data-stu-id="94193-314">LetAppsGetDiagnosticInfo</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsgetdiagnosticinfo)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-315">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="94193-315">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="94193-316">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-316">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94193-317">\_ForceAllowTheseApps LetAppsGetDiagnosticInfo</span><span class="sxs-lookup"><span data-stu-id="94193-317">LetAppsGetDiagnosticInfo\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsgetdiagnosticinfo-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-318">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94193-318">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94193-319">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-319">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94193-320">\_ForceDenyTheseApps LetAppsGetDiagnosticInfo</span><span class="sxs-lookup"><span data-stu-id="94193-320">LetAppsGetDiagnosticInfo\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsgetdiagnosticinfo-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-321">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94193-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94193-322">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-322">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94193-323">\_UserInControlOfTheseApps LetAppsGetDiagnosticInfo</span><span class="sxs-lookup"><span data-stu-id="94193-323">LetAppsGetDiagnosticInfo\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsgetdiagnosticinfo-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-324">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94193-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94193-325">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-325">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94193-326">LetAppsRunInBackground</span><span class="sxs-lookup"><span data-stu-id="94193-326">LetAppsRunInBackground</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsruninbackground)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-327">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="94193-327">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="94193-328">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-328">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94193-329">\_ForceAllowTheseApps LetAppsRunInBackground</span><span class="sxs-lookup"><span data-stu-id="94193-329">LetAppsRunInBackground\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsruninbackground-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-330">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94193-330">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94193-331">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-331">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94193-332">\_ForceDenyTheseApps LetAppsRunInBackground</span><span class="sxs-lookup"><span data-stu-id="94193-332">LetAppsRunInBackground\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsruninbackground-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-333">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94193-333">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94193-334">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-334">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94193-335">\_UserInControlOfTheseApps LetAppsRunInBackground</span><span class="sxs-lookup"><span data-stu-id="94193-335">LetAppsRunInBackground\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsruninbackground-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-336">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94193-336">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94193-337">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-337">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94193-338">LetAppsSyncWithDevices</span><span class="sxs-lookup"><span data-stu-id="94193-338">LetAppsSyncWithDevices</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappssyncwithdevices)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-339">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="94193-339">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="94193-340">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-340">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94193-341">\_ForceAllowTheseApps LetAppsSyncWithDevices</span><span class="sxs-lookup"><span data-stu-id="94193-341">LetAppsSyncWithDevices\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappssyncwithdevices-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-342">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94193-342">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94193-343">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-343">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94193-344">\_ForceDenyTheseApps LetAppsSyncWithDevices</span><span class="sxs-lookup"><span data-stu-id="94193-344">LetAppsSyncWithDevices\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappssyncwithdevices-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-345">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94193-345">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94193-346">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-346">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94193-347">\_UserInControlOfTheseApps LetAppsSyncWithDevices</span><span class="sxs-lookup"><span data-stu-id="94193-347">LetAppsSyncWithDevices\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappssyncwithdevices-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-348">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94193-348">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94193-349">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-349">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="94193-350">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="94193-350">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-351">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94193-351">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94193-352">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="94193-352">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94193-353">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="94193-353">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="94193-354">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="94193-354">Describes the full path to the parent node.</span></span> <span data-ttu-id="94193-355">Per questa classe la stringa è "./Vendor/MSFT/Policy/Result"</span><span class="sxs-lookup"><span data-stu-id="94193-355">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="94193-356">PublishUserActivities</span><span class="sxs-lookup"><span data-stu-id="94193-356">PublishUserActivities</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-publishuseractivities)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94193-357">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="94193-357">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="94193-358">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="94193-358">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="94193-359">Requisiti</span><span class="sxs-lookup"><span data-stu-id="94193-359">Requirements</span></span>



| <span data-ttu-id="94193-360">Requisito</span><span class="sxs-lookup"><span data-stu-id="94193-360">Requirement</span></span> | <span data-ttu-id="94193-361">Valore</span><span class="sxs-lookup"><span data-stu-id="94193-361">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94193-362">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="94193-362">Minimum supported client</span></span><br/> | <span data-ttu-id="94193-363">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="94193-363">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="94193-364">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="94193-364">Minimum supported server</span></span><br/> | <span data-ttu-id="94193-365">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="94193-365">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="94193-366">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="94193-366">Namespace</span></span><br/>                | <span data-ttu-id="94193-367">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="94193-367">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="94193-368">MOF</span><span class="sxs-lookup"><span data-stu-id="94193-368">MOF</span></span><br/>                      | <dl> <span data-ttu-id="94193-369"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="94193-369"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="94193-370">DLL</span><span class="sxs-lookup"><span data-stu-id="94193-370">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94193-371"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94193-371"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94193-372">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="94193-372">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94193-373">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="94193-373">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

