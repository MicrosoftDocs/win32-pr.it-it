---
title: Attributo WM/GenreID
description: L'attributo WM/GenreID è un identificatore di genere conforme al tag TCON in ID3v2.
ms.assetid: 9b68f9be-1f02-4b14-b052-90657b8800e3
keywords:
- Media Player Windows per gli attributi WM/GenreID
topic_type:
- apiref
api_name:
- WM/GenreID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d31e54805f778a51f345c84654056391ec4052e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327014"
---
# <a name="wmgenreid-attribute"></a>Attributo WM/GenreID

L'attributo **WM/GenreID** è un identificatore di genere conforme al tag TCON in id3v2.

## <a name="applies-to"></a>Si applica a

-   [Elementi audio](audio-item-attributes.md)
-   [Attributi di file di Windows Media usati di frequente](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Commenti

Questo attributo viene archiviato solo nel file multimediale digitale.

La versione 2 di ID3 è una convenzione di assegnazione di tag originariamente progettata per il formato MP3. Per ulteriori informazioni, vedere il [sito Web dell'organizzazione ID3](https://id3.org/).

La costante Windows Media Format SDK per questo attributo è g \_ wszGenreID.

Per determinare se è possibile modificare il valore di questo attributo, usare il metodo [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 9 Series Windows Media Player 10 o versioni successive non supporta questo attributo<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento agli attributi**](attribute-reference.md)
</dt> </dl>

 

 





