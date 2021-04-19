---
title: COLUMN. columnID
description: L'attributo columnID specifica o recupera un ID di colonna nel controllo PLAYLIST.
ms.assetid: c7b51f0b-e347-46be-a26d-aaa0bce83e0c
keywords:
- Media Player di Windows COLUMN. columnID
topic_type:
- apiref
api_name:
- COLUMN.columnID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4bc9aa6485443ae17486616b030b903a911a8e9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330252"
---
# <a name="columncolumnid"></a>COLUMN. columnID

L'attributo **ColumnID** specifica o recupera un ID di colonna nel controllo **playlist** .

``` syntax
        elementID.columnID
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una **stringa** di lettura/scrittura.

## <a name="remarks"></a>Commenti

I valori **ColumnID** sono gli stessi valori usati con il metodo **GetItemInfo** su un oggetto **multimediale** . È possibile ottenere un elenco usando i *supporti*. proprietà **attributeCount** per determinare il numero di attributi disponibili per un determinato oggetto **multimediale** . I numeri di indice possono quindi essere usati con il *supporto*. metodo **GetAttribute** per determinare i nomi degli attributi, che a loro volta possono essere passati al *supporto*. **GetItemInfo**. La proprietà **ColumnID** può essere impostata solo su questi valori, ad eccezione di alcuni valori che potrebbero non essere restituiti dal *supporto*. **GetAttributeName**. Tali valori sono elencati di seguito.



| Valore     | Descrizione                                                                        |
|-----------|------------------------------------------------------------------------------------|
| name      | Consente di visualizzare il nome dell'oggetto **supporto** .                                         |
| duration  | Consente di visualizzare la durata dell'oggetto **multimediale** .                                     |
| sourceURL | Consente di visualizzare l'URL dell'oggetto **multimediale** .                                          |
| status    | Visualizza lo stato della copia dei file.                                              |
| size      | Consente di visualizzare le dimensioni del file rappresentato dall'oggetto **multimediale** .                |
| estensione | Consente di visualizzare l'estensione del nome file del file rappresentato dall'oggetto **multimediale** . |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**COLUMN-elemento**](column-element.md)
</dt> <dt>

[**Oggetto multimediale**](media-object.md)
</dt> <dt>

[**Media. attributeCount**](media-attributecount.md)
</dt> <dt>

[**Media. GetAttribute**](media-getattributename.md)
</dt> <dt>

[**Media. getItemInfo**](media-getiteminfo.md)
</dt> </dl>

 

 





