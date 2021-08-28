---
title: DRM_IsDRMCached
description: La proprietà \_ DRM IsDRMCached indica se le informazioni sulla licenza DRM versione 1 sono state archiviate nel computer locale.
ms.assetid: 868e3ada-d608-41d6-93d7-0b7930cbf2f9
keywords:
- DRM_IsDRMCached windows Media Format
topic_type:
- apiref
api_name:
- DRM_IsDRMCached
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9b5bbcf7e4e1c11c8ae992156b7541ac66c7a9d43f2cb1d52878d1ee6762d6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119709041"
---
# <a name="drm_isdrmcached"></a>DRM \_ IsDRMCached

La **proprietà \_ DRM IsDRMCached** indica se le informazioni sulla licenza DRM versione 1 sono state archiviate nel computer locale.

## <a name="global-constant"></a>Costante globale

g \_ wszWMDRM \_ IsDRMCached

## <a name="data-type"></a>Tipo di dati

**TIPO WMT \_ \_ BOOL**

## <a name="remarks"></a>Commenti

Si tratta di una proprietà di sola lettura recuperata tramite [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty). È TRUE **quando** l'URL di acquisizione della licenza corrisponde a uno dei due URL know usati per l'acquisizione della licenza locale in DRM versione 1.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà DRM**](drm-properties.md)
</dt> </dl>

 

 




