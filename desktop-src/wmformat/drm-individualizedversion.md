---
title: DRM_IndividualizedVersion
description: L'attributo DRM \_ IndividualizedVersion viene archiviato nell'intestazione DRM e contiene la versione minima individualizzata necessaria per accedere al contenuto.
ms.assetid: ed3e165c-c6b0-4eea-be79-a715abd4dd0a
keywords:
- DRM_IndividualizedVersion windows Media Format
topic_type:
- apiref
api_name:
- DRM_IndividualizedVersion
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85d7c9f64a7d4d00e95f8e877e7f33c9e6a8177977eff3b523c25cc1432ac57d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118704683"
---
# <a name="drm_individualizedversion"></a>DRM \_ IndividualizedVersion

**L'attributo DRM \_ IndividualizedVersion** viene archiviato nell'intestazione DRM e contiene la versione minima individualizzata necessaria per accedere al contenuto.

## <a name="global-constant"></a>Costante globale

g \_ wszWMDRM \_ IndividualizedVersion

## <a name="data-type"></a>Tipo di dati

**STRINGA DI TIPO WMT \_ \_**

## <a name="remarks"></a>Commenti

Questo attributo è presente solo con contenuto DRM versione 7. Può essere impostato usando [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) e può essere recuperato con [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty). Lo stesso attributo di file può essere recuperato usando [**DRM \_ DRMHeader \_ IndividualizedVersion.**](drm-drmheader-individualizedversion.md)

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elenco degli attributi**](attribute-list.md)
</dt> </dl>

 

 




