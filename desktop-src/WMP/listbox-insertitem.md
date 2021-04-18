---
title: LISTBOX. insertItem
description: Il metodo insertItem inserisce il testo specificato in corrispondenza dell'indice specificato nel controllo casella di riepilogo.
ms.assetid: c45eb75e-074d-4f3f-bfdd-6c3cbbd71f54
keywords:
- LISTBOX. insertItem Media Player Windows
topic_type:
- apiref
api_name:
- LISTBOX.insertItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3600b40ca164c71bd62c0a9a368516d6ad0e1edd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327741"
---
# <a name="listboxinsertitem"></a>LISTBOX. insertItem

Il metodo **InsertItem** inserisce il testo specificato in corrispondenza dell'indice specificato nel controllo casella di riepilogo.

``` syntax
        elementID.insertItem(index, text)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="index"></span><span id="INDEX"></span>*Indice*
</dt> <dd>

**Numero** (**Long**) che contiene l'indice della riga da recuperare.

</dd> <dt>

<span id="text"></span><span id="TEXT"></span>*testo*
</dt> <dd>

**Stringa** contenente il testo da inserire.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Quando viene inserita una riga, gli indici di riga per le linee sotto la riga inserita aumentano di uno.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------|
| Versione<br/> | Windows Media Player per Windows XP o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LISTBOX (elemento)**](listbox-element.md)
</dt> </dl>

 

 





