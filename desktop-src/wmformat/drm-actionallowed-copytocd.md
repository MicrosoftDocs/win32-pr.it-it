---
title: DRM_ActionAllowed_CopyToCD
description: L' \_ \_ attributo COPYTOCD di DRM ActionAllowed indica se il contenuto può essere copiato in un CD.
ms.assetid: c650bb2e-6cec-404a-8ece-7a5687cda99f
keywords:
- DRM_ActionAllowed_CopyToCD formato Windows Media
topic_type:
- apiref
api_name:
- DRM_ActionAllowed_CopyToCD
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ba214fb2f067ba523222f92211bf7a9412a1634
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "106299441"
---
# <a name="drm_actionallowed_copytocd"></a>\_CopyToCD ACTIONALLOWED \_ DRM

L' **attributo \_ \_ CopyToCD di DRM ActionAllowed** indica se il contenuto può essere copiato in un CD.

## <a name="global-constant"></a>Costante globale

g \_ wszWMDRM \_ ActionAllowed \_ CopyToCD

## <a name="data-type"></a>Tipo di dati

**\_tipo WMT \_ bool**

## <a name="remarks"></a>Commenti

Licenze Windows Media DRM 10 usare l'azione di copia per limitare la copia su CD. Controllare la proprietà di [**\_ \_ copia DRM ActionAllowed**](drm-actionallowed-copy.md) per determinare se è consentita la copia.

Si tratta di una proprietà di sola lettura che viene recuperata utilizzando [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà DRM**](drm-properties.md)
</dt> </dl>

 

 




