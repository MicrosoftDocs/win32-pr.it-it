---
title: Classe MDM_Policy_User_Config01_InternetExplorer02
description: La \_ classe del criterio MDM \_ utente \_ Config01 \_ InternetExplorer02 rappresenta i criteri di Internet Explorer disponibili.
ms.assetid: 2b155e65-5a81-4916-815f-23763759bb9a
keywords:
- Classe MDM_Policy_User_Config01_InternetExplorer02
- Classe MDM_Policy_User_Config01_InternetExplorer02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_User_Config01_InternetExplorer02
- MDM_Policy_User_Config01_InternetExplorer02.InstanceID
- MDM_Policy_User_Config01_InternetExplorer02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2f79c00505037508307e93120f9e2545b135678
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048412"
---
# <a name="mdm_policy_user_config01_internetexplorer02-class"></a><span data-ttu-id="5e33d-105">\_Utente criteri \_ MDM \_ Config01 \_ classe InternetExplorer02</span><span class="sxs-lookup"><span data-stu-id="5e33d-105">MDM\_Policy\_User\_Config01\_InternetExplorer02 class</span></span>

<span data-ttu-id="5e33d-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="5e33d-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="5e33d-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="5e33d-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="5e33d-108">La \_ classe del criterio MDM \_ utente \_ Config01 \_ InternetExplorer02 rappresenta i criteri di Internet Explorer disponibili.</span><span class="sxs-lookup"><span data-stu-id="5e33d-108">The MDM\_Policy\_User\_Config01\_InternetExplorer02 class represents the available Internet Explorer policies.</span></span>

<span data-ttu-id="5e33d-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="5e33d-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e33d-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5e33d-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Config01_InternetExplorer02
{
  string InstanceID;
  string ParentID;
  string AddSearchProvider;
  string AllowActiveXFiltering;
  string AllowAddOnList;
  string AllowDeletingBrowsingHistoryOnExit;
  string AllowCertificateAddressMismatchWarning;
  string AllowAutoComplete;
  string AllowEnhancedProtectedMode;
  string AllowEnterpriseModeFromToolsMenu;
  string AllowEnterpriseModeSiteList;
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
  string DisableHomePageChange;
  string DisableProcessesInEnhancedProtectedMode;
  string DisableInPrivateBrowsing;
  string DisableIgnoringCertificateErrors;
  string DisableProxyChange;
  string DisableSearchProviderChange;
  string DisableSecondaryHomePageChange;
  string DoNotAllowActiveXControlsInProtectedMode;
  string DisableSecuritySettingsCheck;
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

## <a name="members"></a><span data-ttu-id="5e33d-111">Members</span><span class="sxs-lookup"><span data-stu-id="5e33d-111">Members</span></span>

<span data-ttu-id="5e33d-112">La **classe \_ \_ \_ Config01 \_ InternetExplorer02 dell'utente dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="5e33d-112">The **MDM\_Policy\_User\_Config01\_InternetExplorer02** class has these types of members:</span></span>

-   [<span data-ttu-id="5e33d-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5e33d-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5e33d-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5e33d-114">Properties</span></span>

<span data-ttu-id="5e33d-115">La **classe \_ \_ \_ Config01 \_ InternetExplorer02 dell'utente dei criteri MDM** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="5e33d-115">The **MDM\_Policy\_User\_Config01\_InternetExplorer02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="5e33d-116">AddSearchProvider</span><span class="sxs-lookup"><span data-stu-id="5e33d-116">AddSearchProvider</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-addsearchprovider)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-119">AllowActiveXFiltering</span><span class="sxs-lookup"><span data-stu-id="5e33d-119">AllowActiveXFiltering</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowactivexfiltering)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-122">AllowAddOnList</span><span class="sxs-lookup"><span data-stu-id="5e33d-122">AllowAddOnList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowaddonlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-124">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-125">AllowAutoComplete</span><span class="sxs-lookup"><span data-stu-id="5e33d-125">AllowAutoComplete</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowautocomplete)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-127">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-128">AllowCertificateAddressMismatchWarning</span><span class="sxs-lookup"><span data-stu-id="5e33d-128">AllowCertificateAddressMismatchWarning</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowcertificateaddressmismatchwarning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-130">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-131">AllowDeletingBrowsingHistoryOnExit</span><span class="sxs-lookup"><span data-stu-id="5e33d-131">AllowDeletingBrowsingHistoryOnExit</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowdeletingbrowsinghistoryonexit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-132">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-133">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-134">AllowEnhancedProtectedMode</span><span class="sxs-lookup"><span data-stu-id="5e33d-134">AllowEnhancedProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenhancedprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-135">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-136">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-137">AllowEnterpriseModeFromToolsMenu</span><span class="sxs-lookup"><span data-stu-id="5e33d-137">AllowEnterpriseModeFromToolsMenu</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenterprisemodefromtoolsmenu)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-138">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-139">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-140">AllowEnterpriseModeSiteList</span><span class="sxs-lookup"><span data-stu-id="5e33d-140">AllowEnterpriseModeSiteList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenterprisemodesitelist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-141">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-142">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-143">AllowInternetExplorer7PolicyList</span><span class="sxs-lookup"><span data-stu-id="5e33d-143">AllowInternetExplorer7PolicyList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetexplorer7policylist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-144">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-145">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-146">AllowInternetExplorerStandardsMode</span><span class="sxs-lookup"><span data-stu-id="5e33d-146">AllowInternetExplorerStandardsMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetexplorerstandardsmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-147">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-148">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-149">AllowInternetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="5e33d-149">AllowInternetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-150">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-151">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-152">AllowIntranetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="5e33d-152">AllowIntranetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowintranetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-153">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-154">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-155">AllowLocalMachineZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="5e33d-155">AllowLocalMachineZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlocalmachinezonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-156">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-157">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-158">AllowLockedDownInternetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="5e33d-158">AllowLockedDownInternetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddowninternetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-159">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-160">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-161">AllowLockedDownIntranetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="5e33d-161">AllowLockedDownIntranetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownintranetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-162">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-163">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-164">AllowLockedDownLocalMachineZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="5e33d-164">AllowLockedDownLocalMachineZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownlocalmachinezonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-165">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-166">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-167">AllowLockedDownRestrictedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="5e33d-167">AllowLockedDownRestrictedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownrestrictedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-168">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-169">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-170">AllowOneWordEntry</span><span class="sxs-lookup"><span data-stu-id="5e33d-170">AllowOneWordEntry</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowonewordentry)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-171">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-172">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-173">AllowSiteToZoneAssignmentList</span><span class="sxs-lookup"><span data-stu-id="5e33d-173">AllowSiteToZoneAssignmentList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsitetozoneassignmentlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-174">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-175">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-176">AllowsLockedDownTrustedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="5e33d-176">AllowsLockedDownTrustedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowslockeddowntrustedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-177">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-178">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-179">AllowSoftwareWhenSignatureIsInvalid</span><span class="sxs-lookup"><span data-stu-id="5e33d-179">AllowSoftwareWhenSignatureIsInvalid</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsoftwarewhensignatureisinvalid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-180">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-181">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-182">AllowsRestrictedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="5e33d-182">AllowsRestrictedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsrestrictedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-183">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-184">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-185">AllowSuggestedSites</span><span class="sxs-lookup"><span data-stu-id="5e33d-185">AllowSuggestedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsuggestedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-186">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-187">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-187">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-188">AllowTrustedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="5e33d-188">AllowTrustedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowtrustedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-189">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-190">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-191">CheckServerCertificateRevocation</span><span class="sxs-lookup"><span data-stu-id="5e33d-191">CheckServerCertificateRevocation</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-checkservercertificaterevocation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-192">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-193">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-193">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-194">CheckSignaturesOnDownloadedPrograms</span><span class="sxs-lookup"><span data-stu-id="5e33d-194">CheckSignaturesOnDownloadedPrograms</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-checksignaturesondownloadedprograms)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-195">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-196">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-196">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-197">ConsistentMimeHandlingInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="5e33d-197">ConsistentMimeHandlingInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-consistentmimehandlinginternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-198">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-199">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-199">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-200">DisableAdobeFlash</span><span class="sxs-lookup"><span data-stu-id="5e33d-200">DisableAdobeFlash</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableadobeflash)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-201">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-202">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-202">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5e33d-203">DisableBlockingOfOutdatedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="5e33d-203">DisableBlockingOfOutdatedActiveXControls</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-204">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-205">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-205">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-206">DisableBypassOfSmartScreenWarnings</span><span class="sxs-lookup"><span data-stu-id="5e33d-206">DisableBypassOfSmartScreenWarnings</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablebypassofsmartscreenwarnings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-207">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-208">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-208">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-209">DisableBypassOfSmartScreenWarningsAboutUncommonFiles</span><span class="sxs-lookup"><span data-stu-id="5e33d-209">DisableBypassOfSmartScreenWarningsAboutUncommonFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablebypassofsmartscreenwarningsaboutuncommonfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-210">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-211">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-212">DisableConfiguringHistory</span><span class="sxs-lookup"><span data-stu-id="5e33d-212">DisableConfiguringHistory</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableconfiguringhistory)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-213">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-214">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-214">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-215">DisableCrashDetection</span><span class="sxs-lookup"><span data-stu-id="5e33d-215">DisableCrashDetection</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablecrashdetection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-216">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-217">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-217">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-218">DisableCustomerExperienceImprovementProgramParticipation</span><span class="sxs-lookup"><span data-stu-id="5e33d-218">DisableCustomerExperienceImprovementProgramParticipation</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablecustomerexperienceimprovementprogramparticipation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-219">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-220">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-220">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-221">DisableDeletingUserVisitedWebsites</span><span class="sxs-lookup"><span data-stu-id="5e33d-221">DisableDeletingUserVisitedWebsites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disabledeletinguservisitedwebsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-222">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-223">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-223">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-224">DisableEnclosureDownloading</span><span class="sxs-lookup"><span data-stu-id="5e33d-224">DisableEnclosureDownloading</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableenclosuredownloading)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-225">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-226">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-226">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-227">DisableEncryptionSupport</span><span class="sxs-lookup"><span data-stu-id="5e33d-227">DisableEncryptionSupport</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableencryptionsupport)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-228">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-229">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-229">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-230">DisableFirstRunWizard</span><span class="sxs-lookup"><span data-stu-id="5e33d-230">DisableFirstRunWizard</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablefirstrunwizard)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-231">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-232">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-232">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-233">DisableFlipAheadFeature</span><span class="sxs-lookup"><span data-stu-id="5e33d-233">DisableFlipAheadFeature</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableflipaheadfeature)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-234">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-235">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-235">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-236">DisableHomePageChange</span><span class="sxs-lookup"><span data-stu-id="5e33d-236">DisableHomePageChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablehomepagechange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-237">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-238">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-238">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-239">DisableIgnoringCertificateErrors</span><span class="sxs-lookup"><span data-stu-id="5e33d-239">DisableIgnoringCertificateErrors</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableignoringcertificateerrors)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-240">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-241">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-241">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-242">DisableInPrivateBrowsing</span><span class="sxs-lookup"><span data-stu-id="5e33d-242">DisableInPrivateBrowsing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableinprivatebrowsing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-243">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-244">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-244">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-245">DisableProcessesInEnhancedProtectedMode</span><span class="sxs-lookup"><span data-stu-id="5e33d-245">DisableProcessesInEnhancedProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableprocessesinenhancedprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-246">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-247">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-247">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-248">DisableProxyChange</span><span class="sxs-lookup"><span data-stu-id="5e33d-248">DisableProxyChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableproxychange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-249">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-250">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-250">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-251">DisableSearchProviderChange</span><span class="sxs-lookup"><span data-stu-id="5e33d-251">DisableSearchProviderChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesearchproviderchange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-252">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-253">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-253">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-254">DisableSecondaryHomePageChange</span><span class="sxs-lookup"><span data-stu-id="5e33d-254">DisableSecondaryHomePageChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesecondaryhomepagechange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-255">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-256">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-256">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-257">DisableSecuritySettingsCheck</span><span class="sxs-lookup"><span data-stu-id="5e33d-257">DisableSecuritySettingsCheck</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesecuritysettingscheck)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-258">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-259">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-259">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-260">DoNotAllowActiveXControlsInProtectedMode</span><span class="sxs-lookup"><span data-stu-id="5e33d-260">DoNotAllowActiveXControlsInProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotallowactivexcontrolsinprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-261">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-262">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-262">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-263">DoNotBlockOutdatedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="5e33d-263">DoNotBlockOutdatedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotblockoutdatedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-264">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-265">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-265">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-266">DoNotBlockOutdatedActiveXControlsOnSpecificDomains</span><span class="sxs-lookup"><span data-stu-id="5e33d-266">DoNotBlockOutdatedActiveXControlsOnSpecificDomains</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotblockoutdatedactivexcontrolsonspecificdomains)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-267">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-268">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-268">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-269">IncludeAllLocalSites</span><span class="sxs-lookup"><span data-stu-id="5e33d-269">IncludeAllLocalSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-includealllocalsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-270">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-270">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-271">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-271">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-272">IncludeAllNetworkPaths</span><span class="sxs-lookup"><span data-stu-id="5e33d-272">IncludeAllNetworkPaths</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-includeallnetworkpaths)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-273">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-274">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-274">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5e33d-275">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="5e33d-275">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-276">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-277">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5e33d-277">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-278">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5e33d-278">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-279">InternetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="5e33d-279">InternetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-280">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-280">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-281">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-281">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-282">InternetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="5e33d-282">InternetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-283">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-283">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-284">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-284">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-285">InternetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="5e33d-285">InternetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-286">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-287">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-287">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-288">InternetZoneAllowCopyPasteViaScript</span><span class="sxs-lookup"><span data-stu-id="5e33d-288">InternetZoneAllowCopyPasteViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowcopypasteviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-289">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-290">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-290">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-291">InternetZoneAllowDragAndDropCopyAndPasteFiles</span><span class="sxs-lookup"><span data-stu-id="5e33d-291">InternetZoneAllowDragAndDropCopyAndPasteFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowdraganddropcopyandpastefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-292">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-293">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-293">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-294">InternetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="5e33d-294">InternetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-295">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-296">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-296">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-297">InternetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="5e33d-297">InternetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-298">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-298">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-299">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-299">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-300">InternetZoneAllowLoadingOfXAMLFiles</span><span class="sxs-lookup"><span data-stu-id="5e33d-300">InternetZoneAllowLoadingOfXAMLFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowloadingofxamlfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-301">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-302">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-302">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-303">InternetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="5e33d-303">InternetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-304">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-305">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-305">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-306">InternetZoneAllowOnlyApprovedDomainsToUseActiveXControls</span><span class="sxs-lookup"><span data-stu-id="5e33d-306">InternetZoneAllowOnlyApprovedDomainsToUseActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowonlyapproveddomainstouseactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-307">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-308">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-308">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-309">InternetZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span><span class="sxs-lookup"><span data-stu-id="5e33d-309">InternetZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowonlyapproveddomainstousetdcactivexcontrol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-310">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-311">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-311">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-312">InternetZoneAllowScriptingOfInternetExplorerWebBrowserControls</span><span class="sxs-lookup"><span data-stu-id="5e33d-312">InternetZoneAllowScriptingOfInternetExplorerWebBrowserControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptingofinternetexplorerwebbrowsercontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-313">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-314">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-314">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-315">InternetZoneAllowScriptInitiatedWindows</span><span class="sxs-lookup"><span data-stu-id="5e33d-315">InternetZoneAllowScriptInitiatedWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptinitiatedwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-316">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-317">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-317">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-318">InternetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="5e33d-318">InternetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-319">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-320">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-320">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-321">InternetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="5e33d-321">InternetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-322">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-323">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-323">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-324">InternetZoneAllowUpdatesToStatusBarViaScript</span><span class="sxs-lookup"><span data-stu-id="5e33d-324">InternetZoneAllowUpdatesToStatusBarViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowupdatestostatusbarviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-325">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-326">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-326">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-327">InternetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="5e33d-327">InternetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-328">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-329">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-329">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-330">InternetZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="5e33d-330">InternetZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-331">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-332">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-332">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-333">InternetZoneDownloadSignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="5e33d-333">InternetZoneDownloadSignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedownloadsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-334">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-335">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-335">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-336">InternetZoneDownloadUnsignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="5e33d-336">InternetZoneDownloadUnsignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedownloadunsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-337">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-338">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-338">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-339">InternetZoneEnableCrossSiteScriptingFilter</span><span class="sxs-lookup"><span data-stu-id="5e33d-339">InternetZoneEnableCrossSiteScriptingFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenablecrosssitescriptingfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-340">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-341">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-341">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-342">InternetZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span><span class="sxs-lookup"><span data-stu-id="5e33d-342">InternetZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenabledraggingofcontentfromdifferentdomainsacrosswindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-343">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-343">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-344">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-344">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-345">InternetZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span><span class="sxs-lookup"><span data-stu-id="5e33d-345">InternetZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenabledraggingofcontentfromdifferentdomainswithinwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-346">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-347">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-347">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-348">InternetZoneEnableMIMESniffing</span><span class="sxs-lookup"><span data-stu-id="5e33d-348">InternetZoneEnableMIMESniffing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenablemimesniffing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-349">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-350">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-350">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-351">InternetZoneEnableProtectedMode</span><span class="sxs-lookup"><span data-stu-id="5e33d-351">InternetZoneEnableProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenableprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-352">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-353">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-353">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-354">InternetZoneIncludeLocalPathWhenUploadingFilesToServer</span><span class="sxs-lookup"><span data-stu-id="5e33d-354">InternetZoneIncludeLocalPathWhenUploadingFilesToServer</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneincludelocalpathwhenuploadingfilestoserver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-355">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-356">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-356">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-357">InternetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="5e33d-357">InternetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-358">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-358">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-359">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-359">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-360">InternetZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="5e33d-360">InternetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-361">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-362">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-362">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-363">InternetZoneLaunchingApplicationsAndFilesInIFRAME</span><span class="sxs-lookup"><span data-stu-id="5e33d-363">InternetZoneLaunchingApplicationsAndFilesInIFRAME</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonelaunchingapplicationsandfilesiniframe)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-364">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-364">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-365">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-365">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-366">InternetZoneLogonOptions</span><span class="sxs-lookup"><span data-stu-id="5e33d-366">InternetZoneLogonOptions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonelogonoptions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-367">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-368">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-368">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-369">InternetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="5e33d-369">InternetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-370">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-370">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-371">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-371">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5e33d-372">InternetZoneRunNETFrameworkReliantComponentsNotSignedWithAuthenticode</span><span class="sxs-lookup"><span data-stu-id="5e33d-372">InternetZoneRunNETFrameworkReliantComponentsNotSignedWithAuthenticode</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-373">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-373">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-374">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-374">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-375">InternetZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span><span class="sxs-lookup"><span data-stu-id="5e33d-375">InternetZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonerunnetframeworkreliantcomponentssignedwithauthenticode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-376">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-376">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-377">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-377">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-378">InternetZoneShowSecurityWarningForPotentiallyUnsafeFiles</span><span class="sxs-lookup"><span data-stu-id="5e33d-378">InternetZoneShowSecurityWarningForPotentiallyUnsafeFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneshowsecuritywarningforpotentiallyunsafefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-379">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-380">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-380">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-381">InternetZoneUsePopupBlocker</span><span class="sxs-lookup"><span data-stu-id="5e33d-381">InternetZoneUsePopupBlocker</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneusepopupblocker)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-382">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-383">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-383">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5e33d-384">InternetZoneWebsitesInLessPrivilegedZonesCanNavigateIntoThisZone</span><span class="sxs-lookup"><span data-stu-id="5e33d-384">InternetZoneWebsitesInLessPrivilegedZonesCanNavigateIntoThisZone</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-385">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-385">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-386">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-386">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-387">IntranetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="5e33d-387">IntranetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-388">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-388">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-389">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-389">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-390">IntranetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="5e33d-390">IntranetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-391">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-391">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-392">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-392">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-393">IntranetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="5e33d-393">IntranetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-394">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-394">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-395">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-395">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-396">IntranetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="5e33d-396">IntranetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-397">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-397">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-398">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-398">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-399">IntranetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="5e33d-399">IntranetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-400">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-400">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-401">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-401">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-402">IntranetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="5e33d-402">IntranetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-403">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-404">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-404">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-405">IntranetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="5e33d-405">IntranetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-406">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-406">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-407">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-407">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-408">IntranetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="5e33d-408">IntranetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-409">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-409">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-410">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-410">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-411">IntranetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="5e33d-411">IntranetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-412">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-412">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-413">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-413">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-414">IntranetZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="5e33d-414">IntranetZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-415">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-415">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-416">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-416">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-417">IntranetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="5e33d-417">IntranetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-418">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-418">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-419">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-419">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5e33d-420">IntranetZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span><span class="sxs-lookup"><span data-stu-id="5e33d-420">IntranetZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-421">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-421">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-422">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-422">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-423">IntranetZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="5e33d-423">IntranetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-424">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-424">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-425">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-425">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-426">IntranetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="5e33d-426">IntranetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-427">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-427">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-428">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-428">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-429">LocalMachineZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="5e33d-429">LocalMachineZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-430">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-430">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-431">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-431">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-432">LocalMachineZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="5e33d-432">LocalMachineZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-433">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-433">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-434">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-434">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-435">LocalMachineZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="5e33d-435">LocalMachineZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-436">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-436">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-437">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-437">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-438">LocalMachineZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="5e33d-438">LocalMachineZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-439">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-439">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-440">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-440">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-441">LocalMachineZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="5e33d-441">LocalMachineZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-442">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-442">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-443">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-443">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-444">LocalMachineZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="5e33d-444">LocalMachineZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-445">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-445">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-446">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-446">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-447">LocalMachineZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="5e33d-447">LocalMachineZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-448">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-448">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-449">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-449">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-450">LocalMachineZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="5e33d-450">LocalMachineZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-451">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-451">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-452">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-452">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-453">LocalMachineZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="5e33d-453">LocalMachineZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-454">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-454">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-455">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-455">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-456">LocalMachineZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="5e33d-456">LocalMachineZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-457">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-457">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-458">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-458">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-459">LocalMachineZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="5e33d-459">LocalMachineZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-460">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-460">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-461">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-461">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-462">LocalMachineZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="5e33d-462">LocalMachineZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-463">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-463">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-464">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-464">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-465">LocalMachineZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="5e33d-465">LocalMachineZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-466">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-466">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-467">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-467">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-468">LockedDownInternetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="5e33d-468">LockedDownInternetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-469">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-469">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-470">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-470">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-471">LockedDownInternetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="5e33d-471">LockedDownInternetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-472">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-472">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-473">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-473">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-474">LockedDownInternetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="5e33d-474">LockedDownInternetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-475">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-475">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-476">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-476">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-477">LockedDownInternetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="5e33d-477">LockedDownInternetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-478">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-478">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-479">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-479">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-480">LockedDownInternetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="5e33d-480">LockedDownInternetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-481">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-481">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-482">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-482">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-483">LockedDownInternetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="5e33d-483">LockedDownInternetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-484">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-484">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-485">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-485">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-486">LockedDownInternetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="5e33d-486">LockedDownInternetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-487">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-487">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-488">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-488">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-489">LockedDownInternetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="5e33d-489">LockedDownInternetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-490">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-490">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-491">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-491">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-492">LockedDownInternetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="5e33d-492">LockedDownInternetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-493">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-493">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-494">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-494">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-495">LockedDownInternetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="5e33d-495">LockedDownInternetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-496">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-496">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-497">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-497">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-498">LockedDownInternetZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="5e33d-498">LockedDownInternetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-499">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-499">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-500">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-500">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-501">LockedDownInternetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="5e33d-501">LockedDownInternetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-502">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-502">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-503">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-503">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-504">LockedDownIntranetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="5e33d-504">LockedDownIntranetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-505">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-505">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-506">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-506">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-507">LockedDownIntranetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="5e33d-507">LockedDownIntranetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-508">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-508">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-509">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-509">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-510">LockedDownIntranetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="5e33d-510">LockedDownIntranetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-511">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-511">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-512">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-512">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-513">LockedDownIntranetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="5e33d-513">LockedDownIntranetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-514">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-514">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-515">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-515">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-516">LockedDownIntranetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="5e33d-516">LockedDownIntranetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-517">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-517">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-518">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-518">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-519">LockedDownIntranetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="5e33d-519">LockedDownIntranetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-520">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-520">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-521">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-521">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-522">LockedDownIntranetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="5e33d-522">LockedDownIntranetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-523">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-523">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-524">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-524">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-525">LockedDownIntranetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="5e33d-525">LockedDownIntranetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-526">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-526">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-527">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-527">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-528">LockedDownIntranetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="5e33d-528">LockedDownIntranetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-529">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-529">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-530">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-530">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-531">LockedDownIntranetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="5e33d-531">LockedDownIntranetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-532">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-532">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-533">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-533">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-534">LockedDownIntranetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="5e33d-534">LockedDownIntranetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-535">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-535">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-536">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-536">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-537">LockedDownLocalMachineZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="5e33d-537">LockedDownLocalMachineZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-538">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-538">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-539">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-539">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-540">LockedDownLocalMachineZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="5e33d-540">LockedDownLocalMachineZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-541">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-541">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-542">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-542">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-543">LockedDownLocalMachineZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="5e33d-543">LockedDownLocalMachineZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-544">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-544">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-545">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-545">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-546">LockedDownLocalMachineZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="5e33d-546">LockedDownLocalMachineZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-547">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-547">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-548">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-548">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-549">LockedDownLocalMachineZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="5e33d-549">LockedDownLocalMachineZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-550">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-550">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-551">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-551">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-552">LockedDownLocalMachineZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="5e33d-552">LockedDownLocalMachineZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-553">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-553">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-554">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-554">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-555">LockedDownLocalMachineZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="5e33d-555">LockedDownLocalMachineZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-556">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-556">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-557">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-557">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-558">LockedDownLocalMachineZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="5e33d-558">LockedDownLocalMachineZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-559">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-559">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-560">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-560">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-561">LockedDownLocalMachineZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="5e33d-561">LockedDownLocalMachineZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-562">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-562">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-563">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-563">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-564">LockedDownLocalMachineZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="5e33d-564">LockedDownLocalMachineZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-565">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-565">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-566">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-566">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-567">LockedDownLocalMachineZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="5e33d-567">LockedDownLocalMachineZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-568">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-568">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-569">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-569">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-570">LockedDownLocalMachineZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="5e33d-570">LockedDownLocalMachineZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-571">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-571">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-572">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-572">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-573">LockedDownRestrictedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="5e33d-573">LockedDownRestrictedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-574">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-574">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-575">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-575">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-576">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="5e33d-576">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-577">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-577">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-578">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-578">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-579">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="5e33d-579">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-580">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-580">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-581">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-581">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-582">LockedDownRestrictedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="5e33d-582">LockedDownRestrictedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-583">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-583">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-584">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-584">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-585">LockedDownRestrictedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="5e33d-585">LockedDownRestrictedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-586">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-586">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-587">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-587">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-588">LockedDownRestrictedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="5e33d-588">LockedDownRestrictedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-589">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-589">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-590">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-590">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-591">LockedDownRestrictedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="5e33d-591">LockedDownRestrictedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-592">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-592">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-593">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-593">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-594">LockedDownRestrictedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="5e33d-594">LockedDownRestrictedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-595">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-595">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-596">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-596">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-597">LockedDownRestrictedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="5e33d-597">LockedDownRestrictedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-598">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-598">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-599">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-599">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-600">LockedDownRestrictedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="5e33d-600">LockedDownRestrictedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-601">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-601">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-602">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-602">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-603">LockedDownRestrictedSitesZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="5e33d-603">LockedDownRestrictedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-604">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-604">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-605">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-605">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-606">LockedDownRestrictedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="5e33d-606">LockedDownRestrictedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-607">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-607">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-608">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-608">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-609">LockedDownTrustedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="5e33d-609">LockedDownTrustedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-610">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-610">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-611">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-611">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-612">LockedDownTrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="5e33d-612">LockedDownTrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-613">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-613">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-614">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-614">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-615">LockedDownTrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="5e33d-615">LockedDownTrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-616">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-616">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-617">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-617">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-618">LockedDownTrustedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="5e33d-618">LockedDownTrustedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-619">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-619">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-620">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-620">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-621">LockedDownTrustedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="5e33d-621">LockedDownTrustedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-622">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-622">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-623">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-623">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-624">LockedDownTrustedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="5e33d-624">LockedDownTrustedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-625">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-625">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-626">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-626">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-627">LockedDownTrustedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="5e33d-627">LockedDownTrustedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-628">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-628">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-629">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-629">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-630">LockedDownTrustedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="5e33d-630">LockedDownTrustedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-631">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-631">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-632">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-632">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-633">LockedDownTrustedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="5e33d-633">LockedDownTrustedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-634">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-634">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-635">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-635">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-636">LockedDownTrustedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="5e33d-636">LockedDownTrustedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-637">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-637">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-638">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-638">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-639">LockedDownTrustedSitesZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="5e33d-639">LockedDownTrustedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-640">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-640">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-641">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-641">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-642">LockedDownTrustedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="5e33d-642">LockedDownTrustedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-643">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-643">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-644">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-644">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-645">MimeSniffingSafetyFeatureInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="5e33d-645">MimeSniffingSafetyFeatureInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-mimesniffingsafetyfeatureinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-646">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-646">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-647">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-647">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-648">MKProtocolSecurityRestrictionInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="5e33d-648">MKProtocolSecurityRestrictionInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-mkprotocolsecurityrestrictioninternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-649">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-649">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-650">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-650">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-651">NotificationBarInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="5e33d-651">NotificationBarInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-notificationbarinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-652">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-652">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-653">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-653">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5e33d-654">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="5e33d-654">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-655">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-655">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-656">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5e33d-656">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-657">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5e33d-657">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-658">PreventManagingSmartScreenFilter</span><span class="sxs-lookup"><span data-stu-id="5e33d-658">PreventManagingSmartScreenFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-preventmanagingsmartscreenfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-659">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-659">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-660">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-660">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-661">PreventPerUserInstallationOfActiveXControls</span><span class="sxs-lookup"><span data-stu-id="5e33d-661">PreventPerUserInstallationOfActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-preventperuserinstallationofactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-662">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-662">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-663">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-663">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-664">ProtectionFromZoneElevationInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="5e33d-664">ProtectionFromZoneElevationInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-protectionfromzoneelevationinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-665">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-665">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-666">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-666">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-667">RemoveRunThisTimeButtonForOutdatedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="5e33d-667">RemoveRunThisTimeButtonForOutdatedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-removerunthistimebuttonforoutdatedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-668">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-668">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-669">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-669">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-670">RestrictActiveXInstallInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="5e33d-670">RestrictActiveXInstallInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictactivexinstallinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-671">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-671">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-672">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-672">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-673">RestrictedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="5e33d-673">RestrictedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-674">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-674">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-675">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-675">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-676">RestrictedSitesZoneAllowActiveScripting</span><span class="sxs-lookup"><span data-stu-id="5e33d-676">RestrictedSitesZoneAllowActiveScripting</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowactivescripting)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-677">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-677">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-678">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-678">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-679">RestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="5e33d-679">RestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-680">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-680">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-681">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-681">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-682">RestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="5e33d-682">RestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-683">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-683">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-684">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-684">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-685">RestrictedSitesZoneAllowBinaryAndScriptBehaviors</span><span class="sxs-lookup"><span data-stu-id="5e33d-685">RestrictedSitesZoneAllowBinaryAndScriptBehaviors</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowbinaryandscriptbehaviors)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-686">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-686">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-687">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-687">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-688">RestrictedSitesZoneAllowCopyPasteViaScript</span><span class="sxs-lookup"><span data-stu-id="5e33d-688">RestrictedSitesZoneAllowCopyPasteViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowcopypasteviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-689">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-689">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-690">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-690">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-691">RestrictedSitesZoneAllowDragAndDropCopyAndPasteFiles</span><span class="sxs-lookup"><span data-stu-id="5e33d-691">RestrictedSitesZoneAllowDragAndDropCopyAndPasteFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowdraganddropcopyandpastefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-692">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-692">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-693">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-693">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-694">RestrictedSitesZoneAllowFileDownloads</span><span class="sxs-lookup"><span data-stu-id="5e33d-694">RestrictedSitesZoneAllowFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-695">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-695">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-696">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-696">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-697">RestrictedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="5e33d-697">RestrictedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-698">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-698">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-699">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-699">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-700">RestrictedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="5e33d-700">RestrictedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-701">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-701">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-702">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-702">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-703">RestrictedSitesZoneAllowLoadingOfXAMLFiles</span><span class="sxs-lookup"><span data-stu-id="5e33d-703">RestrictedSitesZoneAllowLoadingOfXAMLFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowloadingofxamlfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-704">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-704">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-705">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-705">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-706">RestrictedSitesZoneAllowMETAREFRESH</span><span class="sxs-lookup"><span data-stu-id="5e33d-706">RestrictedSitesZoneAllowMETAREFRESH</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowmetarefresh)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-707">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-707">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-708">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-708">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-709">RestrictedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="5e33d-709">RestrictedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-710">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-710">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-711">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-711">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-712">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseActiveXControls</span><span class="sxs-lookup"><span data-stu-id="5e33d-712">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowonlyapproveddomainstouseactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-713">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-713">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-714">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-714">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-715">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span><span class="sxs-lookup"><span data-stu-id="5e33d-715">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowonlyapproveddomainstousetdcactivexcontrol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-716">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-716">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-717">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-717">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-718">RestrictedSitesZoneAllowScriptingOfInternetExplorerWebBrowserControls</span><span class="sxs-lookup"><span data-stu-id="5e33d-718">RestrictedSitesZoneAllowScriptingOfInternetExplorerWebBrowserControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptingofinternetexplorerwebbrowsercontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-719">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-719">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-720">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-720">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-721">RestrictedSitesZoneAllowScriptInitiatedWindows</span><span class="sxs-lookup"><span data-stu-id="5e33d-721">RestrictedSitesZoneAllowScriptInitiatedWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptinitiatedwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-722">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-722">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-723">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-723">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-724">RestrictedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="5e33d-724">RestrictedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-725">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-725">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-726">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-726">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-727">RestrictedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="5e33d-727">RestrictedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-728">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-728">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-729">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-729">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-730">RestrictedSitesZoneAllowUpdatesToStatusBarViaScript</span><span class="sxs-lookup"><span data-stu-id="5e33d-730">RestrictedSitesZoneAllowUpdatesToStatusBarViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowupdatestostatusbarviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-731">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-731">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-732">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-732">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-733">RestrictedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="5e33d-733">RestrictedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-734">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-734">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-735">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-735">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-736">RestrictedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="5e33d-736">RestrictedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-737">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-737">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-738">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-738">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-739">RestrictedSitesZoneDownloadSignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="5e33d-739">RestrictedSitesZoneDownloadSignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedownloadsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-740">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-740">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-741">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-741">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-742">RestrictedSitesZoneDownloadUnsignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="5e33d-742">RestrictedSitesZoneDownloadUnsignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedownloadunsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-743">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-743">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-744">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-744">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-745">RestrictedSitesZoneEnableCrossSiteScriptingFilter</span><span class="sxs-lookup"><span data-stu-id="5e33d-745">RestrictedSitesZoneEnableCrossSiteScriptingFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenablecrosssitescriptingfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-746">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-746">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-747">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-747">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-748">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span><span class="sxs-lookup"><span data-stu-id="5e33d-748">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenabledraggingofcontentfromdifferentdomainsacrosswindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-749">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-749">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-750">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-750">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-751">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span><span class="sxs-lookup"><span data-stu-id="5e33d-751">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenabledraggingofcontentfromdifferentdomainswithinwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-752">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-752">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-753">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-753">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-754">RestrictedSitesZoneEnableMIMESniffing</span><span class="sxs-lookup"><span data-stu-id="5e33d-754">RestrictedSitesZoneEnableMIMESniffing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenablemimesniffing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-755">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-755">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-756">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-756">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-757">RestrictedSitesZoneIncludeLocalPathWhenUploadingFilesToServer</span><span class="sxs-lookup"><span data-stu-id="5e33d-757">RestrictedSitesZoneIncludeLocalPathWhenUploadingFilesToServer</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneincludelocalpathwhenuploadingfilestoserver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-758">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-758">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-759">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-759">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-760">RestrictedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="5e33d-760">RestrictedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-761">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-761">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-762">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-762">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-763">RestrictedSitesZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="5e33d-763">RestrictedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-764">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-764">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-765">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-765">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-766">RestrictedSitesZoneLaunchingApplicationsAndFilesInIFRAME</span><span class="sxs-lookup"><span data-stu-id="5e33d-766">RestrictedSitesZoneLaunchingApplicationsAndFilesInIFRAME</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonelaunchingapplicationsandfilesiniframe)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-767">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-767">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-768">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-768">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-769">RestrictedSitesZoneLogonOptions</span><span class="sxs-lookup"><span data-stu-id="5e33d-769">RestrictedSitesZoneLogonOptions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonelogonoptions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-770">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-770">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-771">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-771">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-772">RestrictedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="5e33d-772">RestrictedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-773">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-773">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-774">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-774">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5e33d-775">RestrictedSitesZoneNavigateWindowsAndFramesAcrossDomains</span><span class="sxs-lookup"><span data-stu-id="5e33d-775">RestrictedSitesZoneNavigateWindowsAndFramesAcrossDomains</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-776">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-776">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-777">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-777">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-778">RestrictedSitesZoneRunActiveXControlsAndPlugins</span><span class="sxs-lookup"><span data-stu-id="5e33d-778">RestrictedSitesZoneRunActiveXControlsAndPlugins</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonerunactivexcontrolsandplugins)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-779">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-779">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-780">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-780">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-781">RestrictedSitesZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span><span class="sxs-lookup"><span data-stu-id="5e33d-781">RestrictedSitesZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonerunnetframeworkreliantcomponentssignedwithauthenticode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-782">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-782">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-783">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-783">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-784">RestrictedSitesZoneScriptActiveXControlsMarkedSafeForScripting</span><span class="sxs-lookup"><span data-stu-id="5e33d-784">RestrictedSitesZoneScriptActiveXControlsMarkedSafeForScripting</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonescriptactivexcontrolsmarkedsafeforscripting)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-785">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-785">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-786">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-786">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-787">RestrictedSitesZoneScriptingOfJavaApplets</span><span class="sxs-lookup"><span data-stu-id="5e33d-787">RestrictedSitesZoneScriptingOfJavaApplets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonescriptingofjavaapplets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-788">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-788">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-789">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-789">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-790">RestrictedSitesZoneShowSecurityWarningForPotentiallyUnsafeFiles</span><span class="sxs-lookup"><span data-stu-id="5e33d-790">RestrictedSitesZoneShowSecurityWarningForPotentiallyUnsafeFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneshowsecuritywarningforpotentiallyunsafefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-791">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-791">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-792">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-792">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5e33d-793">RestrictedSitesZoneTurnOnCrossSiteScriptingFilter</span><span class="sxs-lookup"><span data-stu-id="5e33d-793">RestrictedSitesZoneTurnOnCrossSiteScriptingFilter</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-794">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-794">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-795">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-795">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-796">RestrictedSitesZoneTurnOnProtectedMode</span><span class="sxs-lookup"><span data-stu-id="5e33d-796">RestrictedSitesZoneTurnOnProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneturnonprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-797">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-797">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-798">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-798">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-799">RestrictedSitesZoneUsePopupBlocker</span><span class="sxs-lookup"><span data-stu-id="5e33d-799">RestrictedSitesZoneUsePopupBlocker</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneusepopupblocker)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-800">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-800">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-801">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-801">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-802">RestrictFileDownloadInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="5e33d-802">RestrictFileDownloadInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictfiledownloadinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-803">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-803">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-804">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-804">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-805">ScriptedWindowSecurityRestrictionsInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="5e33d-805">ScriptedWindowSecurityRestrictionsInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-scriptedwindowsecurityrestrictionsinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-806">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-806">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-807">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-807">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-808">SearchProviderList</span><span class="sxs-lookup"><span data-stu-id="5e33d-808">SearchProviderList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-searchproviderlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-809">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-809">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-810">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-810">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-811">SpecifyUseOfActiveXInstallerService</span><span class="sxs-lookup"><span data-stu-id="5e33d-811">SpecifyUseOfActiveXInstallerService</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-specifyuseofactivexinstallerservice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-812">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-812">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-813">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-813">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-814">TrustedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="5e33d-814">TrustedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-815">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-815">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-816">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-816">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-817">TrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="5e33d-817">TrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-818">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-818">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-819">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-819">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-820">TrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="5e33d-820">TrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-821">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-821">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-822">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-822">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-823">TrustedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="5e33d-823">TrustedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-824">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-824">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-825">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-825">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-826">TrustedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="5e33d-826">TrustedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-827">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-827">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-828">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-828">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-829">TrustedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="5e33d-829">TrustedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-830">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-830">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-831">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-831">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-832">TrustedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="5e33d-832">TrustedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-833">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-833">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-834">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-834">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-835">TrustedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="5e33d-835">TrustedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-836">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-836">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-837">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-837">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-838">TrustedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="5e33d-838">TrustedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-839">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-839">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-840">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-840">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-841">TrustedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="5e33d-841">TrustedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-842">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-842">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-843">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-843">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5e33d-844">TrustedSitesZoneDontRunAntimalwareProgramsAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="5e33d-844">TrustedSitesZoneDontRunAntimalwareProgramsAgainstActiveXControls</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-845">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-845">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-846">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-846">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-847">TrustedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="5e33d-847">TrustedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-848">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-848">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-849">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-849">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5e33d-850">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedAsSafe</span><span class="sxs-lookup"><span data-stu-id="5e33d-850">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedAsSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-851">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-851">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-852">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-852">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5e33d-853">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span><span class="sxs-lookup"><span data-stu-id="5e33d-853">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-854">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-854">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-855">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-855">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-856">TrustedSitesZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="5e33d-856">TrustedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-857">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-857">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-858">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-858">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e33d-859">TrustedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="5e33d-859">TrustedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e33d-860">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5e33d-860">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e33d-861">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5e33d-861">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5e33d-862">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5e33d-862">Requirements</span></span>



| <span data-ttu-id="5e33d-863">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e33d-863">Requirement</span></span> | <span data-ttu-id="5e33d-864">Valore</span><span class="sxs-lookup"><span data-stu-id="5e33d-864">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e33d-865">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5e33d-865">Minimum supported client</span></span><br/> | <span data-ttu-id="5e33d-866">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="5e33d-866">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5e33d-867">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5e33d-867">Minimum supported server</span></span><br/> | <span data-ttu-id="5e33d-868">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="5e33d-868">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="5e33d-869">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5e33d-869">Namespace</span></span><br/>                | <span data-ttu-id="5e33d-870">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="5e33d-870">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="5e33d-871">MOF</span><span class="sxs-lookup"><span data-stu-id="5e33d-871">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5e33d-872"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5e33d-872"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="5e33d-873">DLL</span><span class="sxs-lookup"><span data-stu-id="5e33d-873">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e33d-874"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e33d-874"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

