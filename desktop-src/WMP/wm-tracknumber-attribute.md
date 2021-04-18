---
title: Attributo WM/numero
description: L'attributo WM/numero è il numero di traccia dell'elemento sull'album in cui è stato rilasciato originariamente.
ms.assetid: d1fc5bac-c440-470f-be5c-5aca74aee99e
keywords:
- Media Player Windows per gli attributi WM/numero
topic_type:
- apiref
api_name:
- WM/TrackNumber
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecd9adf3a939a5087ee270e8bef4d4d510b678ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329701"
---
# <a name="wmtracknumber-attribute"></a>Attributo WM/numero

L'attributo **WM/numero** è il numero di traccia dell'elemento sull'album in cui è stato rilasciato originariamente.

## <a name="applies-to"></a>Si applica a

-   [Elementi audio](audio-item-attributes.md)
-   [Attributi di file di Windows Media usati di frequente](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Commenti

Questo attributo viene archiviato sia nella libreria che nel file multimediale digitale.

I numeri di traccia per un album iniziano da 1.

**OriginalIndex** e **OriginalIndexLeft** sono alias per questo attributo.

La costante Windows Media Format SDK per questo attributo è g \_ wszWMTrackNumber.

Per determinare se è possibile modificare il valore di questo attributo, usare il metodo [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento agli attributi**](attribute-reference.md)
</dt> </dl>

 

 





