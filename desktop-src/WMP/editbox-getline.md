---
title: EDITBOX.getLine
description: Il metodo getLine recupera il testo per la riga con l'indice specificato.
ms.assetid: a692c32b-86b9-419e-a3a5-464687be04da
keywords:
- EDITBOX.getLine Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.getLine
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 28d555cb684fa849b5fc7cdb42ebaf0ab4fb278b4ef126845add2f12ddf59948
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118578837"
---
# <a name="editboxgetline"></a>EDITBOX.getLine

Il **metodo getLine** recupera il testo per la riga con l'indice specificato.

``` syntax
        elementID.getLine(index)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="index"></span><span id="INDEX"></span>*Indice*
</dt> <dd>

**Numero** (**long**) contenente l'indice della riga da recuperare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un **oggetto String**.

## <a name="remarks"></a>Commenti

Se l'indice non è valido, viene restituita una stringa vuota. Questo metodo può essere chiamato solo dopo che il controllo diventa visibile.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------|
| Versione<br/> | Windows Media Player per Windows XP o versioni successive<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento EDITBOX**](editbox-element.md)
</dt> <dt>

[**EDITBOX.getLineFromChar**](editbox-getlinefromchar.md)
</dt> <dt>

[**EDITBOX.getLineIndex**](editbox-getlineindex.md)
</dt> </dl>

 

 





