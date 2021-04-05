---
title: Classe MDM_Policy_Result01_DeliveryOptimization02
description: La \_ \_ classe Result01 DeliveryOptimization02 dei criteri MDM \_ rappresenta i criteri di ottimizzazione recapito disponibili.
ms.assetid: 0f8a6de1-0f6c-4ee2-9235-9b5dc855f8c4
keywords:
- Classe MDM_Policy_Result01_DeliveryOptimization02
- Classe MDM_Policy_Result01_DeliveryOptimization02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_DeliveryOptimization02
- MDM_Policy_Result01_DeliveryOptimization02.InstanceID
- MDM_Policy_Result01_DeliveryOptimization02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69408228b2ed67c12de83575ddc524387498e91a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740687"
---
# <a name="mdm_policy_result01_deliveryoptimization02-class"></a><span data-ttu-id="1ef6b-105">\_ \_ Classe Result01 DeliveryOptimization02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="1ef6b-105">MDM\_Policy\_Result01\_DeliveryOptimization02 class</span></span>

<span data-ttu-id="1ef6b-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="1ef6b-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="1ef6b-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="1ef6b-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="1ef6b-108">La **classe \_ \_ Result01 \_ DeliveryOptimization02 dei criteri MDM** rappresenta i criteri di ottimizzazione recapito disponibili.</span><span class="sxs-lookup"><span data-stu-id="1ef6b-108">The **MDM\_Policy\_Result01\_DeliveryOptimization02** class represents the delivery optimization policies available.</span></span>

<span data-ttu-id="1ef6b-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="1ef6b-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ef6b-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1ef6b-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_DeliveryOptimization02
{
  string InstanceID;
  string ParentID;
  sint32 DOAbsoluteMaxCacheSize;
  sint32 DOAllowVPNPeerCaching;
  string DOCacheHost;
  string DOGroupID;
  sint32 DOMaxUploadBandwidth;
  sint32 DOPercentageMaxDownloadBandwidth;
  sint32 DOMonthlyUploadDataCap;
  string DOModifyCacheDrive;
  sint32 DOMinBackgroundQos;
  sint32 DOMinRAMAllowedToPeer;
  sint32 DOMinFileSizeToCache;
  sint32 DOMinDiskSizeAllowedToPeer;
  sint32 DOMinBatteryPercentageAllowedToUpload;
  sint32 DOMaxCacheSize;
  sint32 DOMaxDownloadBandwidth;
  sint32 DOMaxCacheAge;
  sint32 DODownloadMode;
};
```

## <a name="members"></a><span data-ttu-id="1ef6b-111">Members</span><span class="sxs-lookup"><span data-stu-id="1ef6b-111">Members</span></span>

<span data-ttu-id="1ef6b-112">La **classe \_ \_ Result01 \_ DeliveryOptimization02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="1ef6b-112">The **MDM\_Policy\_Result01\_DeliveryOptimization02** class has these types of members:</span></span>

-   [<span data-ttu-id="1ef6b-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1ef6b-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1ef6b-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1ef6b-114">Properties</span></span>

<span data-ttu-id="1ef6b-115">La **classe \_ \_ \_ DeliveryOptimization02 dei criteri MDM Result01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="1ef6b-115">The **MDM\_Policy\_Result01\_DeliveryOptimization02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="1ef6b-116">DOAbsoluteMaxCacheSize</span><span class="sxs-lookup"><span data-stu-id="1ef6b-116">DOAbsoluteMaxCacheSize</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-doabsolutemaxcachesize)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ef6b-117">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1ef6b-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1ef6b-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="1ef6b-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1ef6b-119">DOAllowVPNPeerCaching</span><span class="sxs-lookup"><span data-stu-id="1ef6b-119">DOAllowVPNPeerCaching</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-doallowvpnpeercaching)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ef6b-120">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1ef6b-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1ef6b-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="1ef6b-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1ef6b-122">DOCacheHost</span><span class="sxs-lookup"><span data-stu-id="1ef6b-122">DOCacheHost</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-docachehost)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ef6b-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1ef6b-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ef6b-124">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="1ef6b-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1ef6b-125">DODownloadMode</span><span class="sxs-lookup"><span data-stu-id="1ef6b-125">DODownloadMode</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dodownloadmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ef6b-126">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1ef6b-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1ef6b-127">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="1ef6b-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1ef6b-128">DOGroupID</span><span class="sxs-lookup"><span data-stu-id="1ef6b-128">DOGroupID</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dogroupid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ef6b-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1ef6b-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ef6b-130">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="1ef6b-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1ef6b-131">DOMaxCacheAge</span><span class="sxs-lookup"><span data-stu-id="1ef6b-131">DOMaxCacheAge</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domaxcacheage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ef6b-132">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1ef6b-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1ef6b-133">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="1ef6b-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1ef6b-134">DOMaxCacheSize</span><span class="sxs-lookup"><span data-stu-id="1ef6b-134">DOMaxCacheSize</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domaxcachesize)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ef6b-135">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1ef6b-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1ef6b-136">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="1ef6b-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1ef6b-137">DOMaxDownloadBandwidth</span><span class="sxs-lookup"><span data-stu-id="1ef6b-137">DOMaxDownloadBandwidth</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domaxdownloadbandwidth)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ef6b-138">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1ef6b-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1ef6b-139">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="1ef6b-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1ef6b-140">DOMaxUploadBandwidth</span><span class="sxs-lookup"><span data-stu-id="1ef6b-140">DOMaxUploadBandwidth</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domaxuploadbandwidth)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ef6b-141">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1ef6b-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1ef6b-142">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="1ef6b-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1ef6b-143">DOMinBackgroundQos</span><span class="sxs-lookup"><span data-stu-id="1ef6b-143">DOMinBackgroundQos</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dominbackgroundqos)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ef6b-144">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1ef6b-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1ef6b-145">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="1ef6b-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1ef6b-146">DOMinBatteryPercentageAllowedToUpload</span><span class="sxs-lookup"><span data-stu-id="1ef6b-146">DOMinBatteryPercentageAllowedToUpload</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dominbatterypercentageallowedtoupload)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ef6b-147">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1ef6b-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1ef6b-148">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="1ef6b-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1ef6b-149">DOMinDiskSizeAllowedToPeer</span><span class="sxs-lookup"><span data-stu-id="1ef6b-149">DOMinDiskSizeAllowedToPeer</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domindisksizeallowedtopeer)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ef6b-150">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1ef6b-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1ef6b-151">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="1ef6b-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1ef6b-152">DOMinFileSizeToCache</span><span class="sxs-lookup"><span data-stu-id="1ef6b-152">DOMinFileSizeToCache</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dominfilesizetocache)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ef6b-153">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1ef6b-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1ef6b-154">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="1ef6b-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1ef6b-155">DOMinRAMAllowedToPeer</span><span class="sxs-lookup"><span data-stu-id="1ef6b-155">DOMinRAMAllowedToPeer</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dominramallowedtopeer)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ef6b-156">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1ef6b-156">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1ef6b-157">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="1ef6b-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1ef6b-158">DOModifyCacheDrive</span><span class="sxs-lookup"><span data-stu-id="1ef6b-158">DOModifyCacheDrive</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domodifycachedrive)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ef6b-159">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1ef6b-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ef6b-160">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="1ef6b-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1ef6b-161">DOMonthlyUploadDataCap</span><span class="sxs-lookup"><span data-stu-id="1ef6b-161">DOMonthlyUploadDataCap</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domonthlyuploaddatacap)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ef6b-162">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1ef6b-162">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1ef6b-163">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="1ef6b-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1ef6b-164">DOPercentageMaxDownloadBandwidth</span><span class="sxs-lookup"><span data-stu-id="1ef6b-164">DOPercentageMaxDownloadBandwidth</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dopercentagemaxdownloadbandwidth)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ef6b-165">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1ef6b-165">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1ef6b-166">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="1ef6b-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1ef6b-167">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1ef6b-167">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ef6b-168">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1ef6b-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ef6b-169">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1ef6b-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ef6b-170">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1ef6b-170">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1ef6b-171">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="1ef6b-171">Identifies the name of the parent node.</span></span> <span data-ttu-id="1ef6b-172">Per questa classe la stringa è "DeliveryOptimization".</span><span class="sxs-lookup"><span data-stu-id="1ef6b-172">For this class, the string is "DeliveryOptimization".</span></span>

</dd> <dt>

<span data-ttu-id="1ef6b-173">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="1ef6b-173">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ef6b-174">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1ef6b-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ef6b-175">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1ef6b-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ef6b-176">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1ef6b-176">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1ef6b-177">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="1ef6b-177">Describes the full path to the parent node.</span></span> <span data-ttu-id="1ef6b-178">Per questa classe la stringa è "./Vendor/MSFT/Policy/Result"</span><span class="sxs-lookup"><span data-stu-id="1ef6b-178">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1ef6b-179">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1ef6b-179">Requirements</span></span>



| <span data-ttu-id="1ef6b-180">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ef6b-180">Requirement</span></span> | <span data-ttu-id="1ef6b-181">Valore</span><span class="sxs-lookup"><span data-stu-id="1ef6b-181">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ef6b-182">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1ef6b-182">Minimum supported client</span></span><br/> | <span data-ttu-id="1ef6b-183">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="1ef6b-183">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1ef6b-184">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1ef6b-184">Minimum supported server</span></span><br/> | <span data-ttu-id="1ef6b-185">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="1ef6b-185">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="1ef6b-186">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1ef6b-186">Namespace</span></span><br/>                | <span data-ttu-id="1ef6b-187">\\ \\ DMMap MDM CIMv2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="1ef6b-187">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="1ef6b-188">MOF</span><span class="sxs-lookup"><span data-stu-id="1ef6b-188">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1ef6b-189"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1ef6b-189"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="1ef6b-190">DLL</span><span class="sxs-lookup"><span data-stu-id="1ef6b-190">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1ef6b-191"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1ef6b-191"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ef6b-192">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1ef6b-192">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ef6b-193">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="1ef6b-193">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

