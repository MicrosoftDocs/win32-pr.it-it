---
title: Attributo WM/AlbumCoverURL
description: L'attributo WM/AlbumCoverURL è l'URL (Uniform Resource Locator) per l'immagine dell'album o un'anteprima.
ms.assetid: 0134867a-7c11-4d50-9ab5-b48c1ca6c473
keywords:
- Media Player Windows per gli attributi WM/AlbumCoverURL
topic_type:
- apiref
api_name:
- WM/AlbumCoverURL Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6939c5451f3ae8f41214a817293e3c7f3cb3b66c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327038"
---
# <a name="wmalbumcoverurl-attribute"></a>Attributo WM/AlbumCoverURL

L'attributo **WM/AlbumCoverURL** è l'URL (Uniform Resource Locator) per l'immagine dell'album o un'anteprima.

## <a name="applies-to"></a>Si applica a

-   [**Elementi audio**](audio-item-attributes.md)
-   [**Elementi foto**](photo-item-attributes.md)
-   [**Elementi video**](video-item-attributes.md)

## <a name="remarks"></a>Commenti

Per un elemento audio, questo attributo è l'URL dell'immagine dell'album. Per un elemento Photo o video, questo attributo è l'URL di un'immagine di anteprima.

Questo attributo non è disponibile per gli elementi multimediali nella libreria locale dell'utente corrente. È disponibile solo per gli elementi multimediali che appartengono a una libreria remota; ovvero una libreria che è stata resa disponibile da un altro utente nella rete domestica. Per determinare se un catalogo multimediale è remoto, chiamare [**IWMPLibrary:: Get \_ Type**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------|
| Versione<br/> | Windows Media Player 12 o versione successiva.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento agli attributi**](attribute-reference.md)
</dt> </dl>

 

 





