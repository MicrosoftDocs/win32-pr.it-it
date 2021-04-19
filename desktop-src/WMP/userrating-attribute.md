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
ms.openlocfilehash: 4a25dd7b4e55195deaecf5228b9ad5bad9195c2c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324083"
---
# <a name="userrating-attribute"></a>Attributo UserRating

L'attributo **UserRating** è la classificazione specificata dall'utente nella libreria.

## <a name="applies-to"></a>Si applica a

-   [Elementi audio](audio-item-attributes.md)
-   [Altri elementi](other-item-attributes.md)
-   [Elementi foto](photo-item-attributes.md)
-   [Playlist](playlist-attributes-ref.md)
-   [Elementi video](video-item-attributes.md)

## <a name="remarks"></a>Commenti

Le classificazioni utente sono rappresentate da valori integer, come descritto nella tabella seguente. Quando si specifica un valore, usare uno dei valori della colonna valore di scrittura. Quando si recuperano i valori, è possibile utilizzare gli intervalli nella colonna valori di lettura per determinare il numero di stelle.



| Classificazione  | Valore di scrittura | Lettura di valori |
|---------|---------------|----------------|
| Senza classificazione | 0             | 0              |
| 1 stella  | 1             | Da 1 a 12        |
| 2 stelle | 25            | da 13 a 37       |
| 3 stelle | 50            | da 38 a 62       |
| 4 stelle | 75            | da 63 a 86       |
| 5 stelle | 99            | da 87 a 99       |



 

Questo attributo viene archiviato solo nella libreria.

Per determinare se è possibile modificare il valore di questo attributo, usare il metodo [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 9 Series o versione successiva (l'elemento Photo è supportato solo in Windows Media Player 10 o versione successiva)<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento agli attributi**](attribute-reference.md)
</dt> </dl>

 

 





