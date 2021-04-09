---
title: Classe MDM_Policy_Config01_DeliveryOptimization02
description: La \_ \_ classe Config01 DeliveryOptimization02 dei criteri MDM \_ rappresenta i criteri di ottimizzazione recapito disponibili.
ms.assetid: 10dfb751-f044-4f30-90e0-af0fcb0931fb
keywords:
- Classe MDM_Policy_Config01_DeliveryOptimization02
- Classe MDM_Policy_Config01_DeliveryOptimization02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_DeliveryOptimization02
- MDM_Policy_Config01_DeliveryOptimization02.InstanceID
- MDM_Policy_Config01_DeliveryOptimization02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9fb9675f87a5bf9951e125bded69ae5eb10feb0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119414"
---
# <a name="mdm_policy_config01_deliveryoptimization02-class"></a><span data-ttu-id="917ab-105">\_ \_ Classe Config01 DeliveryOptimization02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="917ab-105">MDM\_Policy\_Config01\_DeliveryOptimization02 class</span></span>

<span data-ttu-id="917ab-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="917ab-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="917ab-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="917ab-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="917ab-108">La **classe \_ \_ Config01 \_ DeliveryOptimization02 dei criteri MDM** rappresenta i criteri di ottimizzazione recapito disponibili.</span><span class="sxs-lookup"><span data-stu-id="917ab-108">The **MDM\_Policy\_Config01\_DeliveryOptimization02** class represents the delivery optimization policies available.</span></span>

<span data-ttu-id="917ab-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="917ab-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="917ab-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="917ab-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_DeliveryOptimization02
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

## <a name="members"></a><span data-ttu-id="917ab-111">Members</span><span class="sxs-lookup"><span data-stu-id="917ab-111">Members</span></span>

<span data-ttu-id="917ab-112">La **classe \_ \_ Config01 \_ DeliveryOptimization02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="917ab-112">The **MDM\_Policy\_Config01\_DeliveryOptimization02** class has these types of members:</span></span>

-   [<span data-ttu-id="917ab-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="917ab-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="917ab-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="917ab-114">Properties</span></span>

<span data-ttu-id="917ab-115">La **classe \_ \_ \_ DeliveryOptimization02 dei criteri MDM Config01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="917ab-115">The **MDM\_Policy\_Config01\_DeliveryOptimization02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="917ab-116">DOAbsoluteMaxCacheSize</span><span class="sxs-lookup"><span data-stu-id="917ab-116">DOAbsoluteMaxCacheSize</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-doabsolutemaxcachesize)
</dt> <dd> <dl> <dt>

<span data-ttu-id="917ab-117">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="917ab-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="917ab-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="917ab-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="917ab-119">DOAllowVPNPeerCaching</span><span class="sxs-lookup"><span data-stu-id="917ab-119">DOAllowVPNPeerCaching</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-doallowvpnpeercaching)
</dt> <dd> <dl> <dt>

<span data-ttu-id="917ab-120">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="917ab-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="917ab-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="917ab-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="917ab-122">DOCacheHost</span><span class="sxs-lookup"><span data-stu-id="917ab-122">DOCacheHost</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-docachehost)
</dt> <dd> <dl> <dt>

<span data-ttu-id="917ab-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="917ab-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="917ab-124">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="917ab-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="917ab-125">DODownloadMode</span><span class="sxs-lookup"><span data-stu-id="917ab-125">DODownloadMode</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dodownloadmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="917ab-126">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="917ab-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="917ab-127">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="917ab-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="917ab-128">DOGroupID</span><span class="sxs-lookup"><span data-stu-id="917ab-128">DOGroupID</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dogroupid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="917ab-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="917ab-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="917ab-130">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="917ab-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="917ab-131">DOMaxCacheAge</span><span class="sxs-lookup"><span data-stu-id="917ab-131">DOMaxCacheAge</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domaxcacheage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="917ab-132">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="917ab-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="917ab-133">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="917ab-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="917ab-134">DOMaxCacheSize</span><span class="sxs-lookup"><span data-stu-id="917ab-134">DOMaxCacheSize</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domaxcachesize)
</dt> <dd> <dl> <dt>

<span data-ttu-id="917ab-135">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="917ab-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="917ab-136">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="917ab-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="917ab-137">DOMaxDownloadBandwidth</span><span class="sxs-lookup"><span data-stu-id="917ab-137">DOMaxDownloadBandwidth</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domaxdownloadbandwidth)
</dt> <dd> <dl> <dt>

<span data-ttu-id="917ab-138">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="917ab-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="917ab-139">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="917ab-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="917ab-140">DOMaxUploadBandwidth</span><span class="sxs-lookup"><span data-stu-id="917ab-140">DOMaxUploadBandwidth</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domaxuploadbandwidth)
</dt> <dd> <dl> <dt>

<span data-ttu-id="917ab-141">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="917ab-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="917ab-142">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="917ab-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="917ab-143">DOMinBackgroundQos</span><span class="sxs-lookup"><span data-stu-id="917ab-143">DOMinBackgroundQos</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dominbackgroundqos)
</dt> <dd> <dl> <dt>

<span data-ttu-id="917ab-144">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="917ab-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="917ab-145">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="917ab-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="917ab-146">DOMinBatteryPercentageAllowedToUpload</span><span class="sxs-lookup"><span data-stu-id="917ab-146">DOMinBatteryPercentageAllowedToUpload</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dominbatterypercentageallowedtoupload)
</dt> <dd> <dl> <dt>

<span data-ttu-id="917ab-147">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="917ab-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="917ab-148">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="917ab-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="917ab-149">DOMinDiskSizeAllowedToPeer</span><span class="sxs-lookup"><span data-stu-id="917ab-149">DOMinDiskSizeAllowedToPeer</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domindisksizeallowedtopeer)
</dt> <dd> <dl> <dt>

<span data-ttu-id="917ab-150">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="917ab-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="917ab-151">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="917ab-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="917ab-152">DOMinFileSizeToCache</span><span class="sxs-lookup"><span data-stu-id="917ab-152">DOMinFileSizeToCache</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dominfilesizetocache)
</dt> <dd> <dl> <dt>

<span data-ttu-id="917ab-153">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="917ab-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="917ab-154">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="917ab-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="917ab-155">DOMinRAMAllowedToPeer</span><span class="sxs-lookup"><span data-stu-id="917ab-155">DOMinRAMAllowedToPeer</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dominramallowedtopeer)
</dt> <dd> <dl> <dt>

<span data-ttu-id="917ab-156">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="917ab-156">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="917ab-157">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="917ab-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="917ab-158">DOModifyCacheDrive</span><span class="sxs-lookup"><span data-stu-id="917ab-158">DOModifyCacheDrive</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domodifycachedrive)
</dt> <dd> <dl> <dt>

<span data-ttu-id="917ab-159">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="917ab-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="917ab-160">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="917ab-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="917ab-161">DOMonthlyUploadDataCap</span><span class="sxs-lookup"><span data-stu-id="917ab-161">DOMonthlyUploadDataCap</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domonthlyuploaddatacap)
</dt> <dd> <dl> <dt>

<span data-ttu-id="917ab-162">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="917ab-162">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="917ab-163">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="917ab-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="917ab-164">DOPercentageMaxDownloadBandwidth</span><span class="sxs-lookup"><span data-stu-id="917ab-164">DOPercentageMaxDownloadBandwidth</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dopercentagemaxdownloadbandwidth)
</dt> <dd> <dl> <dt>

<span data-ttu-id="917ab-165">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="917ab-165">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="917ab-166">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="917ab-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="917ab-167">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="917ab-167">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="917ab-168">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="917ab-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="917ab-169">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="917ab-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="917ab-170">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="917ab-170">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="917ab-171">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="917ab-171">Identifies the name of the parent node.</span></span> <span data-ttu-id="917ab-172">Per questa classe la stringa è "DeliveryOptimization".</span><span class="sxs-lookup"><span data-stu-id="917ab-172">For this class, the string is "DeliveryOptimization".</span></span>

</dd> <dt>

<span data-ttu-id="917ab-173">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="917ab-173">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="917ab-174">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="917ab-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="917ab-175">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="917ab-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="917ab-176">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="917ab-176">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="917ab-177">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="917ab-177">Describes the full path to the parent node.</span></span> <span data-ttu-id="917ab-178">Per questa classe la stringa è "./Vendor/MSFT/Policy/Config"</span><span class="sxs-lookup"><span data-stu-id="917ab-178">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="917ab-179">Requisiti</span><span class="sxs-lookup"><span data-stu-id="917ab-179">Requirements</span></span>



| <span data-ttu-id="917ab-180">Requisito</span><span class="sxs-lookup"><span data-stu-id="917ab-180">Requirement</span></span> | <span data-ttu-id="917ab-181">Valore</span><span class="sxs-lookup"><span data-stu-id="917ab-181">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="917ab-182">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="917ab-182">Minimum supported client</span></span><br/> | <span data-ttu-id="917ab-183">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="917ab-183">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="917ab-184">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="917ab-184">Minimum supported server</span></span><br/> | <span data-ttu-id="917ab-185">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="917ab-185">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="917ab-186">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="917ab-186">Namespace</span></span><br/>                | <span data-ttu-id="917ab-187">\\ \\ DMMap MDM CIMv2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="917ab-187">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="917ab-188">MOF</span><span class="sxs-lookup"><span data-stu-id="917ab-188">MOF</span></span><br/>                      | <dl> <span data-ttu-id="917ab-189"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="917ab-189"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="917ab-190">DLL</span><span class="sxs-lookup"><span data-stu-id="917ab-190">DLL</span></span><br/>                      | <dl> <span data-ttu-id="917ab-191"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="917ab-191"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="917ab-192">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="917ab-192">See also</span></span>

<dl> <dt>

[<span data-ttu-id="917ab-193">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="917ab-193">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

