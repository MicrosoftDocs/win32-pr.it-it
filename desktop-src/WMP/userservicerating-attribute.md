---
title: Attributo UserServiceRating
description: L'attributo UserServiceRating è riservato per un utilizzo futuro.
ms.assetid: e6113474-725d-4eb1-9c05-cff7749f2010
keywords:
- Attributo UserServiceRating Windows Media Player
topic_type:
- apiref
api_name:
- UserServiceRating
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 690a090aaa9d07ee850caee004242272368129f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324081"
---
# <a name="userservicerating-attribute"></a>Attributo UserServiceRating

L'attributo **UserServiceRating** è riservato per un utilizzo futuro.

## <a name="applies-to"></a>Si applica a

-   [Elementi audio](audio-item-attributes.md)
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
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento agli attributi**](attribute-reference.md)
</dt> </dl>

 

 





