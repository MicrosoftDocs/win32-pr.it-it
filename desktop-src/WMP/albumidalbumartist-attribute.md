---
title: Attributo AlbumIDAlbumArtist
description: L'attributo AlbumIDAlbumArtist è un identificatore univoco per l'album.
ms.assetid: beaa8d01-1722-4545-8705-6b3d130113b1
keywords:
- Attributo AlbumIDAlbumArtist Windows Media Player
topic_type:
- apiref
api_name:
- AlbumIDAlbumArtist
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4905f0448c7e08abe308a57b1ad08020d47563847db1aa32744c0de3279cdcdb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055389"
---
# <a name="albumidalbumartist-attribute"></a>Attributo AlbumIDAlbumArtist

**L'attributo AlbumIDAlbumArtist** è un identificatore univoco per l'album.

## <a name="applies-to"></a>Si applica a

-   [Elementi audio](audio-item-attributes.md)

## <a name="remarks"></a>Commenti

Questo attributo viene archiviato solo nella libreria .

L'identificatore univoco è una combinazione del titolo dell'album e del nome dell'artista dell'album. In questo attributo il nome dell'artista dell'album viene fornito per primo. Quando si usa il [metodo MediaCollection.getAttributeStringCollection](mediacollection-getattributestringcollection.md) per ottenere un oggetto **StringCollection** usando questo attributo, i valori vengono ordinati in base al nome dell'artista dell'album.

Per determinare se è possibile modificare il valore di questo attributo, usare il [metodo Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player serie 9 o successive<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Attributo AlbumID**](albumid-attribute.md)
</dt> <dt>

[**Riferimento all'attributo**](attribute-reference.md)
</dt> </dl>

 

 





