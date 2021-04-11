---
title: Classe MDM_Policy_Config01_AppVirtualization02
description: La \_ \_ classe Config01 AppVirtualization02 di criteri MDM \_ Configura i criteri di virtualizzazione delle app disponibili.
ms.assetid: d270704c-8652-4f97-89f7-fcb6e68ee6fe
keywords:
- Classe MDM_Policy_Config01_AppVirtualization02
- Classe MDM_Policy_Config01_AppVirtualization02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_AppVirtualization02
- MDM_Policy_Config01_AppVirtualization02.InstanceID
- MDM_Policy_Config01_AppVirtualization02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 871d09b306cff2833601100d9a645cde5c59e33f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119431"
---
# <a name="mdm_policy_config01_appvirtualization02-class"></a><span data-ttu-id="3c900-105">\_ \_ Classe Config01 AppVirtualization02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="3c900-105">MDM\_Policy\_Config01\_AppVirtualization02 class</span></span>

<span data-ttu-id="3c900-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="3c900-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="3c900-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="3c900-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="3c900-108">La \_ \_ classe Config01 AppVirtualization02 di criteri MDM \_ Configura i criteri di virtualizzazione delle app disponibili.</span><span class="sxs-lookup"><span data-stu-id="3c900-108">The MDM\_Policy\_Config01\_AppVirtualization02 class configures the available app virtualization policies.</span></span>

<span data-ttu-id="3c900-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="3c900-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c900-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3c900-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_AppVirtualization02
{
  string InstanceID;
  string ParentID;
  string AllowAppVClient;
  string AllowDynamicVirtualization;
  string AllowPackageCleanup;
  string AllowPackageScripts;
  string AllowPublishingRefreshUX;
  string AllowReportingServer;
  string AllowRoamingFileExclusions;
  string AllowRoamingRegistryExclusions;
  string AllowStreamingAutoload;
  string ClientCoexistenceAllowMigrationmode;
  string IntegrationAllowRootGlobal;
  string IntegrationAllowRootUser;
  string PublishingAllowServer1;
  string PublishingAllowServer2;
  string PublishingAllowServer3;
  string PublishingAllowServer4;
  string PublishingAllowServer5;
  string StreamingAllowCertificateFilterForClient_SSL;
  string StreamingAllowHighCostLaunch;
  string StreamingAllowLocationProvider;
  string StreamingAllowPackageInstallationRoot;
  string StreamingAllowPackageSourceRoot;
  string StreamingAllowReestablishmentInterval;
  string StreamingAllowReestablishmentRetries;
  string StreamingSharedContentStoreMode;
  string StreamingSupportBranchCache;
  string StreamingVerifyCertificateRevocationList;
  string VirtualComponentsAllowList;
};
```

## <a name="members"></a><span data-ttu-id="3c900-111">Members</span><span class="sxs-lookup"><span data-stu-id="3c900-111">Members</span></span>

<span data-ttu-id="3c900-112">La **classe \_ \_ Config01 \_ AppVirtualization02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="3c900-112">The **MDM\_Policy\_Config01\_AppVirtualization02** class has these types of members:</span></span>

-   [<span data-ttu-id="3c900-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3c900-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3c900-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3c900-114">Properties</span></span>

<span data-ttu-id="3c900-115">La **classe \_ \_ \_ AppVirtualization02 dei criteri MDM Config01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="3c900-115">The **MDM\_Policy\_Config01\_AppVirtualization02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="3c900-116">AllowAppVClient</span><span class="sxs-lookup"><span data-stu-id="3c900-116">AllowAppVClient</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowappvclient)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c900-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3c900-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c900-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="3c900-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3c900-119">AllowDynamicVirtualization</span><span class="sxs-lookup"><span data-stu-id="3c900-119">AllowDynamicVirtualization</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowdynamicvirtualization)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c900-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3c900-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c900-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="3c900-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3c900-122">AllowPackageCleanup</span><span class="sxs-lookup"><span data-stu-id="3c900-122">AllowPackageCleanup</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowpackagecleanup)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c900-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3c900-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c900-124">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="3c900-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3c900-125">AllowPackageScripts</span><span class="sxs-lookup"><span data-stu-id="3c900-125">AllowPackageScripts</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowpackagescripts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c900-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3c900-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c900-127">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="3c900-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3c900-128">AllowPublishingRefreshUX</span><span class="sxs-lookup"><span data-stu-id="3c900-128">AllowPublishingRefreshUX</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowpublishingrefreshux)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c900-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3c900-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c900-130">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="3c900-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3c900-131">AllowReportingServer</span><span class="sxs-lookup"><span data-stu-id="3c900-131">AllowReportingServer</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowreportingserver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c900-132">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3c900-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c900-133">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="3c900-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3c900-134">AllowRoamingFileExclusions</span><span class="sxs-lookup"><span data-stu-id="3c900-134">AllowRoamingFileExclusions</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowroamingfileexclusions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c900-135">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3c900-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c900-136">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="3c900-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3c900-137">AllowRoamingRegistryExclusions</span><span class="sxs-lookup"><span data-stu-id="3c900-137">AllowRoamingRegistryExclusions</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowroamingregistryexclusions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c900-138">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3c900-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c900-139">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="3c900-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3c900-140">AllowStreamingAutoload</span><span class="sxs-lookup"><span data-stu-id="3c900-140">AllowStreamingAutoload</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowstreamingautoload)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c900-141">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3c900-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c900-142">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="3c900-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3c900-143">ClientCoexistenceAllowMigrationmode</span><span class="sxs-lookup"><span data-stu-id="3c900-143">ClientCoexistenceAllowMigrationmode</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-clientcoexistenceallowmigrationmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c900-144">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3c900-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c900-145">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="3c900-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3c900-146">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="3c900-146">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c900-147">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3c900-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c900-148">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3c900-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c900-149">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3c900-149">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3c900-150">IntegrationAllowRootGlobal</span><span class="sxs-lookup"><span data-stu-id="3c900-150">IntegrationAllowRootGlobal</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-integrationallowrootglobal)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c900-151">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3c900-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c900-152">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="3c900-152">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3c900-153">IntegrationAllowRootUser</span><span class="sxs-lookup"><span data-stu-id="3c900-153">IntegrationAllowRootUser</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-integrationallowrootuser)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c900-154">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3c900-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c900-155">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="3c900-155">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3c900-156">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="3c900-156">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c900-157">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3c900-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c900-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3c900-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c900-159">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3c900-159">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3c900-160">PublishingAllowServer1</span><span class="sxs-lookup"><span data-stu-id="3c900-160">PublishingAllowServer1</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-publishingallowserver1)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c900-161">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3c900-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c900-162">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="3c900-162">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3c900-163">PublishingAllowServer2</span><span class="sxs-lookup"><span data-stu-id="3c900-163">PublishingAllowServer2</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-publishingallowserver2)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c900-164">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3c900-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c900-165">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="3c900-165">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3c900-166">PublishingAllowServer3</span><span class="sxs-lookup"><span data-stu-id="3c900-166">PublishingAllowServer3</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-publishingallowserver3)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c900-167">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3c900-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c900-168">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="3c900-168">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3c900-169">PublishingAllowServer4</span><span class="sxs-lookup"><span data-stu-id="3c900-169">PublishingAllowServer4</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-publishingallowserver4)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c900-170">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3c900-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c900-171">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="3c900-171">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3c900-172">PublishingAllowServer5</span><span class="sxs-lookup"><span data-stu-id="3c900-172">PublishingAllowServer5</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-publishingallowserver5)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c900-173">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3c900-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c900-174">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="3c900-174">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3c900-175">\_SSL StreamingAllowCertificateFilterForClient</span><span class="sxs-lookup"><span data-stu-id="3c900-175">StreamingAllowCertificateFilterForClient\_SSL</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingallowcertificatefilterforclient-ssl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c900-176">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3c900-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c900-177">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="3c900-177">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3c900-178">StreamingAllowHighCostLaunch</span><span class="sxs-lookup"><span data-stu-id="3c900-178">StreamingAllowHighCostLaunch</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingallowhighcostlaunch)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c900-179">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3c900-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c900-180">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="3c900-180">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3c900-181">StreamingAllowLocationProvider</span><span class="sxs-lookup"><span data-stu-id="3c900-181">StreamingAllowLocationProvider</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingallowlocationprovider)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c900-182">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3c900-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c900-183">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="3c900-183">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3c900-184">StreamingAllowPackageInstallationRoot</span><span class="sxs-lookup"><span data-stu-id="3c900-184">StreamingAllowPackageInstallationRoot</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingallowpackageinstallationroot)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c900-185">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3c900-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c900-186">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="3c900-186">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3c900-187">StreamingAllowPackageSourceRoot</span><span class="sxs-lookup"><span data-stu-id="3c900-187">StreamingAllowPackageSourceRoot</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingallowpackagesourceroot)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c900-188">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3c900-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c900-189">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="3c900-189">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3c900-190">StreamingAllowReestablishmentInterval</span><span class="sxs-lookup"><span data-stu-id="3c900-190">StreamingAllowReestablishmentInterval</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingallowreestablishmentinterval)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c900-191">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3c900-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c900-192">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="3c900-192">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3c900-193">StreamingAllowReestablishmentRetries</span><span class="sxs-lookup"><span data-stu-id="3c900-193">StreamingAllowReestablishmentRetries</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingallowreestablishmentretries)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c900-194">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3c900-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c900-195">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="3c900-195">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3c900-196">StreamingSharedContentStoreMode</span><span class="sxs-lookup"><span data-stu-id="3c900-196">StreamingSharedContentStoreMode</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingsharedcontentstoremode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c900-197">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3c900-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c900-198">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="3c900-198">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3c900-199">StreamingSupportBranchCache</span><span class="sxs-lookup"><span data-stu-id="3c900-199">StreamingSupportBranchCache</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingsupportbranchcache)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c900-200">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3c900-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c900-201">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="3c900-201">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3c900-202">StreamingVerifyCertificateRevocationList</span><span class="sxs-lookup"><span data-stu-id="3c900-202">StreamingVerifyCertificateRevocationList</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingverifycertificaterevocationlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c900-203">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3c900-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c900-204">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="3c900-204">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3c900-205">VirtualComponentsAllowList</span><span class="sxs-lookup"><span data-stu-id="3c900-205">VirtualComponentsAllowList</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-virtualcomponentsallowlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c900-206">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3c900-206">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c900-207">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="3c900-207">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3c900-208">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3c900-208">Requirements</span></span>



| <span data-ttu-id="3c900-209">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c900-209">Requirement</span></span> | <span data-ttu-id="3c900-210">Valore</span><span class="sxs-lookup"><span data-stu-id="3c900-210">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c900-211">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3c900-211">Minimum supported client</span></span><br/> | <span data-ttu-id="3c900-212">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="3c900-212">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3c900-213">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3c900-213">Minimum supported server</span></span><br/> | <span data-ttu-id="3c900-214">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="3c900-214">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="3c900-215">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3c900-215">Namespace</span></span><br/>                | <span data-ttu-id="3c900-216">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="3c900-216">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="3c900-217">MOF</span><span class="sxs-lookup"><span data-stu-id="3c900-217">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3c900-218"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3c900-218"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="3c900-219">DLL</span><span class="sxs-lookup"><span data-stu-id="3c900-219">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c900-220"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c900-220"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

