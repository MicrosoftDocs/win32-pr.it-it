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
# <a name="drm_drmheader_licenseacqurl"></a>\_LicenseAcqURL DRMHEADER \_ DRM

L'attributo **DRM \_ DRMHeader \_ LICENSEACQURL** contiene l'URL di acquisizione della licenza per una licenza DRM versione 7.

## <a name="global-constant"></a>Costante globale

g \_ wszWMDRM \_ DRMHeader \_ LicenseAcqURL

## <a name="data-type"></a>Tipo di dati

**\_stringa di tipo WMT \_**

## <a name="remarks"></a>Commenti

Questo attributo è presente solo con contenuto DRM versione 7. Può essere recuperato con [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty). Per impostare l'URL di acquisizione della licenza nel file usando [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) , è necessario usare la proprietà [**DRM \_ LicenseAcqURL**](drm-licenseacqurl.md) .

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elenco degli attributi**](attribute-list.md)
</dt> </dl>

 

 




