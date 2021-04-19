---
title: Attributo IsVBR
description: L'attributo IsVBR indica se il contenuto è stato codificato tramite la codifica con velocità in bit variabile (VBR).
ms.assetid: faec0940-ef53-40a1-be54-a990884e907d
keywords:
- Attributo IsVBR Windows Media Player
topic_type:
- apiref
api_name:
- IsVBR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eaec9f740e7b251c73ed12f5897ff9d95b023886
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328715"
---
# <a name="isvbr-attribute"></a>Attributo IsVBR

L'attributo **IsVBR** indica se il contenuto è stato codificato tramite la codifica con velocità in bit variabile (VBR).

## <a name="applies-to"></a>Si applica a

-   [File di Windows Media usati di frequente](commonly-used-windows-media-file-attributes.md)
-   [Elementi video](video-item-attributes.md)

## <a name="remarks"></a>Commenti

Questo attributo viene archiviato solo nel file multimediale digitale.

La costante Windows Media Format SDK per questo attributo è g \_ wszWMIsVBR.

Per determinare se è possibile modificare il valore di questo attributo, usare il metodo [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento agli attributi**](attribute-reference.md)
</dt> </dl>

 

 





