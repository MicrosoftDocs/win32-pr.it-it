---
title: AmbientAttributes.nineGridMargins
description: L'attributo nineGridMargins specifica le larghezze dei margini per il ridimensionamento non uniforme dell'elemento Skin.
ms.assetid: b8a7efd0-6c12-4436-9d53-0dcfa1600aa5
keywords:
- Media Player Windows AmbientAttributes. nineGridMargins
topic_type:
- apiref
api_name:
- AmbientAttributes.nineGridMargins
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3cf77c1fcfdb64fb9e4b0dde8753572255c17eda
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326030"
---
# <a name="ambientattributesninegridmargins"></a>AmbientAttributes.nineGridMargins

L'attributo **nineGridMargins** specifica le larghezze dei margini per il ridimensionamento non uniforme dell'elemento Skin.

``` syntax
        elementID.nineGridMargins
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una **stringa** di lettura/scrittura che contiene le larghezze dei margini nel formato "*widthLeft*,*widthTop*,*widthRight*,*widthBottom*". Ogni valore di larghezza è un numero che rappresenta la larghezza, in pixel, di un margine per la nove griglia.

## <a name="remarks"></a>Commenti

Un *nove griglia* è una tecnica utilizzata per dividere gli elementi dell'interfaccia utente in nove aree rettangolari disposte in una matrice 3 per 3. Quando un elemento viene ridimensionato, le nove aree della griglia possono essere ridimensionate in base a un fattore diverso.

Ognuno dei quattro valori di larghezza specificati rappresenta la larghezza di una riga o di una colonna di tre aree adiacenti. Ogni riga o colonna costituisce il lato sinistro, superiore, destro o inferiore della griglia nove.

Per il funzionamento di questo attributo, [AmbientAttributes. resizeImages](ambientattributes-resizeimages.md) deve essere impostato su true.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------|
| Versione<br/> | Windows Media Player 11<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Attributi di ambiente**](ambient-attributes.md)
</dt> </dl>

 

 





