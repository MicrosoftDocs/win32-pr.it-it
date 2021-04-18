---
title: Metodo mediacollection. Add
description: Il metodo Add aggiunge un nuovo elemento multimediale o una playlist alla raccolta. | Metodo mediacollection. Add
ms.assetid: 8adf93d1-368b-4916-937f-342901a1592b
keywords:
- Aggiungi metodo Windows Media Player
- Metodo Add Media Player Windows, classe Mediacollection
- Mediacollection (classe) Windows Media Player, Aggiungi metodo
topic_type:
- apiref
api_name:
- MediaCollection.add
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7731a42c8e1317355b129acb6921676c0a33f4a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330358"
---
# <a name="mediacollectionadd-method"></a>Metodo mediacollection. Add

Il metodo **Add** aggiunge un nuovo elemento multimediale o una playlist alla raccolta.

## <a name="syntax"></a>Sintassi


```JScript
retVal = MediaCollection.add(
  path
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*percorso* \[ in\]
</dt> <dd>

**Stringa** che contiene il percorso.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un oggetto **multimediale** .

## <a name="remarks"></a>Commenti

Questo metodo carica un elemento multimediale o una playlist esistente nella libreria, dato un percorso a un file. Questo metodo non sposta o modifica il file. Questo metodo ha esito negativo se viene specificato un percorso locale non valido, ma non viene verificata la validità dei file multimediali digitali prima che vengano aggiunti alla libreria.

Questo metodo accetta sia i file di playlist statici che quelli automatici. *PlaylistCollection*. il metodo **importPlaylist** può essere usato anche per aggiungere una playlist statica alla libreria.

Per usare questo metodo, è necessario l'accesso completo alla libreria. Per altre informazioni, vedere [accesso alla libreria](library-access.md).

## <a name="examples"></a>Esempio

Nell'esempio Microsoft JScript seguente vengono aggiunti tre oggetti multimediali alla raccolta di supporti Windows Media Player. L'oggetto **Player** è stato creato con ID = "Player".


```JScript
// Adding a media object using a website.
Player.mediaCollection.add("https://www.proseware.com/Media/Laure.wma");

// Adding a media object from a local network.
// You must add an escape sequence of a backslash for 
// every original backslash.
Player.mediaCollection.add("\\\\yourservername\\Public\\Jeanne.wma");

// Adding a media object from a file on a local drive.
// Be sure to add appropriate escape sequences.
Player.mediaCollection.add("C:\\WMSDK\\WMPSDK\\docs\\samples\\media\\house.wma");
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Gestione delle playlist**](managing-playlists.md)
</dt> <dt>

[**Oggetto multimediale**](media-object.md)
</dt> <dt>

[**Mediacollection (oggetto)**](mediacollection-object.md)
</dt> <dt>

[**Mediacollection. Remove**](mediacollection-remove.md)
</dt> <dt>

[**PlaylistCollection. importPlaylist**](playlistcollection-importplaylist.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





