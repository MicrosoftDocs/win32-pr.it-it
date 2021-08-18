---
title: LISTBOX.insertItem
description: Il metodo insertItem inserisce il testo specificato in corrispondenza dell'indice specificato nel controllo casella di riepilogo.
ms.assetid: c45eb75e-074d-4f3f-bfdd-6c3cbbd71f54
keywords:
- LISTBOX.insertItem Windows Media Player
topic_type:
- apiref
api_name:
- LISTBOX.insertItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0344bbc9fbe4f8f2b680866f70c0fe16398ad08cbf4a916c454223fdff04614e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135304"
---
# <a name="listboxinsertitem"></a>LISTBOX.insertItem

Il **metodo insertItem** inserisce il testo specificato in corrispondenza dell'indice specificato nel controllo casella di riepilogo.

``` syntax
        elementID.insertItem(index, text)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="index"></span><span id="INDEX"></span>*Indice*
</dt> <dd>

**Numero** (**long**) contenente l'indice della riga da recuperare.

</dd> <dt>

<span id="text"></span><span id="TEXT"></span>*Testo*
</dt> <dd>

**Stringa** contenente il testo da inserire.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Quando viene inserita una riga, gli indici delle righe sotto la riga inserita aumentano di uno.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------|
| Versione<br/> | Windows Media Player per Windows XP o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento LISTBOX**](listbox-element.md)
</dt> </dl>

 

 





