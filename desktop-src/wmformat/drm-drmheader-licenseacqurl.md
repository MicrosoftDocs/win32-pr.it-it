---
title: DRM_DRMHeader_LicenseAcqURL
description: L' \_ attributo DRM DRMHeader \_ LicenseAcqURL contiene l'URL di acquisizione della licenza per una licenza DRM versione 7.
ms.assetid: 00c788b4-b291-4df5-9926-0badc7357faf
keywords:
- DRM_DRMHeader_LicenseAcqURL formato Windows Media
topic_type:
- apiref
api_name:
- DRM_DRMHeader_LicenseAcqURL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c394df01703befbb17c61b340b8ea4239740ac3
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104046304"
---
# <a name="drm_drmheader_licenseacqurl"></a><span data-ttu-id="a6d68-104">\_LicenseAcqURL DRMHEADER \_ DRM</span><span class="sxs-lookup"><span data-stu-id="a6d68-104">DRM\_DRMHeader\_LicenseAcqURL</span></span>

<span data-ttu-id="a6d68-105">L'attributo **DRM \_ DRMHeader \_ LICENSEACQURL** contiene l'URL di acquisizione della licenza per una licenza DRM versione 7.</span><span class="sxs-lookup"><span data-stu-id="a6d68-105">The **DRM\_DRMHeader\_LicenseAcqURL** attribute contains the license acquisition URL for a DRM version 7 license.</span></span>

## <a name="global-constant"></a><span data-ttu-id="a6d68-106">Costante globale</span><span class="sxs-lookup"><span data-stu-id="a6d68-106">Global Constant</span></span>

<span data-ttu-id="a6d68-107">g \_ wszWMDRM \_ DRMHeader \_ LicenseAcqURL</span><span class="sxs-lookup"><span data-stu-id="a6d68-107">g\_wszWMDRM\_DRMHeader\_LicenseAcqURL</span></span>

## <a name="data-type"></a><span data-ttu-id="a6d68-108">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="a6d68-108">Data Type</span></span>

<span data-ttu-id="a6d68-109">**\_stringa di tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="a6d68-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="a6d68-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="a6d68-110">Remarks</span></span>

<span data-ttu-id="a6d68-111">Questo attributo è presente solo con contenuto DRM versione 7.</span><span class="sxs-lookup"><span data-stu-id="a6d68-111">This attribute is present with DRM Version 7 content only.</span></span> <span data-ttu-id="a6d68-112">Può essere recuperato con [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span><span class="sxs-lookup"><span data-stu-id="a6d68-112">It can be retrieved with [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span> <span data-ttu-id="a6d68-113">Per impostare l'URL di acquisizione della licenza nel file usando [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) , è necessario usare la proprietà [**DRM \_ LicenseAcqURL**](drm-licenseacqurl.md) .</span><span class="sxs-lookup"><span data-stu-id="a6d68-113">To set the license acquisition URL on the file using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) you must use the [**DRM\_LicenseAcqURL**](drm-licenseacqurl.md) property.</span></span>

## <a name="see-also"></a><span data-ttu-id="a6d68-114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a6d68-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6d68-115">**Elenco degli attributi**</span><span class="sxs-lookup"><span data-stu-id="a6d68-115">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




