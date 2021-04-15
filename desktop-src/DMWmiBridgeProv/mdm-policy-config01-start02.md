---
title: Classe MDM_Policy_Config01_Start02
description: La \_ \_ classe Config01 Start02 dei criteri MDM \_ rappresenta i criteri della schermata iniziale disponibili.
ms.assetid: 2aef29c8-164a-4111-9c1a-e63eeec2531e
keywords:
- Classe MDM_Policy_Config01_Start02
- Classe MDM_Policy_Config01_Start02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Start02
- MDM_Policy_Config01_Start02.InstanceID
- MDM_Policy_Config01_Start02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9095fcf1611ef106fed5ad93f059e165ebcac15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476930"
---
# <a name="mdm_policy_config01_start02-class"></a><span data-ttu-id="5951e-105">\_ \_ Classe Config01 Start02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="5951e-105">MDM\_Policy\_Config01\_Start02 class</span></span>

<span data-ttu-id="5951e-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="5951e-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="5951e-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="5951e-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="5951e-108">La **classe \_ \_ Config01 \_ Start02 dei criteri MDM** rappresenta i criteri della schermata iniziale disponibili.</span><span class="sxs-lookup"><span data-stu-id="5951e-108">The **MDM\_Policy\_Config01\_Start02** class represents the start screen policies available.</span></span>

<span data-ttu-id="5951e-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="5951e-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5951e-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5951e-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Start02
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

## <a name="members"></a><span data-ttu-id="5951e-111">Members</span><span class="sxs-lookup"><span data-stu-id="5951e-111">Members</span></span>

<span data-ttu-id="5951e-112">La **classe \_ \_ Config01 \_ Start02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="5951e-112">The **MDM\_Policy\_Config01\_Start02** class has these types of members:</span></span>

-   [<span data-ttu-id="5951e-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5951e-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5951e-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5951e-114">Properties</span></span>

<span data-ttu-id="5951e-115">La **classe \_ \_ \_ Start02 dei criteri MDM Config01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="5951e-115">The **MDM\_Policy\_Config01\_Start02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="5951e-116">AllowPinnedFolderDocuments</span><span class="sxs-lookup"><span data-stu-id="5951e-116">AllowPinnedFolderDocuments</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfolderdocuments)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5951e-117">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5951e-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5951e-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5951e-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5951e-119">AllowPinnedFolderDownloads</span><span class="sxs-lookup"><span data-stu-id="5951e-119">AllowPinnedFolderDownloads</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfolderdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5951e-120">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5951e-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5951e-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5951e-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5951e-122">AllowPinnedFolderFileExplorer</span><span class="sxs-lookup"><span data-stu-id="5951e-122">AllowPinnedFolderFileExplorer</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfolderfileexplorer)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5951e-123">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5951e-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5951e-124">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5951e-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5951e-125">AllowPinnedFolderHomeGroup</span><span class="sxs-lookup"><span data-stu-id="5951e-125">AllowPinnedFolderHomeGroup</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfolderhomegroup)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5951e-126">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5951e-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5951e-127">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5951e-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5951e-128">AllowPinnedFolderMusic</span><span class="sxs-lookup"><span data-stu-id="5951e-128">AllowPinnedFolderMusic</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfoldermusic)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5951e-129">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5951e-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5951e-130">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5951e-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5951e-131">AllowPinnedFolderNetwork</span><span class="sxs-lookup"><span data-stu-id="5951e-131">AllowPinnedFolderNetwork</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfoldernetwork)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5951e-132">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5951e-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5951e-133">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5951e-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5951e-134">AllowPinnedFolderPersonalFolder</span><span class="sxs-lookup"><span data-stu-id="5951e-134">AllowPinnedFolderPersonalFolder</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfolderpersonalfolder)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5951e-135">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5951e-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5951e-136">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5951e-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5951e-137">AllowPinnedFolderPictures</span><span class="sxs-lookup"><span data-stu-id="5951e-137">AllowPinnedFolderPictures</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfolderpictures)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5951e-138">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5951e-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5951e-139">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5951e-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5951e-140">AllowPinnedFolderSettings</span><span class="sxs-lookup"><span data-stu-id="5951e-140">AllowPinnedFolderSettings</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfoldersettings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5951e-141">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5951e-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5951e-142">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5951e-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5951e-143">AllowPinnedFolderVideos</span><span class="sxs-lookup"><span data-stu-id="5951e-143">AllowPinnedFolderVideos</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfoldervideos)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5951e-144">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5951e-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5951e-145">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5951e-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5951e-146">ForceStartSize</span><span class="sxs-lookup"><span data-stu-id="5951e-146">ForceStartSize</span></span>](/windows/client-management/mdm/policy-csp-start#start-forcestartsize)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5951e-147">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5951e-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5951e-148">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5951e-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5951e-149">HideAppList</span><span class="sxs-lookup"><span data-stu-id="5951e-149">HideAppList</span></span>](/windows/client-management/mdm/policy-csp-start#start-hideapplist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5951e-150">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5951e-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5951e-151">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5951e-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5951e-152">HideChangeAccountSettings</span><span class="sxs-lookup"><span data-stu-id="5951e-152">HideChangeAccountSettings</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidechangeaccountsettings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5951e-153">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5951e-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5951e-154">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5951e-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5951e-155">HideFrequentlyUsedApps</span><span class="sxs-lookup"><span data-stu-id="5951e-155">HideFrequentlyUsedApps</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidefrequentlyusedapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5951e-156">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5951e-156">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5951e-157">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5951e-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5951e-158">HideHibernate</span><span class="sxs-lookup"><span data-stu-id="5951e-158">HideHibernate</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidehibernate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5951e-159">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5951e-159">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5951e-160">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5951e-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5951e-161">HideLock</span><span class="sxs-lookup"><span data-stu-id="5951e-161">HideLock</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidelock)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5951e-162">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5951e-162">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5951e-163">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5951e-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5951e-164">HidePowerButton</span><span class="sxs-lookup"><span data-stu-id="5951e-164">HidePowerButton</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidepowerbutton)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5951e-165">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5951e-165">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5951e-166">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5951e-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5951e-167">HideRecentJumplists</span><span class="sxs-lookup"><span data-stu-id="5951e-167">HideRecentJumplists</span></span>](/windows/client-management/mdm/policy-csp-start#start-hiderecentjumplists)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5951e-168">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5951e-168">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5951e-169">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5951e-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5951e-170">HideRecentlyAddedApps</span><span class="sxs-lookup"><span data-stu-id="5951e-170">HideRecentlyAddedApps</span></span>](/windows/client-management/mdm/policy-csp-start#start-hiderecentlyaddedapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5951e-171">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5951e-171">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5951e-172">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5951e-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5951e-173">HideRestart</span><span class="sxs-lookup"><span data-stu-id="5951e-173">HideRestart</span></span>](/windows/client-management/mdm/policy-csp-start#start-hiderestart)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5951e-174">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5951e-174">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5951e-175">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5951e-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5951e-176">HideShutDown</span><span class="sxs-lookup"><span data-stu-id="5951e-176">HideShutDown</span></span>](/windows/client-management/mdm/policy-csp-start#start-hideshutdown)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5951e-177">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5951e-177">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5951e-178">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5951e-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5951e-179">HideSignOut</span><span class="sxs-lookup"><span data-stu-id="5951e-179">HideSignOut</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidesignout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5951e-180">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5951e-180">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5951e-181">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5951e-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5951e-182">HideSleep</span><span class="sxs-lookup"><span data-stu-id="5951e-182">HideSleep</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidesleep)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5951e-183">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5951e-183">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5951e-184">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5951e-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5951e-185">HideSwitchAccount</span><span class="sxs-lookup"><span data-stu-id="5951e-185">HideSwitchAccount</span></span>](/windows/client-management/mdm/policy-csp-start#start-hideswitchaccount)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5951e-186">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5951e-186">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5951e-187">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5951e-187">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5951e-188">HideUserTile</span><span class="sxs-lookup"><span data-stu-id="5951e-188">HideUserTile</span></span>](/windows/client-management/mdm/policy-csp-start#start-hideusertile)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5951e-189">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5951e-189">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5951e-190">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5951e-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5951e-191">ImportEdgeAssets</span><span class="sxs-lookup"><span data-stu-id="5951e-191">ImportEdgeAssets</span></span>](/windows/client-management/mdm/policy-csp-start#start-importedgeassets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5951e-192">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5951e-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5951e-193">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5951e-193">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5951e-194">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="5951e-194">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5951e-195">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5951e-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5951e-196">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5951e-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5951e-197">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5951e-197">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5951e-198">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="5951e-198">Identifies the name of the parent node.</span></span> <span data-ttu-id="5951e-199">Per questa classe la stringa è "Start"</span><span class="sxs-lookup"><span data-stu-id="5951e-199">For this class, the string is "Start"</span></span>

</dd> <dt>

[<span data-ttu-id="5951e-200">NoPinningToTaskbar</span><span class="sxs-lookup"><span data-stu-id="5951e-200">NoPinningToTaskbar</span></span>](/windows/client-management/mdm/policy-csp-start#start-nopinningtotaskbar)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5951e-201">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5951e-201">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5951e-202">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5951e-202">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5951e-203">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="5951e-203">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5951e-204">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5951e-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5951e-205">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5951e-205">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5951e-206">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5951e-206">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5951e-207">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="5951e-207">Describes the full path to the parent node.</span></span> <span data-ttu-id="5951e-208">Per questa classe la stringa è "./Vendor/MSFT/Policy/Config"</span><span class="sxs-lookup"><span data-stu-id="5951e-208">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="5951e-209">StartLayout</span><span class="sxs-lookup"><span data-stu-id="5951e-209">StartLayout</span></span>](/windows/client-management/mdm/policy-csp-start#start-startlayout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5951e-210">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5951e-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5951e-211">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5951e-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5951e-212">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5951e-212">Requirements</span></span>



| <span data-ttu-id="5951e-213">Requisito</span><span class="sxs-lookup"><span data-stu-id="5951e-213">Requirement</span></span> | <span data-ttu-id="5951e-214">Valore</span><span class="sxs-lookup"><span data-stu-id="5951e-214">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5951e-215">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5951e-215">Minimum supported client</span></span><br/> | <span data-ttu-id="5951e-216">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="5951e-216">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5951e-217">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5951e-217">Minimum supported server</span></span><br/> | <span data-ttu-id="5951e-218">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="5951e-218">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="5951e-219">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5951e-219">Namespace</span></span><br/>                | <span data-ttu-id="5951e-220">\\ \\ DMMap MDM CIMv2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="5951e-220">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="5951e-221">MOF</span><span class="sxs-lookup"><span data-stu-id="5951e-221">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5951e-222"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5951e-222"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="5951e-223">DLL</span><span class="sxs-lookup"><span data-stu-id="5951e-223">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5951e-224"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5951e-224"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5951e-225">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5951e-225">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5951e-226">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="5951e-226">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

