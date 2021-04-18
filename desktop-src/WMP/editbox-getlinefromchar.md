---
title: CASELLA. getLineFromChar
description: Il metodo getLineFromChar recupera l'indice di riga per l'indice dei caratteri specificato.
ms.assetid: c3a29bdf-ff63-4b6d-90e8-d414dde87f85
keywords:
- Media Player Windows casella. getLineFromChar
topic_type:
- apiref
api_name:
- EDITBOX.getLineFromChar
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3462ce628da72ca1e55df79e408fc79e0ec8b63a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333852"
---
# <a name="editboxgetlinefromchar"></a>CASELLA. getLineFromChar

Il metodo **getLineFromChar** recupera l'indice di riga per l'indice dei caratteri specificato.

``` syntax
        elementID.getLineFromChar(index)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="index"></span><span id="INDEX"></span>*Indice*
</dt> <dd>

**Numero** (**Long**) che contiene l'indice del carattere il cui indice di riga deve essere recuperato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un **numero** (**Long**).

## <a name="remarks"></a>Commenti

Se la posizione del carattere specificata è 1, questo metodo recupera l'indice di riga della riga corrente.

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

[**CASELLA. getLineIndex**](editbox-getlineindex.md)
</dt> </dl>

 

 





