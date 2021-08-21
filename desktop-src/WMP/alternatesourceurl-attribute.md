---
title: Attributo AlternateSourceURL
description: L'attributo AlternateSourceURL è un localizzatore di risorse uniformi per l'elemento multimediale che funge da alternativa agli attributi DLNASourceURI e SourceURL.
ms.assetid: 2be88d9b-4fd8-4e70-9a4d-114a2bf8b23c
keywords:
- Attributo AlternateSourceURL Windows Media Player
topic_type:
- apiref
api_name:
- AlternateSourceURL Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 765c7a3945224e82a0112c0f4dd7249e4340ec13e0d78adbd59039d25f234aaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055239"
---
# <a name="alternatesourceurl-attribute"></a>Attributo AlternateSourceURL

**L'attributo AlternateSourceURL** è un localizzatore di risorse uniformi per l'elemento multimediale che funge da alternativa agli attributi [**DLNASourceURI**](dlnasourceuri-attribute.md) [**e SourceURL.**](sourceurl-attribute.md)

## <a name="applies-to"></a>Si applica a

-   [**Elementi audio**](audio-item-attributes.md)
-   [**Elementi foto**](photo-item-attributes.md)
-   [**Elementi playlist**](playlist-attributes-ref.md)
-   [**Elementi video**](video-item-attributes.md)

## <a name="remarks"></a>Commenti

Questo attributo non è disponibile per gli elementi multimediali nella libreria locale dell'utente corrente. È disponibile solo per gli elementi multimediali che appartengono a una libreria remota. una libreria resa disponibile da un altro utente nella rete domestica. Per determinare se una raccolta multimediale è remota, chiamare il tipo [**IWMPLibrary::get \_**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------|
| Versione<br/> | Windows Media Player 12<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento all'attributo**](attribute-reference.md)
</dt> </dl>

 

 





