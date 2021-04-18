---
title: Attributo AlbumID
description: L'attributo AlbumID è un identificatore univoco per l'album.
ms.assetid: 0412d91a-11a7-434c-8717-a71d85655679
keywords:
- Attributo AlbumID Windows Media Player
topic_type:
- apiref
api_name:
- AlbumID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 339253c82554579fa549371e2ebe4cb2f1926cc5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333774"
---
# <a name="albumid-attribute"></a>Attributo AlbumID

L'attributo **AlbumID** è un identificatore univoco per l'album.

## <a name="applies-to"></a>Si applica a

-   [Elementi audio](audio-item-attributes.md)

## <a name="remarks"></a>Commenti

Questo attributo viene archiviato solo nella libreria.

L'identificatore univoco è una combinazione del titolo dell'album e del nome dell'artista dell'album. In questo attributo, il titolo dell'album viene visualizzato per primo. Quando si utilizza il metodo [mediacollection. getAttributeStringCollection](mediacollection-getattributestringcollection.md) per ottenere un oggetto **StringCollection** utilizzando questo attributo, i valori vengono ordinati in base al titolo dell'album.

Per determinare se è possibile modificare il valore di questo attributo, usare il metodo [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Attributo AlbumIDAlbumArtist**](albumidalbumartist-attribute.md)
</dt> <dt>

[**Riferimento agli attributi**](attribute-reference.md)
</dt> </dl>

 

 





