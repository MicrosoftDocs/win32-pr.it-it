---
title: External. libraryLocationID
description: Si noti che in questo argomento viene descritta la funzionalità progettata per l'utilizzo da punti vendita online. | External. libraryLocationID
ms.assetid: 9a9bea89-c05c-4759-be22-86588bbeca2c
keywords:
- Media Player di Windows External. libraryLocationID
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
ms.openlocfilehash: 89f411ad8575bc7419cf9300d1aab46073ee869c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324565"
---
# <a name="externallibrarylocationid"></a>External. libraryLocationID

> [!Note]  
> Questo argomento descrive la funzionalità progettata per l'uso da punti vendita online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.

 

La proprietà **libraryLocationID** recupera l'identificatore dell'elemento multimediale specifico attualmente visualizzato nella visualizzazione del lettore.

``` syntax
window.external.libraryLocationID
      
```

## <a name="possible-values"></a>Valori possibili

Questa proprietà è una **stringa** di sola lettura.

## <a name="remarks"></a>Commenti

Questa proprietà funziona in combinazione con la proprietà [External. libraryLocationType](external-librarylocationtype.md) . Si supponga, ad esempio, che **libraryLocationType** sia uguale a CPAlbumID e che **libraryLocationID** sia uguale a 3. Ciò significa che nella visualizzazione corrente di Windows Media Player viene visualizzato l'album con ID 3. Per ulteriori informazioni sul modo in cui Windows Media Player caratterizza le visualizzazioni del contenuto di un negozio online, vedere [posizione e elemento selezionato](location-and-selected-item.md).

Alcune visualizzazioni in Windows Media Player sono associate a un particolare elemento multimediale. Ad esempio, se la visualizzazione corrente rappresenta un singolo album, **libraryLocationType** è uguale a CPAlbumID e **LIBRARYLOCATIONID** è l'ID dell'album. Altre viste non sono associate a un particolare elemento multimediale. Se, ad esempio, la visualizzazione corrente rappresenta tutti gli album, **libraryLocationType** è uguale a AllCPAlbumIDs, ma non esiste alcun valore significativo che può essere assegnato a **libraryLocationID**. Nei casi in cui la proprietà **libraryLocationID** non ha un valore significativo, è uguale alla stringa vuota.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto esterno per i negozi di tipo 1 online**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External. libraryLocationType**](external-librarylocationtype.md)
</dt> <dt>

[**Posizione e elemento selezionato**](location-and-selected-item.md)
</dt> </dl>

 

 





