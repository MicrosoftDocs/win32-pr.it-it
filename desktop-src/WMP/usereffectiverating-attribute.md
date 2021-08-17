---
title: Attributo UserEffectiveRating
description: L'attributo UserEffectiveRating è la classificazione calcolata Windows Media Player in base alla frequenza di riproduzione dell'elemento.
ms.assetid: 6a420e20-f61d-4e15-84f8-a738caabd1d7
keywords:
- Attributo UserEffectiveRating Windows Media Player
topic_type:
- apiref
api_name:
- UserEffectiveRating
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25e3244d793288fe1535c7e7cb4d44c05a3b71404531cf2ae344eb77528dd4a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134444"
---
# <a name="usereffectiverating-attribute"></a>Attributo UserEffectiveRating

**L'attributo UserEffectiveRating** è la classificazione calcolata Windows Media Player in base alla frequenza di riproduzione dell'elemento.

## <a name="applies-to"></a>Si applica a

-   [Elementi audio](audio-item-attributes.md)
-   [Altri elementi](other-item-attributes.md)
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
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player serie 9 o successive<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Informazioni di riferimento su attributi**](attribute-reference.md)
</dt> </dl>

 

 





