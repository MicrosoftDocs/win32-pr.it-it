---
title: Metodo mediacollection. Remove
description: Il metodo Remove rimuove un elemento dall'insieme di supporti.
ms.assetid: 7d4c03ed-01c8-4112-90b6-5de52eacb199
keywords:
- rimuovere il metodo Windows Media Player
- Metodo Remove Media Player Windows, classe Mediacollection
- Mediacollection (classe) Windows Media Player, Remove (metodo)
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
ms.openlocfilehash: 6667a5b95920ac63f38d3a581e6f8e05bdf8d233
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327161"
---
# <a name="mediacollectionremove-method"></a>Metodo mediacollection. Remove

Il metodo **Remove** rimuove un elemento dall'insieme di supporti.

## <a name="syntax"></a>Sintassi


```JScript
MediaCollection.remove(
  item,
  delete
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*elemento* \[ di in\]
</dt> <dd>

Oggetto **multimediale** da rimuovere.

</dd> <dt>

*Elimina* \[ in\]
</dt> <dd>

**Valore booleano** che indica se rimuovere l'elemento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo elimina un elemento dalla libreria. Questo metodo non elimina i file dal computer dell'utente.

Per usare questo metodo, è necessario l'accesso completo alla libreria. Per altre informazioni, vedere [accesso alla libreria](library-access.md).

## <a name="examples"></a>Esempio

Il seguente esempio di JScript, dopo la richiesta all'utente, Elimina definitivamente il primo elemento multimediale della raccolta di supporti usando *mediacollection*. **rimuovere**. L'oggetto **Player** è stato creato con ID = "Player".


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
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto multimediale**](media-object.md)
</dt> <dt>

[**Mediacollection (oggetto)**](mediacollection-object.md)
</dt> <dt>

[**Mediacollection. Add**](mediacollection-add.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





