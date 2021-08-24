---
title: External.libraryLocationID
description: Nota In questo argomento vengono descritte le funzionalità progettate per l'uso da parte dei negozi online. | External.libraryLocationID
ms.assetid: 9a9bea89-c05c-4759-be22-86588bbeca2c
keywords:
- External.libraryLocationID Windows Media Player
topic_type:
- apiref
api_name:
- External.libraryLocationID
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65119db42e8a4d6a06414f1c7790fb8716c0f9423391ed0a58f74a6913cb3b8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649131"
---
# <a name="externallibrarylocationid"></a>External.libraryLocationID

> [!Note]  
> Questo argomento descrive le funzionalità progettate per l'uso da parte dei negozi online. L'uso di questa funzionalità all'esterno del contesto di un negozio online non è supportato.

 

La **proprietà libraryLocationID** recupera l'identificatore dell'elemento multimediale specifico attualmente visualizzato nella visualizzazione del lettore.

``` syntax
window.external.libraryLocationID
      
```

## <a name="possible-values"></a>Valori possibili

Questa proprietà è una stringa di sola **lettura.**

## <a name="remarks"></a>Commenti

Questa proprietà funziona in combinazione con la [proprietà External.libraryLocationType.](external-librarylocationtype.md) Si supponga, ad esempio, **che libraryLocationType** sia uguale a CPAlbumID e **libraryLocationID** sia uguale a 3. Ciò significa che la visualizzazione corrente Windows Media Player l'album con ID 3. Per altre informazioni su come Windows Media Player le visualizzazioni del contenuto del negozio online, vedere [Posizione e elemento selezionato.](location-and-selected-item.md)

Alcune visualizzazioni in Windows Media Player sono associate a un particolare elemento multimediale. Ad esempio, se la vista corrente rappresenta un singolo album, **libraryLocationType** è uguale a CPAlbumID e **libraryLocationID** è l'ID dell'album. Altre visualizzazioni non sono associate ad alcun elemento multimediale specifico. Ad esempio, se la vista corrente rappresenta tutti gli album, **libraryLocationType** è uguale a AllCPAlbumIDs, ma non esiste alcun valore significativo che possa essere assegnato a **libraryLocationID**. Nei casi in cui **la proprietà libraryLocationID** non ha un valore significativo, è uguale alla stringa vuota.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto esterno per i negozi online di tipo 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External.libraryLocationType**](external-librarylocationtype.md)
</dt> <dt>

[**Posizione e elemento selezionato**](location-and-selected-item.md)
</dt> </dl>

 

 





