---
title: Classe MDM_Policy_User_Config01_InternetExplorer02
description: La \_ classe del criterio MDM \_ utente \_ Result01 \_ InternetExplorer02 rappresenta i criteri di Internet Explorer disponibili.
ms.assetid: efd999aa-4aa8-486d-82d4-20af7e2005fe
keywords:
- Classe MDM_Policy_User_Config01_InternetExplorer02
- Classe MDM_Policy_User_Result01_InternetExplorer02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_User_Result01_InternetExplorer02
- MDM_Policy_User_Result01_InternetExplorer02.InstanceID
- MDM_Policy_User_Result01_InternetExplorer02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8693720c7a973cc6bc689abbf76a4674f185e23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475310"
---
# <a name="mdm_policy_user_result01_internetexplorer02-class"></a><span data-ttu-id="ffc46-105">\_Utente criteri \_ MDM \_ Result01 \_ classe InternetExplorer02</span><span class="sxs-lookup"><span data-stu-id="ffc46-105">MDM\_Policy\_User\_Result01\_InternetExplorer02 class</span></span>

<span data-ttu-id="ffc46-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="ffc46-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="ffc46-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="ffc46-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="ffc46-108">La \_ classe del criterio MDM \_ utente \_ Result01 \_ InternetExplorer02 rappresenta i criteri di Internet Explorer disponibili.</span><span class="sxs-lookup"><span data-stu-id="ffc46-108">The MDM\_Policy\_User\_Result01\_InternetExplorer02 class represents the available Internet Explorer policies.</span></span>

<span data-ttu-id="ffc46-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="ffc46-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffc46-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ffc46-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Result01_InternetExplorer02
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

## <a name="members"></a><span data-ttu-id="ffc46-111">Members</span><span class="sxs-lookup"><span data-stu-id="ffc46-111">Members</span></span>

<span data-ttu-id="ffc46-112">La **classe \_ \_ \_ Result01 \_ InternetExplorer02 dell'utente dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ffc46-112">The **MDM\_Policy\_User\_Result01\_InternetExplorer02** class has these types of members:</span></span>

-   [<span data-ttu-id="ffc46-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ffc46-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ffc46-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ffc46-114">Properties</span></span>

<span data-ttu-id="ffc46-115">La **classe \_ \_ \_ Result01 \_ InternetExplorer02 dell'utente dei criteri MDM** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="ffc46-115">The **MDM\_Policy\_User\_Result01\_InternetExplorer02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="ffc46-116">AddSearchProvider</span><span class="sxs-lookup"><span data-stu-id="ffc46-116">AddSearchProvider</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-addsearchprovider)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-119">AllowActiveXFiltering</span><span class="sxs-lookup"><span data-stu-id="ffc46-119">AllowActiveXFiltering</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowactivexfiltering)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-122">AllowAddOnList</span><span class="sxs-lookup"><span data-stu-id="ffc46-122">AllowAddOnList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowaddonlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-124">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-125">AllowAutoComplete</span><span class="sxs-lookup"><span data-stu-id="ffc46-125">AllowAutoComplete</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowautocomplete)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-127">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-128">AllowCertificateAddressMismatchWarning</span><span class="sxs-lookup"><span data-stu-id="ffc46-128">AllowCertificateAddressMismatchWarning</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowcertificateaddressmismatchwarning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-130">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-131">AllowDeletingBrowsingHistoryOnExit</span><span class="sxs-lookup"><span data-stu-id="ffc46-131">AllowDeletingBrowsingHistoryOnExit</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowdeletingbrowsinghistoryonexit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-132">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-133">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-134">AllowEnhancedProtectedMode</span><span class="sxs-lookup"><span data-stu-id="ffc46-134">AllowEnhancedProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenhancedprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-135">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-136">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-137">AllowEnterpriseModeFromToolsMenu</span><span class="sxs-lookup"><span data-stu-id="ffc46-137">AllowEnterpriseModeFromToolsMenu</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenterprisemodefromtoolsmenu)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-138">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-139">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-140">AllowEnterpriseModeSiteList</span><span class="sxs-lookup"><span data-stu-id="ffc46-140">AllowEnterpriseModeSiteList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenterprisemodesitelist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-141">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-142">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-143">AllowInternetExplorer7PolicyList</span><span class="sxs-lookup"><span data-stu-id="ffc46-143">AllowInternetExplorer7PolicyList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetexplorer7policylist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-144">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-145">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-146">AllowInternetExplorerStandardsMode</span><span class="sxs-lookup"><span data-stu-id="ffc46-146">AllowInternetExplorerStandardsMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetexplorerstandardsmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-147">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-148">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-149">AllowInternetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="ffc46-149">AllowInternetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-150">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-151">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-152">AllowIntranetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="ffc46-152">AllowIntranetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowintranetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-153">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-154">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-155">AllowLocalMachineZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="ffc46-155">AllowLocalMachineZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlocalmachinezonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-156">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-157">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-158">AllowLockedDownInternetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="ffc46-158">AllowLockedDownInternetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddowninternetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-159">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-160">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-161">AllowLockedDownIntranetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="ffc46-161">AllowLockedDownIntranetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownintranetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-162">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-163">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-164">AllowLockedDownLocalMachineZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="ffc46-164">AllowLockedDownLocalMachineZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownlocalmachinezonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-165">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-166">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-167">AllowLockedDownRestrictedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="ffc46-167">AllowLockedDownRestrictedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownrestrictedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-168">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-169">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-170">AllowOneWordEntry</span><span class="sxs-lookup"><span data-stu-id="ffc46-170">AllowOneWordEntry</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowonewordentry)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-171">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-172">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-173">AllowSiteToZoneAssignmentList</span><span class="sxs-lookup"><span data-stu-id="ffc46-173">AllowSiteToZoneAssignmentList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsitetozoneassignmentlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-174">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-175">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-176">AllowsLockedDownTrustedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="ffc46-176">AllowsLockedDownTrustedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowslockeddowntrustedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-177">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-178">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-179">AllowSoftwareWhenSignatureIsInvalid</span><span class="sxs-lookup"><span data-stu-id="ffc46-179">AllowSoftwareWhenSignatureIsInvalid</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsoftwarewhensignatureisinvalid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-180">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-181">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-182">AllowsRestrictedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="ffc46-182">AllowsRestrictedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsrestrictedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-183">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-184">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-185">AllowSuggestedSites</span><span class="sxs-lookup"><span data-stu-id="ffc46-185">AllowSuggestedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsuggestedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-186">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-187">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-187">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-188">AllowTrustedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="ffc46-188">AllowTrustedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowtrustedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-189">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-190">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-191">CheckServerCertificateRevocation</span><span class="sxs-lookup"><span data-stu-id="ffc46-191">CheckServerCertificateRevocation</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-checkservercertificaterevocation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-192">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-193">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-193">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-194">CheckSignaturesOnDownloadedPrograms</span><span class="sxs-lookup"><span data-stu-id="ffc46-194">CheckSignaturesOnDownloadedPrograms</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-checksignaturesondownloadedprograms)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-195">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-196">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-196">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-197">ConsistentMimeHandlingInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="ffc46-197">ConsistentMimeHandlingInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-consistentmimehandlinginternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-198">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-199">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-199">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-200">DisableAdobeFlash</span><span class="sxs-lookup"><span data-stu-id="ffc46-200">DisableAdobeFlash</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableadobeflash)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-201">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-202">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-202">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ffc46-203">DisableBlockingOfOutdatedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="ffc46-203">DisableBlockingOfOutdatedActiveXControls</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-204">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-205">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-205">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-206">DisableBypassOfSmartScreenWarnings</span><span class="sxs-lookup"><span data-stu-id="ffc46-206">DisableBypassOfSmartScreenWarnings</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablebypassofsmartscreenwarnings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-207">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-208">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-208">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-209">DisableBypassOfSmartScreenWarningsAboutUncommonFiles</span><span class="sxs-lookup"><span data-stu-id="ffc46-209">DisableBypassOfSmartScreenWarningsAboutUncommonFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablebypassofsmartscreenwarningsaboutuncommonfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-210">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-211">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-212">DisableConfiguringHistory</span><span class="sxs-lookup"><span data-stu-id="ffc46-212">DisableConfiguringHistory</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableconfiguringhistory)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-213">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-214">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-214">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-215">DisableCrashDetection</span><span class="sxs-lookup"><span data-stu-id="ffc46-215">DisableCrashDetection</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablecrashdetection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-216">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-217">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-217">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-218">DisableCustomerExperienceImprovementProgramParticipation</span><span class="sxs-lookup"><span data-stu-id="ffc46-218">DisableCustomerExperienceImprovementProgramParticipation</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablecustomerexperienceimprovementprogramparticipation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-219">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-220">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-220">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-221">DisableDeletingUserVisitedWebsites</span><span class="sxs-lookup"><span data-stu-id="ffc46-221">DisableDeletingUserVisitedWebsites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disabledeletinguservisitedwebsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-222">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-223">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-223">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-224">DisableEnclosureDownloading</span><span class="sxs-lookup"><span data-stu-id="ffc46-224">DisableEnclosureDownloading</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableenclosuredownloading)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-225">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-226">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-226">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-227">DisableEncryptionSupport</span><span class="sxs-lookup"><span data-stu-id="ffc46-227">DisableEncryptionSupport</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableencryptionsupport)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-228">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-229">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-229">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-230">DisableFirstRunWizard</span><span class="sxs-lookup"><span data-stu-id="ffc46-230">DisableFirstRunWizard</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablefirstrunwizard)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-231">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-232">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-232">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-233">DisableFlipAheadFeature</span><span class="sxs-lookup"><span data-stu-id="ffc46-233">DisableFlipAheadFeature</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableflipaheadfeature)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-234">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-235">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-235">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-236">DisableHomePageChange</span><span class="sxs-lookup"><span data-stu-id="ffc46-236">DisableHomePageChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablehomepagechange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-237">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-238">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-238">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-239">DisableIgnoringCertificateErrors</span><span class="sxs-lookup"><span data-stu-id="ffc46-239">DisableIgnoringCertificateErrors</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableignoringcertificateerrors)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-240">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-241">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-241">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-242">DisableInPrivateBrowsing</span><span class="sxs-lookup"><span data-stu-id="ffc46-242">DisableInPrivateBrowsing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableinprivatebrowsing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-243">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-244">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-244">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-245">DisableProcessesInEnhancedProtectedMode</span><span class="sxs-lookup"><span data-stu-id="ffc46-245">DisableProcessesInEnhancedProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableprocessesinenhancedprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-246">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-247">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-247">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-248">DisableProxyChange</span><span class="sxs-lookup"><span data-stu-id="ffc46-248">DisableProxyChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableproxychange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-249">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-250">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-250">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-251">DisableSearchProviderChange</span><span class="sxs-lookup"><span data-stu-id="ffc46-251">DisableSearchProviderChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesearchproviderchange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-252">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-253">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-253">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-254">DisableSecondaryHomePageChange</span><span class="sxs-lookup"><span data-stu-id="ffc46-254">DisableSecondaryHomePageChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesecondaryhomepagechange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-255">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-256">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-256">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-257">DisableSecuritySettingsCheck</span><span class="sxs-lookup"><span data-stu-id="ffc46-257">DisableSecuritySettingsCheck</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesecuritysettingscheck)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-258">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-259">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-259">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-260">DoNotAllowActiveXControlsInProtectedMode</span><span class="sxs-lookup"><span data-stu-id="ffc46-260">DoNotAllowActiveXControlsInProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotallowactivexcontrolsinprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-261">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-262">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-262">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-263">DoNotBlockOutdatedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="ffc46-263">DoNotBlockOutdatedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotblockoutdatedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-264">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-265">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-265">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-266">DoNotBlockOutdatedActiveXControlsOnSpecificDomains</span><span class="sxs-lookup"><span data-stu-id="ffc46-266">DoNotBlockOutdatedActiveXControlsOnSpecificDomains</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotblockoutdatedactivexcontrolsonspecificdomains)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-267">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-268">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-268">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-269">IncludeAllLocalSites</span><span class="sxs-lookup"><span data-stu-id="ffc46-269">IncludeAllLocalSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-includealllocalsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-270">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-270">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-271">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-271">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-272">IncludeAllNetworkPaths</span><span class="sxs-lookup"><span data-stu-id="ffc46-272">IncludeAllNetworkPaths</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-includeallnetworkpaths)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-273">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-274">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-274">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ffc46-275">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ffc46-275">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-276">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-277">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ffc46-277">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-278">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ffc46-278">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-279">InternetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="ffc46-279">InternetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-280">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-280">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-281">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-281">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-282">InternetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="ffc46-282">InternetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-283">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-283">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-284">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-284">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-285">InternetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="ffc46-285">InternetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-286">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-287">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-287">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-288">InternetZoneAllowCopyPasteViaScript</span><span class="sxs-lookup"><span data-stu-id="ffc46-288">InternetZoneAllowCopyPasteViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowcopypasteviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-289">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-290">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-290">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-291">InternetZoneAllowDragAndDropCopyAndPasteFiles</span><span class="sxs-lookup"><span data-stu-id="ffc46-291">InternetZoneAllowDragAndDropCopyAndPasteFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowdraganddropcopyandpastefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-292">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-293">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-293">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-294">InternetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="ffc46-294">InternetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-295">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-296">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-296">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-297">InternetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="ffc46-297">InternetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-298">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-298">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-299">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-299">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-300">InternetZoneAllowLoadingOfXAMLFiles</span><span class="sxs-lookup"><span data-stu-id="ffc46-300">InternetZoneAllowLoadingOfXAMLFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowloadingofxamlfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-301">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-302">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-302">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-303">InternetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="ffc46-303">InternetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-304">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-305">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-305">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-306">InternetZoneAllowOnlyApprovedDomainsToUseActiveXControls</span><span class="sxs-lookup"><span data-stu-id="ffc46-306">InternetZoneAllowOnlyApprovedDomainsToUseActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowonlyapproveddomainstouseactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-307">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-308">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-308">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-309">InternetZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span><span class="sxs-lookup"><span data-stu-id="ffc46-309">InternetZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowonlyapproveddomainstousetdcactivexcontrol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-310">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-311">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-311">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-312">InternetZoneAllowScriptingOfInternetExplorerWebBrowserControls</span><span class="sxs-lookup"><span data-stu-id="ffc46-312">InternetZoneAllowScriptingOfInternetExplorerWebBrowserControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptingofinternetexplorerwebbrowsercontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-313">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-314">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-314">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-315">InternetZoneAllowScriptInitiatedWindows</span><span class="sxs-lookup"><span data-stu-id="ffc46-315">InternetZoneAllowScriptInitiatedWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptinitiatedwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-316">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-317">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-317">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-318">InternetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="ffc46-318">InternetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-319">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-320">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-320">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-321">InternetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="ffc46-321">InternetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-322">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-323">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-323">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-324">InternetZoneAllowUpdatesToStatusBarViaScript</span><span class="sxs-lookup"><span data-stu-id="ffc46-324">InternetZoneAllowUpdatesToStatusBarViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowupdatestostatusbarviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-325">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-326">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-326">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-327">InternetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="ffc46-327">InternetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-328">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-329">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-329">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-330">InternetZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="ffc46-330">InternetZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-331">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-332">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-332">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-333">InternetZoneDownloadSignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="ffc46-333">InternetZoneDownloadSignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedownloadsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-334">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-335">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-335">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-336">InternetZoneDownloadUnsignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="ffc46-336">InternetZoneDownloadUnsignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedownloadunsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-337">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-338">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-338">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-339">InternetZoneEnableCrossSiteScriptingFilter</span><span class="sxs-lookup"><span data-stu-id="ffc46-339">InternetZoneEnableCrossSiteScriptingFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenablecrosssitescriptingfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-340">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-341">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-341">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-342">InternetZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span><span class="sxs-lookup"><span data-stu-id="ffc46-342">InternetZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenabledraggingofcontentfromdifferentdomainsacrosswindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-343">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-343">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-344">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-344">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-345">InternetZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span><span class="sxs-lookup"><span data-stu-id="ffc46-345">InternetZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenabledraggingofcontentfromdifferentdomainswithinwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-346">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-347">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-347">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-348">InternetZoneEnableMIMESniffing</span><span class="sxs-lookup"><span data-stu-id="ffc46-348">InternetZoneEnableMIMESniffing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenablemimesniffing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-349">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-350">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-350">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-351">InternetZoneEnableProtectedMode</span><span class="sxs-lookup"><span data-stu-id="ffc46-351">InternetZoneEnableProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenableprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-352">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-353">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-353">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-354">InternetZoneIncludeLocalPathWhenUploadingFilesToServer</span><span class="sxs-lookup"><span data-stu-id="ffc46-354">InternetZoneIncludeLocalPathWhenUploadingFilesToServer</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneincludelocalpathwhenuploadingfilestoserver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-355">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-356">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-356">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-357">InternetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="ffc46-357">InternetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-358">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-358">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-359">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-359">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-360">InternetZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="ffc46-360">InternetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-361">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-362">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-362">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-363">InternetZoneLaunchingApplicationsAndFilesInIFRAME</span><span class="sxs-lookup"><span data-stu-id="ffc46-363">InternetZoneLaunchingApplicationsAndFilesInIFRAME</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonelaunchingapplicationsandfilesiniframe)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-364">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-364">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-365">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-365">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-366">InternetZoneLogonOptions</span><span class="sxs-lookup"><span data-stu-id="ffc46-366">InternetZoneLogonOptions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonelogonoptions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-367">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-368">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-368">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-369">InternetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="ffc46-369">InternetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-370">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-370">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-371">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-371">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ffc46-372">InternetZoneRunNETFrameworkReliantComponentsNotSignedWithAuthenticode</span><span class="sxs-lookup"><span data-stu-id="ffc46-372">InternetZoneRunNETFrameworkReliantComponentsNotSignedWithAuthenticode</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-373">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-373">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-374">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-374">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-375">InternetZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span><span class="sxs-lookup"><span data-stu-id="ffc46-375">InternetZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonerunnetframeworkreliantcomponentssignedwithauthenticode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-376">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-376">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-377">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-377">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-378">InternetZoneShowSecurityWarningForPotentiallyUnsafeFiles</span><span class="sxs-lookup"><span data-stu-id="ffc46-378">InternetZoneShowSecurityWarningForPotentiallyUnsafeFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneshowsecuritywarningforpotentiallyunsafefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-379">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-380">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-380">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-381">InternetZoneUsePopupBlocker</span><span class="sxs-lookup"><span data-stu-id="ffc46-381">InternetZoneUsePopupBlocker</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneusepopupblocker)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-382">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-383">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-383">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ffc46-384">InternetZoneWebsitesInLessPrivilegedZonesCanNavigateIntoThisZone</span><span class="sxs-lookup"><span data-stu-id="ffc46-384">InternetZoneWebsitesInLessPrivilegedZonesCanNavigateIntoThisZone</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-385">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-385">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-386">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-386">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-387">IntranetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="ffc46-387">IntranetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-388">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-388">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-389">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-389">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-390">IntranetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="ffc46-390">IntranetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-391">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-391">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-392">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-392">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-393">IntranetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="ffc46-393">IntranetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-394">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-394">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-395">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-395">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-396">IntranetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="ffc46-396">IntranetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-397">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-397">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-398">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-398">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-399">IntranetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="ffc46-399">IntranetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-400">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-400">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-401">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-401">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-402">IntranetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="ffc46-402">IntranetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-403">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-404">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-404">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-405">IntranetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="ffc46-405">IntranetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-406">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-406">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-407">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-407">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-408">IntranetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="ffc46-408">IntranetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-409">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-409">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-410">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-410">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-411">IntranetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="ffc46-411">IntranetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-412">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-412">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-413">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-413">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-414">IntranetZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="ffc46-414">IntranetZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-415">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-415">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-416">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-416">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-417">IntranetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="ffc46-417">IntranetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-418">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-418">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-419">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-419">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ffc46-420">IntranetZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span><span class="sxs-lookup"><span data-stu-id="ffc46-420">IntranetZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-421">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-421">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-422">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-422">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-423">IntranetZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="ffc46-423">IntranetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-424">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-424">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-425">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-425">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-426">IntranetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="ffc46-426">IntranetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-427">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-427">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-428">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-428">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-429">LocalMachineZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="ffc46-429">LocalMachineZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-430">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-430">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-431">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-431">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-432">LocalMachineZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="ffc46-432">LocalMachineZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-433">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-433">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-434">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-434">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-435">LocalMachineZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="ffc46-435">LocalMachineZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-436">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-436">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-437">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-437">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-438">LocalMachineZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="ffc46-438">LocalMachineZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-439">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-439">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-440">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-440">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-441">LocalMachineZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="ffc46-441">LocalMachineZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-442">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-442">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-443">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-443">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-444">LocalMachineZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="ffc46-444">LocalMachineZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-445">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-445">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-446">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-446">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-447">LocalMachineZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="ffc46-447">LocalMachineZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-448">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-448">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-449">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-449">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-450">LocalMachineZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="ffc46-450">LocalMachineZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-451">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-451">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-452">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-452">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-453">LocalMachineZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="ffc46-453">LocalMachineZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-454">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-454">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-455">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-455">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-456">LocalMachineZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="ffc46-456">LocalMachineZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-457">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-457">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-458">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-458">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-459">LocalMachineZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="ffc46-459">LocalMachineZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-460">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-460">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-461">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-461">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-462">LocalMachineZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="ffc46-462">LocalMachineZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-463">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-463">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-464">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-464">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-465">LocalMachineZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="ffc46-465">LocalMachineZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-466">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-466">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-467">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-467">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-468">LockedDownInternetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="ffc46-468">LockedDownInternetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-469">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-469">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-470">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-470">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-471">LockedDownInternetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="ffc46-471">LockedDownInternetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-472">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-472">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-473">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-473">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-474">LockedDownInternetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="ffc46-474">LockedDownInternetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-475">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-475">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-476">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-476">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-477">LockedDownInternetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="ffc46-477">LockedDownInternetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-478">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-478">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-479">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-479">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-480">LockedDownInternetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="ffc46-480">LockedDownInternetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-481">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-481">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-482">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-482">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-483">LockedDownInternetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="ffc46-483">LockedDownInternetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-484">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-484">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-485">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-485">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-486">LockedDownInternetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="ffc46-486">LockedDownInternetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-487">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-487">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-488">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-488">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-489">LockedDownInternetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="ffc46-489">LockedDownInternetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-490">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-490">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-491">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-491">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-492">LockedDownInternetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="ffc46-492">LockedDownInternetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-493">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-493">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-494">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-494">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-495">LockedDownInternetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="ffc46-495">LockedDownInternetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-496">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-496">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-497">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-497">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-498">LockedDownInternetZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="ffc46-498">LockedDownInternetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-499">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-499">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-500">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-500">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-501">LockedDownInternetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="ffc46-501">LockedDownInternetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-502">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-502">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-503">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-503">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-504">LockedDownIntranetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="ffc46-504">LockedDownIntranetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-505">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-505">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-506">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-506">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-507">LockedDownIntranetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="ffc46-507">LockedDownIntranetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-508">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-508">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-509">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-509">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-510">LockedDownIntranetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="ffc46-510">LockedDownIntranetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-511">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-511">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-512">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-512">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-513">LockedDownIntranetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="ffc46-513">LockedDownIntranetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-514">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-514">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-515">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-515">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-516">LockedDownIntranetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="ffc46-516">LockedDownIntranetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-517">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-517">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-518">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-518">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-519">LockedDownIntranetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="ffc46-519">LockedDownIntranetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-520">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-520">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-521">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-521">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-522">LockedDownIntranetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="ffc46-522">LockedDownIntranetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-523">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-523">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-524">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-524">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-525">LockedDownIntranetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="ffc46-525">LockedDownIntranetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-526">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-526">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-527">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-527">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-528">LockedDownIntranetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="ffc46-528">LockedDownIntranetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-529">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-529">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-530">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-530">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-531">LockedDownIntranetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="ffc46-531">LockedDownIntranetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-532">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-532">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-533">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-533">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-534">LockedDownIntranetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="ffc46-534">LockedDownIntranetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-535">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-535">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-536">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-536">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-537">LockedDownLocalMachineZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="ffc46-537">LockedDownLocalMachineZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-538">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-538">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-539">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-539">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-540">LockedDownLocalMachineZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="ffc46-540">LockedDownLocalMachineZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-541">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-541">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-542">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-542">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-543">LockedDownLocalMachineZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="ffc46-543">LockedDownLocalMachineZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-544">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-544">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-545">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-545">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-546">LockedDownLocalMachineZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="ffc46-546">LockedDownLocalMachineZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-547">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-547">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-548">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-548">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-549">LockedDownLocalMachineZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="ffc46-549">LockedDownLocalMachineZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-550">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-550">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-551">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-551">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-552">LockedDownLocalMachineZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="ffc46-552">LockedDownLocalMachineZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-553">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-553">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-554">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-554">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-555">LockedDownLocalMachineZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="ffc46-555">LockedDownLocalMachineZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-556">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-556">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-557">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-557">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-558">LockedDownLocalMachineZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="ffc46-558">LockedDownLocalMachineZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-559">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-559">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-560">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-560">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-561">LockedDownLocalMachineZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="ffc46-561">LockedDownLocalMachineZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-562">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-562">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-563">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-563">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-564">LockedDownLocalMachineZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="ffc46-564">LockedDownLocalMachineZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-565">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-565">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-566">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-566">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-567">LockedDownLocalMachineZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="ffc46-567">LockedDownLocalMachineZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-568">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-568">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-569">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-569">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-570">LockedDownLocalMachineZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="ffc46-570">LockedDownLocalMachineZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-571">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-571">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-572">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-572">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-573">LockedDownRestrictedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="ffc46-573">LockedDownRestrictedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-574">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-574">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-575">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-575">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-576">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="ffc46-576">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-577">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-577">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-578">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-578">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-579">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="ffc46-579">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-580">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-580">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-581">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-581">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-582">LockedDownRestrictedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="ffc46-582">LockedDownRestrictedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-583">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-583">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-584">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-584">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-585">LockedDownRestrictedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="ffc46-585">LockedDownRestrictedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-586">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-586">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-587">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-587">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-588">LockedDownRestrictedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="ffc46-588">LockedDownRestrictedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-589">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-589">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-590">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-590">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-591">LockedDownRestrictedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="ffc46-591">LockedDownRestrictedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-592">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-592">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-593">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-593">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-594">LockedDownRestrictedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="ffc46-594">LockedDownRestrictedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-595">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-595">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-596">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-596">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-597">LockedDownRestrictedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="ffc46-597">LockedDownRestrictedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-598">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-598">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-599">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-599">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-600">LockedDownRestrictedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="ffc46-600">LockedDownRestrictedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-601">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-601">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-602">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-602">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-603">LockedDownRestrictedSitesZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="ffc46-603">LockedDownRestrictedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-604">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-604">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-605">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-605">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-606">LockedDownRestrictedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="ffc46-606">LockedDownRestrictedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-607">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-607">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-608">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-608">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-609">LockedDownTrustedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="ffc46-609">LockedDownTrustedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-610">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-610">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-611">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-611">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-612">LockedDownTrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="ffc46-612">LockedDownTrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-613">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-613">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-614">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-614">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-615">LockedDownTrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="ffc46-615">LockedDownTrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-616">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-616">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-617">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-617">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-618">LockedDownTrustedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="ffc46-618">LockedDownTrustedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-619">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-619">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-620">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-620">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-621">LockedDownTrustedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="ffc46-621">LockedDownTrustedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-622">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-622">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-623">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-623">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-624">LockedDownTrustedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="ffc46-624">LockedDownTrustedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-625">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-625">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-626">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-626">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-627">LockedDownTrustedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="ffc46-627">LockedDownTrustedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-628">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-628">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-629">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-629">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-630">LockedDownTrustedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="ffc46-630">LockedDownTrustedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-631">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-631">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-632">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-632">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-633">LockedDownTrustedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="ffc46-633">LockedDownTrustedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-634">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-634">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-635">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-635">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-636">LockedDownTrustedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="ffc46-636">LockedDownTrustedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-637">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-637">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-638">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-638">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-639">LockedDownTrustedSitesZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="ffc46-639">LockedDownTrustedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-640">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-640">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-641">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-641">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-642">LockedDownTrustedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="ffc46-642">LockedDownTrustedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-643">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-643">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-644">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-644">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-645">MimeSniffingSafetyFeatureInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="ffc46-645">MimeSniffingSafetyFeatureInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-mimesniffingsafetyfeatureinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-646">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-646">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-647">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-647">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-648">MKProtocolSecurityRestrictionInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="ffc46-648">MKProtocolSecurityRestrictionInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-mkprotocolsecurityrestrictioninternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-649">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-649">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-650">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-650">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-651">NotificationBarInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="ffc46-651">NotificationBarInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-notificationbarinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-652">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-652">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-653">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-653">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ffc46-654">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="ffc46-654">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-655">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-655">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-656">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ffc46-656">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-657">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ffc46-657">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-658">PreventManagingSmartScreenFilter</span><span class="sxs-lookup"><span data-stu-id="ffc46-658">PreventManagingSmartScreenFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-preventmanagingsmartscreenfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-659">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-659">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-660">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-660">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-661">PreventPerUserInstallationOfActiveXControls</span><span class="sxs-lookup"><span data-stu-id="ffc46-661">PreventPerUserInstallationOfActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-preventperuserinstallationofactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-662">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-662">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-663">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-663">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-664">ProtectionFromZoneElevationInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="ffc46-664">ProtectionFromZoneElevationInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-protectionfromzoneelevationinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-665">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-665">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-666">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-666">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-667">RemoveRunThisTimeButtonForOutdatedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="ffc46-667">RemoveRunThisTimeButtonForOutdatedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-removerunthistimebuttonforoutdatedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-668">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-668">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-669">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-669">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-670">RestrictActiveXInstallInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="ffc46-670">RestrictActiveXInstallInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictactivexinstallinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-671">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-671">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-672">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-672">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-673">RestrictedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="ffc46-673">RestrictedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-674">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-674">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-675">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-675">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-676">RestrictedSitesZoneAllowActiveScripting</span><span class="sxs-lookup"><span data-stu-id="ffc46-676">RestrictedSitesZoneAllowActiveScripting</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowactivescripting)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-677">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-677">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-678">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-678">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-679">RestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="ffc46-679">RestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-680">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-680">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-681">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-681">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-682">RestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="ffc46-682">RestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-683">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-683">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-684">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-684">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-685">RestrictedSitesZoneAllowBinaryAndScriptBehaviors</span><span class="sxs-lookup"><span data-stu-id="ffc46-685">RestrictedSitesZoneAllowBinaryAndScriptBehaviors</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowbinaryandscriptbehaviors)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-686">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-686">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-687">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-687">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-688">RestrictedSitesZoneAllowCopyPasteViaScript</span><span class="sxs-lookup"><span data-stu-id="ffc46-688">RestrictedSitesZoneAllowCopyPasteViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowcopypasteviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-689">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-689">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-690">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-690">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-691">RestrictedSitesZoneAllowDragAndDropCopyAndPasteFiles</span><span class="sxs-lookup"><span data-stu-id="ffc46-691">RestrictedSitesZoneAllowDragAndDropCopyAndPasteFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowdraganddropcopyandpastefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-692">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-692">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-693">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-693">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-694">RestrictedSitesZoneAllowFileDownloads</span><span class="sxs-lookup"><span data-stu-id="ffc46-694">RestrictedSitesZoneAllowFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-695">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-695">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-696">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-696">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-697">RestrictedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="ffc46-697">RestrictedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-698">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-698">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-699">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-699">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-700">RestrictedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="ffc46-700">RestrictedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-701">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-701">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-702">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-702">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-703">RestrictedSitesZoneAllowLoadingOfXAMLFiles</span><span class="sxs-lookup"><span data-stu-id="ffc46-703">RestrictedSitesZoneAllowLoadingOfXAMLFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowloadingofxamlfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-704">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-704">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-705">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-705">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-706">RestrictedSitesZoneAllowMETAREFRESH</span><span class="sxs-lookup"><span data-stu-id="ffc46-706">RestrictedSitesZoneAllowMETAREFRESH</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowmetarefresh)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-707">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-707">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-708">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-708">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-709">RestrictedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="ffc46-709">RestrictedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-710">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-710">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-711">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-711">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-712">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseActiveXControls</span><span class="sxs-lookup"><span data-stu-id="ffc46-712">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowonlyapproveddomainstouseactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-713">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-713">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-714">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-714">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-715">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span><span class="sxs-lookup"><span data-stu-id="ffc46-715">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowonlyapproveddomainstousetdcactivexcontrol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-716">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-716">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-717">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-717">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-718">RestrictedSitesZoneAllowScriptingOfInternetExplorerWebBrowserControls</span><span class="sxs-lookup"><span data-stu-id="ffc46-718">RestrictedSitesZoneAllowScriptingOfInternetExplorerWebBrowserControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptingofinternetexplorerwebbrowsercontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-719">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-719">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-720">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-720">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-721">RestrictedSitesZoneAllowScriptInitiatedWindows</span><span class="sxs-lookup"><span data-stu-id="ffc46-721">RestrictedSitesZoneAllowScriptInitiatedWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptinitiatedwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-722">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-722">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-723">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-723">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-724">RestrictedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="ffc46-724">RestrictedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-725">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-725">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-726">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-726">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-727">RestrictedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="ffc46-727">RestrictedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-728">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-728">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-729">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-729">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-730">RestrictedSitesZoneAllowUpdatesToStatusBarViaScript</span><span class="sxs-lookup"><span data-stu-id="ffc46-730">RestrictedSitesZoneAllowUpdatesToStatusBarViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowupdatestostatusbarviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-731">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-731">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-732">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-732">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-733">RestrictedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="ffc46-733">RestrictedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-734">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-734">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-735">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-735">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-736">RestrictedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="ffc46-736">RestrictedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-737">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-737">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-738">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-738">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-739">RestrictedSitesZoneDownloadSignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="ffc46-739">RestrictedSitesZoneDownloadSignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedownloadsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-740">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-740">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-741">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-741">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-742">RestrictedSitesZoneDownloadUnsignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="ffc46-742">RestrictedSitesZoneDownloadUnsignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedownloadunsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-743">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-743">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-744">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-744">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-745">RestrictedSitesZoneEnableCrossSiteScriptingFilter</span><span class="sxs-lookup"><span data-stu-id="ffc46-745">RestrictedSitesZoneEnableCrossSiteScriptingFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenablecrosssitescriptingfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-746">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-746">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-747">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-747">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-748">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span><span class="sxs-lookup"><span data-stu-id="ffc46-748">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenabledraggingofcontentfromdifferentdomainsacrosswindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-749">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-749">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-750">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-750">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-751">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span><span class="sxs-lookup"><span data-stu-id="ffc46-751">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenabledraggingofcontentfromdifferentdomainswithinwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-752">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-752">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-753">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-753">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-754">RestrictedSitesZoneEnableMIMESniffing</span><span class="sxs-lookup"><span data-stu-id="ffc46-754">RestrictedSitesZoneEnableMIMESniffing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenablemimesniffing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-755">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-755">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-756">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-756">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-757">RestrictedSitesZoneIncludeLocalPathWhenUploadingFilesToServer</span><span class="sxs-lookup"><span data-stu-id="ffc46-757">RestrictedSitesZoneIncludeLocalPathWhenUploadingFilesToServer</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneincludelocalpathwhenuploadingfilestoserver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-758">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-758">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-759">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-759">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-760">RestrictedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="ffc46-760">RestrictedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-761">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-761">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-762">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-762">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-763">RestrictedSitesZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="ffc46-763">RestrictedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-764">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-764">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-765">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-765">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-766">RestrictedSitesZoneLaunchingApplicationsAndFilesInIFRAME</span><span class="sxs-lookup"><span data-stu-id="ffc46-766">RestrictedSitesZoneLaunchingApplicationsAndFilesInIFRAME</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonelaunchingapplicationsandfilesiniframe)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-767">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-767">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-768">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-768">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-769">RestrictedSitesZoneLogonOptions</span><span class="sxs-lookup"><span data-stu-id="ffc46-769">RestrictedSitesZoneLogonOptions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonelogonoptions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-770">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-770">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-771">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-771">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-772">RestrictedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="ffc46-772">RestrictedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-773">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-773">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-774">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-774">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ffc46-775">RestrictedSitesZoneNavigateWindowsAndFramesAcrossDomains</span><span class="sxs-lookup"><span data-stu-id="ffc46-775">RestrictedSitesZoneNavigateWindowsAndFramesAcrossDomains</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-776">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-776">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-777">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-777">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-778">RestrictedSitesZoneRunActiveXControlsAndPlugins</span><span class="sxs-lookup"><span data-stu-id="ffc46-778">RestrictedSitesZoneRunActiveXControlsAndPlugins</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonerunactivexcontrolsandplugins)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-779">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-779">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-780">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-780">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-781">RestrictedSitesZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span><span class="sxs-lookup"><span data-stu-id="ffc46-781">RestrictedSitesZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonerunnetframeworkreliantcomponentssignedwithauthenticode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-782">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-782">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-783">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-783">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-784">RestrictedSitesZoneScriptActiveXControlsMarkedSafeForScripting</span><span class="sxs-lookup"><span data-stu-id="ffc46-784">RestrictedSitesZoneScriptActiveXControlsMarkedSafeForScripting</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonescriptactivexcontrolsmarkedsafeforscripting)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-785">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-785">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-786">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-786">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-787">RestrictedSitesZoneScriptingOfJavaApplets</span><span class="sxs-lookup"><span data-stu-id="ffc46-787">RestrictedSitesZoneScriptingOfJavaApplets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonescriptingofjavaapplets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-788">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-788">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-789">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-789">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-790">RestrictedSitesZoneShowSecurityWarningForPotentiallyUnsafeFiles</span><span class="sxs-lookup"><span data-stu-id="ffc46-790">RestrictedSitesZoneShowSecurityWarningForPotentiallyUnsafeFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneshowsecuritywarningforpotentiallyunsafefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-791">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-791">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-792">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-792">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ffc46-793">RestrictedSitesZoneTurnOnCrossSiteScriptingFilter</span><span class="sxs-lookup"><span data-stu-id="ffc46-793">RestrictedSitesZoneTurnOnCrossSiteScriptingFilter</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-794">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-794">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-795">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-795">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-796">RestrictedSitesZoneTurnOnProtectedMode</span><span class="sxs-lookup"><span data-stu-id="ffc46-796">RestrictedSitesZoneTurnOnProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneturnonprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-797">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-797">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-798">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-798">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-799">RestrictedSitesZoneUsePopupBlocker</span><span class="sxs-lookup"><span data-stu-id="ffc46-799">RestrictedSitesZoneUsePopupBlocker</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneusepopupblocker)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-800">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-800">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-801">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-801">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-802">RestrictFileDownloadInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="ffc46-802">RestrictFileDownloadInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictfiledownloadinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-803">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-803">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-804">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-804">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-805">ScriptedWindowSecurityRestrictionsInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="ffc46-805">ScriptedWindowSecurityRestrictionsInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-scriptedwindowsecurityrestrictionsinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-806">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-806">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-807">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-807">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-808">SearchProviderList</span><span class="sxs-lookup"><span data-stu-id="ffc46-808">SearchProviderList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-searchproviderlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-809">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-809">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-810">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-810">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-811">SpecifyUseOfActiveXInstallerService</span><span class="sxs-lookup"><span data-stu-id="ffc46-811">SpecifyUseOfActiveXInstallerService</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-specifyuseofactivexinstallerservice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-812">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-812">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-813">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-813">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-814">TrustedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="ffc46-814">TrustedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-815">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-815">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-816">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-816">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-817">TrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="ffc46-817">TrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-818">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-818">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-819">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-819">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-820">TrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="ffc46-820">TrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-821">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-821">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-822">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-822">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-823">TrustedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="ffc46-823">TrustedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-824">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-824">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-825">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-825">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-826">TrustedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="ffc46-826">TrustedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-827">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-827">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-828">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-828">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-829">TrustedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="ffc46-829">TrustedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-830">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-830">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-831">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-831">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-832">TrustedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="ffc46-832">TrustedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-833">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-833">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-834">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-834">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-835">TrustedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="ffc46-835">TrustedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-836">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-836">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-837">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-837">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-838">TrustedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="ffc46-838">TrustedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-839">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-839">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-840">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-840">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-841">TrustedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="ffc46-841">TrustedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-842">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-842">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-843">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-843">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ffc46-844">TrustedSitesZoneDontRunAntimalwareProgramsAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="ffc46-844">TrustedSitesZoneDontRunAntimalwareProgramsAgainstActiveXControls</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-845">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-845">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-846">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-846">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-847">TrustedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="ffc46-847">TrustedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-848">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-848">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-849">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-849">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ffc46-850">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedAsSafe</span><span class="sxs-lookup"><span data-stu-id="ffc46-850">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedAsSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-851">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-851">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-852">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-852">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ffc46-853">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span><span class="sxs-lookup"><span data-stu-id="ffc46-853">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-854">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-854">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-855">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-855">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-856">TrustedSitesZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="ffc46-856">TrustedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-857">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-857">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-858">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-858">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffc46-859">TrustedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="ffc46-859">TrustedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc46-860">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ffc46-860">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffc46-861">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ffc46-861">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ffc46-862">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ffc46-862">Requirements</span></span>



| <span data-ttu-id="ffc46-863">Requisito</span><span class="sxs-lookup"><span data-stu-id="ffc46-863">Requirement</span></span> | <span data-ttu-id="ffc46-864">Valore</span><span class="sxs-lookup"><span data-stu-id="ffc46-864">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffc46-865">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ffc46-865">Minimum supported client</span></span><br/> | <span data-ttu-id="ffc46-866">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="ffc46-866">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ffc46-867">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ffc46-867">Minimum supported server</span></span><br/> | <span data-ttu-id="ffc46-868">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="ffc46-868">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="ffc46-869">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ffc46-869">Namespace</span></span><br/>                | <span data-ttu-id="ffc46-870">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="ffc46-870">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="ffc46-871">MOF</span><span class="sxs-lookup"><span data-stu-id="ffc46-871">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ffc46-872"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ffc46-872"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="ffc46-873">DLL</span><span class="sxs-lookup"><span data-stu-id="ffc46-873">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ffc46-874"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ffc46-874"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

