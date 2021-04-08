---
title: DRM_ActionAllowed_CopyToNonSDMIDevice
description: L' \_ \_ attributo COPYTONONSDMIDEVICE di DRM ActionAllowed indica se il contenuto può essere copiato in un dispositivo non SDMI.
ms.assetid: 517ceeb5-4979-4667-ba54-8b9b1c6069f2
keywords:
- DRM_ActionAllowed_CopyToNonSDMIDevice formato Windows Media
topic_type:
- apiref
api_name:
- DRM_ActionAllowed_CopyToNonSDMIDevice
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8043c6384fbe0ce57ba56fc9799810d7b6a126b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104046336"
---
# <a name="drm_actionallowed_copytononsdmidevice"></a>\_CopyToNonSDMIDevice ACTIONALLOWED \_ DRM

L' **attributo \_ \_ CopyToNonSDMIDevice di DRM ActionAllowed** indica se il contenuto può essere copiato in un dispositivo non SDMI

## <a name="global-constant"></a>Costante globale

g \_ wszWMDRM \_ ActionAllowed \_ CopyToNonSDMIDevice

## <a name="data-type"></a>Tipo di dati

**\_tipo WMT \_ bool**

## <a name="remarks"></a>Commenti

Licenze Windows Media DRM 10 usare l'azione di copia per limitare la copia ai dispositivi. Controllare la proprietà di [**\_ \_ copia DRM ActionAllowed**](drm-actionallowed-copy.md) per determinare se è consentita la copia.

Si tratta di una proprietà di sola lettura che viene recuperata utilizzando [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà DRM**](drm-properties.md)
</dt> </dl>

 

 




