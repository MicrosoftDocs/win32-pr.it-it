---
title: DRM_DRMHeader_IndividualizedVersion
description: L'attributo DRMHeaderIndividualizedVersion DRM contiene la versione \_ minima individualizzata necessaria per riprodurre il file.
ms.assetid: 2ac24660-8b7a-4dba-9f9f-ad8b13a22f5c
keywords:
- DRM_DRMHeader_IndividualizedVersion windows Media Format
topic_type:
- apiref
api_name:
- DRM_DRMHeader_IndividualizedVersion
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5793fa81a7c6c57542991d582607edb0cf3e38b62b037ad46974a4211a7ef8ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931181"
---
# <a name="drm_drmheader_individualizedversion"></a>DRM \_ DRMHeader \_ IndividualizedVersion

**L'attributo \_ DRMHeaderIndividualizedVersion DRM** contiene la versione minima individualizzata necessaria per riprodurre il file.

## <a name="global-constant"></a>Costante globale

g \_ wszWMDRM \_ DRMHeader \_ IndividualizedVersion

## <a name="data-type"></a>Tipo di dati

**STRINGA DI \_ TIPO \_ WMT**

## <a name="remarks"></a>Commenti

Questo attributo è presente solo con contenuto DRM versione 7. Può essere recuperato con [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty). Per impostare la versione individualizzata (detta anche versione di sicurezza) nel file usando [**IWMDRMWriter::SetDRMAttribute,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) è necessario usare la [**proprietà \_ DRM IndividualizedVersion.**](drm-individualizedversion.md)

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elenco degli attributi**](attribute-list.md)
</dt> </dl>

 

 




