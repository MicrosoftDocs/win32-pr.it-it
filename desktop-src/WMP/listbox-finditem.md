---
title: LISTBOX. findItem
description: Il metodo findItem cerca una determinata stringa a partire dall'elemento che segue l'indice dell'elemento specificato.
ms.assetid: 8d112d99-1866-45e5-b0ef-5d4a3c8b388d
keywords:
- Media Player di Windows LISTBOX. findItem
topic_type:
- apiref
api_name:
- LISTBOX.findItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 161f4dd8b93fe4fed6a794dffde3e58e840c74e5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327759"
---
# <a name="listboxfinditem"></a>LISTBOX. findItem

Il metodo **FindItem** cerca una determinata stringa a partire dall'elemento che segue l'indice dell'elemento specificato.

``` syntax
        elementID.findItem(startIndex, searchString)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="startIndex"></span><span id="startindex"></span><span id="STARTINDEX"></span>*startIndex*
</dt> <dd>

**Numero** (**Long**) che contiene l'indice dell'elemento da cui iniziare la ricerca.

</dd> <dt>

<span id="searchString"></span><span id="searchstring"></span><span id="SEARCHSTRING"></span>*searchString*
</dt> <dd>

**Stringa** contenente il testo da ricercare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un **numero** (**Long**) contenente l'indice dell'elemento che contiene la stringa.

## <a name="remarks"></a>Commenti

Per avviare la ricerca nella prima riga del controllo casella di riepilogo, utilizzare 1 come *startIndex*. Per continuare a cercare testo dopo aver trovato la prima riga, usare l'indice di riga restituito come *startIndex* e la ricerca verrà avviata nella riga successiva. Questo metodo effettuerà la ricerca di sottostringhe e non distingue tra maiuscole e minuscole.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------|
| Versione<br/> | Windows Media Player per Windows XP o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LISTBOX (elemento)**](listbox-element.md)
</dt> </dl>

 

 





