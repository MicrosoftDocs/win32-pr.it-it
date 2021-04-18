---
title: Media. imageSourceHeight
description: La proprietà ImageSourceHeight recupera l'altezza in pixel dell'elemento multimediale corrente.
ms.assetid: fa98ec62-4c58-46ab-98f3-8017096d46d8
keywords:
- Media Player Windows Media. imageSourceHeight
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
ms.openlocfilehash: 0de364243e71c6653085b4c9c9ff81f148dc299d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329926"
---
# <a name="mediaimagesourceheight"></a>Media. imageSourceHeight

La proprietà **ImageSourceHeight** recupera l'altezza in pixel dell'elemento multimediale corrente.

## <a name="syntax"></a>Sintassi

*Player*. *currentMedia*. **imageSourceHeight**

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un **numero** di sola lettura (**Long**).

## <a name="remarks"></a>Commenti

Se l'elemento multimediale non è quello corrente, questa proprietà restituisce zero.

Per recuperare il valore di questa proprietà, è necessario l'accesso in lettura alla libreria. Per altre informazioni, vedere [accesso alla libreria](library-access.md).

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene utilizzato *media*. imageSourceHeight per visualizzare la dimensione dell'immagine, in pixel, dell'elemento multimediale corrente. Le informazioni vengono stampate in un elemento TEXTAREA HTML denominato VideoSize. L'oggetto **Player** è stato creato con ID = "Player".


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
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto multimediale**](media-object.md)
</dt> <dt>

[**Player. currentMedia**](player-currentmedia.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





