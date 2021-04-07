---
title: Classe MDM_Policy_Result01_Start02
description: La \_ \_ classe Result01 Start02 dei criteri MDM \_ rappresenta i criteri della schermata iniziale disponibili.
ms.assetid: 997d64f9-b2be-47b8-8a84-97438e7fa842
keywords:
- Classe MDM_Policy_Result01_Start02
- Classe MDM_Policy_Result01_Start02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Start02
- MDM_Policy_Result01_Start02.InstanceID
- MDM_Policy_Result01_Start02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 412e9ccecdc9f691b03a94ba5528eb6b7e3d7315
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048244"
---
# <a name="mdm_policy_result01_start02-class"></a><span data-ttu-id="9f06b-105">\_ \_ Classe Result01 Start02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="9f06b-105">MDM\_Policy\_Result01\_Start02 class</span></span>

<span data-ttu-id="9f06b-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="9f06b-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="9f06b-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="9f06b-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="9f06b-108">La **classe \_ \_ Result01 \_ Start02 dei criteri MDM** rappresenta i criteri della schermata iniziale disponibili.</span><span class="sxs-lookup"><span data-stu-id="9f06b-108">The **MDM\_Policy\_Result01\_Start02** class represents the start screen policies available.</span></span>

<span data-ttu-id="9f06b-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="9f06b-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f06b-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9f06b-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Start02
{
  string InstanceID;
  string ParentID;
  sint32 AllowPinnedFolderVideos;
  sint32 AllowPinnedFolderSettings;
  sint32 AllowPinnedFolderPictures;
  sint32 AllowPinnedFolderPersonalFolder;
  sint32 AllowPinnedFolderNetwork;
  sint32 AllowPinnedFolderMusic;
  sint32 AllowPinnedFolderHomeGroup;
  sint32 AllowPinnedFolderFileExplorer;
  sint32 AllowPinnedFolderDownloads;
  sint32 AllowPinnedFolderDocuments;
  sint32 ForceStartSize;
  string StartLayout;
  sint32 NoPinningToTaskbar;
  string ImportEdgeAssets;
  sint32 HideUserTile;
  sint32 HideSwitchAccount;
  sint32 HideSleep;
  sint32 HideSignOut;
  sint32 HideShutDown;
  sint32 HideRestart;
  sint32 HideRecentlyAddedApps;
  sint32 HideRecentJumplists;
  sint32 HidePowerButton;
  sint32 HideLock;
  sint32 HideHibernate;
  sint32 HideFrequentlyUsedApps;
  sint32 HideChangeAccountSettings;
  sint32 HideAppList;
};
```

## <a name="members"></a><span data-ttu-id="9f06b-111">Members</span><span class="sxs-lookup"><span data-stu-id="9f06b-111">Members</span></span>

<span data-ttu-id="9f06b-112">La **classe \_ \_ Result01 \_ Start02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="9f06b-112">The **MDM\_Policy\_Result01\_Start02** class has these types of members:</span></span>

-   [<span data-ttu-id="9f06b-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9f06b-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9f06b-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9f06b-114">Properties</span></span>

<span data-ttu-id="9f06b-115">La **classe \_ \_ \_ Start02 dei criteri MDM Result01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="9f06b-115">The **MDM\_Policy\_Result01\_Start02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="9f06b-116">AllowPinnedFolderDocuments</span><span class="sxs-lookup"><span data-stu-id="9f06b-116">AllowPinnedFolderDocuments</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfolderdocuments)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f06b-117">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9f06b-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f06b-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9f06b-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f06b-119">AllowPinnedFolderDownloads</span><span class="sxs-lookup"><span data-stu-id="9f06b-119">AllowPinnedFolderDownloads</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfolderdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f06b-120">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9f06b-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f06b-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9f06b-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f06b-122">AllowPinnedFolderFileExplorer</span><span class="sxs-lookup"><span data-stu-id="9f06b-122">AllowPinnedFolderFileExplorer</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfolderfileexplorer)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f06b-123">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9f06b-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f06b-124">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9f06b-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f06b-125">AllowPinnedFolderHomeGroup</span><span class="sxs-lookup"><span data-stu-id="9f06b-125">AllowPinnedFolderHomeGroup</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfolderhomegroup)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f06b-126">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9f06b-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f06b-127">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9f06b-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f06b-128">AllowPinnedFolderMusic</span><span class="sxs-lookup"><span data-stu-id="9f06b-128">AllowPinnedFolderMusic</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfoldermusic)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f06b-129">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9f06b-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f06b-130">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9f06b-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f06b-131">AllowPinnedFolderNetwork</span><span class="sxs-lookup"><span data-stu-id="9f06b-131">AllowPinnedFolderNetwork</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfoldernetwork)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f06b-132">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9f06b-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f06b-133">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9f06b-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f06b-134">AllowPinnedFolderPersonalFolder</span><span class="sxs-lookup"><span data-stu-id="9f06b-134">AllowPinnedFolderPersonalFolder</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfolderpersonalfolder)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f06b-135">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9f06b-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f06b-136">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9f06b-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f06b-137">AllowPinnedFolderPictures</span><span class="sxs-lookup"><span data-stu-id="9f06b-137">AllowPinnedFolderPictures</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfolderpictures)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f06b-138">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9f06b-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f06b-139">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9f06b-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f06b-140">AllowPinnedFolderSettings</span><span class="sxs-lookup"><span data-stu-id="9f06b-140">AllowPinnedFolderSettings</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfoldersettings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f06b-141">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9f06b-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f06b-142">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9f06b-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f06b-143">AllowPinnedFolderVideos</span><span class="sxs-lookup"><span data-stu-id="9f06b-143">AllowPinnedFolderVideos</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfoldervideos)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f06b-144">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9f06b-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f06b-145">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9f06b-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f06b-146">ForceStartSize</span><span class="sxs-lookup"><span data-stu-id="9f06b-146">ForceStartSize</span></span>](/windows/client-management/mdm/policy-csp-start#start-forcestartsize)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f06b-147">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9f06b-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f06b-148">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9f06b-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f06b-149">HideAppList</span><span class="sxs-lookup"><span data-stu-id="9f06b-149">HideAppList</span></span>](/windows/client-management/mdm/policy-csp-start#start-hideapplist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f06b-150">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9f06b-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f06b-151">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9f06b-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f06b-152">HideChangeAccountSettings</span><span class="sxs-lookup"><span data-stu-id="9f06b-152">HideChangeAccountSettings</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidechangeaccountsettings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f06b-153">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9f06b-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f06b-154">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9f06b-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f06b-155">HideFrequentlyUsedApps</span><span class="sxs-lookup"><span data-stu-id="9f06b-155">HideFrequentlyUsedApps</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidefrequentlyusedapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f06b-156">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9f06b-156">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f06b-157">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9f06b-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f06b-158">HideHibernate</span><span class="sxs-lookup"><span data-stu-id="9f06b-158">HideHibernate</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidehibernate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f06b-159">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9f06b-159">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f06b-160">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9f06b-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f06b-161">HideLock</span><span class="sxs-lookup"><span data-stu-id="9f06b-161">HideLock</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidelock)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f06b-162">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9f06b-162">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f06b-163">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9f06b-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f06b-164">HidePowerButton</span><span class="sxs-lookup"><span data-stu-id="9f06b-164">HidePowerButton</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidepowerbutton)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f06b-165">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9f06b-165">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f06b-166">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9f06b-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f06b-167">HideRecentJumplists</span><span class="sxs-lookup"><span data-stu-id="9f06b-167">HideRecentJumplists</span></span>](/windows/client-management/mdm/policy-csp-start#start-hiderecentjumplists)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f06b-168">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9f06b-168">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f06b-169">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9f06b-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f06b-170">HideRecentlyAddedApps</span><span class="sxs-lookup"><span data-stu-id="9f06b-170">HideRecentlyAddedApps</span></span>](/windows/client-management/mdm/policy-csp-start#start-hiderecentlyaddedapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f06b-171">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9f06b-171">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f06b-172">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9f06b-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f06b-173">HideRestart</span><span class="sxs-lookup"><span data-stu-id="9f06b-173">HideRestart</span></span>](/windows/client-management/mdm/policy-csp-start#start-hiderestart)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f06b-174">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9f06b-174">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f06b-175">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9f06b-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f06b-176">HideShutDown</span><span class="sxs-lookup"><span data-stu-id="9f06b-176">HideShutDown</span></span>](/windows/client-management/mdm/policy-csp-start#start-hideshutdown)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f06b-177">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9f06b-177">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f06b-178">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9f06b-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f06b-179">HideSignOut</span><span class="sxs-lookup"><span data-stu-id="9f06b-179">HideSignOut</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidesignout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f06b-180">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9f06b-180">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f06b-181">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9f06b-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f06b-182">HideSleep</span><span class="sxs-lookup"><span data-stu-id="9f06b-182">HideSleep</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidesleep)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f06b-183">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9f06b-183">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f06b-184">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9f06b-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f06b-185">HideSwitchAccount</span><span class="sxs-lookup"><span data-stu-id="9f06b-185">HideSwitchAccount</span></span>](/windows/client-management/mdm/policy-csp-start#start-hideswitchaccount)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f06b-186">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9f06b-186">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f06b-187">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9f06b-187">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f06b-188">HideUserTile</span><span class="sxs-lookup"><span data-stu-id="9f06b-188">HideUserTile</span></span>](/windows/client-management/mdm/policy-csp-start#start-hideusertile)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f06b-189">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9f06b-189">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f06b-190">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9f06b-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f06b-191">ImportEdgeAssets</span><span class="sxs-lookup"><span data-stu-id="9f06b-191">ImportEdgeAssets</span></span>](/windows/client-management/mdm/policy-csp-start#start-importedgeassets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f06b-192">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9f06b-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f06b-193">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9f06b-193">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9f06b-194">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="9f06b-194">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f06b-195">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9f06b-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f06b-196">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9f06b-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f06b-197">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9f06b-197">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9f06b-198">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="9f06b-198">Identifies the name of the parent node.</span></span> <span data-ttu-id="9f06b-199">Per questa classe la stringa è "Start"</span><span class="sxs-lookup"><span data-stu-id="9f06b-199">For this class, the string is "Start"</span></span>

</dd> <dt>

[<span data-ttu-id="9f06b-200">NoPinningToTaskbar</span><span class="sxs-lookup"><span data-stu-id="9f06b-200">NoPinningToTaskbar</span></span>](/windows/client-management/mdm/policy-csp-start#start-nopinningtotaskbar)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f06b-201">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9f06b-201">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f06b-202">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9f06b-202">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9f06b-203">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="9f06b-203">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f06b-204">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9f06b-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f06b-205">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9f06b-205">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f06b-206">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9f06b-206">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9f06b-207">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="9f06b-207">Describes the full path to the parent node.</span></span> <span data-ttu-id="9f06b-208">Per questa classe la stringa è "./Vendor/MSFT/Policy/Result"</span><span class="sxs-lookup"><span data-stu-id="9f06b-208">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="9f06b-209">StartLayout</span><span class="sxs-lookup"><span data-stu-id="9f06b-209">StartLayout</span></span>](/windows/client-management/mdm/policy-csp-start#start-startlayout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f06b-210">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9f06b-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f06b-211">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9f06b-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9f06b-212">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9f06b-212">Requirements</span></span>



| <span data-ttu-id="9f06b-213">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f06b-213">Requirement</span></span> | <span data-ttu-id="9f06b-214">Valore</span><span class="sxs-lookup"><span data-stu-id="9f06b-214">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f06b-215">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9f06b-215">Minimum supported client</span></span><br/> | <span data-ttu-id="9f06b-216">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="9f06b-216">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9f06b-217">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9f06b-217">Minimum supported server</span></span><br/> | <span data-ttu-id="9f06b-218">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="9f06b-218">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="9f06b-219">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9f06b-219">Namespace</span></span><br/>                | <span data-ttu-id="9f06b-220">\\ \\ DMMap MDM CIMv2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="9f06b-220">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="9f06b-221">MOF</span><span class="sxs-lookup"><span data-stu-id="9f06b-221">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9f06b-222"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9f06b-222"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="9f06b-223">DLL</span><span class="sxs-lookup"><span data-stu-id="9f06b-223">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f06b-224"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f06b-224"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f06b-225">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9f06b-225">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f06b-226">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="9f06b-226">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

