---
title: DRM_DRMHeader_ContentDistributor
description: L'attributo \_ DRM DRMHeader \_ ContentDistributor contiene una stringa che identifica il server di distribuzione del contenuto.
ms.assetid: ea9ae7ba-35cc-4e86-995c-9abcdae48f9c
keywords:
- DRM_DRMHeader_ContentDistributor windows Media Format
topic_type:
- apiref
api_name:
- DRM_DRMHeader_ContentDistributor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a82e570c43acbe065ec20e1d7296cff701853591759e9187e2b9329ffed8efe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119586461"
---
# <a name="drm_drmheader_contentdistributor"></a>DRM \_ DRMHeader \_ ContentDistributor

**L'attributo \_ DRM DRMHeader \_ ContentDistributor** contiene una stringa che identifica il server di distribuzione del contenuto.

## <a name="global-constant"></a>Costante globale

g \_ wszWMDRM \_ DRMHeader \_ ContentDistributor

## <a name="data-type"></a>Tipo di dati

**STRINGA DI \_ TIPO \_ WMT**

## <a name="remarks"></a>Commenti

L'ID contenuto è facoltativo ed è determinato esclusivamente dall'autore del contenuto. L'oggetto writer non esegue alcuna operazione con questo attributo. Questo attributo è presente solo con contenuto DRM versione 7. Può essere impostato usando [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) e può essere recuperato con [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elenco degli attributi**](attribute-list.md)
</dt> </dl>

 

 




