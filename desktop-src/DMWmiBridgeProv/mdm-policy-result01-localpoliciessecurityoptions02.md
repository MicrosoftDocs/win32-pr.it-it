---
title: Classe MDM_Policy_Result01_LocalPoliciesSecurityOptions02
description: La \_ \_ classe Result01 LocalPoliciesSecurityOptions02 dei criteri MDM \_ rappresenta le opzioni di sicurezza dei criteri locali.
ms.assetid: 75ac4789-781f-4722-8b0a-33e53b307296
keywords:
- Classe MDM_Policy_Result01_LocalPoliciesSecurityOptions02
- Classe MDM_Policy_Result01_LocalPoliciesSecurityOptions02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_LocalPoliciesSecurityOptions02
- MDM_Policy_Result01_LocalPoliciesSecurityOptions02.InstanceID
- MDM_Policy_Result01_LocalPoliciesSecurityOptions02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f1ece3790bf5a6a6ac51310d04661366bbe9e2a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048248"
---
# <a name="mdm_policy_result01_localpoliciessecurityoptions02-class"></a><span data-ttu-id="ecdd1-105">\_ \_ Classe Result01 LocalPoliciesSecurityOptions02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="ecdd1-105">MDM\_Policy\_Result01\_LocalPoliciesSecurityOptions02 class</span></span>

<span data-ttu-id="ecdd1-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="ecdd1-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="ecdd1-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="ecdd1-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="ecdd1-108">La \_ \_ classe Result01 LocalPoliciesSecurityOptions02 dei criteri MDM \_ rappresenta le opzioni di sicurezza dei criteri locali.</span><span class="sxs-lookup"><span data-stu-id="ecdd1-108">The MDM\_Policy\_Result01\_LocalPoliciesSecurityOptions02 class represents the local policies security options.</span></span>

<span data-ttu-id="ecdd1-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="ecdd1-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ecdd1-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ecdd1-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_LocalPoliciesSecurityOptions02
{
  string InstanceID;
  string ParentID;
  sint32 Accounts_BlockMicrosoftAccounts;
  sint32 Accounts_EnableGuestAccountStatus;
  sint32 Accounts_EnableAdministratorAccountStatus;
  sint32 Accounts_LimitLocalAccountUseOfBlankPasswordsToConsoleLogonOnly;
  string Accounts_RenameAdministratorAccount;
  string Accounts_RenameGuestAccount;
  string Devices_RestrictCDROMAccessToLocallyLoggedOnUserOnly;
  sint32 Devices_PreventUsersFromInstallingPrinterDriversWhenConnectingToSharedPrinters;
  sint32 Devices_AllowUndockWithoutHavingToLogon;
  string Devices_AllowedToFormatAndEjectRemovableMedia;
  sint32 InteractiveLogon_DisplayUserInformationWhenTheSessionIsLocked;
  sint32 Interactivelogon_DoNotDisplayLastSignedIn;
  sint32 Interactivelogon_DoNotDisplayUsernameAtSignIn;
  sint32 Interactivelogon_DoNotRequireCTRLALTDEL;
  sint32 InteractiveLogon_MachineInactivityLimit;
  string InteractiveLogon_MessageTextForUsersAttemptingToLogOn;
  string InteractiveLogon_MessageTitleForUsersAttemptingToLogOn;
  sint32 NetworkAccess_DoNotAllowAnonymousEnumerationOfSAMAccountsAndShares;
  sint32 NetworkAccess_RestrictAnonymousAccessToNamedPipesAndShares;
  string NetworkAccess_RestrictClientsAllowedToMakeRemoteCallsToSAM;
  sint32 NetworkSecurity_AllowPKU2UAuthenticationRequests;
  sint32 RecoveryConsole_AllowAutomaticAdministrativeLogon;
  sint32 Shutdown_AllowSystemToBeShutDownWithoutHavingToLogOn;
  sint32 Shutdown_ClearVirtualMemoryPageFile;
  sint32 UserAccountControl_AllowUIAccessApplicationsToPromptForElevation;
  sint32 UserAccountControl_BehaviorOfTheElevationPromptForAdministrators;
  sint32 UserAccountControl_BehaviorOfTheElevationPromptForStandardUsers;
  sint32 UserAccountControl_DetectApplicationInstallationsAndPromptForElevation;
  sint32 UserAccountControl_OnlyElevateExecutableFilesThatAreSignedAndValidated;
  sint32 UserAccountControl_OnlyElevateUIAccessApplicationsThatAreInstalledInSecureLocations;
  sint32 UserAccountControl_RunAllAdministratorsInAdminApprovalMode;
  sint32 UserAccountControl_SwitchToTheSecureDesktopWhenPromptingForElevation;
  sint32 UserAccountControl_UseAdminApprovalMode;
  sint32 UserAccountControl_VirtualizeFileAndRegistryWriteFailuresToPerUserLocations;
};
```

## <a name="members"></a><span data-ttu-id="ecdd1-111">Members</span><span class="sxs-lookup"><span data-stu-id="ecdd1-111">Members</span></span>

<span data-ttu-id="ecdd1-112">La **classe \_ \_ Result01 \_ LocalPoliciesSecurityOptions02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ecdd1-112">The **MDM\_Policy\_Result01\_LocalPoliciesSecurityOptions02** class has these types of members:</span></span>

-   [<span data-ttu-id="ecdd1-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ecdd1-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ecdd1-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ecdd1-114">Properties</span></span>

<span data-ttu-id="ecdd1-115">La **classe \_ \_ \_ LocalPoliciesSecurityOptions02 dei criteri MDM Result01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="ecdd1-115">The **MDM\_Policy\_Result01\_LocalPoliciesSecurityOptions02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="ecdd1-116">Account \_ BlockMicrosoftAccounts</span><span class="sxs-lookup"><span data-stu-id="ecdd1-116">Accounts\_BlockMicrosoftAccounts</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-accounts-blockmicrosoftaccounts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecdd1-117">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ecdd1-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ecdd1-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ecdd1-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ecdd1-119">Accounts_EnableAdministratorAccountStatus</span><span class="sxs-lookup"><span data-stu-id="ecdd1-119">Accounts_EnableAdministratorAccountStatus</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecdd1-120">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ecdd1-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ecdd1-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ecdd1-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ecdd1-122">Accounts_EnableGuestAccountStatus</span><span class="sxs-lookup"><span data-stu-id="ecdd1-122">Accounts_EnableGuestAccountStatus</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecdd1-123">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ecdd1-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ecdd1-124">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ecdd1-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ecdd1-125">Account \_ LimitLocalAccountUseOfBlankPasswordsToConsoleLogonOnly</span><span class="sxs-lookup"><span data-stu-id="ecdd1-125">Accounts\_LimitLocalAccountUseOfBlankPasswordsToConsoleLogonOnly</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-accounts-limitlocalaccountuseofblankpasswordstoconsolelogononly)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecdd1-126">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ecdd1-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ecdd1-127">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ecdd1-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ecdd1-128">Account \_ RenameAdministratorAccount</span><span class="sxs-lookup"><span data-stu-id="ecdd1-128">Accounts\_RenameAdministratorAccount</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-accounts-renameadministratoraccount)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecdd1-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ecdd1-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ecdd1-130">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ecdd1-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ecdd1-131">Account \_ RenameGuestAccount</span><span class="sxs-lookup"><span data-stu-id="ecdd1-131">Accounts\_RenameGuestAccount</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-accounts-renameguestaccount)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecdd1-132">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ecdd1-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ecdd1-133">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ecdd1-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ecdd1-134">Dispositivi \_ AllowedToFormatAndEjectRemovableMedia</span><span class="sxs-lookup"><span data-stu-id="ecdd1-134">Devices\_AllowedToFormatAndEjectRemovableMedia</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-devices-allowedtoformatandejectremovablemedia)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecdd1-135">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ecdd1-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ecdd1-136">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ecdd1-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ecdd1-137">Dispositivi \_ AllowUndockWithoutHavingToLogon</span><span class="sxs-lookup"><span data-stu-id="ecdd1-137">Devices\_AllowUndockWithoutHavingToLogon</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-devices-allowundockwithouthavingtologon)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecdd1-138">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ecdd1-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ecdd1-139">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ecdd1-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ecdd1-140">Dispositivi \_ PreventUsersFromInstallingPrinterDriversWhenConnectingToSharedPrinters</span><span class="sxs-lookup"><span data-stu-id="ecdd1-140">Devices\_PreventUsersFromInstallingPrinterDriversWhenConnectingToSharedPrinters</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-devices-preventusersfrominstallingprinterdriverswhenconnectingtosharedprinters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecdd1-141">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ecdd1-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ecdd1-142">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ecdd1-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ecdd1-143">Dispositivi \_ RestrictCDROMAccessToLocallyLoggedOnUserOnly</span><span class="sxs-lookup"><span data-stu-id="ecdd1-143">Devices\_RestrictCDROMAccessToLocallyLoggedOnUserOnly</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-devices-restrictcdromaccesstolocallyloggedonuseronly)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecdd1-144">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ecdd1-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ecdd1-145">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ecdd1-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ecdd1-146">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ecdd1-146">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecdd1-147">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ecdd1-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ecdd1-148">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ecdd1-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ecdd1-149">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ecdd1-149">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ecdd1-150">\_DisplayUserInformationWhenTheSessionIsLocked InteractiveLogon</span><span class="sxs-lookup"><span data-stu-id="ecdd1-150">InteractiveLogon\_DisplayUserInformationWhenTheSessionIsLocked</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-interactivelogon-displayuserinformationwhenthesessionislocked)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecdd1-151">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ecdd1-151">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ecdd1-152">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ecdd1-152">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ecdd1-153">\_DoNotDisplayLastSignedIn Interactivelogon</span><span class="sxs-lookup"><span data-stu-id="ecdd1-153">Interactivelogon\_DoNotDisplayLastSignedIn</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-interactivelogon-donotdisplaylastsignedin)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecdd1-154">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ecdd1-154">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ecdd1-155">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ecdd1-155">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ecdd1-156">\_DoNotDisplayUsernameAtSignIn Interactivelogon</span><span class="sxs-lookup"><span data-stu-id="ecdd1-156">Interactivelogon\_DoNotDisplayUsernameAtSignIn</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-interactivelogon-donotdisplayusernameatsignin)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecdd1-157">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ecdd1-157">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ecdd1-158">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ecdd1-158">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ecdd1-159">\_DoNotRequireCTRLALTDEL Interactivelogon</span><span class="sxs-lookup"><span data-stu-id="ecdd1-159">Interactivelogon\_DoNotRequireCTRLALTDEL</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-interactivelogon-donotrequirectrlaltdel)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecdd1-160">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ecdd1-160">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ecdd1-161">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ecdd1-161">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ecdd1-162">\_MachineInactivityLimit InteractiveLogon</span><span class="sxs-lookup"><span data-stu-id="ecdd1-162">InteractiveLogon\_MachineInactivityLimit</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-interactivelogon-machineinactivitylimit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecdd1-163">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ecdd1-163">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ecdd1-164">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ecdd1-164">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ecdd1-165">\_MessageTextForUsersAttemptingToLogOn InteractiveLogon</span><span class="sxs-lookup"><span data-stu-id="ecdd1-165">InteractiveLogon\_MessageTextForUsersAttemptingToLogOn</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-interactivelogon-messagetextforusersattemptingtologon)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecdd1-166">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ecdd1-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ecdd1-167">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ecdd1-167">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ecdd1-168">\_MessageTitleForUsersAttemptingToLogOn InteractiveLogon</span><span class="sxs-lookup"><span data-stu-id="ecdd1-168">InteractiveLogon\_MessageTitleForUsersAttemptingToLogOn</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-interactivelogon-messagetitleforusersattemptingtologon)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecdd1-169">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ecdd1-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ecdd1-170">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ecdd1-170">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ecdd1-171">\_DoNotAllowAnonymousEnumerationOfSAMAccountsAndShares NetworkAccess</span><span class="sxs-lookup"><span data-stu-id="ecdd1-171">NetworkAccess\_DoNotAllowAnonymousEnumerationOfSAMAccountsAndShares</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-networkaccess-donotallowanonymousenumerationofsamaccountsandshares)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecdd1-172">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ecdd1-172">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ecdd1-173">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ecdd1-173">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ecdd1-174">\_RestrictAnonymousAccessToNamedPipesAndShares NetworkAccess</span><span class="sxs-lookup"><span data-stu-id="ecdd1-174">NetworkAccess\_RestrictAnonymousAccessToNamedPipesAndShares</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-networkaccess-restrictanonymousaccesstonamedpipesandshares)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecdd1-175">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ecdd1-175">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ecdd1-176">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ecdd1-176">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ecdd1-177">\_RestrictClientsAllowedToMakeRemoteCallsToSAM NetworkAccess</span><span class="sxs-lookup"><span data-stu-id="ecdd1-177">NetworkAccess\_RestrictClientsAllowedToMakeRemoteCallsToSAM</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-networkaccess-restrictclientsallowedtomakeremotecallstosam)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecdd1-178">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ecdd1-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ecdd1-179">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ecdd1-179">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ecdd1-180">\_AllowPKU2UAuthenticationRequests NetworkSecurity</span><span class="sxs-lookup"><span data-stu-id="ecdd1-180">NetworkSecurity\_AllowPKU2UAuthenticationRequests</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-networksecurity-allowpku2uauthenticationrequests)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecdd1-181">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ecdd1-181">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ecdd1-182">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ecdd1-182">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ecdd1-183">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="ecdd1-183">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecdd1-184">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ecdd1-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ecdd1-185">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ecdd1-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ecdd1-186">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ecdd1-186">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ecdd1-187">\_AllowAutomaticAdministrativeLogon RecoveryConsole</span><span class="sxs-lookup"><span data-stu-id="ecdd1-187">RecoveryConsole\_AllowAutomaticAdministrativeLogon</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-recoveryconsole-allowautomaticadministrativelogon)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecdd1-188">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ecdd1-188">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ecdd1-189">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ecdd1-189">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ecdd1-190">Arresta \_ AllowSystemToBeShutDownWithoutHavingToLogOn</span><span class="sxs-lookup"><span data-stu-id="ecdd1-190">Shutdown\_AllowSystemToBeShutDownWithoutHavingToLogOn</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-shutdown-allowsystemtobeshutdownwithouthavingtologon)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecdd1-191">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ecdd1-191">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ecdd1-192">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ecdd1-192">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ecdd1-193">Arresta \_ ClearVirtualMemoryPageFile</span><span class="sxs-lookup"><span data-stu-id="ecdd1-193">Shutdown\_ClearVirtualMemoryPageFile</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-shutdown-clearvirtualmemorypagefile)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecdd1-194">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ecdd1-194">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ecdd1-195">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ecdd1-195">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ecdd1-196">\_AllowUIAccessApplicationsToPromptForElevation userAccountControl</span><span class="sxs-lookup"><span data-stu-id="ecdd1-196">UserAccountControl\_AllowUIAccessApplicationsToPromptForElevation</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-allowuiaccessapplicationstopromptforelevation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecdd1-197">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ecdd1-197">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ecdd1-198">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ecdd1-198">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ecdd1-199">\_BehaviorOfTheElevationPromptForAdministrators userAccountControl</span><span class="sxs-lookup"><span data-stu-id="ecdd1-199">UserAccountControl\_BehaviorOfTheElevationPromptForAdministrators</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-behavioroftheelevationpromptforadministrators)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecdd1-200">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ecdd1-200">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ecdd1-201">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ecdd1-201">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ecdd1-202">\_BehaviorOfTheElevationPromptForStandardUsers userAccountControl</span><span class="sxs-lookup"><span data-stu-id="ecdd1-202">UserAccountControl\_BehaviorOfTheElevationPromptForStandardUsers</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-behavioroftheelevationpromptforstandardusers)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecdd1-203">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ecdd1-203">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ecdd1-204">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ecdd1-204">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ecdd1-205">\_DetectApplicationInstallationsAndPromptForElevation userAccountControl</span><span class="sxs-lookup"><span data-stu-id="ecdd1-205">UserAccountControl\_DetectApplicationInstallationsAndPromptForElevation</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-detectapplicationinstallationsandpromptforelevation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecdd1-206">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ecdd1-206">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ecdd1-207">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ecdd1-207">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ecdd1-208">\_OnlyElevateExecutableFilesThatAreSignedAndValidated userAccountControl</span><span class="sxs-lookup"><span data-stu-id="ecdd1-208">UserAccountControl\_OnlyElevateExecutableFilesThatAreSignedAndValidated</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-onlyelevateexecutablefilesthataresignedandvalidated)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecdd1-209">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ecdd1-209">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ecdd1-210">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ecdd1-210">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ecdd1-211">\_OnlyElevateUIAccessApplicationsThatAreInstalledInSecureLocations userAccountControl</span><span class="sxs-lookup"><span data-stu-id="ecdd1-211">UserAccountControl\_OnlyElevateUIAccessApplicationsThatAreInstalledInSecureLocations</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-onlyelevateuiaccessapplicationsthatareinstalledinsecurelocations)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecdd1-212">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ecdd1-212">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ecdd1-213">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ecdd1-213">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ecdd1-214">\_RunAllAdministratorsInAdminApprovalMode userAccountControl</span><span class="sxs-lookup"><span data-stu-id="ecdd1-214">UserAccountControl\_RunAllAdministratorsInAdminApprovalMode</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-runalladministratorsinadminapprovalmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecdd1-215">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ecdd1-215">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ecdd1-216">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ecdd1-216">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ecdd1-217">\_SwitchToTheSecureDesktopWhenPromptingForElevation userAccountControl</span><span class="sxs-lookup"><span data-stu-id="ecdd1-217">UserAccountControl\_SwitchToTheSecureDesktopWhenPromptingForElevation</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-switchtothesecuredesktopwhenpromptingforelevation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecdd1-218">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ecdd1-218">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ecdd1-219">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ecdd1-219">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ecdd1-220">\_UseAdminApprovalMode userAccountControl</span><span class="sxs-lookup"><span data-stu-id="ecdd1-220">UserAccountControl\_UseAdminApprovalMode</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-useadminapprovalmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecdd1-221">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ecdd1-221">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ecdd1-222">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ecdd1-222">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ecdd1-223">\_VirtualizeFileAndRegistryWriteFailuresToPerUserLocations userAccountControl</span><span class="sxs-lookup"><span data-stu-id="ecdd1-223">UserAccountControl\_VirtualizeFileAndRegistryWriteFailuresToPerUserLocations</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-virtualizefileandregistrywritefailurestoperuserlocations)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecdd1-224">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ecdd1-224">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ecdd1-225">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ecdd1-225">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ecdd1-226">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ecdd1-226">Requirements</span></span>



| <span data-ttu-id="ecdd1-227">Requisito</span><span class="sxs-lookup"><span data-stu-id="ecdd1-227">Requirement</span></span> | <span data-ttu-id="ecdd1-228">Valore</span><span class="sxs-lookup"><span data-stu-id="ecdd1-228">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ecdd1-229">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ecdd1-229">Minimum supported client</span></span><br/> | <span data-ttu-id="ecdd1-230">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="ecdd1-230">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ecdd1-231">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ecdd1-231">Minimum supported server</span></span><br/> | <span data-ttu-id="ecdd1-232">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="ecdd1-232">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="ecdd1-233">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ecdd1-233">Namespace</span></span><br/>                | <span data-ttu-id="ecdd1-234">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="ecdd1-234">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="ecdd1-235">MOF</span><span class="sxs-lookup"><span data-stu-id="ecdd1-235">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ecdd1-236"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ecdd1-236"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="ecdd1-237">DLL</span><span class="sxs-lookup"><span data-stu-id="ecdd1-237">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ecdd1-238"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ecdd1-238"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

