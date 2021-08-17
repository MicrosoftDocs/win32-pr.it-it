---
title: EDITBOX.getLineFromChar
description: Il metodo getLineFromChar recupera l'indice di riga per l'indice dei caratteri specificato.
ms.assetid: c3a29bdf-ff63-4b6d-90e8-d414dde87f85
keywords:
- EDITBOX.getLineFromChar Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.getLineFromChar
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 110030c3c756a91c993857cef125c51669f71eb9a358eb7261205fde0b0ad4a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117749307"
---
# <a name="editboxgetlinefromchar"></a>EDITBOX.getLineFromChar

Il **metodo getLineFromChar** recupera l'indice di riga per l'indice dei caratteri specificato.

``` syntax
        elementID.getLineFromChar(index)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="index"></span><span id="INDEX"></span>*Indice*
</dt> <dd>

**Numero** (**long**) contenente l'indice del carattere di cui recuperare l'indice di riga.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un **valore Number** (**long**).

## <a name="remarks"></a>Commenti

Se la posizione del carattere specificata è 1, questo metodo recupera l'indice di riga della riga corrente.

Questo metodo può essere chiamato solo dopo che il controllo diventa visibile.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------|
| Versione<br/> | Windows Media Player per Windows XP o versioni successive<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento EDITBOX**](editbox-element.md)
</dt> <dt>

[**EDITBOX.getLine**](editbox-getline.md)
</dt> <dt>

[**EDITBOX.getLineIndex**](editbox-getlineindex.md)
</dt> </dl>

 

 





