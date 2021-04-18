---
title: Attributo WM/Year
description: L'attributo WM/Year è l'anno in cui è stato pubblicato il contenuto.
ms.assetid: b64e37f1-6f12-43a6-8a66-7d61b470853c
keywords:
- Media Player di Windows per gli attributi WM/Year
topic_type:
- apiref
api_name:
- WM/Year
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10bf10d4e905e10c74cfaf9986445ce9a68dc9b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329679"
---
# <a name="wmyear-attribute"></a>Attributo WM/Year

L'attributo **WM/Year** è l'anno in cui è stato pubblicato il contenuto.

## <a name="applies-to"></a>Si applica a

-   [Elementi audio](audio-item-attributes.md)
-   [Attributi di file di Windows Media usati di frequente](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Commenti

Questo attributo viene archiviato solo nel file multimediale digitale.

Per determinare se è possibile modificare il valore di questo attributo, usare il metodo [Media. isReadOnlyItem](media-isreadonlyitem.md) .

Questo attributo non deve essere utilizzato come parte di una condizione di query. È derivato da un altro attributo e non può essere sottoposto a query direttamente in una raccolta di supporti.

La costante Windows Media Format SDK per questo attributo è g \_ wszWMYear.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 9 Series Windows Media Player 10 o versioni successive non supporta questo attributo<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento agli attributi**](attribute-reference.md)
</dt> </dl>

 

 





