---
title: Metodo MediaCollection.setDeleted
description: Il metodo setDeleted sposta l'elemento multimediale specificato nella cartella degli elementi eliminati. | Metodo MediaCollection.setDeleted
ms.assetid: 3e3c9a16-37e1-41b4-8593-58aaf4541eb9
keywords:
- Metodo setDeleted Windows Media Player
- Metodo setDeleted Windows Media Player , classe MediaCollection
- Classe MediaCollection Windows Media Player, metodo setDeleted
topic_type:
- apiref
api_name:
- MediaCollection.setDeleted
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63dcb4c0062acbd5f457cd09b9c1370ff9c4f7683fd8758a4a64ce5f510a6948
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119647841"
---
# <a name="mediacollectionsetdeleted-method"></a>Metodo MediaCollection.setDeleted

Il **metodo setDeleted** sposta l'elemento multimediale specificato nella cartella degli elementi eliminati.

## <a name="syntax"></a>Sintassi


```JScript
MediaCollection.setDeleted(
  item,
  true
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*item* \[ Pollici\]
</dt> <dd>

**Oggetto** multimediale da spostare.

</dd> <dt>

*true* \[ Pollici\]
</dt> <dd>

Specificare sempre questo valore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo non rimuove i file dal computer dell'utente.

Per usare questo metodo, è necessario l'accesso completo alla libreria. Per altre informazioni, vedere [Accesso alla libreria.](library-access.md)

**Windows Media Player 10 Mobile:** Questo metodo non è supportato.

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene utilizzato *MediaCollection*. **setDeleted per** spostare un particolare elemento multimediale, archiviato nella variabile denominata mediaObject, nella cartella degli elementi eliminati. Oggetto *MediaCollection.* **Il metodo isDeleted** verifica innanzitutto se l'elemento è già stato eliminato. **L'oggetto Player** è stato creato con ID = "Player".


```JScript
// Test whether the media item is in the deleted items folder.
if (!Player.mediaCollection.isDeleted(mediaObject)){

    // The item is available to be deleted; move it to 
    // the deleted items folder.
    Player.mediaCollection.setDeleted(mediaObject, true);

    // Inform the user that the operation succeeded.
    alert("Item moved to deleted items folder.");}

else
    // Tell the user the operation is unnecessary.
    alert("Item is already deleted!");
}

```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0, Windows Media Player 7.1 o Windows Media Player per Windows XP. Questo metodo non è supportato per Windows Media Player serie 9 o versioni successive.<br/> |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl>                                                                                                              |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto multimediale**](media-object.md)
</dt> <dt>

[**Oggetto MediaCollection**](mediacollection-object.md)
</dt> <dt>

[**MediaCollection.isDeleted**](mediacollection-isdeleted.md)
</dt> <dt>

[**Impostazioni.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Impostazioni.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





