---
title: DRM_DRMHeader_ContentID
description: L' \_ \_ attributo CONTENTID di DRM DRMHeader contiene il ContentId generato dal proprietario del contenuto.
ms.assetid: fda38778-2fdf-4218-aad2-e4cf351d74e9
keywords:
- DRM_DRMHeader_ContentID formato Windows Media
topic_type:
- apiref
api_name:
- DRM_DRMHeader_ContentID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e66edd858451e5d1a58b2a91f9f2362d4cabe9da
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103956187"
---
# <a name="drm_drmheader_contentid"></a>\_ContentID DRMHEADER \_ DRM

L' **attributo \_ \_ ContentID di DRM DRMHeader** contiene il ContentId generato dal proprietario del contenuto.

## <a name="global-constant"></a>Costante globale

g \_ wszWMDRM \_ DRMHeader \_ ContentID

## <a name="data-type"></a>Tipo di dati

**\_stringa di tipo WMT \_**

## <a name="remarks"></a>Commenti

Questo attributo è presente solo con contenuto DRM versione 7. Può essere recuperato con [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty). Per impostare l'ID contenuto nel file usando [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) è necessario usare la proprietà [**DRM \_ ContentID**](drm-contentid.md) .

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elenco degli attributi**](attribute-list.md)
</dt> </dl>

 

 




