---
title: DRM_DRMHeader_IndividualizedVersion
description: L' \_ attributo DRMHeaderIndividualizedVersion di DRM contiene la versione minima individualizzata richiesta per riprodurre il file.
ms.assetid: 2ac24660-8b7a-4dba-9f9f-ad8b13a22f5c
keywords:
- DRM_DRMHeader_IndividualizedVersion formato Windows Media
topic_type:
- apiref
api_name:
- DRM_DRMHeader_IndividualizedVersion
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 167065f99a72245c6d7cc677ce24fa1ff96dec84
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "106299405"
---
# <a name="drm_drmheader_individualizedversion"></a>\_IndividualizedVersion DRMHEADER \_ DRM

L' **attributo \_ DRMHeaderIndividualizedVersion di DRM** contiene la versione minima individualizzata richiesta per riprodurre il file.

## <a name="global-constant"></a>Costante globale

g \_ wszWMDRM \_ DRMHeader \_ IndividualizedVersion

## <a name="data-type"></a>Tipo di dati

**\_stringa di tipo WMT \_**

## <a name="remarks"></a>Commenti

Questo attributo è presente solo con contenuto DRM versione 7. Può essere recuperato con [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty). Per impostare la versione individualizzata (detta anche versione di sicurezza) del file usando [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) , è necessario usare la proprietà [**DRM \_ IndividualizedVersion**](drm-individualizedversion.md) .

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elenco degli attributi**](attribute-list.md)
</dt> </dl>

 

 




