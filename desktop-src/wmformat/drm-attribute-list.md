---
title: Elenco attributi DRM
description: Elenco attributi DRM
ms.assetid: 222ef91c-b776-4de8-b1ad-88c2beca05aa
keywords:
- Windows Media Format SDK, attributi
- ASF (Advanced Systems Format), attributi
- ASF (formato avanzato dei sistemi), attributi
- attributi, Digital Rights Management (DRM)
- Digital Rights Management (DRM), attributi
- DRM (Digital Rights Management), attributi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3beccc33a48f57015040f06c140a55f5f9691daa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298901"
---
# <a name="drm-attribute-list"></a><span data-ttu-id="0865c-109">Elenco attributi DRM</span><span class="sxs-lookup"><span data-stu-id="0865c-109">DRM Attribute List</span></span>

<span data-ttu-id="0865c-110">Per praticità, nella tabella seguente sono elencati tutti gli attributi di file correlati a DRM.</span><span class="sxs-lookup"><span data-stu-id="0865c-110">For convenience, the following table lists all the DRM-related file attributes.</span></span> <span data-ttu-id="0865c-111">Questi attributi sono elencati anche nella tabella di tutti gli attributi in [elenco attributi](attribute-list.md).</span><span class="sxs-lookup"><span data-stu-id="0865c-111">(These attributes are also listed in the table of all attributes under [Attribute List](attribute-list.md).)</span></span>

<span data-ttu-id="0865c-112">Le applicazioni possono impostare questi valori durante la scrittura di file DRM e possono recuperarli durante la lettura.</span><span class="sxs-lookup"><span data-stu-id="0865c-112">Applications can set these values when writing DRM files and can retrieve them when reading.</span></span>



| <span data-ttu-id="0865c-113">Attributo file DRM</span><span class="sxs-lookup"><span data-stu-id="0865c-113">DRM file attribute</span></span>                                                                   | <span data-ttu-id="0865c-114">Identificatore globale</span><span class="sxs-lookup"><span data-stu-id="0865c-114">Global identifier</span></span>                             | <span data-ttu-id="0865c-115">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="0865c-115">Data type</span></span>             |
|--------------------------------------------------------------------------------------|-----------------------------------------------|-----------------------|
| [<span data-ttu-id="0865c-116">**\_CONTENTID DRM**</span><span class="sxs-lookup"><span data-stu-id="0865c-116">**DRM\_ContentID**</span></span>](drm-contentid.md)                                              | <span data-ttu-id="0865c-117">g \_ wszWMDRM \_ ContentID</span><span class="sxs-lookup"><span data-stu-id="0865c-117">g\_wszWMDRM\_ContentID</span></span>                        | <span data-ttu-id="0865c-118">**\_stringa di tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="0865c-118">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="0865c-119">**\_Contentdistributor DRMHEADER \_ DRM**</span><span class="sxs-lookup"><span data-stu-id="0865c-119">**DRM\_DRMHeader\_ContentDistributor**</span></span>](drm-drmheader-contentdistributor.md)       | <span data-ttu-id="0865c-120">g \_ wszWMDRM \_ DRMHeader \_ contentdistributor</span><span class="sxs-lookup"><span data-stu-id="0865c-120">g\_wszWMDRM\_DRMHeader\_ContentDistributor</span></span>    | <span data-ttu-id="0865c-121">**\_stringa di tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="0865c-121">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="0865c-122">**\_ContentID DRMHEADER \_ DRM**</span><span class="sxs-lookup"><span data-stu-id="0865c-122">**DRM\_DRMHeader\_ContentID**</span></span>](drm-drmheader-contentid.md)                         | <span data-ttu-id="0865c-123">g \_ wszWMDRM \_ DRMHeader \_ ContentID</span><span class="sxs-lookup"><span data-stu-id="0865c-123">g\_wszWMDRM\_DRMHeader\_ContentID</span></span>             | <span data-ttu-id="0865c-124">**\_stringa di tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="0865c-124">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="0865c-125">**\_IndividualizedVersion DRMHEADER \_ DRM**</span><span class="sxs-lookup"><span data-stu-id="0865c-125">**DRM\_DRMHeader\_IndividualizedVersion**</span></span>](drm-drmheader-individualizedversion.md) | <span data-ttu-id="0865c-126">g \_ wszWMDRM \_ DRMHeader \_ IndividualizedVersion</span><span class="sxs-lookup"><span data-stu-id="0865c-126">g\_wszWMDRM\_DRMHeader\_IndividualizedVersion</span></span> | <span data-ttu-id="0865c-127">**\_stringa di tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="0865c-127">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="0865c-128">**\_KeyId DRMHEADER \_ DRM**</span><span class="sxs-lookup"><span data-stu-id="0865c-128">**DRM\_DRMHeader\_KeyID**</span></span>](drm-drmheader-keyid.md)                                 | <span data-ttu-id="0865c-129">g \_ wszWMDRM \_ DRMHeader \_ keyId</span><span class="sxs-lookup"><span data-stu-id="0865c-129">g\_wszWMDRM\_DRMHeader\_KeyID</span></span>                 | <span data-ttu-id="0865c-130">**\_stringa di tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="0865c-130">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="0865c-131">**\_LicenseAcqURL DRMHEADER \_ DRM**</span><span class="sxs-lookup"><span data-stu-id="0865c-131">**DRM\_DRMHeader\_LicenseAcqURL**</span></span>](drm-drmheader-licenseacqurl.md)                 | <span data-ttu-id="0865c-132">g \_ wszWMDRM \_ DRMHeader \_ LicenseAcqURL</span><span class="sxs-lookup"><span data-stu-id="0865c-132">g\_wszWMDRM\_DRMHeader\_LicenseAcqURL</span></span>         | <span data-ttu-id="0865c-133">**\_stringa di tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="0865c-133">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="0865c-134">**\_SubscriptionContentID DRMHEADER \_ DRM**</span><span class="sxs-lookup"><span data-stu-id="0865c-134">**DRM\_DRMHeader\_SubscriptionContentID**</span></span>](drm-drmheader-subscriptioncontentid.md) | <span data-ttu-id="0865c-135">g \_ wszWMDRM \_ DRMHeader \_ SubscriptionContentID</span><span class="sxs-lookup"><span data-stu-id="0865c-135">g\_wszWMDRM\_DRMHeader\_SubscriptionContentID</span></span> | <span data-ttu-id="0865c-136">**\_stringa di tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="0865c-136">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="0865c-137">**\_DRMHEADER DRM**</span><span class="sxs-lookup"><span data-stu-id="0865c-137">**DRM\_DRMHeader**</span></span>](drm-drmheader.md)                                              | <span data-ttu-id="0865c-138">g \_ wszWMDRM \_ DRMHeader</span><span class="sxs-lookup"><span data-stu-id="0865c-138">g\_wszWMDRM\_DRMHeader</span></span>                        | <span data-ttu-id="0865c-139">**\_stringa di tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="0865c-139">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="0865c-140">**\_INDIVIDUALIZEDVERSION DRM**</span><span class="sxs-lookup"><span data-stu-id="0865c-140">**DRM\_IndividualizedVersion**</span></span>](drm-individualizedversion.md)                      | <span data-ttu-id="0865c-141">g \_ wszWMDRM \_ IndividualizedVersion</span><span class="sxs-lookup"><span data-stu-id="0865c-141">g\_wszWMDRM\_IndividualizedVersion</span></span>            | <span data-ttu-id="0865c-142">**\_stringa di tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="0865c-142">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="0865c-143">**\_KEYID DRM**</span><span class="sxs-lookup"><span data-stu-id="0865c-143">**DRM\_KeyID**</span></span>](drm-keyid.md)                                                      | <span data-ttu-id="0865c-144">g \_ wszWMDRM \_ keyId</span><span class="sxs-lookup"><span data-stu-id="0865c-144">g\_wszWMDRM\_KeyID</span></span>                            | <span data-ttu-id="0865c-145">**\_stringa di tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="0865c-145">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="0865c-146">**\_LASIGNATURECERT DRM**</span><span class="sxs-lookup"><span data-stu-id="0865c-146">**DRM\_LASignatureCert**</span></span>](drm-lasignaturecert.md)                                  | <span data-ttu-id="0865c-147">g \_ wszWMDRM \_ LASignatureCert</span><span class="sxs-lookup"><span data-stu-id="0865c-147">g\_wszWMDRM\_LASignatureCert</span></span>                  | <span data-ttu-id="0865c-148">**\_stringa di tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="0865c-148">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="0865c-149">**\_LASIGNATURELICSRVCERT DRM**</span><span class="sxs-lookup"><span data-stu-id="0865c-149">**DRM\_LASignatureLicSrvCert**</span></span>](drm-lasignaturelicsrvcert.md)                      | <span data-ttu-id="0865c-150">g \_ wszWMDRM \_ LASignatureLicSrvCert</span><span class="sxs-lookup"><span data-stu-id="0865c-150">g\_wszWMDRM\_LASignatureLicSrvCert</span></span>            | <span data-ttu-id="0865c-151">**\_stringa di tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="0865c-151">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="0865c-152">**\_LASIGNATUREPRIVKEY DRM**</span><span class="sxs-lookup"><span data-stu-id="0865c-152">**DRM\_LASignaturePrivKey**</span></span>](drm-lasignatureprivkey.md)                            | <span data-ttu-id="0865c-153">g \_ wszWMDRM \_ LASignaturePrivKey</span><span class="sxs-lookup"><span data-stu-id="0865c-153">g\_wszWMDRM\_LASignaturePrivKey</span></span>               | <span data-ttu-id="0865c-154">**\_stringa di tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="0865c-154">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="0865c-155">**\_LASIGNATUREROOTCERT DRM**</span><span class="sxs-lookup"><span data-stu-id="0865c-155">**DRM\_LASignatureRootCert**</span></span>](drm-lasignaturerootcert.md)                          | <span data-ttu-id="0865c-156">g \_ wszWMDRM \_ LASignatureRootCert</span><span class="sxs-lookup"><span data-stu-id="0865c-156">g\_wszWMDRM\_LASignatureRootCert</span></span>              | <span data-ttu-id="0865c-157">**\_stringa di tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="0865c-157">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="0865c-158">**\_LICENSEACQURL DRM**</span><span class="sxs-lookup"><span data-stu-id="0865c-158">**DRM\_LicenseAcqURL**</span></span>](drm-licenseacqurl.md)                                      | <span data-ttu-id="0865c-159">g \_ wszWMDRM \_ LicenseAcqURL</span><span class="sxs-lookup"><span data-stu-id="0865c-159">g\_wszWMDRM\_LicenseAcqURL</span></span>                    | <span data-ttu-id="0865c-160">**\_stringa di tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="0865c-160">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="0865c-161">**\_V1LICENSEACQURL DRM**</span><span class="sxs-lookup"><span data-stu-id="0865c-161">**DRM\_V1LicenseAcqURL**</span></span>](drm-v1licenseacqurl.md)                                  | <span data-ttu-id="0865c-162">g \_ wszWMDRM \_ V1LicenseAcqURL</span><span class="sxs-lookup"><span data-stu-id="0865c-162">g\_wszWMDRM\_V1LicenseAcqURL</span></span>                  | <span data-ttu-id="0865c-163">**\_stringa di tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="0865c-163">**WMT\_TYPE\_STRING**</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="0865c-164">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0865c-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0865c-165">**Attributi per tipo**</span><span class="sxs-lookup"><span data-stu-id="0865c-165">**Attributes By Type**</span></span>](attributes-by-type.md)
</dt> <dt>

[<span data-ttu-id="0865c-166">**Proprietà DRM**</span><span class="sxs-lookup"><span data-stu-id="0865c-166">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




