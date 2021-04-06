---
title: Classe MDM_Policy_Result01_Browser02
description: La \_ \_ classe Result01 Browser02 dei criteri MDM \_ rappresenta i criteri del browser disponibili. \_Criteri MDM \_ Result01 \_ la classe Browser02 rappresenta i criteri del browser disponibili.
ms.assetid: 06dc9f68-d9ea-4eec-93cb-1f26e8a6050d
keywords:
- Classe MDM_Policy_Result01_Browser02
- Classe MDM_Policy_Result01_Browser02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Browser02
- MDM_Policy_Result01_Browser02.InstanceID
- MDM_Policy_Result01_Browser02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19d132c43b88b242864e248b705a0f6bca02e546
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873361"
---
# <a name="mdm_policy_result01_browser02-class"></a><span data-ttu-id="530cf-105">\_ \_ Classe Result01 Browser02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="530cf-105">MDM\_Policy\_Result01\_Browser02 class</span></span>

<span data-ttu-id="530cf-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="530cf-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="530cf-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="530cf-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="530cf-108">La **classe \_ \_ Result01 \_ Browser02 dei criteri MDM** rappresenta i criteri del browser disponibili.</span><span class="sxs-lookup"><span data-stu-id="530cf-108">The **MDM\_Policy\_Result01\_Browser02** class represents the browser policies available.</span></span>

<span data-ttu-id="530cf-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="530cf-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="530cf-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="530cf-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Browser02
{
  string InstanceID;
  string ParentID;
  sint32 AllowAddressBarDropdown;
  sint32 AllowAutofill;
  sint32 AllowCookies;
  sint32 AllowDeveloperTools;
  sint32 AllowInPrivate;
  sint32 AllowMicrosoftCompatibilityList;
  sint32 AllowDoNotTrack;
  sint32 AllowFlashClickToRun;
  sint32 AllowFlash;
  sint32 AllowExtensions;
  sint32 AllowPasswordManager;
  sint32 AllowPopups;
  sint32 AllowSearchEngineCustomization;
  sint32 AllowSearchSuggestionsinAddressBar;
  sint32 AllowSmartScreen;
  sint32 AlwaysEnableBooksLibrary;
  sint32 DisableLockdownOfStartPages;
  string ConfigureAdditionalSearchEngines;
  sint32 ClearBrowsingDataOnExit;
  string EnterpriseModeSiteList;
  string EnterpriseSiteListServiceUrl;
  string Homepages;
  sint32 LockdownFavorites;
  sint32 PreventAccessToAboutFlagsInMicrosoftEdge;
  sint32 PreventLiveTileDataCollection;
  sint32 PreventFirstRunPage;
  sint32 PreventSmartScreenPromptOverride;
  sint32 PreventSmartScreenPromptOverrideForFiles;
  sint32 PreventUsingLocalHostIPAddressForWebRTC;
  string ProvisionFavorites;
  sint32 SendIntranetTraffictoInternetExplorer;
  string SetDefaultSearchEngine;
  sint32 ShowMessageWhenOpeningSitesInInternetExplorer;
  sint32 SyncFavoritesBetweenIEAndMicrosoftEdge;
};
```

## <a name="members"></a><span data-ttu-id="530cf-111">Members</span><span class="sxs-lookup"><span data-stu-id="530cf-111">Members</span></span>

<span data-ttu-id="530cf-112">La **classe \_ \_ Result01 \_ Browser02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="530cf-112">The **MDM\_Policy\_Result01\_Browser02** class has these types of members:</span></span>

-   [<span data-ttu-id="530cf-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="530cf-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="530cf-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="530cf-114">Properties</span></span>

<span data-ttu-id="530cf-115">La **classe \_ \_ \_ Browser02 dei criteri MDM Result01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="530cf-115">The **MDM\_Policy\_Result01\_Browser02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="530cf-116">AllowAddressBarDropdown</span><span class="sxs-lookup"><span data-stu-id="530cf-116">AllowAddressBarDropdown</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowaddressbardropdown)
</dt> <dd> <dl> <dt>

<span data-ttu-id="530cf-117">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="530cf-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="530cf-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="530cf-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="530cf-119">AllowAutofill</span><span class="sxs-lookup"><span data-stu-id="530cf-119">AllowAutofill</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowautofill)
</dt> <dd> <dl> <dt>

<span data-ttu-id="530cf-120">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="530cf-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="530cf-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="530cf-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="530cf-122">AllowCookies</span><span class="sxs-lookup"><span data-stu-id="530cf-122">AllowCookies</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowcookies)
</dt> <dd> <dl> <dt>

<span data-ttu-id="530cf-123">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="530cf-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="530cf-124">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="530cf-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="530cf-125">AllowDeveloperTools</span><span class="sxs-lookup"><span data-stu-id="530cf-125">AllowDeveloperTools</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowdevelopertools)
</dt> <dd> <dl> <dt>

<span data-ttu-id="530cf-126">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="530cf-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="530cf-127">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="530cf-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="530cf-128">AllowDoNotTrack</span><span class="sxs-lookup"><span data-stu-id="530cf-128">AllowDoNotTrack</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowdonottrack)
</dt> <dd> <dl> <dt>

<span data-ttu-id="530cf-129">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="530cf-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="530cf-130">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="530cf-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="530cf-131">AllowExtensions</span><span class="sxs-lookup"><span data-stu-id="530cf-131">AllowExtensions</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowextensions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="530cf-132">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="530cf-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="530cf-133">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="530cf-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="530cf-134">AllowFlash</span><span class="sxs-lookup"><span data-stu-id="530cf-134">AllowFlash</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowflash)
</dt> <dd> <dl> <dt>

<span data-ttu-id="530cf-135">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="530cf-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="530cf-136">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="530cf-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="530cf-137">AllowFlashClickToRun</span><span class="sxs-lookup"><span data-stu-id="530cf-137">AllowFlashClickToRun</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowflashclicktorun)
</dt> <dd> <dl> <dt>

<span data-ttu-id="530cf-138">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="530cf-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="530cf-139">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="530cf-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="530cf-140">AllowInPrivate</span><span class="sxs-lookup"><span data-stu-id="530cf-140">AllowInPrivate</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowinprivate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="530cf-141">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="530cf-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="530cf-142">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="530cf-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="530cf-143">AllowMicrosoftCompatibilityList</span><span class="sxs-lookup"><span data-stu-id="530cf-143">AllowMicrosoftCompatibilityList</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowmicrosoftcompatibilitylist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="530cf-144">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="530cf-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="530cf-145">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="530cf-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="530cf-146">AllowPasswordManager</span><span class="sxs-lookup"><span data-stu-id="530cf-146">AllowPasswordManager</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowpasswordmanager)
</dt> <dd> <dl> <dt>

<span data-ttu-id="530cf-147">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="530cf-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="530cf-148">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="530cf-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="530cf-149">AllowPopups</span><span class="sxs-lookup"><span data-stu-id="530cf-149">AllowPopups</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowpopups)
</dt> <dd> <dl> <dt>

<span data-ttu-id="530cf-150">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="530cf-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="530cf-151">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="530cf-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="530cf-152">AllowSearchEngineCustomization</span><span class="sxs-lookup"><span data-stu-id="530cf-152">AllowSearchEngineCustomization</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowsearchenginecustomization)
</dt> <dd> <dl> <dt>

<span data-ttu-id="530cf-153">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="530cf-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="530cf-154">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="530cf-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="530cf-155">AllowSearchSuggestionsinAddressBar</span><span class="sxs-lookup"><span data-stu-id="530cf-155">AllowSearchSuggestionsinAddressBar</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowsearchsuggestionsinaddressbar)
</dt> <dd> <dl> <dt>

<span data-ttu-id="530cf-156">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="530cf-156">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="530cf-157">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="530cf-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="530cf-158">AllowSmartScreen</span><span class="sxs-lookup"><span data-stu-id="530cf-158">AllowSmartScreen</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowsmartscreen)
</dt> <dd> <dl> <dt>

<span data-ttu-id="530cf-159">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="530cf-159">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="530cf-160">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="530cf-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="530cf-161">AlwaysEnableBooksLibrary</span><span class="sxs-lookup"><span data-stu-id="530cf-161">AlwaysEnableBooksLibrary</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-alwaysenablebookslibrary)
</dt> <dd> <dl> <dt>

<span data-ttu-id="530cf-162">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="530cf-162">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="530cf-163">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="530cf-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="530cf-164">ClearBrowsingDataOnExit</span><span class="sxs-lookup"><span data-stu-id="530cf-164">ClearBrowsingDataOnExit</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-clearbrowsingdataonexit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="530cf-165">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="530cf-165">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="530cf-166">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="530cf-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="530cf-167">ConfigureAdditionalSearchEngines</span><span class="sxs-lookup"><span data-stu-id="530cf-167">ConfigureAdditionalSearchEngines</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-configureadditionalsearchengines)
</dt> <dd> <dl> <dt>

<span data-ttu-id="530cf-168">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="530cf-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="530cf-169">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="530cf-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="530cf-170">DisableLockdownOfStartPages</span><span class="sxs-lookup"><span data-stu-id="530cf-170">DisableLockdownOfStartPages</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-disablelockdownofstartpages)
</dt> <dd> <dl> <dt>

<span data-ttu-id="530cf-171">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="530cf-171">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="530cf-172">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="530cf-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="530cf-173">EnterpriseModeSiteList</span><span class="sxs-lookup"><span data-stu-id="530cf-173">EnterpriseModeSiteList</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-enterprisemodesitelist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="530cf-174">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="530cf-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="530cf-175">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="530cf-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="530cf-176">EnterpriseSiteListServiceUrl</span><span class="sxs-lookup"><span data-stu-id="530cf-176">EnterpriseSiteListServiceUrl</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-enterprisesitelistserviceurl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="530cf-177">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="530cf-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="530cf-178">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="530cf-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="530cf-179">Pagine iniziali</span><span class="sxs-lookup"><span data-stu-id="530cf-179">Homepages</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-homepages)
</dt> <dd> <dl> <dt>

<span data-ttu-id="530cf-180">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="530cf-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="530cf-181">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="530cf-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="530cf-182">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="530cf-182">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="530cf-183">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="530cf-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="530cf-184">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="530cf-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="530cf-185">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="530cf-185">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="530cf-186">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="530cf-186">Identifies the name of the parent node.</span></span> <span data-ttu-id="530cf-187">Per questa classe la stringa è "browser".</span><span class="sxs-lookup"><span data-stu-id="530cf-187">For this class, the string is "Browser".</span></span>

</dd> <dt>

[<span data-ttu-id="530cf-188">LockdownFavorites</span><span class="sxs-lookup"><span data-stu-id="530cf-188">LockdownFavorites</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-lockdownfavorites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="530cf-189">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="530cf-189">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="530cf-190">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="530cf-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="530cf-191">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="530cf-191">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="530cf-192">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="530cf-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="530cf-193">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="530cf-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="530cf-194">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="530cf-194">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="530cf-195">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="530cf-195">Describes the full path to the parent node.</span></span> <span data-ttu-id="530cf-196">Per questa classe la stringa è "./Vendor/MSFT/Policy/Result"</span><span class="sxs-lookup"><span data-stu-id="530cf-196">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="530cf-197">PreventAccessToAboutFlagsInMicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="530cf-197">PreventAccessToAboutFlagsInMicrosoftEdge</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventaccesstoaboutflagsinmicrosoftedge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="530cf-198">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="530cf-198">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="530cf-199">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="530cf-199">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="530cf-200">PreventFirstRunPage</span><span class="sxs-lookup"><span data-stu-id="530cf-200">PreventFirstRunPage</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventfirstrunpage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="530cf-201">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="530cf-201">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="530cf-202">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="530cf-202">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="530cf-203">PreventLiveTileDataCollection</span><span class="sxs-lookup"><span data-stu-id="530cf-203">PreventLiveTileDataCollection</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventlivetiledatacollection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="530cf-204">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="530cf-204">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="530cf-205">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="530cf-205">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="530cf-206">PreventSmartScreenPromptOverride</span><span class="sxs-lookup"><span data-stu-id="530cf-206">PreventSmartScreenPromptOverride</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventsmartscreenpromptoverride)
</dt> <dd> <dl> <dt>

<span data-ttu-id="530cf-207">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="530cf-207">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="530cf-208">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="530cf-208">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="530cf-209">PreventSmartScreenPromptOverrideForFiles</span><span class="sxs-lookup"><span data-stu-id="530cf-209">PreventSmartScreenPromptOverrideForFiles</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventsmartscreenpromptoverrideforfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="530cf-210">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="530cf-210">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="530cf-211">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="530cf-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="530cf-212">PreventUsingLocalHostIPAddressForWebRTC</span><span class="sxs-lookup"><span data-stu-id="530cf-212">PreventUsingLocalHostIPAddressForWebRTC</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventusinglocalhostipaddressforwebrtc)
</dt> <dd> <dl> <dt>

<span data-ttu-id="530cf-213">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="530cf-213">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="530cf-214">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="530cf-214">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="530cf-215">ProvisionFavorites</span><span class="sxs-lookup"><span data-stu-id="530cf-215">ProvisionFavorites</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-provisionfavorites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="530cf-216">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="530cf-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="530cf-217">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="530cf-217">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="530cf-218">SendIntranetTraffictoInternetExplorer</span><span class="sxs-lookup"><span data-stu-id="530cf-218">SendIntranetTraffictoInternetExplorer</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-sendintranettraffictointernetexplorer)
</dt> <dd> <dl> <dt>

<span data-ttu-id="530cf-219">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="530cf-219">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="530cf-220">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="530cf-220">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="530cf-221">SetDefaultSearchEngine</span><span class="sxs-lookup"><span data-stu-id="530cf-221">SetDefaultSearchEngine</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-setdefaultsearchengine)
</dt> <dd> <dl> <dt>

<span data-ttu-id="530cf-222">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="530cf-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="530cf-223">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="530cf-223">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="530cf-224">ShowMessageWhenOpeningSitesInInternetExplorer</span><span class="sxs-lookup"><span data-stu-id="530cf-224">ShowMessageWhenOpeningSitesInInternetExplorer</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-showmessagewhenopeningsitesininternetexplorer)
</dt> <dd> <dl> <dt>

<span data-ttu-id="530cf-225">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="530cf-225">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="530cf-226">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="530cf-226">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="530cf-227">SyncFavoritesBetweenIEAndMicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="530cf-227">SyncFavoritesBetweenIEAndMicrosoftEdge</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-syncfavoritesbetweenieandmicrosoftedge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="530cf-228">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="530cf-228">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="530cf-229">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="530cf-229">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="530cf-230">Requisiti</span><span class="sxs-lookup"><span data-stu-id="530cf-230">Requirements</span></span>



| <span data-ttu-id="530cf-231">Requisito</span><span class="sxs-lookup"><span data-stu-id="530cf-231">Requirement</span></span> | <span data-ttu-id="530cf-232">Valore</span><span class="sxs-lookup"><span data-stu-id="530cf-232">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="530cf-233">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="530cf-233">Minimum supported client</span></span><br/> | <span data-ttu-id="530cf-234">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="530cf-234">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="530cf-235">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="530cf-235">Minimum supported server</span></span><br/> | <span data-ttu-id="530cf-236">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="530cf-236">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="530cf-237">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="530cf-237">Namespace</span></span><br/>                | <span data-ttu-id="530cf-238">\\ \\ DMMap MDM CIMv2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="530cf-238">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="530cf-239">MOF</span><span class="sxs-lookup"><span data-stu-id="530cf-239">MOF</span></span><br/>                      | <dl> <span data-ttu-id="530cf-240"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="530cf-240"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="530cf-241">DLL</span><span class="sxs-lookup"><span data-stu-id="530cf-241">DLL</span></span><br/>                      | <dl> <span data-ttu-id="530cf-242"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="530cf-242"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="530cf-243">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="530cf-243">See also</span></span>

<dl> <dt>

[<span data-ttu-id="530cf-244">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="530cf-244">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

