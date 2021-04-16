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
# <a name="drm_licenseacqurl"></a>\_LICENSEACQURL DRM

L' **attributo \_ LicenseAcqURL di DRM** contiene l'indirizzo di una pagina Web a cui l'applicazione client può accedere per ottenere una licenza per il contenuto DRM versione 7.

## <a name="global-constant"></a>Costante globale

g \_ wszWMDRM \_ LicenseAcqURL

## <a name="data-type"></a>Tipo di dati

**\_stringa di tipo WMT \_**

## <a name="remarks"></a>Commenti

Questo attributo può essere impostato usando [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) e può essere recuperato con [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty). Lo stesso attributo file può essere recuperato usando [**DRM \_ DRMHeader \_ LicenseAcqURL**](drm-drmheader-licenseacqurl.md).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elenco degli attributi**](attribute-list.md)
</dt> </dl>

 

 




