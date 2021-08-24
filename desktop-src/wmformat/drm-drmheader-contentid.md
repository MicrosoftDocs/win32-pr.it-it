---
title: DRM_DRMHeader_ContentID
description: L'attributo \_ ContentID DRM DRMHeader \_ contiene il contentID generato dal proprietario del contenuto.
ms.assetid: fda38778-2fdf-4218-aad2-e4cf351d74e9
keywords:
- DRM_DRMHeader_ContentID windows Media Format
topic_type:
- apiref
api_name:
- DRM_DRMHeader_ContentID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b17df75902ec41eed935a9b10dbbf4799c92bae2a54c76b4ed676c9e7a3a572
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119586430"
---
# <a name="drm_drmheader_contentid"></a>DRM \_ DRMHeader \_ ContentID

**L'attributo \_ \_ ContentID DRM DRMHeader** contiene il contentID generato dal proprietario del contenuto.

## <a name="global-constant"></a>Costante globale

g \_ wszWMDRM \_ DRMHeader \_ ContentID

## <a name="data-type"></a>Tipo di dati

**STRINGA DI \_ TIPO \_ WMT**

## <a name="remarks"></a>Commenti

Questo attributo è presente solo con contenuto DRM versione 7. Può essere recuperato con [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty). Per impostare l'ID contenuto nel file [**usando IWMDRMWriter::SetDRMAttribute,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) è necessario usare la [**proprietà \_ ContentID DRM.**](drm-contentid.md)

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elenco degli attributi**](attribute-list.md)
</dt> </dl>

 

 




