---
title: Classe MDM_Policy_Result01_InternetExplorer02
description: Il \_ criterio MDM \_ Result01 \_ InternetExplorer02 rappresenta i criteri di Internet Explorer.
ms.assetid: 4b14c9ea-2f4d-4e5a-8aab-3741f15b0b1e
keywords:
- Classe MDM_Policy_Result01_InternetExplorer02
- Classe MDM_Policy_Result01_InternetExplorer02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_InternetExplorer02
- MDM_Policy_Result01_InternetExplorer02.InstanceID
- MDM_Policy_Result01_InternetExplorer02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63308b6100d6bd4ec924307a9dcd3892096fc0fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964107"
---
# <a name="mdm_policy_result01_internetexplorer02-class"></a><span data-ttu-id="82605-105">\_ \_ Classe Result01 InternetExplorer02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="82605-105">MDM\_Policy\_Result01\_InternetExplorer02 class</span></span>

<span data-ttu-id="82605-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="82605-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="82605-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="82605-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="82605-108">Il \_ criterio MDM \_ Result01 \_ InternetExplorer02 rappresenta i criteri di Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="82605-108">The MDM\_Policy\_Result01\_InternetExplorer02 represents the Internet Explorer policies.</span></span>

<span data-ttu-id="82605-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="82605-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="82605-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="82605-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_InternetExplorer02
{
  string InstanceID;
  string ParentID;
  string AddSearchProvider;
  string AllowActiveXFiltering;
  string AllowAddOnList;
  string AllowDeletingBrowsingHistoryOnExit;
  string AllowCertificateAddressMismatchWarning;
  string AllowEnhancedProtectedMode;
  string AllowEnterpriseModeFromToolsMenu;
  string AllowEnterpriseModeSiteList;
  string AllowFallbackToSSL3;
  string AllowInternetExplorer7PolicyList;
  string AllowInternetExplorerStandardsMode;
  string AllowInternetZoneTemplate;
  string AllowIntranetZoneTemplate;
  string AllowLocalMachineZoneTemplate;
  string AllowLockedDownInternetZoneTemplate;
  string AllowLockedDownIntranetZoneTemplate;
  string AllowLockedDownLocalMachineZoneTemplate;
  string AllowLockedDownRestrictedSitesZoneTemplate;
  string AllowOneWordEntry;
  string AllowSiteToZoneAssignmentList;
  string AllowsLockedDownTrustedSitesZoneTemplate;
  string AllowSoftwareWhenSignatureIsInvalid;
  string AllowsRestrictedSitesZoneTemplate;
  string AllowSuggestedSites;
  string AllowTrustedSitesZoneTemplate;
  string ConsistentMimeHandlingInternetExplorerProcesses;
  string CheckSignaturesOnDownloadedPrograms;
  string CheckServerCertificateRevocation;
  string DisableAdobeFlash;
  string DisableBlockingOfOutdatedActiveXControls;
  string DisableBypassOfSmartScreenWarnings;
  string DisableBypassOfSmartScreenWarningsAboutUncommonFiles;
  string DisableCrashDetection;
  string DisableConfiguringHistory;
  string DisableCustomerExperienceImprovementProgramParticipation;
  string DisableDeletingUserVisitedWebsites;
  string DisableEnclosureDownloading;
  string DisableEncryptionSupport;
  string DisableFirstRunWizard;
  string DisableFlipAheadFeature;
  string DisableProcessesInEnhancedProtectedMode;
  string DisableInPrivateBrowsing;
  string DisableIgnoringCertificateErrors;
  string DisableProxyChange;
  string DisableSearchProviderChange;
  string DisableSecondaryHomePageChange;
  string DisableSecuritySettingsCheck;
  string DisableUpdateCheck;
  string DoNotAllowActiveXControlsInProtectedMode;
  string DoNotAllowUsersToAddSites;
  string DoNotAllowUsersToChangePolicies;
  string DoNotBlockOutdatedActiveXControls;
  string DoNotBlockOutdatedActiveXControlsOnSpecificDomains;
  string IncludeAllLocalSites;
  string IncludeAllNetworkPaths;
  string InternetZoneAllowAccessToDataSources;
  string InternetZoneAllowAutomaticPromptingForActiveXControls;
  string InternetZoneAllowAutomaticPromptingForFileDownloads;
  string InternetZoneAllowDragAndDropCopyAndPasteFiles;
  string InternetZoneAllowCopyPasteViaScript;
  string InternetZoneAllowFontDownloads;
  string InternetZoneAllowLessPrivilegedSites;
  string InternetZoneAllowLoadingOfXAMLFiles;
  string InternetZoneAllowNETFrameworkReliantComponents;
  string InternetZoneAllowScriptInitiatedWindows;
  string InternetZoneAllowScriptingOfInternetExplorerWebBrowserControls;
  string InternetZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl;
  string InternetZoneAllowOnlyApprovedDomainsToUseActiveXControls;
  string InternetZoneAllowScriptlets;
  string InternetZoneAllowSmartScreenIE;
  string InternetZoneAllowUpdatesToStatusBarViaScript;
  string InternetZoneAllowUserDataPersistence;
  string InternetZoneDoNotRunAntimalwareAgainstActiveXControls;
  string InternetZoneIncludeLocalPathWhenUploadingFilesToServer;
  string InternetZoneEnableProtectedMode;
  string InternetZoneEnableMIMESniffing;
  string InternetZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows;
  string InternetZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows;
  string InternetZoneEnableCrossSiteScriptingFilter;
  string InternetZoneDownloadUnsignedActiveXControls;
  string InternetZoneDownloadSignedActiveXControls;
  string InternetZoneInitializeAndScriptActiveXControls;
  string InternetZoneJavaPermissions;
  string InternetZoneLogonOptions;
  string InternetZoneLaunchingApplicationsAndFilesInIFRAME;
  string InternetZoneNavigateWindowsAndFrames;
  string InternetZoneWebsitesInLessPrivilegedZonesCanNavigateIntoThisZone;
  string InternetZoneUsePopupBlocker;
  string InternetZoneShowSecurityWarningForPotentiallyUnsafeFiles;
  string InternetZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode;
  string InternetZoneRunNETFrameworkReliantComponentsNotSignedWithAuthenticode;
  string IntranetZoneAllowAccessToDataSources;
  string IntranetZoneAllowAutomaticPromptingForActiveXControls;
  string IntranetZoneAllowAutomaticPromptingForFileDownloads;
  string IntranetZoneAllowFontDownloads;
  string IntranetZoneAllowLessPrivilegedSites;
  string IntranetZoneAllowNETFrameworkReliantComponents;
  string IntranetZoneAllowScriptlets;
  string IntranetZoneAllowSmartScreenIE;
  string IntranetZoneAllowUserDataPersistence;
  string IntranetZoneDoNotRunAntimalwareAgainstActiveXControls;
  string IntranetZoneInitializeAndScriptActiveXControls;
  string IntranetZoneJavaPermissions;
  string IntranetZoneInitializeAndScriptActiveXControlsNotMarkedSafe;
  string IntranetZoneNavigateWindowsAndFrames;
  string LocalMachineZoneAllowAccessToDataSources;
  string LocalMachineZoneAllowAutomaticPromptingForActiveXControls;
  string LocalMachineZoneAllowAutomaticPromptingForFileDownloads;
  string LocalMachineZoneAllowFontDownloads;
  string LocalMachineZoneAllowLessPrivilegedSites;
  string LocalMachineZoneAllowNETFrameworkReliantComponents;
  string LocalMachineZoneAllowScriptlets;
  string LocalMachineZoneAllowSmartScreenIE;
  string LocalMachineZoneAllowUserDataPersistence;
  string LocalMachineZoneDoNotRunAntimalwareAgainstActiveXControls;
  string LocalMachineZoneInitializeAndScriptActiveXControls;
  string LocalMachineZoneJavaPermissions;
  string LocalMachineZoneNavigateWindowsAndFrames;
  string LockedDownInternetZoneAllowAccessToDataSources;
  string LockedDownInternetZoneAllowAutomaticPromptingForActiveXControls;
  string LockedDownInternetZoneAllowAutomaticPromptingForFileDownloads;
  string LockedDownInternetZoneAllowFontDownloads;
  string LockedDownInternetZoneAllowLessPrivilegedSites;
  string LockedDownInternetZoneAllowNETFrameworkReliantComponents;
  string LockedDownInternetZoneAllowScriptlets;
  string LockedDownInternetZoneAllowSmartScreenIE;
  string LockedDownInternetZoneAllowUserDataPersistence;
  string LockedDownInternetZoneInitializeAndScriptActiveXControls;
  string LockedDownInternetZoneJavaPermissions;
  string LockedDownInternetZoneNavigateWindowsAndFrames;
  string LockedDownIntranetZoneAllowAccessToDataSources;
  string LockedDownIntranetZoneAllowAutomaticPromptingForActiveXControls;
  string LockedDownIntranetZoneAllowAutomaticPromptingForFileDownloads;
  string LockedDownIntranetZoneAllowFontDownloads;
  string LockedDownIntranetZoneAllowLessPrivilegedSites;
  string LockedDownIntranetZoneAllowNETFrameworkReliantComponents;
  string LockedDownIntranetZoneAllowScriptlets;
  string LockedDownIntranetZoneAllowSmartScreenIE;
  string LockedDownIntranetZoneAllowUserDataPersistence;
  string LockedDownIntranetZoneInitializeAndScriptActiveXControls;
  string LockedDownIntranetZoneNavigateWindowsAndFrames;
  string LockedDownLocalMachineZoneAllowAccessToDataSources;
  string LockedDownLocalMachineZoneAllowAutomaticPromptingForActiveXControls;
  string LockedDownLocalMachineZoneAllowAutomaticPromptingForFileDownloads;
  string LockedDownLocalMachineZoneAllowFontDownloads;
  string LockedDownLocalMachineZoneAllowLessPrivilegedSites;
  string LockedDownLocalMachineZoneAllowNETFrameworkReliantComponents;
  string LockedDownLocalMachineZoneAllowScriptlets;
  string LockedDownLocalMachineZoneAllowSmartScreenIE;
  string LockedDownLocalMachineZoneAllowUserDataPersistence;
  string LockedDownLocalMachineZoneInitializeAndScriptActiveXControls;
  string LockedDownLocalMachineZoneJavaPermissions;
  string LockedDownLocalMachineZoneNavigateWindowsAndFrames;
  string LockedDownRestrictedSitesZoneAllowAccessToDataSources;
  string LockedDownRestrictedSitesZoneAllowAutomaticPromptingForActiveXControls;
  string LockedDownRestrictedSitesZoneAllowAutomaticPromptingForFileDownloads;
  string LockedDownRestrictedSitesZoneAllowFontDownloads;
  string LockedDownRestrictedSitesZoneAllowLessPrivilegedSites;
  string LockedDownRestrictedSitesZoneAllowNETFrameworkReliantComponents;
  string LockedDownRestrictedSitesZoneAllowScriptlets;
  string LockedDownRestrictedSitesZoneAllowSmartScreenIE;
  string LockedDownRestrictedSitesZoneAllowUserDataPersistence;
  string LockedDownRestrictedSitesZoneInitializeAndScriptActiveXControls;
  string LockedDownRestrictedSitesZoneJavaPermissions;
  string LockedDownRestrictedSitesZoneNavigateWindowsAndFrames;
  string LockedDownTrustedSitesZoneAllowAccessToDataSources;
  string LockedDownTrustedSitesZoneAllowAutomaticPromptingForActiveXControls;
  string LockedDownTrustedSitesZoneAllowAutomaticPromptingForFileDownloads;
  string LockedDownTrustedSitesZoneAllowFontDownloads;
  string LockedDownTrustedSitesZoneAllowLessPrivilegedSites;
  string LockedDownTrustedSitesZoneAllowNETFrameworkReliantComponents;
  string LockedDownTrustedSitesZoneAllowScriptlets;
  string LockedDownTrustedSitesZoneAllowSmartScreenIE;
  string LockedDownTrustedSitesZoneAllowUserDataPersistence;
  string LockedDownTrustedSitesZoneInitializeAndScriptActiveXControls;
  string LockedDownTrustedSitesZoneJavaPermissions;
  string LockedDownTrustedSitesZoneNavigateWindowsAndFrames;
  string RestrictActiveXInstallInternetExplorerProcesses;
  string RemoveRunThisTimeButtonForOutdatedActiveXControls;
  string ProtectionFromZoneElevationInternetExplorerProcesses;
  string PreventPerUserInstallationOfActiveXControls;
  string PreventManagingSmartScreenFilter;
  string NotificationBarInternetExplorerProcesses;
  string MKProtocolSecurityRestrictionInternetExplorerProcesses;
  string MimeSniffingSafetyFeatureInternetExplorerProcesses;
  string RestrictedSitesZoneAllowAccessToDataSources;
  string RestrictedSitesZoneAllowActiveScripting;
  string RestrictedSitesZoneAllowAutomaticPromptingForActiveXControls;
  string RestrictedSitesZoneAllowAutomaticPromptingForFileDownloads;
  string RestrictedSitesZoneAllowFileDownloads;
  string RestrictedSitesZoneAllowDragAndDropCopyAndPasteFiles;
  string RestrictedSitesZoneAllowCopyPasteViaScript;
  string RestrictedSitesZoneAllowBinaryAndScriptBehaviors;
  string RestrictedSitesZoneAllowFontDownloads;
  string RestrictedSitesZoneAllowLessPrivilegedSites;
  string RestrictedSitesZoneAllowMETAREFRESH;
  string RestrictedSitesZoneAllowLoadingOfXAMLFiles;
  string RestrictedSitesZoneAllowNETFrameworkReliantComponents;
  string RestrictedSitesZoneAllowScriptInitiatedWindows;
  string RestrictedSitesZoneAllowScriptingOfInternetExplorerWebBrowserControls;
  string RestrictedSitesZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl;
  string RestrictedSitesZoneAllowOnlyApprovedDomainsToUseActiveXControls;
  string RestrictedSitesZoneAllowScriptlets;
  string RestrictedSitesZoneAllowSmartScreenIE;
  string RestrictedSitesZoneAllowUpdatesToStatusBarViaScript;
  string RestrictedSitesZoneAllowUserDataPersistence;
  string RestrictedSitesZoneIncludeLocalPathWhenUploadingFilesToServer;
  string RestrictedSitesZoneEnableMIMESniffing;
  string RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows;
  string RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows;
  string RestrictedSitesZoneDownloadUnsignedActiveXControls;
  string RestrictedSitesZoneEnableCrossSiteScriptingFilter;
  string RestrictedSitesZoneDownloadSignedActiveXControls;
  string RestrictedSitesZoneDoNotRunAntimalwareAgainstActiveXControls;
  string RestrictedSitesZoneInitializeAndScriptActiveXControls;
  string RestrictedSitesZoneLogonOptions;
  string RestrictedSitesZoneLaunchingApplicationsAndFilesInIFRAME;
  string RestrictedSitesZoneJavaPermissions;
  string RestrictedSitesZoneNavigateWindowsAndFrames;
  string ScriptedWindowSecurityRestrictionsInternetExplorerProcesses;
  string RestrictFileDownloadInternetExplorerProcesses;
  string RestrictedSitesZoneScriptActiveXControlsMarkedSafeForScripting;
  string RestrictedSitesZoneUsePopupBlocker;
  string RestrictedSitesZoneTurnOnProtectedMode;
  string RestrictedSitesZoneTurnOnCrossSiteScriptingFilter;
  string RestrictedSitesZoneShowSecurityWarningForPotentiallyUnsafeFiles;
  string RestrictedSitesZoneScriptingOfJavaApplets;
  string RestrictedSitesZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode;
  string RestrictedSitesZoneRunActiveXControlsAndPlugins;
  string RestrictedSitesZoneNavigateWindowsAndFramesAcrossDomains;
  string SearchProviderList;
  string SpecifyUseOfActiveXInstallerService;
  string SecurityZonesUseOnlyMachineSettings;
  string TrustedSitesZoneAllowAccessToDataSources;
  string TrustedSitesZoneAllowAutomaticPromptingForActiveXControls;
  string TrustedSitesZoneAllowAutomaticPromptingForFileDownloads;
  string TrustedSitesZoneAllowFontDownloads;
  string TrustedSitesZoneAllowLessPrivilegedSites;
  string TrustedSitesZoneAllowNETFrameworkReliantComponents;
  string TrustedSitesZoneAllowScriptlets;
  string TrustedSitesZoneAllowSmartScreenIE;
  string TrustedSitesZoneAllowUserDataPersistence;
  string TrustedSitesZoneDontRunAntimalwareProgramsAgainstActiveXControls;
  string TrustedSitesZoneDoNotRunAntimalwareAgainstActiveXControls;
  string TrustedSitesZoneInitializeAndScriptActiveXControls;
  string TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedSafe;
  string TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedAsSafe;
  string TrustedSitesZoneJavaPermissions;
  string TrustedSitesZoneNavigateWindowsAndFrames;
};
```

## <a name="members"></a><span data-ttu-id="82605-111">Members</span><span class="sxs-lookup"><span data-stu-id="82605-111">Members</span></span>

<span data-ttu-id="82605-112">La **classe \_ \_ Result01 \_ InternetExplorer02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="82605-112">The **MDM\_Policy\_Result01\_InternetExplorer02** class has these types of members:</span></span>

-   [<span data-ttu-id="82605-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="82605-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="82605-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="82605-114">Properties</span></span>

<span data-ttu-id="82605-115">La **classe \_ \_ \_ InternetExplorer02 dei criteri MDM Result01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="82605-115">The **MDM\_Policy\_Result01\_InternetExplorer02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="82605-116">AddSearchProvider</span><span class="sxs-lookup"><span data-stu-id="82605-116">AddSearchProvider</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-addsearchprovider)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-119">AllowActiveXFiltering</span><span class="sxs-lookup"><span data-stu-id="82605-119">AllowActiveXFiltering</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowactivexfiltering)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-122">AllowAddOnList</span><span class="sxs-lookup"><span data-stu-id="82605-122">AllowAddOnList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowaddonlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-124">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-125">AllowCertificateAddressMismatchWarning</span><span class="sxs-lookup"><span data-stu-id="82605-125">AllowCertificateAddressMismatchWarning</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowcertificateaddressmismatchwarning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-127">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-128">AllowDeletingBrowsingHistoryOnExit</span><span class="sxs-lookup"><span data-stu-id="82605-128">AllowDeletingBrowsingHistoryOnExit</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowdeletingbrowsinghistoryonexit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-130">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-131">AllowEnhancedProtectedMode</span><span class="sxs-lookup"><span data-stu-id="82605-131">AllowEnhancedProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenhancedprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-132">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-133">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-134">AllowEnterpriseModeFromToolsMenu</span><span class="sxs-lookup"><span data-stu-id="82605-134">AllowEnterpriseModeFromToolsMenu</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenterprisemodefromtoolsmenu)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-135">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-136">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-137">AllowEnterpriseModeSiteList</span><span class="sxs-lookup"><span data-stu-id="82605-137">AllowEnterpriseModeSiteList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenterprisemodesitelist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-138">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-139">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-140">AllowFallbackToSSL3</span><span class="sxs-lookup"><span data-stu-id="82605-140">AllowFallbackToSSL3</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowfallbacktossl3)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-141">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-142">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-143">AllowInternetExplorer7PolicyList</span><span class="sxs-lookup"><span data-stu-id="82605-143">AllowInternetExplorer7PolicyList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetexplorer7policylist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-144">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-145">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-146">AllowInternetExplorerStandardsMode</span><span class="sxs-lookup"><span data-stu-id="82605-146">AllowInternetExplorerStandardsMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetexplorerstandardsmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-147">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-148">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-149">AllowInternetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="82605-149">AllowInternetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-150">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-151">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-152">AllowIntranetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="82605-152">AllowIntranetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowintranetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-153">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-154">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-155">AllowLocalMachineZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="82605-155">AllowLocalMachineZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlocalmachinezonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-156">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-157">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-158">AllowLockedDownInternetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="82605-158">AllowLockedDownInternetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddowninternetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-159">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-160">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-161">AllowLockedDownIntranetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="82605-161">AllowLockedDownIntranetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownintranetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-162">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-163">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-164">AllowLockedDownLocalMachineZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="82605-164">AllowLockedDownLocalMachineZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownlocalmachinezonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-165">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-166">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-167">AllowLockedDownRestrictedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="82605-167">AllowLockedDownRestrictedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownrestrictedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-168">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-169">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-170">AllowOneWordEntry</span><span class="sxs-lookup"><span data-stu-id="82605-170">AllowOneWordEntry</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowonewordentry)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-171">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-172">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-173">AllowSiteToZoneAssignmentList</span><span class="sxs-lookup"><span data-stu-id="82605-173">AllowSiteToZoneAssignmentList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsitetozoneassignmentlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-174">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-175">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-176">AllowsLockedDownTrustedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="82605-176">AllowsLockedDownTrustedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowslockeddowntrustedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-177">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-178">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-179">AllowSoftwareWhenSignatureIsInvalid</span><span class="sxs-lookup"><span data-stu-id="82605-179">AllowSoftwareWhenSignatureIsInvalid</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsoftwarewhensignatureisinvalid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-180">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-181">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-182">AllowsRestrictedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="82605-182">AllowsRestrictedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsrestrictedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-183">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-184">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-185">AllowSuggestedSites</span><span class="sxs-lookup"><span data-stu-id="82605-185">AllowSuggestedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsuggestedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-186">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-187">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-187">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-188">AllowTrustedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="82605-188">AllowTrustedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowtrustedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-189">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-190">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-191">CheckServerCertificateRevocation</span><span class="sxs-lookup"><span data-stu-id="82605-191">CheckServerCertificateRevocation</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-checkservercertificaterevocation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-192">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-193">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-193">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-194">CheckSignaturesOnDownloadedPrograms</span><span class="sxs-lookup"><span data-stu-id="82605-194">CheckSignaturesOnDownloadedPrograms</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-checksignaturesondownloadedprograms)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-195">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-196">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-196">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-197">ConsistentMimeHandlingInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="82605-197">ConsistentMimeHandlingInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-consistentmimehandlinginternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-198">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-199">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-199">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-200">DisableAdobeFlash</span><span class="sxs-lookup"><span data-stu-id="82605-200">DisableAdobeFlash</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableadobeflash)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-201">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-202">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-202">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="82605-203">DisableBlockingOfOutdatedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="82605-203">DisableBlockingOfOutdatedActiveXControls</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-204">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-205">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-205">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-206">DisableBypassOfSmartScreenWarnings</span><span class="sxs-lookup"><span data-stu-id="82605-206">DisableBypassOfSmartScreenWarnings</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablebypassofsmartscreenwarnings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-207">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-208">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-208">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-209">DisableBypassOfSmartScreenWarningsAboutUncommonFiles</span><span class="sxs-lookup"><span data-stu-id="82605-209">DisableBypassOfSmartScreenWarningsAboutUncommonFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablebypassofsmartscreenwarningsaboutuncommonfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-210">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-211">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-212">DisableConfiguringHistory</span><span class="sxs-lookup"><span data-stu-id="82605-212">DisableConfiguringHistory</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableconfiguringhistory)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-213">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-214">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-214">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-215">DisableCrashDetection</span><span class="sxs-lookup"><span data-stu-id="82605-215">DisableCrashDetection</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablecrashdetection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-216">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-217">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-217">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-218">DisableCustomerExperienceImprovementProgramParticipation</span><span class="sxs-lookup"><span data-stu-id="82605-218">DisableCustomerExperienceImprovementProgramParticipation</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablecustomerexperienceimprovementprogramparticipation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-219">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-220">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-220">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-221">DisableDeletingUserVisitedWebsites</span><span class="sxs-lookup"><span data-stu-id="82605-221">DisableDeletingUserVisitedWebsites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disabledeletinguservisitedwebsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-222">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-223">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-223">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-224">DisableEnclosureDownloading</span><span class="sxs-lookup"><span data-stu-id="82605-224">DisableEnclosureDownloading</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableenclosuredownloading)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-225">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-226">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-226">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-227">DisableEncryptionSupport</span><span class="sxs-lookup"><span data-stu-id="82605-227">DisableEncryptionSupport</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableencryptionsupport)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-228">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-229">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-229">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-230">DisableFirstRunWizard</span><span class="sxs-lookup"><span data-stu-id="82605-230">DisableFirstRunWizard</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablefirstrunwizard)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-231">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-232">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-232">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-233">DisableFlipAheadFeature</span><span class="sxs-lookup"><span data-stu-id="82605-233">DisableFlipAheadFeature</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableflipaheadfeature)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-234">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-235">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-235">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-236">DisableIgnoringCertificateErrors</span><span class="sxs-lookup"><span data-stu-id="82605-236">DisableIgnoringCertificateErrors</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableignoringcertificateerrors)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-237">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-238">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-238">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-239">DisableInPrivateBrowsing</span><span class="sxs-lookup"><span data-stu-id="82605-239">DisableInPrivateBrowsing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableinprivatebrowsing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-240">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-241">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-241">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-242">DisableProcessesInEnhancedProtectedMode</span><span class="sxs-lookup"><span data-stu-id="82605-242">DisableProcessesInEnhancedProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableprocessesinenhancedprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-243">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-244">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-244">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-245">DisableProxyChange</span><span class="sxs-lookup"><span data-stu-id="82605-245">DisableProxyChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableproxychange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-246">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-247">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-247">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-248">DisableSearchProviderChange</span><span class="sxs-lookup"><span data-stu-id="82605-248">DisableSearchProviderChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesearchproviderchange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-249">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-250">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-250">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-251">DisableSecondaryHomePageChange</span><span class="sxs-lookup"><span data-stu-id="82605-251">DisableSecondaryHomePageChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesecondaryhomepagechange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-252">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-253">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-253">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-254">DisableSecuritySettingsCheck</span><span class="sxs-lookup"><span data-stu-id="82605-254">DisableSecuritySettingsCheck</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesecuritysettingscheck)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-255">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-256">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-256">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-257">DisableUpdateCheck</span><span class="sxs-lookup"><span data-stu-id="82605-257">DisableUpdateCheck</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableupdatecheck)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-258">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-259">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-259">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-260">DoNotAllowActiveXControlsInProtectedMode</span><span class="sxs-lookup"><span data-stu-id="82605-260">DoNotAllowActiveXControlsInProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotallowactivexcontrolsinprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-261">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-262">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-262">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-263">DoNotAllowUsersToAddSites</span><span class="sxs-lookup"><span data-stu-id="82605-263">DoNotAllowUsersToAddSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotallowuserstoaddsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-264">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-265">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-265">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-266">DoNotAllowUsersToChangePolicies</span><span class="sxs-lookup"><span data-stu-id="82605-266">DoNotAllowUsersToChangePolicies</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotallowuserstochangepolicies)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-267">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-268">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-268">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-269">DoNotBlockOutdatedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="82605-269">DoNotBlockOutdatedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotblockoutdatedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-270">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-270">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-271">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-271">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-272">DoNotBlockOutdatedActiveXControlsOnSpecificDomains</span><span class="sxs-lookup"><span data-stu-id="82605-272">DoNotBlockOutdatedActiveXControlsOnSpecificDomains</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotblockoutdatedactivexcontrolsonspecificdomains)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-273">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-274">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-274">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-275">IncludeAllLocalSites</span><span class="sxs-lookup"><span data-stu-id="82605-275">IncludeAllLocalSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-includealllocalsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-276">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-277">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-277">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-278">IncludeAllNetworkPaths</span><span class="sxs-lookup"><span data-stu-id="82605-278">IncludeAllNetworkPaths</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-includeallnetworkpaths)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-279">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-280">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-280">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="82605-281">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="82605-281">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-282">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-283">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="82605-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="82605-284">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="82605-284">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-285">InternetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="82605-285">InternetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-286">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-287">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-287">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-288">InternetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="82605-288">InternetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-289">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-290">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-290">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-291">InternetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="82605-291">InternetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-292">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-293">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-293">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-294">InternetZoneAllowCopyPasteViaScript</span><span class="sxs-lookup"><span data-stu-id="82605-294">InternetZoneAllowCopyPasteViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowcopypasteviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-295">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-296">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-296">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-297">InternetZoneAllowDragAndDropCopyAndPasteFiles</span><span class="sxs-lookup"><span data-stu-id="82605-297">InternetZoneAllowDragAndDropCopyAndPasteFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowdraganddropcopyandpastefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-298">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-298">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-299">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-299">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-300">InternetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="82605-300">InternetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-301">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-302">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-302">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-303">InternetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="82605-303">InternetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-304">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-305">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-305">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-306">InternetZoneAllowLoadingOfXAMLFiles</span><span class="sxs-lookup"><span data-stu-id="82605-306">InternetZoneAllowLoadingOfXAMLFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowloadingofxamlfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-307">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-308">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-308">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-309">InternetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="82605-309">InternetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-310">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-311">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-311">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-312">InternetZoneAllowOnlyApprovedDomainsToUseActiveXControls</span><span class="sxs-lookup"><span data-stu-id="82605-312">InternetZoneAllowOnlyApprovedDomainsToUseActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowonlyapproveddomainstouseactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-313">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-314">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-314">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-315">InternetZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span><span class="sxs-lookup"><span data-stu-id="82605-315">InternetZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowonlyapproveddomainstousetdcactivexcontrol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-316">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-317">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-317">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-318">InternetZoneAllowScriptingOfInternetExplorerWebBrowserControls</span><span class="sxs-lookup"><span data-stu-id="82605-318">InternetZoneAllowScriptingOfInternetExplorerWebBrowserControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptingofinternetexplorerwebbrowsercontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-319">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-320">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-320">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-321">InternetZoneAllowScriptInitiatedWindows</span><span class="sxs-lookup"><span data-stu-id="82605-321">InternetZoneAllowScriptInitiatedWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptinitiatedwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-322">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-323">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-323">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-324">InternetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="82605-324">InternetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-325">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-326">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-326">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-327">InternetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="82605-327">InternetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-328">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-329">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-329">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-330">InternetZoneAllowUpdatesToStatusBarViaScript</span><span class="sxs-lookup"><span data-stu-id="82605-330">InternetZoneAllowUpdatesToStatusBarViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowupdatestostatusbarviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-331">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-332">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-332">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-333">InternetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="82605-333">InternetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-334">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-335">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-335">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-336">InternetZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="82605-336">InternetZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-337">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-338">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-338">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-339">InternetZoneDownloadSignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="82605-339">InternetZoneDownloadSignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedownloadsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-340">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-341">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-341">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-342">InternetZoneDownloadUnsignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="82605-342">InternetZoneDownloadUnsignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedownloadunsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-343">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-343">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-344">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-344">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-345">InternetZoneEnableCrossSiteScriptingFilter</span><span class="sxs-lookup"><span data-stu-id="82605-345">InternetZoneEnableCrossSiteScriptingFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenablecrosssitescriptingfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-346">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-347">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-347">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-348">InternetZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span><span class="sxs-lookup"><span data-stu-id="82605-348">InternetZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenabledraggingofcontentfromdifferentdomainsacrosswindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-349">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-350">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-350">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-351">InternetZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span><span class="sxs-lookup"><span data-stu-id="82605-351">InternetZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenabledraggingofcontentfromdifferentdomainswithinwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-352">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-353">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-353">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-354">InternetZoneEnableMIMESniffing</span><span class="sxs-lookup"><span data-stu-id="82605-354">InternetZoneEnableMIMESniffing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenablemimesniffing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-355">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-356">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-356">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-357">InternetZoneEnableProtectedMode</span><span class="sxs-lookup"><span data-stu-id="82605-357">InternetZoneEnableProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenableprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-358">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-358">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-359">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-359">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-360">InternetZoneIncludeLocalPathWhenUploadingFilesToServer</span><span class="sxs-lookup"><span data-stu-id="82605-360">InternetZoneIncludeLocalPathWhenUploadingFilesToServer</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneincludelocalpathwhenuploadingfilestoserver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-361">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-362">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-362">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-363">InternetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="82605-363">InternetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-364">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-364">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-365">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-365">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-366">InternetZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="82605-366">InternetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-367">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-368">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-368">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-369">InternetZoneLaunchingApplicationsAndFilesInIFRAME</span><span class="sxs-lookup"><span data-stu-id="82605-369">InternetZoneLaunchingApplicationsAndFilesInIFRAME</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonelaunchingapplicationsandfilesiniframe)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-370">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-370">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-371">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-371">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-372">InternetZoneLogonOptions</span><span class="sxs-lookup"><span data-stu-id="82605-372">InternetZoneLogonOptions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonelogonoptions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-373">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-373">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-374">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-374">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-375">InternetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="82605-375">InternetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-376">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-376">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-377">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-377">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="82605-378">InternetZoneRunNETFrameworkReliantComponentsNotSignedWithAuthenticode</span><span class="sxs-lookup"><span data-stu-id="82605-378">InternetZoneRunNETFrameworkReliantComponentsNotSignedWithAuthenticode</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-379">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-380">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-380">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-381">InternetZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span><span class="sxs-lookup"><span data-stu-id="82605-381">InternetZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonerunnetframeworkreliantcomponentssignedwithauthenticode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-382">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-383">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-383">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-384">InternetZoneShowSecurityWarningForPotentiallyUnsafeFiles</span><span class="sxs-lookup"><span data-stu-id="82605-384">InternetZoneShowSecurityWarningForPotentiallyUnsafeFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneshowsecuritywarningforpotentiallyunsafefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-385">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-385">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-386">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-386">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-387">InternetZoneUsePopupBlocker</span><span class="sxs-lookup"><span data-stu-id="82605-387">InternetZoneUsePopupBlocker</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneusepopupblocker)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-388">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-388">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-389">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-389">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="82605-390">InternetZoneWebsitesInLessPrivilegedZonesCanNavigateIntoThisZone</span><span class="sxs-lookup"><span data-stu-id="82605-390">InternetZoneWebsitesInLessPrivilegedZonesCanNavigateIntoThisZone</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-391">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-391">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-392">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-392">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-393">IntranetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="82605-393">IntranetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-394">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-394">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-395">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-395">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-396">IntranetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="82605-396">IntranetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-397">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-397">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-398">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-398">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-399">IntranetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="82605-399">IntranetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-400">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-400">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-401">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-401">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-402">IntranetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="82605-402">IntranetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-403">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-404">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-404">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-405">IntranetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="82605-405">IntranetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-406">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-406">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-407">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-407">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-408">IntranetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="82605-408">IntranetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-409">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-409">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-410">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-410">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-411">IntranetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="82605-411">IntranetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-412">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-412">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-413">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-413">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-414">IntranetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="82605-414">IntranetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-415">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-415">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-416">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-416">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-417">IntranetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="82605-417">IntranetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-418">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-418">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-419">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-419">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-420">IntranetZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="82605-420">IntranetZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-421">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-421">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-422">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-422">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-423">IntranetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="82605-423">IntranetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-424">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-424">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-425">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-425">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="82605-426">IntranetZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span><span class="sxs-lookup"><span data-stu-id="82605-426">IntranetZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-427">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-427">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-428">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-428">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-429">IntranetZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="82605-429">IntranetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-430">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-430">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-431">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-431">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-432">IntranetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="82605-432">IntranetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-433">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-433">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-434">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-434">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-435">LocalMachineZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="82605-435">LocalMachineZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-436">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-436">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-437">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-437">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-438">LocalMachineZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="82605-438">LocalMachineZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-439">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-439">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-440">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-440">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-441">LocalMachineZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="82605-441">LocalMachineZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-442">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-442">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-443">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-443">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-444">LocalMachineZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="82605-444">LocalMachineZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-445">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-445">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-446">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-446">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-447">LocalMachineZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="82605-447">LocalMachineZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-448">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-448">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-449">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-449">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-450">LocalMachineZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="82605-450">LocalMachineZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-451">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-451">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-452">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-452">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-453">LocalMachineZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="82605-453">LocalMachineZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-454">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-454">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-455">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-455">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-456">LocalMachineZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="82605-456">LocalMachineZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-457">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-457">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-458">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-458">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-459">LocalMachineZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="82605-459">LocalMachineZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-460">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-460">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-461">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-461">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-462">LocalMachineZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="82605-462">LocalMachineZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-463">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-463">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-464">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-464">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-465">LocalMachineZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="82605-465">LocalMachineZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-466">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-466">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-467">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-467">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-468">LocalMachineZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="82605-468">LocalMachineZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-469">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-469">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-470">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-470">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-471">LocalMachineZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="82605-471">LocalMachineZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-472">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-472">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-473">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-473">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-474">LockedDownInternetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="82605-474">LockedDownInternetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-475">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-475">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-476">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-476">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-477">LockedDownInternetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="82605-477">LockedDownInternetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-478">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-478">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-479">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-479">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-480">LockedDownInternetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="82605-480">LockedDownInternetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-481">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-481">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-482">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-482">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-483">LockedDownInternetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="82605-483">LockedDownInternetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-484">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-484">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-485">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-485">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-486">LockedDownInternetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="82605-486">LockedDownInternetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-487">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-487">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-488">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-488">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-489">LockedDownInternetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="82605-489">LockedDownInternetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-490">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-490">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-491">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-491">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-492">LockedDownInternetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="82605-492">LockedDownInternetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-493">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-493">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-494">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-494">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-495">LockedDownInternetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="82605-495">LockedDownInternetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-496">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-496">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-497">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-497">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-498">LockedDownInternetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="82605-498">LockedDownInternetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-499">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-499">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-500">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-500">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-501">LockedDownInternetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="82605-501">LockedDownInternetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-502">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-502">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-503">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-503">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-504">LockedDownInternetZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="82605-504">LockedDownInternetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-505">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-505">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-506">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-506">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-507">LockedDownInternetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="82605-507">LockedDownInternetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-508">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-508">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-509">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-509">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-510">LockedDownIntranetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="82605-510">LockedDownIntranetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-511">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-511">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-512">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-512">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-513">LockedDownIntranetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="82605-513">LockedDownIntranetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-514">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-514">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-515">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-515">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-516">LockedDownIntranetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="82605-516">LockedDownIntranetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-517">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-517">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-518">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-518">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-519">LockedDownIntranetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="82605-519">LockedDownIntranetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-520">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-520">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-521">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-521">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-522">LockedDownIntranetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="82605-522">LockedDownIntranetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-523">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-523">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-524">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-524">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-525">LockedDownIntranetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="82605-525">LockedDownIntranetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-526">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-526">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-527">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-527">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-528">LockedDownIntranetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="82605-528">LockedDownIntranetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-529">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-529">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-530">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-530">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-531">LockedDownIntranetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="82605-531">LockedDownIntranetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-532">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-532">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-533">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-533">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-534">LockedDownIntranetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="82605-534">LockedDownIntranetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-535">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-535">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-536">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-536">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-537">LockedDownIntranetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="82605-537">LockedDownIntranetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-538">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-538">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-539">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-539">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-540">LockedDownIntranetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="82605-540">LockedDownIntranetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-541">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-541">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-542">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-542">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-543">LockedDownLocalMachineZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="82605-543">LockedDownLocalMachineZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-544">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-544">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-545">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-545">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-546">LockedDownLocalMachineZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="82605-546">LockedDownLocalMachineZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-547">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-547">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-548">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-548">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-549">LockedDownLocalMachineZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="82605-549">LockedDownLocalMachineZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-550">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-550">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-551">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-551">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-552">LockedDownLocalMachineZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="82605-552">LockedDownLocalMachineZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-553">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-553">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-554">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-554">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-555">LockedDownLocalMachineZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="82605-555">LockedDownLocalMachineZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-556">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-556">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-557">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-557">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-558">LockedDownLocalMachineZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="82605-558">LockedDownLocalMachineZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-559">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-559">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-560">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-560">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-561">LockedDownLocalMachineZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="82605-561">LockedDownLocalMachineZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-562">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-562">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-563">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-563">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-564">LockedDownLocalMachineZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="82605-564">LockedDownLocalMachineZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-565">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-565">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-566">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-566">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-567">LockedDownLocalMachineZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="82605-567">LockedDownLocalMachineZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-568">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-568">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-569">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-569">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-570">LockedDownLocalMachineZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="82605-570">LockedDownLocalMachineZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-571">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-571">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-572">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-572">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-573">LockedDownLocalMachineZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="82605-573">LockedDownLocalMachineZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-574">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-574">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-575">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-575">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-576">LockedDownLocalMachineZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="82605-576">LockedDownLocalMachineZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-577">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-577">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-578">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-578">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-579">LockedDownRestrictedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="82605-579">LockedDownRestrictedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-580">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-580">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-581">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-581">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-582">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="82605-582">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-583">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-583">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-584">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-584">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-585">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="82605-585">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-586">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-586">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-587">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-587">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-588">LockedDownRestrictedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="82605-588">LockedDownRestrictedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-589">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-589">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-590">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-590">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-591">LockedDownRestrictedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="82605-591">LockedDownRestrictedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-592">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-592">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-593">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-593">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-594">LockedDownRestrictedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="82605-594">LockedDownRestrictedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-595">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-595">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-596">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-596">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-597">LockedDownRestrictedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="82605-597">LockedDownRestrictedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-598">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-598">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-599">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-599">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-600">LockedDownRestrictedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="82605-600">LockedDownRestrictedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-601">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-601">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-602">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-602">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-603">LockedDownRestrictedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="82605-603">LockedDownRestrictedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-604">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-604">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-605">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-605">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-606">LockedDownRestrictedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="82605-606">LockedDownRestrictedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-607">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-607">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-608">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-608">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-609">LockedDownRestrictedSitesZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="82605-609">LockedDownRestrictedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-610">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-610">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-611">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-611">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-612">LockedDownRestrictedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="82605-612">LockedDownRestrictedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-613">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-613">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-614">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-614">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-615">LockedDownTrustedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="82605-615">LockedDownTrustedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-616">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-616">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-617">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-617">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-618">LockedDownTrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="82605-618">LockedDownTrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-619">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-619">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-620">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-620">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-621">LockedDownTrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="82605-621">LockedDownTrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-622">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-622">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-623">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-623">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-624">LockedDownTrustedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="82605-624">LockedDownTrustedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-625">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-625">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-626">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-626">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-627">LockedDownTrustedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="82605-627">LockedDownTrustedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-628">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-628">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-629">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-629">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-630">LockedDownTrustedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="82605-630">LockedDownTrustedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-631">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-631">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-632">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-632">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-633">LockedDownTrustedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="82605-633">LockedDownTrustedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-634">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-634">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-635">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-635">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-636">LockedDownTrustedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="82605-636">LockedDownTrustedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-637">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-637">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-638">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-638">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-639">LockedDownTrustedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="82605-639">LockedDownTrustedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-640">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-640">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-641">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-641">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-642">LockedDownTrustedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="82605-642">LockedDownTrustedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-643">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-643">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-644">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-644">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-645">LockedDownTrustedSitesZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="82605-645">LockedDownTrustedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-646">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-646">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-647">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-647">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-648">LockedDownTrustedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="82605-648">LockedDownTrustedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-649">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-649">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-650">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-650">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-651">MimeSniffingSafetyFeatureInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="82605-651">MimeSniffingSafetyFeatureInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-mimesniffingsafetyfeatureinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-652">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-652">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-653">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-653">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-654">MKProtocolSecurityRestrictionInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="82605-654">MKProtocolSecurityRestrictionInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-mkprotocolsecurityrestrictioninternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-655">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-655">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-656">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-656">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-657">NotificationBarInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="82605-657">NotificationBarInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-notificationbarinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-658">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-658">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-659">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-659">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="82605-660">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="82605-660">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-661">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-661">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-662">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="82605-662">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="82605-663">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="82605-663">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-664">PreventManagingSmartScreenFilter</span><span class="sxs-lookup"><span data-stu-id="82605-664">PreventManagingSmartScreenFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-preventmanagingsmartscreenfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-665">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-665">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-666">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-666">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-667">PreventPerUserInstallationOfActiveXControls</span><span class="sxs-lookup"><span data-stu-id="82605-667">PreventPerUserInstallationOfActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-preventperuserinstallationofactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-668">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-668">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-669">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-669">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-670">ProtectionFromZoneElevationInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="82605-670">ProtectionFromZoneElevationInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-protectionfromzoneelevationinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-671">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-671">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-672">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-672">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-673">RemoveRunThisTimeButtonForOutdatedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="82605-673">RemoveRunThisTimeButtonForOutdatedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-removerunthistimebuttonforoutdatedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-674">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-674">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-675">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-675">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-676">RestrictActiveXInstallInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="82605-676">RestrictActiveXInstallInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictactivexinstallinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-677">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-677">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-678">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-678">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-679">RestrictedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="82605-679">RestrictedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-680">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-680">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-681">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-681">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-682">RestrictedSitesZoneAllowActiveScripting</span><span class="sxs-lookup"><span data-stu-id="82605-682">RestrictedSitesZoneAllowActiveScripting</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowactivescripting)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-683">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-683">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-684">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-684">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-685">RestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="82605-685">RestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-686">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-686">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-687">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-687">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-688">RestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="82605-688">RestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-689">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-689">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-690">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-690">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-691">RestrictedSitesZoneAllowBinaryAndScriptBehaviors</span><span class="sxs-lookup"><span data-stu-id="82605-691">RestrictedSitesZoneAllowBinaryAndScriptBehaviors</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowbinaryandscriptbehaviors)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-692">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-692">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-693">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-693">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-694">RestrictedSitesZoneAllowCopyPasteViaScript</span><span class="sxs-lookup"><span data-stu-id="82605-694">RestrictedSitesZoneAllowCopyPasteViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowcopypasteviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-695">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-695">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-696">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-696">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-697">RestrictedSitesZoneAllowDragAndDropCopyAndPasteFiles</span><span class="sxs-lookup"><span data-stu-id="82605-697">RestrictedSitesZoneAllowDragAndDropCopyAndPasteFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowdraganddropcopyandpastefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-698">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-698">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-699">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-699">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-700">RestrictedSitesZoneAllowFileDownloads</span><span class="sxs-lookup"><span data-stu-id="82605-700">RestrictedSitesZoneAllowFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-701">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-701">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-702">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-702">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-703">RestrictedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="82605-703">RestrictedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-704">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-704">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-705">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-705">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-706">RestrictedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="82605-706">RestrictedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-707">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-707">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-708">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-708">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-709">RestrictedSitesZoneAllowLoadingOfXAMLFiles</span><span class="sxs-lookup"><span data-stu-id="82605-709">RestrictedSitesZoneAllowLoadingOfXAMLFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowloadingofxamlfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-710">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-710">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-711">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-711">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-712">RestrictedSitesZoneAllowMETAREFRESH</span><span class="sxs-lookup"><span data-stu-id="82605-712">RestrictedSitesZoneAllowMETAREFRESH</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowmetarefresh)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-713">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-713">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-714">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-714">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-715">RestrictedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="82605-715">RestrictedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-716">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-716">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-717">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-717">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-718">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseActiveXControls</span><span class="sxs-lookup"><span data-stu-id="82605-718">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowonlyapproveddomainstouseactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-719">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-719">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-720">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-720">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-721">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span><span class="sxs-lookup"><span data-stu-id="82605-721">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowonlyapproveddomainstousetdcactivexcontrol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-722">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-722">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-723">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-723">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-724">RestrictedSitesZoneAllowScriptingOfInternetExplorerWebBrowserControls</span><span class="sxs-lookup"><span data-stu-id="82605-724">RestrictedSitesZoneAllowScriptingOfInternetExplorerWebBrowserControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptingofinternetexplorerwebbrowsercontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-725">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-725">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-726">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-726">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-727">RestrictedSitesZoneAllowScriptInitiatedWindows</span><span class="sxs-lookup"><span data-stu-id="82605-727">RestrictedSitesZoneAllowScriptInitiatedWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptinitiatedwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-728">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-728">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-729">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-729">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-730">RestrictedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="82605-730">RestrictedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-731">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-731">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-732">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-732">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-733">RestrictedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="82605-733">RestrictedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-734">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-734">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-735">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-735">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-736">RestrictedSitesZoneAllowUpdatesToStatusBarViaScript</span><span class="sxs-lookup"><span data-stu-id="82605-736">RestrictedSitesZoneAllowUpdatesToStatusBarViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowupdatestostatusbarviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-737">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-737">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-738">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-738">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-739">RestrictedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="82605-739">RestrictedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-740">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-740">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-741">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-741">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-742">RestrictedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="82605-742">RestrictedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-743">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-743">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-744">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-744">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-745">RestrictedSitesZoneDownloadSignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="82605-745">RestrictedSitesZoneDownloadSignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedownloadsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-746">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-746">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-747">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-747">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-748">RestrictedSitesZoneDownloadUnsignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="82605-748">RestrictedSitesZoneDownloadUnsignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedownloadunsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-749">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-749">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-750">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-750">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-751">RestrictedSitesZoneEnableCrossSiteScriptingFilter</span><span class="sxs-lookup"><span data-stu-id="82605-751">RestrictedSitesZoneEnableCrossSiteScriptingFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenablecrosssitescriptingfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-752">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-752">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-753">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-753">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-754">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span><span class="sxs-lookup"><span data-stu-id="82605-754">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenabledraggingofcontentfromdifferentdomainsacrosswindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-755">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-755">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-756">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-756">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-757">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span><span class="sxs-lookup"><span data-stu-id="82605-757">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenabledraggingofcontentfromdifferentdomainswithinwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-758">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-758">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-759">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-759">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-760">RestrictedSitesZoneEnableMIMESniffing</span><span class="sxs-lookup"><span data-stu-id="82605-760">RestrictedSitesZoneEnableMIMESniffing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenablemimesniffing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-761">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-761">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-762">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-762">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-763">RestrictedSitesZoneIncludeLocalPathWhenUploadingFilesToServer</span><span class="sxs-lookup"><span data-stu-id="82605-763">RestrictedSitesZoneIncludeLocalPathWhenUploadingFilesToServer</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneincludelocalpathwhenuploadingfilestoserver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-764">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-764">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-765">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-765">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-766">RestrictedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="82605-766">RestrictedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-767">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-767">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-768">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-768">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-769">RestrictedSitesZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="82605-769">RestrictedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-770">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-770">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-771">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-771">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-772">RestrictedSitesZoneLaunchingApplicationsAndFilesInIFRAME</span><span class="sxs-lookup"><span data-stu-id="82605-772">RestrictedSitesZoneLaunchingApplicationsAndFilesInIFRAME</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonelaunchingapplicationsandfilesiniframe)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-773">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-773">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-774">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-774">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-775">RestrictedSitesZoneLogonOptions</span><span class="sxs-lookup"><span data-stu-id="82605-775">RestrictedSitesZoneLogonOptions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonelogonoptions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-776">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-776">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-777">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-777">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-778">RestrictedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="82605-778">RestrictedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-779">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-779">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-780">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-780">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="82605-781">RestrictedSitesZoneNavigateWindowsAndFramesAcrossDomains</span><span class="sxs-lookup"><span data-stu-id="82605-781">RestrictedSitesZoneNavigateWindowsAndFramesAcrossDomains</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-782">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-782">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-783">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-783">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-784">RestrictedSitesZoneRunActiveXControlsAndPlugins</span><span class="sxs-lookup"><span data-stu-id="82605-784">RestrictedSitesZoneRunActiveXControlsAndPlugins</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonerunactivexcontrolsandplugins)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-785">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-785">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-786">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-786">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-787">RestrictedSitesZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span><span class="sxs-lookup"><span data-stu-id="82605-787">RestrictedSitesZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonerunnetframeworkreliantcomponentssignedwithauthenticode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-788">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-788">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-789">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-789">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-790">RestrictedSitesZoneScriptActiveXControlsMarkedSafeForScripting</span><span class="sxs-lookup"><span data-stu-id="82605-790">RestrictedSitesZoneScriptActiveXControlsMarkedSafeForScripting</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonescriptactivexcontrolsmarkedsafeforscripting)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-791">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-791">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-792">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-792">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-793">RestrictedSitesZoneScriptingOfJavaApplets</span><span class="sxs-lookup"><span data-stu-id="82605-793">RestrictedSitesZoneScriptingOfJavaApplets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonescriptingofjavaapplets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-794">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-794">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-795">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-795">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-796">RestrictedSitesZoneShowSecurityWarningForPotentiallyUnsafeFiles</span><span class="sxs-lookup"><span data-stu-id="82605-796">RestrictedSitesZoneShowSecurityWarningForPotentiallyUnsafeFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneshowsecuritywarningforpotentiallyunsafefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-797">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-797">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-798">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-798">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="82605-799">RestrictedSitesZoneTurnOnCrossSiteScriptingFilter</span><span class="sxs-lookup"><span data-stu-id="82605-799">RestrictedSitesZoneTurnOnCrossSiteScriptingFilter</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-800">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-800">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-801">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-801">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-802">RestrictedSitesZoneTurnOnProtectedMode</span><span class="sxs-lookup"><span data-stu-id="82605-802">RestrictedSitesZoneTurnOnProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneturnonprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-803">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-803">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-804">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-804">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-805">RestrictedSitesZoneUsePopupBlocker</span><span class="sxs-lookup"><span data-stu-id="82605-805">RestrictedSitesZoneUsePopupBlocker</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneusepopupblocker)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-806">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-806">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-807">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-807">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-808">RestrictFileDownloadInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="82605-808">RestrictFileDownloadInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictfiledownloadinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-809">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-809">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-810">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-810">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-811">ScriptedWindowSecurityRestrictionsInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="82605-811">ScriptedWindowSecurityRestrictionsInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-scriptedwindowsecurityrestrictionsinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-812">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-812">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-813">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-813">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-814">SearchProviderList</span><span class="sxs-lookup"><span data-stu-id="82605-814">SearchProviderList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-searchproviderlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-815">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-815">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-816">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-816">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-817">SecurityZonesUseOnlyMachineSettings</span><span class="sxs-lookup"><span data-stu-id="82605-817">SecurityZonesUseOnlyMachineSettings</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-securityzonesuseonlymachinesettings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-818">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-818">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-819">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-819">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-820">SpecifyUseOfActiveXInstallerService</span><span class="sxs-lookup"><span data-stu-id="82605-820">SpecifyUseOfActiveXInstallerService</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-specifyuseofactivexinstallerservice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-821">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-821">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-822">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-822">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-823">TrustedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="82605-823">TrustedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-824">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-824">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-825">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-825">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-826">TrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="82605-826">TrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-827">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-827">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-828">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-828">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-829">TrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="82605-829">TrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-830">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-830">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-831">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-831">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-832">TrustedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="82605-832">TrustedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-833">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-833">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-834">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-834">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-835">TrustedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="82605-835">TrustedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-836">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-836">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-837">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-837">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-838">TrustedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="82605-838">TrustedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-839">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-839">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-840">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-840">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-841">TrustedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="82605-841">TrustedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-842">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-842">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-843">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-843">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-844">TrustedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="82605-844">TrustedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-845">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-845">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-846">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-846">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-847">TrustedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="82605-847">TrustedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-848">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-848">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-849">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-849">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-850">TrustedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="82605-850">TrustedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-851">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-851">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-852">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-852">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="82605-853">TrustedSitesZoneDontRunAntimalwareProgramsAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="82605-853">TrustedSitesZoneDontRunAntimalwareProgramsAgainstActiveXControls</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-854">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-854">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-855">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-855">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-856">TrustedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="82605-856">TrustedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-857">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-857">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-858">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-858">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="82605-859">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedAsSafe</span><span class="sxs-lookup"><span data-stu-id="82605-859">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedAsSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-860">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-860">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-861">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-861">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="82605-862">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span><span class="sxs-lookup"><span data-stu-id="82605-862">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-863">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-863">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-864">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-864">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-865">TrustedSitesZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="82605-865">TrustedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-866">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-866">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-867">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-867">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="82605-868">TrustedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="82605-868">TrustedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82605-869">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82605-869">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82605-870">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="82605-870">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="82605-871">Requisiti</span><span class="sxs-lookup"><span data-stu-id="82605-871">Requirements</span></span>



| <span data-ttu-id="82605-872">Requisito</span><span class="sxs-lookup"><span data-stu-id="82605-872">Requirement</span></span> | <span data-ttu-id="82605-873">Valore</span><span class="sxs-lookup"><span data-stu-id="82605-873">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82605-874">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="82605-874">Minimum supported client</span></span><br/> | <span data-ttu-id="82605-875">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="82605-875">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="82605-876">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="82605-876">Minimum supported server</span></span><br/> | <span data-ttu-id="82605-877">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="82605-877">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="82605-878">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="82605-878">Namespace</span></span><br/>                | <span data-ttu-id="82605-879">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="82605-879">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="82605-880">MOF</span><span class="sxs-lookup"><span data-stu-id="82605-880">MOF</span></span><br/>                      | <dl> <span data-ttu-id="82605-881"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="82605-881"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="82605-882">DLL</span><span class="sxs-lookup"><span data-stu-id="82605-882">DLL</span></span><br/>                      | <dl> <span data-ttu-id="82605-883"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82605-883"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

