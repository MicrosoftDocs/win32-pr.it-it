---
title: Metodo MediaCollection.add
description: Il metodo add aggiunge un nuovo elemento multimediale o playlist alla libreria. | Metodo MediaCollection.add
ms.assetid: 8adf93d1-368b-4916-937f-342901a1592b
keywords:
- Metodo add Windows Media Player
- Metodo add Windows Media Player , classe MediaCollection
- Classe MediaCollection Windows Media Player , metodo add
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
ms.openlocfilehash: 8b26d21f67496f345324efdca93dbf85e59947f1616e0c5620faead2807a6ed2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119647911"
---
# <a name="mediacollectionadd-method"></a>Metodo MediaCollection.add

Il **metodo add** aggiunge un nuovo elemento multimediale o playlist alla libreria.

## <a name="syntax"></a>Sintassi


```JScript
retVal = MediaCollection.add(
  path
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*path* \[ Pollici\]
</dt> <dd>

**Stringa** contenente il percorso.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un **oggetto Media.**

## <a name="remarks"></a>Commenti

Questo metodo carica un elemento multimediale o una playlist esistente nella libreria, dato il percorso di un file. Questo metodo non sposta o modifica il file. Questo metodo ha esito negativo se viene specificato un percorso locale non valido, ma non viene verificata la validità dei file multimediali digitali prima di essere aggiunti alla libreria.

Questo metodo accetta sia i file di playlist statici che i file di playlist automatici. *PlaylistCollection*. **Il metodo importPlaylist** può essere usato anche per aggiungere una playlist statica alla libreria.

Per usare questo metodo, è necessario l'accesso completo alla libreria. Per altre informazioni, vedere [Accesso alla libreria](library-access.md).

## <a name="examples"></a>Esempio

Nell'esempio di Microsoft JScript seguente vengono aggiunti tre oggetti multimediali alla Windows Media Player raccolta di supporti. **L'oggetto** Player è stato creato con ID="Player".


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
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Gestione delle playlist**](managing-playlists.md)
</dt> <dt>

[**Oggetto multimediale**](media-object.md)
</dt> <dt>

[**Oggetto MediaCollection**](mediacollection-object.md)
</dt> <dt>

[**MediaCollection.remove**](mediacollection-remove.md)
</dt> <dt>

[**PlaylistCollection.importPlaylist**](playlistcollection-importplaylist.md)
</dt> <dt>

[**Impostazioni.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Impostazioni.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





