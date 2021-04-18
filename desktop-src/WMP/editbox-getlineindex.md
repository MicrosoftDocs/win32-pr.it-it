---
title: CASELLA. getLineIndex
description: Il metodo getLineIndex recupera l'indice dei caratteri del primo carattere nella riga con l'indice di riga specificato.
ms.assetid: 1298227a-d839-44fc-bacb-44c3c968bd94
keywords:
- Media Player Windows casella. getLineIndex
topic_type:
- apiref
api_name:
- EDITBOX.getLineIndex
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5f55027bb7d577b7080ad2f006a5a006e718c2d5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333853"
---
# <a name="editboxgetlineindex"></a>CASELLA. getLineIndex

Il metodo **getLineIndex** recupera l'indice dei caratteri del primo carattere nella riga con l'indice di riga specificato.

``` syntax
        elementID.getLineIndex(index)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="index"></span><span id="INDEX"></span>*Indice*
</dt> <dd>

**Numero** (**Long**) che contiene l'indice della riga di cui deve essere recuperato l'indice dei caratteri.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un **numero** (**Long**).

## <a name="remarks"></a>Commenti

Se l'indice di riga specificato è 1, viene utilizzata la riga contenente il punto di inserimento.

Questo metodo può essere chiamato solo dopo che il controllo diventa visibile.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------|
| Versione<br/> | Windows Media Player per Windows XP o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento casella**](editbox-element.md)
</dt> <dt>

[**CASELLA. getline**](editbox-getline.md)
</dt> <dt>

[**CASELLA. getLineFromChar**](editbox-getlinefromchar.md)
</dt> </dl>

 

 





