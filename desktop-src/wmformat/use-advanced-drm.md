---
title: Use_Advanced_DRM
description: L' \_ attributo use Advanced \_ DRM specifica se il DRM versione 7 viene usato per proteggere il contenuto.
ms.assetid: a385152f-d72e-473c-93a0-5697659df23c
keywords:
- Use_Advanced_DRM formato Windows Media
topic_type:
- apiref
api_name:
- Use_Advanced_DRM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8720d5b401a1a1cec5240920bfb4a3811012420
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104223393"
---
# <a name="use_advanced_drm"></a>USA \_ \_ DRM avanzato

L'attributo **use \_ Advanced \_ DRM** specifica se il DRM versione 7 viene usato per proteggere il contenuto.

## <a name="global-constant"></a>Costante globale

g \_ wszWMUse \_ Advanced \_ DRM

## <a name="data-type"></a>Tipo di dati

**\_tipo WMT \_ bool**

## <a name="remarks"></a>Commenti

Si tratta di una proprietà di lettura/scrittura che viene recuperata utilizzando [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty) e impostata utilizzando [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute). Questa proprietà non è accessibile dall'oggetto Reader.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà DRM**](drm-properties.md)
</dt> </dl>

 

 




