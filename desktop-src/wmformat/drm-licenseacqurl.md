---
title: DRM_LicenseAcqURL
description: L' \_ attributo LicenseAcqURL di DRM contiene l'indirizzo di una pagina Web a cui l'applicazione client può accedere per ottenere una licenza per il contenuto DRM versione 7.
ms.assetid: bee29e39-ded8-439d-9164-fc318cb535c0
keywords:
- DRM_LicenseAcqURL formato Windows Media
topic_type:
- apiref
api_name:
- DRM_LicenseAcqURL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 231efc4334a4d893b4bdd1e7545bd50b1bed2a5c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104516621"
---
# <a name="drm_licenseacqurl"></a><span data-ttu-id="d9179-104">\_LICENSEACQURL DRM</span><span class="sxs-lookup"><span data-stu-id="d9179-104">DRM\_LicenseAcqURL</span></span>

<span data-ttu-id="d9179-105">L' **attributo \_ LicenseAcqURL di DRM** contiene l'indirizzo di una pagina Web a cui l'applicazione client può accedere per ottenere una licenza per il contenuto DRM versione 7.</span><span class="sxs-lookup"><span data-stu-id="d9179-105">The **DRM\_LicenseAcqURL** attribute contains the address of a Web page that the client application can navigate to in order to obtain a content license for DRM version 7 content.</span></span>

## <a name="global-constant"></a><span data-ttu-id="d9179-106">Costante globale</span><span class="sxs-lookup"><span data-stu-id="d9179-106">Global Constant</span></span>

<span data-ttu-id="d9179-107">g \_ wszWMDRM \_ LicenseAcqURL</span><span class="sxs-lookup"><span data-stu-id="d9179-107">g\_wszWMDRM\_LicenseAcqURL</span></span>

## <a name="data-type"></a><span data-ttu-id="d9179-108">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="d9179-108">Data Type</span></span>

<span data-ttu-id="d9179-109">**\_stringa di tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="d9179-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="d9179-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="d9179-110">Remarks</span></span>

<span data-ttu-id="d9179-111">Questo attributo può essere impostato usando [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) e può essere recuperato con [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span><span class="sxs-lookup"><span data-stu-id="d9179-111">This attribute can be set using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) and it can be retrieved with [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span> <span data-ttu-id="d9179-112">Lo stesso attributo file può essere recuperato usando [**DRM \_ DRMHeader \_ LicenseAcqURL**](drm-drmheader-licenseacqurl.md).</span><span class="sxs-lookup"><span data-stu-id="d9179-112">The same file attribute can be retrieved using [**DRM\_DRMHeader\_LicenseAcqURL**](drm-drmheader-licenseacqurl.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="d9179-113">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d9179-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9179-114">**Elenco degli attributi**</span><span class="sxs-lookup"><span data-stu-id="d9179-114">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




