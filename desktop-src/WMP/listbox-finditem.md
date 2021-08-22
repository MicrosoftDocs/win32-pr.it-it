---
title: LISTBOX.findItem
description: Il metodo findItem cerca una determinata stringa a partire dall'elemento che segue l'indice dell'elemento specificato.
ms.assetid: 8d112d99-1866-45e5-b0ef-5d4a3c8b388d
keywords:
- LISTBOX.findItem Windows Media Player
topic_type:
- apiref
api_name:
- LISTBOX.findItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e3625c8d8e9993d09e7b5b41911ead8df857c257a7a2354d71c8d81c1fecc645
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135324"
---
# <a name="listboxfinditem"></a>LISTBOX.findItem

Il **metodo findItem** cerca una stringa specificata a partire dall'elemento che segue l'indice dell'elemento specificato.

``` syntax
        elementID.findItem(startIndex, searchString)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="startIndex"></span><span id="startindex"></span><span id="STARTINDEX"></span>*Startindex*
</dt> <dd>

**Numero** (**long**) contenente l'indice dell'elemento in corrispondenza del quale avviare la ricerca.

</dd> <dt>

<span id="searchString"></span><span id="searchstring"></span><span id="SEARCHSTRING"></span>*searchString*
</dt> <dd>

**Stringa** contenente il testo da cercare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un **valore Number** (**long**) contenente l'indice dell'elemento che contiene la stringa.

## <a name="remarks"></a>Commenti

Per avviare la ricerca nella prima riga del controllo casella di riepilogo, usare 1 come *startIndex*. Per continuare a cercare testo dopo aver trovato la prima riga, usare l'indice di riga restituito come *startIndex* e la ricerca inizierà dalla riga successiva. Questo metodo cerca le sottostringhe e non fa distinzione tra maiuscole e minuscole.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------|
| Versione<br/> | Windows Media Player per Windows XP o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento LISTBOX**](listbox-element.md)
</dt> </dl>

 

 





