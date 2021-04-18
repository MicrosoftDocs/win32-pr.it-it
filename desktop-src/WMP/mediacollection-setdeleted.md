---
title: Mediacollection. sedeleted (metodo)
description: Il metodo sedeleted sposta l'elemento multimediale specificato nella cartella degli elementi eliminati. | Mediacollection. sedeleted (metodo)
ms.assetid: 3e3c9a16-37e1-41b4-8593-58aaf4541eb9
keywords:
- Metodo sedeleted Media Player Windows
- Metodo sedeleted Windows Media Player, classe Mediacollection
- Mediacollection (classe) Windows Media Player, metodo sedeleted
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
ms.openlocfilehash: f545953899883933286f3c38def62d9f254dfdc0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327154"
---
# <a name="mediacollectionsetdeleted-method"></a>Mediacollection. sedeleted (metodo)

Il metodo **Sedeleted** sposta l'elemento multimediale specificato nella cartella degli elementi eliminati.

## <a name="syntax"></a>Sintassi


```JScript
MediaCollection.setDeleted(
  item,
  true
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*elemento* \[ di in\]
</dt> <dd>

Oggetto **multimediale** da spostare.

</dd> <dt>

valore *true* \[ in\]
</dt> <dd>

Specificare sempre questo valore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo non rimuove i file dal computer dell'utente.

Per usare questo metodo, è necessario l'accesso completo alla libreria. Per altre informazioni, vedere [accesso alla libreria](library-access.md).

**Windows Media Player 10 Mobile:** Questo metodo non è supportato.

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene utilizzato *mediacollection*. viene **eliminato per spostare** un particolare elemento multimediale, archiviato nella variabile denominata mediaObject, nella cartella Deleted Items. *Mediacollection*. il metodo **undeleted** verifica prima di tutto se l'elemento è già stato eliminato. L'oggetto **Player** è stato creato con ID = "Player".


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
| Versione<br/> | Windows Media Player versione 7,0, Windows Media Player versione 7,1 o Windows Media Player per Windows XP. Questo metodo non è supportato per Windows Media Player 9 Series o versioni successive.<br/> |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl>                                                                                                              |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto multimediale**](media-object.md)
</dt> <dt>

[**Mediacollection (oggetto)**](mediacollection-object.md)
</dt> <dt>

[**Mediacollection. viene eliminato**](mediacollection-isdeleted.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





