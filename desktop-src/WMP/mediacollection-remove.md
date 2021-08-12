---
title: Metodo MediaCollection.remove
description: Il metodo remove rimuove un elemento dalla raccolta di supporti.
ms.assetid: 7d4c03ed-01c8-4112-90b6-5de52eacb199
keywords:
- Rimuovere il metodo Windows Media Player
- Metodo remove Windows Media Player , classe MediaCollection
- Classe MediaCollection Windows Media Player , metodo remove
topic_type:
- apiref
api_name:
- MediaCollection.remove
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8dd0643741a15bf114acfef63459e67c332b06b33e6284b032979d4ad15c1d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118574608"
---
# <a name="mediacollectionremove-method"></a>Metodo MediaCollection.remove

Il **metodo remove** rimuove un elemento dalla raccolta di supporti.

## <a name="syntax"></a>Sintassi


```JScript
MediaCollection.remove(
  item,
  delete
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*item* \[ Pollici\]
</dt> <dd>

**Oggetto** multimediale da rimuovere.

</dd> <dt>

*eliminazione* \[ Pollici\]
</dt> <dd>

**Valore** booleano che indica se rimuovere l'elemento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo elimina un elemento dalla libreria. Questo metodo non elimina i file dal computer dell'utente.

Per usare questo metodo, è necessario l'accesso completo alla libreria. Per altre informazioni, vedere [Accesso alla libreria.](library-access.md)

## <a name="examples"></a>Esempio

Nell'JScript seguente, dopo la richiesta all'utente, elimina definitivamente il primo elemento multimediale nella raccolta multimediale usando *MediaCollection*. **rimuovere**. **L'oggetto Player** è stato creato con ID = "Player".


```JScript
// Retrieve the first item from the media collection.
var mediaObject = Player.mediaCollection.getAll().item(0);

// Store the name of the retrieved object.
var mediaName = mediaObject.name;

// Prompt the user for permission to delete the object.
var answer = confirm("OK to permanently delete " + mediaName + "?");

// Check the user response.
if (answer){

    // Permanently delete the item.
    Player.mediaCollection.remove(mediaObject, true);

    // Report that the item was deleted.
    alert("Deleted item " + mediaName);
}

```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto multimediale**](media-object.md)
</dt> <dt>

[**Oggetto MediaCollection**](mediacollection-object.md)
</dt> <dt>

[**MediaCollection.add**](mediacollection-add.md)
</dt> <dt>

[**Impostazioni.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Impostazioni.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





