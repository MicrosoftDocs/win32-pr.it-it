---
title: Attributo WM/AlbumCoverURL
description: L'attributo WM/AlbumCoverURL è l'URL (Uniform Resource Locator) per la grafica degli album o un'immagine di anteprima.
ms.assetid: 0134867a-7c11-4d50-9ab5-b48c1ca6c473
keywords:
- Attributo WM/AlbumCoverURL Windows Media Player
topic_type:
- apiref
api_name:
- WM/AlbumCoverURL Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce3e3d2948419761a139139493e737df1a9a709147613eadd3e077f0f5101f3a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118332627"
---
# <a name="wmalbumcoverurl-attribute"></a>Attributo WM/AlbumCoverURL

**L'attributo WM/AlbumCoverURL** è l'URL (Uniform Resource Locator) per la grafica degli album o un'immagine di anteprima.

## <a name="applies-to"></a>Si applica a

-   [**Elementi audio**](audio-item-attributes.md)
-   [**Elementi foto**](photo-item-attributes.md)
-   [**Elementi video**](video-item-attributes.md)

## <a name="remarks"></a>Commenti

Per un elemento audio, questo attributo è l'URL della grafica dell'album. Per una foto o un elemento video, questo attributo è l'URL di un'immagine di anteprima.

Questo attributo non è disponibile per gli elementi multimediali nella libreria locale dell'utente corrente. È disponibile solo per gli elementi multimediali che appartengono a una libreria remota. una libreria resa disponibile da un altro utente nella rete domestica. Per determinare se una raccolta multimediale è remota, chiamare il tipo [**IWMPLibrary::get \_**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------|
| Versione<br/> | Windows Media Player 12 o versione successiva.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento all'attributo**](attribute-reference.md)
</dt> </dl>

 

 





