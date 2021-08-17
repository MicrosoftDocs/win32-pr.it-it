---
title: Attributo WM/GenreID
description: L'attributo WM/GenreID è un identificatore di genere conforme al tag TCON in ID3v2.
ms.assetid: 9b68f9be-1f02-4b14-b052-90657b8800e3
keywords:
- Attributo WM/GenreID Windows Media Player
topic_type:
- apiref
api_name:
- WM/GenreID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52fdb409453bbdc6a30026b5d36cb35bbaeb2a21264e5049c9e5fff520aea08b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118332327"
---
# <a name="wmgenreid-attribute"></a>Attributo WM/GenreID

**L'attributo WM/GenreID** è un identificatore di genere conforme al tag TCON in ID3v2.

## <a name="applies-to"></a>Si applica a

-   [Elementi audio](audio-item-attributes.md)
-   [Attributi di file multimediali Windows comunemente usati](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Commenti

Questo attributo viene archiviato solo nel file multimediale digitale.

ID3 versione 2 è una convenzione di assegnazione di tag originariamente progettata per MP3. Per altre informazioni, vedere il sito [Web dell'organizzazione ID3.](https://id3.org/)

La Windows media format SDK costante per questo attributo è g \_ wszGenreID.

Per determinare se è possibile modificare il valore di questo attributo, usare il [metodo Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player serie 9 Windows Media Player 10 o versione successiva non supporta questo attributo<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento all'attributo**](attribute-reference.md)
</dt> </dl>

 

 





