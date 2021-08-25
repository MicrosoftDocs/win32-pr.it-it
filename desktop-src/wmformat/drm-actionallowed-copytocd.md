---
title: DRM_ActionAllowed_CopyToCD
description: L'attributo DRM \_ ActionAllowed CopyToCD indica se il contenuto \_ può essere copiato in un CD.
ms.assetid: c650bb2e-6cec-404a-8ece-7a5687cda99f
keywords:
- DRM_ActionAllowed_CopyToCD windows Media Format
topic_type:
- apiref
api_name:
- DRM_ActionAllowed_CopyToCD
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 852d44a4c812aed0d2f188b5ab18e9b74a1813bd9605bf348ca23b96b72f7d2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809411"
---
# <a name="drm_actionallowed_copytocd"></a>Azione \_ DRMAllowed \_ CopyToCD

**L'attributo DRM \_ ActionAllowed \_ CopyToCD** indica se il contenuto può essere copiato in un CD.

## <a name="global-constant"></a>Costante globale

g \_ wszWMDRM \_ ActionAllowed \_ CopyToCD

## <a name="data-type"></a>Tipo di dati

**TIPO WMT \_ \_ BOOL**

## <a name="remarks"></a>Commenti

Windows Le licenze DRM 10 multimediali usano l'azione Copia per limitare la copia su CD. È necessario controllare la [**proprietà DRM \_ ActionAllowed \_ Copy**](drm-actionallowed-copy.md) per determinare se la copia è consentita.

Si tratta di una proprietà di sola lettura recuperata tramite [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà DRM**](drm-properties.md)
</dt> </dl>

 

 




