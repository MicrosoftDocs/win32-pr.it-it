---
title: Player.currentMedia
description: La proprietà currentMedia specifica o recupera l'oggetto Media corrente.
ms.assetid: 5cf45a10-9d0d-435e-97f1-d2c9c51f4b47
keywords:
- Player.currentMedia Windows Media Player
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
ms.openlocfilehash: 7df5e8cd2032d772cbd781d0b45794e86cc19eff7c730a6a963778d54a6f283d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054399"
---
# <a name="playercurrentmedia"></a>Player.currentMedia

La **proprietà currentMedia** specifica o recupera l'oggetto Media corrente.

## <a name="syntax"></a>Sintassi

*lettore* . **currentMedia**

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un oggetto multimediale di lettura/scrittura.

## <a name="remarks"></a>Commenti

Se *l'Impostazioni*. **la proprietà autoStart** è true, la riproduzione inizia automaticamente ogni volta che si imposta **currentMedia.**

Questa proprietà accetta un oggetto Media, che può essere acquisito usando *playlist.* **Elemento**. Per caricare un **elemento Multimediale** usando un nome file, impostare la proprietà URL o usare **newMedia**.

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene recuperato il primo elemento multimediale nella libreria. Usa quindi **currentMedia per** impostare l'elemento multimediale recuperato come elemento multimediale corrente e quindi per visualizzare il nome dell'elemento multimediale corrente. **L'oggetto Player** è stato creato con ID = "Player".


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
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto multimediale**](media-object.md)
</dt> <dt>

[**Oggetto Player**](player-object.md)
</dt> <dt>

[**Player.newMedia**](player-newmedia.md)
</dt> <dt>

[**Playlist.item**](playlist-item.md)
</dt> <dt>

[**Impostazioni.autoStart**](settings-autostart.md)
</dt> </dl>

 

 





