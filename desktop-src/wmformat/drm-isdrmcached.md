---
title: DRM_IsDRMCached
description: La \_ Proprietà DRM IsDRMCached indica se le informazioni sulla licenza DRM versione 1 sono state archiviate nel computer locale.
ms.assetid: 868e3ada-d608-41d6-93d7-0b7930cbf2f9
keywords:
- DRM_IsDRMCached formato Windows Media
topic_type:
- apiref
api_name:
- DRM_IsDRMCached
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 185a8b2c94ca5ec517eb1a781262e3f988001a01
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "106299447"
---
# <a name="drm_isdrmcached"></a>\_ISDRMCACHED DRM

La proprietà **DRM \_ IsDRMCached** indica se le informazioni sulla licenza DRM versione 1 sono state archiviate nel computer locale.

## <a name="global-constant"></a>Costante globale

g \_ wszWMDRM \_ IsDRMCached

## <a name="data-type"></a>Tipo di dati

**\_tipo WMT \_ bool**

## <a name="remarks"></a>Commenti

Si tratta di una proprietà di sola lettura che viene recuperata utilizzando [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty). È **vero** quando l'URL di acquisizione della licenza corrisponde a uno dei due URL di conoscenza usati per l'acquisizione della licenza locale in DRM versione 1.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà DRM**](drm-properties.md)
</dt> </dl>

 

 




