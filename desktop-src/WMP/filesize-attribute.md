---
title: Attributo Filesize
description: L'attributo Filesize corrisponde alla dimensione del file in byte.
ms.assetid: e845cc82-6975-4fd9-800f-a66f59a5fb39
keywords:
- Finestra degli attributi Filesize Media Player
topic_type:
- apiref
api_name:
- FileSize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cee243d85be59502acead3614dced49494c11104
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328394"
---
# <a name="filesize-attribute"></a>Attributo Filesize

L'attributo **Filesize** corrisponde alla dimensione del file in byte.

## <a name="applies-to"></a>Si applica a

-   [Elementi audio](audio-item-attributes.md)
-   [File di Windows Media usati di frequente](commonly-used-windows-media-file-attributes.md)
-   [Altri elementi](other-item-attributes.md)
-   [Elementi foto](photo-item-attributes.md)
-   [Elementi video](video-item-attributes.md)

## <a name="remarks"></a>Commenti

Questo attributo viene archiviato sia nella libreria che nel file multimediale digitale.

**Size** è un alias per questo attributo.

La costante Windows Media Format SDK per questo attributo è g \_ wszWMFileSize.

Per determinare se è possibile modificare il valore di questo attributo, usare il metodo [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 9 Series o versione successiva (l'elemento Photo è supportato solo in Windows Media Player 10 o versione successiva)<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento agli attributi**](attribute-reference.md)
</dt> </dl>

 

 





