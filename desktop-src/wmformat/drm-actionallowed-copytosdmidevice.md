---
title: DRM_ActionAllowed_CopyToSDMIDevice
description: L' \_ \_ attributo COPYTOSDMIDEVICE di DRM ActionAllowed indica se il contenuto può essere copiato in un dispositivo SDMI.
ms.assetid: 3ffb9c8f-5640-4ab5-9939-f9525ab960c6
keywords:
- DRM_ActionAllowed_CopyToSDMIDevice formato Windows Media
topic_type:
- apiref
api_name:
- DRM_ActionAllowed_CopyToSDMIDevice
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f61da53fd060bd4fb06dbbb7586d923ac17fc0f
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104398527"
---
# <a name="drm_actionallowed_copytosdmidevice"></a>\_CopyToSDMIDevice ACTIONALLOWED \_ DRM

L' **attributo \_ \_ CopyToSDMIDevice di DRM ActionAllowed** indica se il contenuto può essere copiato in un dispositivo SDMI.

## <a name="global-constant"></a>Costante globale

g \_ wszWMDRM \_ ActionAllowed \_ CopyToSDMIDevice

## <a name="data-type"></a>Tipo di dati

**\_tipo WMT \_ bool**

## <a name="remarks"></a>Commenti

Licenze Windows Media DRM 10 usare l'azione di copia per limitare la copia ai dispositivi. Controllare la proprietà di [**\_ \_ copia DRM ActionAllowed**](drm-actionallowed-copy.md) per determinare se è consentita la copia.

Si tratta di una proprietà di sola lettura che viene recuperata utilizzando [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà DRM**](drm-properties.md)
</dt> </dl>

 

 




