---
title: Media.imageSourceHeight
description: La proprietà ImageSourceHeight recupera l'altezza dell'elemento multimediale corrente in pixel.
ms.assetid: fa98ec62-4c58-46ab-98f3-8017096d46d8
keywords:
- Media.imageSourceHeight Windows Media Player
topic_type:
- apiref
api_name:
- Media.imageSourceHeight
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2c399efa33d542de14c0753f5812298de83024c8856ea00a1e1fda002cd33c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119390099"
---
# <a name="mediaimagesourceheight"></a>Media.imageSourceHeight

La **proprietà ImageSourceHeight** recupera l'altezza dell'elemento multimediale corrente in pixel.

## <a name="syntax"></a>Sintassi

*lettore*. *currentMedia*. **imageSourceHeight**

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un numero di sola **lettura** (**long**).

## <a name="remarks"></a>Commenti

Se l'elemento multimediale non è quello corrente, questa proprietà restituisce zero.

Per recuperare il valore di questa proprietà, è necessario l'accesso in lettura alla libreria. Per altre informazioni, vedere [Accesso alla libreria](library-access.md).

## <a name="examples"></a>Esempio

L'JScript seguente usa *Media*.imageSourceHeight per visualizzare le dimensioni dell'immagine, in pixel, dell'elemento multimediale corrente. Le informazioni vengono stampate in un elemento HTML TEXTAREA denominato VideoSize. **L'oggetto** Player è stato creato con ID = "player".


```JScript
<!-- Create an event handler to refresh the information when the current media changes. -->
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = OpenStateChange(NewState)>

// Test whether the new media item is open.
if (NewState == 13){

   // Store the height and width of the new media item.
   var Height = Player.currentMedia.imageSourceHeight;
   var Width =  Player.currentMedia.imageSourceWidth;

   // Erase the information in the text area.
   VideoSize.value = "";

   // Test whether an image is visible.
   if (Height != 0 && Width != 0)

      // Display the image size information.
      VideoSize.value = Width + " x " + Height;
}
</SCRIPT>

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

[**Impostazioni.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Impostazioni.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





