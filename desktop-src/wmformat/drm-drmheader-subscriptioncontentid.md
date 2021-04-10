---
title: DRM_DRMHeader_SubscriptionContentID
description: L' \_ attributo DRM DRMHeader \_ SubscriptionContentID contiene l'ID contenuto della sottoscrizione.
ms.assetid: e582d841-4865-40d3-889e-847d3aac0a7c
keywords:
- DRM_DRMHeader_SubscriptionContentID formato Windows Media
topic_type:
- apiref
api_name:
- DRM_DRMHeader_SubscriptionContentID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 151665777aa6b68078361eb6e063e374a52f30bf
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103956186"
---
# <a name="drm_drmheader_subscriptioncontentid"></a>\_SubscriptionContentID DRMHEADER \_ DRM

L'attributo **DRM \_ DRMHeader \_ SUBSCRIPTIONCONTENTID** contiene l'ID contenuto della sottoscrizione.

## <a name="global-constant"></a>Costante globale

g \_ wszWMDRM \_ DRMHeader \_ SubscriptionContentID

## <a name="data-type"></a>Tipo di dati

**\_stringa di tipo WMT \_**

## <a name="remarks"></a>Commenti

Questo attributo è presente solo con contenuto DRM versione 7. L'ID contenuto della sottoscrizione è facoltativo e viene determinato esclusivamente dall'autore del contenuto. L'oggetto writer non esegue alcuna operazione con questo attributo. Può essere impostato usando [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) e può essere recuperato con [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elenco degli attributi**](attribute-list.md)
</dt> </dl>

 

 




