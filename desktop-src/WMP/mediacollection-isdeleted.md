---
title: Mediacollection. Metodo eliminato
description: Il metodo IsValid recupera un valore che indica se l'elemento multimediale specificato si trova nella cartella Deleted Items.
ms.assetid: bb3ce9c9-9e43-45a5-8802-dc6783cf2ad7
keywords:
- Metodo eliminato Media Player Windows
- Metodo di eliminazione di Windows Media Player, classe Mediacollection
- Mediacollection (classe) Windows Media Player, metodo eliminato
topic_type:
- apiref
api_name:
- MediaCollection.isDeleted
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd3cdc27c84c88eb65df5b7635f34c79c1b4fe82
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327162"
---
# <a name="mediacollectionisdeleted-method"></a>Mediacollection. Metodo eliminato

Il **Metodo IsValid** recupera un valore che indica se l'elemento multimediale specificato si trova nella cartella Deleted Items.

## <a name="syntax"></a>Sintassi


```JScript
bRetVal = MediaCollection.isDeleted(
  item
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*elemento* \[ di in\]
</dt> <dd>

Oggetto **multimediale** che può essere eliminato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un **valore booleano**.

## <a name="remarks"></a>Commenti

Per usare questo metodo, è necessario l'accesso in lettura alla libreria. Per altre informazioni, vedere [accesso alla libreria](library-access.md).

**Windows Media Player 10 Mobile:** Questo metodo restituisce sempre **false**.

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene utilizzato *mediacollection*. viene **eliminato per verificare** se un particolare elemento multimediale, archiviato nella variabile denominata mediaObject, si trova nella cartella elementi eliminati. Se l'elemento multimediale non è già stato eliminato, viene spostato nella cartella elementi eliminati. L'oggetto **Player** è stato creato con ID = "Player".


```JScript
// Test whether the media item is in the deleted items folder.
if (!Player.mediaCollection.isDeleted(mediaObject)){

    // The media item is available to be deleted, move it to 
    // the deleted items folder.
    Player.mediaCollection.setDeleted(mediaObject, true);

    // Inform the user that the operation succeeded.
    alert("Media item moved to deleted items folder.");}

else
    // Tell the user the operation is unnecessary.
    alert("Item is already deleted!");
}

```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0, Windows Media Player versione 7,1 o Windows Media Player per Windows XP. Questo metodo non è supportato per Windows Media Player 9 Series o versioni successive.<br/> |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl>                                                                                                              |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto multimediale**](media-object.md)
</dt> <dt>

[**Mediacollection (oggetto)**](mediacollection-object.md)
</dt> <dt>

[**Mediacollection. sedeleted**](mediacollection-setdeleted.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





