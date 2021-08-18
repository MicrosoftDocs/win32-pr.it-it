---
title: Media.duration
description: La proprietà duration recupera la durata dell'elemento multimediale corrente in secondi.
ms.assetid: d7d36858-812d-471b-84ce-fe2ab96b86b3
keywords:
- Media.duration Windows Media Player
topic_type:
- apiref
api_name:
- Media.duration
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e89eab1ffbb8c9f3d48c3f61eb6d831af66b4931ed1d858658eed3fc21d08183
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118118801"
---
# <a name="mediaduration"></a>Media.duration

La **proprietà duration** recupera la durata dell'elemento multimediale corrente in secondi.

## <a name="syntax"></a>Sintassi

*lettore*. *currentMedia*. **duration**

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un numero di sola **lettura** ( **double**).

## <a name="remarks"></a>Commenti

Se questa proprietà viene utilizzata con un elemento multimediale diverso da quello specificato in *Player*. **currentMedia**, potrebbe non contenere un valore valido.

Per recuperare la durata dei file non presenti nella libreria dell'utente, è necessario attendere Windows Media Player aprire il file. ciò significa che l'oggetto OpenState corrente deve essere uguale a MediaOpen. È possibile verificarlo gestendo *player*. **Evento OpenStateChange** o controllando periodicamente il valore di *Player*. **openState**.

Per le playlist, la durata di ogni elemento multimediale può essere recuperata quando viene aperto il singolo elemento multimediale, anziché quando viene aperta la playlist.

Per recuperare il valore di questa proprietà, è necessario l'accesso in lettura alla libreria. Per altre informazioni, vedere [Accesso alla libreria](library-access.md).

Nell'esempio JScript seguente viene utilizzato *Media*. **duration** per visualizzare il tempo rimanente nell'elemento multimediale corrente. Un elemento DIV HTML denominato RemTime visualizza le informazioni. Un timer HTML aggiorna il testo nell'elemento DIV ogni secondo.

Il codice JScript seguente avvia il timer:


```JScript
// Execute the update() function at one-second intervals.
idTmr = window.setInterval("update()",1000);
```



Il codice JScript seguente arresta il timer:


```JScript
window.clearInterval(idTmr);
```



Usare il *lettore*. **Evento PlayStateChange** con **un'istruzione switch** per determinare quando avviare e arrestare il timer.

Il codice JScript seguente viene eseguito ogni volta che il timer chiama la funzione di aggiornamento:


```JScript
// Store the current position of the current media item.
var TimeNow = Player.controls.currentPosition;

// Display the time remaining information.
RemTime.innerHTML = "Seconds remaining: ";

// Subtract the current position from the duration of the current media.
// Use the Math.floor method to round the result down to the nearest integer.
RemTime.innerHTML += Math.floor(Player.currentMedia.duration - TimeNow);
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

[**Player.currentMedia**](player-currentmedia.md)
</dt> <dt>

[**Evento Player.PlayStateChange**](player-player-playstatechange.md)
</dt> <dt>

[**Impostazioni.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Impostazioni.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





