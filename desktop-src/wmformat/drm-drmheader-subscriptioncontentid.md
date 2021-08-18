---
title: DRM_DRMHeader_SubscriptionContentID
description: L'attributo \_ DRM DRMHeader \_ SubscriptionContentID contiene l'ID contenuto della sottoscrizione.
ms.assetid: e582d841-4865-40d3-889e-847d3aac0a7c
keywords:
- DRM_DRMHeader_SubscriptionContentID windows Media Format
topic_type:
- apiref
api_name:
- DRM_DRMHeader_SubscriptionContentID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2b273cf95d2bbb271b055eeff3da80a788a38c88bb2e87db37f5a73e6e918e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086151"
---
# <a name="drm_drmheader_subscriptioncontentid"></a>DRM \_ DRMHeader \_ SubscriptionContentID

**L'attributo \_ DRM DRMHeader \_ SubscriptionContentID** contiene l'ID contenuto della sottoscrizione.

## <a name="global-constant"></a>Costante globale

g \_ wszWMDRM \_ DRMHeader \_ SubscriptionContentID

## <a name="data-type"></a>Tipo di dati

**STRINGA DI TIPO WMT \_ \_**

## <a name="remarks"></a>Commenti

Questo attributo è presente solo con contenuto DRM versione 7. L'ID contenuto della sottoscrizione è facoltativo ed è determinato esclusivamente dall'autore del contenuto. L'oggetto writer non esegue alcuna operazione con questo attributo. Può essere impostato usando [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) e può essere recuperato con [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elenco degli attributi**](attribute-list.md)
</dt> </dl>

 

 




