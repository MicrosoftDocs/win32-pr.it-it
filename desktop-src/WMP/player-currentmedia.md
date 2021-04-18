---
title: Player. currentMedia
description: La proprietà currentMedia specifica o recupera l'oggetto multimediale corrente.
ms.assetid: 5cf45a10-9d0d-435e-97f1-d2c9c51f4b47
keywords:
- Player. currentMedia Windows Media Player
topic_type:
- apiref
api_name:
- Player.currentMedia
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea90b7be72bcb10a8ec0d3c49116f3effceb9a93
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328208"
---
# <a name="playercurrentmedia"></a>Player. currentMedia

La proprietà **currentMedia** specifica o recupera l'oggetto multimediale corrente.

## <a name="syntax"></a>Sintassi

*Player* . **currentMedia**

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un oggetto multimediale di lettura/scrittura.

## <a name="remarks"></a>Commenti

Se le *Impostazioni*. la proprietà **autostart** è true, la riproduzione viene avviata automaticamente quando si imposta **currentMedia**.

Questa proprietà accetta un oggetto multimediale, che può essere acquisito tramite *playlist*. **elemento**. Per caricare un elemento **multimediale** usando un nome di file, impostare la proprietà URL o usare **newMedia**.

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene recuperato il primo elemento multimediale nella libreria. USA quindi **currentMedia** per rendere l'elemento multimediale recuperato l'elemento multimediale corrente e quindi per visualizzare il nome dell'elemento multimediale corrente. L'oggetto **Player** è stato creato con ID = "Player".


```JScript
// Retrieve the first media item from the library.
var firstMedia = Player.mediaCollection.getAll().item(0);

// Make the retrieved media item the current media item.
Player.currentMedia = firstMedia;

// Display the name of the current media item.
document.write("Found first media item. Name = " + Player.currentMedia.name);
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

[**Oggetto Player**](player-object.md)
</dt> <dt>

[**Player. newMedia**](player-newmedia.md)
</dt> <dt>

[**Playlist. Item**](playlist-item.md)
</dt> <dt>

[**Impostazioni. avvio automatico**](settings-autostart.md)
</dt> </dl>

 

 





