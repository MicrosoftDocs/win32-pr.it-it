---
title: DRM_IndividualizedVersion
description: L' \_ attributo DRM IndividualizedVersion viene archiviato nell'intestazione DRM e contiene la versione minima individualizzata richiesta per accedere al contenuto.
ms.assetid: ed3e165c-c6b0-4eea-be79-a715abd4dd0a
keywords:
- DRM_IndividualizedVersion formato Windows Media
topic_type:
- apiref
api_name:
- DRM_IndividualizedVersion
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03ecde48ef3d68e30116cdd7fc8a77179f2282c4
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104336441"
---
# <a name="drm_individualizedversion"></a>\_INDIVIDUALIZEDVERSION DRM

L'attributo **DRM \_ IndividualizedVersion** viene archiviato nell'intestazione DRM e contiene la versione minima individualizzata richiesta per accedere al contenuto.

## <a name="global-constant"></a>Costante globale

g \_ wszWMDRM \_ IndividualizedVersion

## <a name="data-type"></a>Tipo di dati

**\_stringa di tipo WMT \_**

## <a name="remarks"></a>Commenti

Questo attributo è presente solo con contenuto DRM versione 7. Può essere impostato usando [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) e può essere recuperato con [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty). Lo stesso attributo file può essere recuperato usando [**DRM \_ DRMHeader \_ IndividualizedVersion**](drm-drmheader-individualizedversion.md).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elenco degli attributi**](attribute-list.md)
</dt> </dl>

 

 




