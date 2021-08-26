---
title: Attributo UserRating
description: L'attributo UserRating è la classificazione specificata dall'utente nella libreria.
ms.assetid: 33df5316-1506-4ecb-b729-c2d66b878825
keywords:
- Attributo UserRating Windows Media Player
topic_type:
- apiref
api_name:
- UserRating
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41725119f97e0609931a3c9b7789e86d16a20507523e76a3f5642a0955998d6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001651"
---
# <a name="userrating-attribute"></a>Attributo UserRating

**L'attributo UserRating** è la classificazione specificata dall'utente nella libreria.

## <a name="applies-to"></a>Si applica a

-   [Elementi audio](audio-item-attributes.md)
-   [Altri elementi](other-item-attributes.md)
-   [Elementi foto](photo-item-attributes.md)
-   [Playlist](playlist-attributes-ref.md)
-   [Elementi video](video-item-attributes.md)

## <a name="remarks"></a>Commenti

Le classificazioni utente sono rappresentate da valori interi, come descritto nella tabella seguente. Quando si specifica un valore, usare uno dei valori della colonna Valore di scrittura. Quando si recuperano valori, è possibile usare gli intervalli nella colonna Valori di lettura per determinare il numero di stelle.



| Classificazione  | Valore di scrittura | Lettura dei valori |
|---------|---------------|----------------|
| Unrated | 0             | 0              |
| 1 stella  | 1             | Da 1 a 12        |
| 2 stelle | 25            | Da 13 a 37       |
| 3 stelle | 50            | Da 38 a 62       |
| 4 stelle | 75            | Da 63 a 86       |
| 5 stelle | 99            | Da 87 a 99       |



 

Questo attributo viene archiviato solo nella libreria.

Per determinare se è possibile modificare il valore di questo attributo, usare il [metodo Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player serie 9 o successiva (l'elemento foto è supportato solo in Windows Media Player 10 o versioni successive)<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Informazioni di riferimento su attributi**](attribute-reference.md)
</dt> </dl>

 

 





