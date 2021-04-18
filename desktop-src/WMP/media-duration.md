---
title: Media. durata
description: La proprietà Duration recupera la durata dell'elemento multimediale corrente in secondi.
ms.assetid: d7d36858-812d-471b-84ce-fe2ab96b86b3
keywords:
- Media. Duration Windows Media Player
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
ms.openlocfilehash: 71586f6aa37401d56a9e9537bfbea6c5af23f318
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331385"
---
# <a name="mediaduration"></a>Media. durata

La proprietà **Duration** recupera la durata dell'elemento multimediale corrente in secondi.

## <a name="syntax"></a>Sintassi

*Player*. *currentMedia*. **durata**

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un **numero** di sola lettura ( **Double**).

## <a name="remarks"></a>Commenti

Se questa proprietà viene utilizzata con un elemento multimediale diverso da quello specificato in *Player*. **currentMedia**, non può contenere un valore valido.

Per recuperare la durata per i file che non si trovano nella libreria dell'utente, è necessario attendere che Windows Media Player Apra il file; ovvero, il OpenState corrente deve essere uguale a MediaOpen. Per verificarlo, è possibile gestire il *lettore*. Evento **OpenStateChange** o verificando periodicamente il valore di *Player*. **openState**.

Per le playlist, la durata di ogni elemento multimediale può essere recuperata quando viene aperto il singolo elemento multimediale, anziché quando viene aperta la playlist.

Per recuperare il valore di questa proprietà, è necessario l'accesso in lettura alla libreria. Per altre informazioni, vedere [accesso alla libreria](library-access.md).

Nell'esempio JScript seguente viene usato il *supporto*. **durata** per visualizzare il tempo rimanente nell'elemento multimediale corrente. Un elemento DIV HTML denominato RemTime Visualizza le informazioni. Un timer HTML aggiorna il testo nell'elemento DIV ogni secondo.

Il codice JScript seguente avvia il timer:


```JScript
// Execute the update() function at one-second intervals.
idTmr = window.setInterval("update()",1000);
```



Il codice JScript seguente arresta il timer:


```JScript
window.clearInterval(idTmr);
```



Usare il *lettore*. Evento **PlayStateChange** con un'istruzione **Switch** per determinare quando avviare e arrestare il timer.

Il codice JScript seguente viene eseguito ogni volta che il timer chiama la funzione Update:


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
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto multimediale**](media-object.md)
</dt> <dt>

[**Player. currentMedia**](player-currentmedia.md)
</dt> <dt>

[**Evento Player. PlayStateChange**](player-player-playstatechange.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





