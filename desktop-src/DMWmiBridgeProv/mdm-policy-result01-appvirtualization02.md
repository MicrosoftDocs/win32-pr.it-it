---
title: Classe MDM_Policy_Result01_AppVirtualization02
description: La \_ classe AppVirtualization02 dei criteri MDM \_ Result01 \_ rappresenta i criteri di virtualizzazione delle app disponibili.
ms.assetid: fc28646f-f4b9-4648-a22d-b90d32ff888f
keywords:
- Classe MDM_Policy_Result01_AppVirtualization02
- Classe MDM_Policy_Result01_AppVirtualization02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_AppVirtualization02
- MDM_Policy_Result01_AppVirtualization02.InstanceID
- MDM_Policy_Result01_AppVirtualization02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 968c4718d7978bdf6770bdf8f828e6ef268cd32d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477284"
---
# <a name="mdm_policy_result01_appvirtualization02-class"></a><span data-ttu-id="7d2e7-105">\_ \_ Classe Result01 AppVirtualization02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="7d2e7-105">MDM\_Policy\_Result01\_AppVirtualization02 class</span></span>

<span data-ttu-id="7d2e7-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="7d2e7-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="7d2e7-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="7d2e7-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="7d2e7-108">La \_ classe AppVirtualization02 dei criteri MDM \_ Result01 \_ rappresenta i criteri di virtualizzazione delle app disponibili.</span><span class="sxs-lookup"><span data-stu-id="7d2e7-108">The MDM\_Policy\_Result01\_AppVirtualization02 class represents the available app virtualization policies.</span></span>

<span data-ttu-id="7d2e7-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="7d2e7-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d2e7-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7d2e7-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_AppVirtualization02
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

## <a name="members"></a><span data-ttu-id="7d2e7-111">Members</span><span class="sxs-lookup"><span data-stu-id="7d2e7-111">Members</span></span>

<span data-ttu-id="7d2e7-112">La **classe \_ \_ Result01 \_ AppVirtualization02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="7d2e7-112">The **MDM\_Policy\_Result01\_AppVirtualization02** class has these types of members:</span></span>

-   [<span data-ttu-id="7d2e7-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7d2e7-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7d2e7-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7d2e7-114">Properties</span></span>

<span data-ttu-id="7d2e7-115">La **classe \_ \_ \_ AppVirtualization02 dei criteri MDM Result01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="7d2e7-115">The **MDM\_Policy\_Result01\_AppVirtualization02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="7d2e7-116">AllowAppVClient</span><span class="sxs-lookup"><span data-stu-id="7d2e7-116">AllowAppVClient</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowappvclient)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d2e7-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7d2e7-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d2e7-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="7d2e7-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7d2e7-119">AllowDynamicVirtualization</span><span class="sxs-lookup"><span data-stu-id="7d2e7-119">AllowDynamicVirtualization</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowdynamicvirtualization)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d2e7-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7d2e7-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d2e7-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="7d2e7-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7d2e7-122">AllowPackageCleanup</span><span class="sxs-lookup"><span data-stu-id="7d2e7-122">AllowPackageCleanup</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowpackagecleanup)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d2e7-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7d2e7-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d2e7-124">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="7d2e7-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7d2e7-125">AllowPackageScripts</span><span class="sxs-lookup"><span data-stu-id="7d2e7-125">AllowPackageScripts</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowpackagescripts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d2e7-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7d2e7-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d2e7-127">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="7d2e7-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7d2e7-128">AllowPublishingRefreshUX</span><span class="sxs-lookup"><span data-stu-id="7d2e7-128">AllowPublishingRefreshUX</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowpublishingrefreshux)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d2e7-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7d2e7-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d2e7-130">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="7d2e7-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7d2e7-131">AllowReportingServer</span><span class="sxs-lookup"><span data-stu-id="7d2e7-131">AllowReportingServer</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowreportingserver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d2e7-132">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7d2e7-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d2e7-133">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="7d2e7-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7d2e7-134">AllowRoamingFileExclusions</span><span class="sxs-lookup"><span data-stu-id="7d2e7-134">AllowRoamingFileExclusions</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowroamingfileexclusions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d2e7-135">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7d2e7-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d2e7-136">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="7d2e7-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7d2e7-137">AllowRoamingRegistryExclusions</span><span class="sxs-lookup"><span data-stu-id="7d2e7-137">AllowRoamingRegistryExclusions</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowroamingregistryexclusions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d2e7-138">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7d2e7-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d2e7-139">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="7d2e7-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7d2e7-140">AllowStreamingAutoload</span><span class="sxs-lookup"><span data-stu-id="7d2e7-140">AllowStreamingAutoload</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowstreamingautoload)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d2e7-141">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7d2e7-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d2e7-142">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="7d2e7-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7d2e7-143">ClientCoexistenceAllowMigrationmode</span><span class="sxs-lookup"><span data-stu-id="7d2e7-143">ClientCoexistenceAllowMigrationmode</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-clientcoexistenceallowmigrationmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d2e7-144">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7d2e7-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d2e7-145">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="7d2e7-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7d2e7-146">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="7d2e7-146">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d2e7-147">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7d2e7-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d2e7-148">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7d2e7-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7d2e7-149">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7d2e7-149">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7d2e7-150">IntegrationAllowRootGlobal</span><span class="sxs-lookup"><span data-stu-id="7d2e7-150">IntegrationAllowRootGlobal</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-integrationallowrootglobal)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d2e7-151">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7d2e7-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d2e7-152">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="7d2e7-152">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7d2e7-153">IntegrationAllowRootUser</span><span class="sxs-lookup"><span data-stu-id="7d2e7-153">IntegrationAllowRootUser</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-integrationallowrootuser)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d2e7-154">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7d2e7-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d2e7-155">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="7d2e7-155">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7d2e7-156">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="7d2e7-156">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d2e7-157">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7d2e7-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d2e7-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7d2e7-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7d2e7-159">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7d2e7-159">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7d2e7-160">PublishingAllowServer1</span><span class="sxs-lookup"><span data-stu-id="7d2e7-160">PublishingAllowServer1</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-publishingallowserver1)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d2e7-161">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7d2e7-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d2e7-162">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="7d2e7-162">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7d2e7-163">PublishingAllowServer2</span><span class="sxs-lookup"><span data-stu-id="7d2e7-163">PublishingAllowServer2</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-publishingallowserver2)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d2e7-164">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7d2e7-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d2e7-165">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="7d2e7-165">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7d2e7-166">PublishingAllowServer3</span><span class="sxs-lookup"><span data-stu-id="7d2e7-166">PublishingAllowServer3</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-publishingallowserver3)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d2e7-167">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7d2e7-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d2e7-168">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="7d2e7-168">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7d2e7-169">PublishingAllowServer4</span><span class="sxs-lookup"><span data-stu-id="7d2e7-169">PublishingAllowServer4</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-publishingallowserver4)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d2e7-170">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7d2e7-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d2e7-171">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="7d2e7-171">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7d2e7-172">PublishingAllowServer5</span><span class="sxs-lookup"><span data-stu-id="7d2e7-172">PublishingAllowServer5</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-publishingallowserver5)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d2e7-173">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7d2e7-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d2e7-174">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="7d2e7-174">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7d2e7-175">\_SSL StreamingAllowCertificateFilterForClient</span><span class="sxs-lookup"><span data-stu-id="7d2e7-175">StreamingAllowCertificateFilterForClient\_SSL</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingallowcertificatefilterforclient-ssl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d2e7-176">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7d2e7-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d2e7-177">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="7d2e7-177">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7d2e7-178">StreamingAllowHighCostLaunch</span><span class="sxs-lookup"><span data-stu-id="7d2e7-178">StreamingAllowHighCostLaunch</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingallowhighcostlaunch)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d2e7-179">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7d2e7-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d2e7-180">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="7d2e7-180">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7d2e7-181">StreamingAllowLocationProvider</span><span class="sxs-lookup"><span data-stu-id="7d2e7-181">StreamingAllowLocationProvider</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingallowlocationprovider)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d2e7-182">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7d2e7-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d2e7-183">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="7d2e7-183">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7d2e7-184">StreamingAllowPackageInstallationRoot</span><span class="sxs-lookup"><span data-stu-id="7d2e7-184">StreamingAllowPackageInstallationRoot</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingallowpackageinstallationroot)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d2e7-185">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7d2e7-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d2e7-186">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="7d2e7-186">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7d2e7-187">StreamingAllowPackageSourceRoot</span><span class="sxs-lookup"><span data-stu-id="7d2e7-187">StreamingAllowPackageSourceRoot</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingallowpackagesourceroot)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d2e7-188">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7d2e7-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d2e7-189">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="7d2e7-189">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7d2e7-190">StreamingAllowReestablishmentInterval</span><span class="sxs-lookup"><span data-stu-id="7d2e7-190">StreamingAllowReestablishmentInterval</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingallowreestablishmentinterval)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d2e7-191">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7d2e7-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d2e7-192">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="7d2e7-192">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7d2e7-193">StreamingAllowReestablishmentRetries</span><span class="sxs-lookup"><span data-stu-id="7d2e7-193">StreamingAllowReestablishmentRetries</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingallowreestablishmentretries)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d2e7-194">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7d2e7-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d2e7-195">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="7d2e7-195">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7d2e7-196">StreamingSharedContentStoreMode</span><span class="sxs-lookup"><span data-stu-id="7d2e7-196">StreamingSharedContentStoreMode</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingsharedcontentstoremode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d2e7-197">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7d2e7-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d2e7-198">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="7d2e7-198">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7d2e7-199">StreamingSupportBranchCache</span><span class="sxs-lookup"><span data-stu-id="7d2e7-199">StreamingSupportBranchCache</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingsupportbranchcache)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d2e7-200">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7d2e7-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d2e7-201">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="7d2e7-201">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7d2e7-202">StreamingVerifyCertificateRevocationList</span><span class="sxs-lookup"><span data-stu-id="7d2e7-202">StreamingVerifyCertificateRevocationList</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingverifycertificaterevocationlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d2e7-203">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7d2e7-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d2e7-204">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="7d2e7-204">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7d2e7-205">VirtualComponentsAllowList</span><span class="sxs-lookup"><span data-stu-id="7d2e7-205">VirtualComponentsAllowList</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-virtualcomponentsallowlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d2e7-206">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7d2e7-206">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d2e7-207">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="7d2e7-207">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7d2e7-208">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7d2e7-208">Requirements</span></span>



| <span data-ttu-id="7d2e7-209">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d2e7-209">Requirement</span></span> | <span data-ttu-id="7d2e7-210">Valore</span><span class="sxs-lookup"><span data-stu-id="7d2e7-210">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d2e7-211">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7d2e7-211">Minimum supported client</span></span><br/> | <span data-ttu-id="7d2e7-212">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="7d2e7-212">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7d2e7-213">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7d2e7-213">Minimum supported server</span></span><br/> | <span data-ttu-id="7d2e7-214">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="7d2e7-214">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="7d2e7-215">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7d2e7-215">Namespace</span></span><br/>                | <span data-ttu-id="7d2e7-216">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="7d2e7-216">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="7d2e7-217">MOF</span><span class="sxs-lookup"><span data-stu-id="7d2e7-217">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7d2e7-218"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7d2e7-218"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="7d2e7-219">DLL</span><span class="sxs-lookup"><span data-stu-id="7d2e7-219">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7d2e7-220"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7d2e7-220"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

