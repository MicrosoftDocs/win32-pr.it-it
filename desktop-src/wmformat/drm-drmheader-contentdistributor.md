---
title: DRM_DRMHeader_ContentDistributor
description: L' \_ attributo contentdistributor di DRM DRMHeader \_ contiene una stringa identifiying il server di distribuzione del contenuto.
ms.assetid: ea9ae7ba-35cc-4e86-995c-9abcdae48f9c
keywords:
- DRM_DRMHeader_ContentDistributor formato Windows Media
topic_type:
- apiref
api_name:
- DRM_DRMHeader_ContentDistributor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2494f80e612e03f9d25372d38e875c1df814fd7d
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "106299449"
---
# <a name="drm_drmheader_contentdistributor"></a>\_Contentdistributor DRMHEADER \_ DRM

L' **attributo \_ \_ contentdistributor di DRM DRMHeader** contiene una stringa identifiying il server di distribuzione del contenuto.

## <a name="global-constant"></a>Costante globale

g \_ wszWMDRM \_ DRMHeader \_ contentdistributor

## <a name="data-type"></a>Tipo di dati

**\_stringa di tipo WMT \_**

## <a name="remarks"></a>Commenti

L'ID contenuto è facoltativo e viene determinato esclusivamente dall'autore del contenuto. L'oggetto writer non esegue alcuna operazione con questo attributo. Questo attributo è presente solo con contenuto DRM versione 7. Può essere impostato usando [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) e può essere recuperato con [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elenco degli attributi**](attribute-list.md)
</dt> </dl>

 

 




