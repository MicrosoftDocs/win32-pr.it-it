---
title: Media. imageSourceWidth
description: La proprietà imageSourceWidth recupera la larghezza dell'elemento multimediale corrente in pixel.
ms.assetid: 6559bd51-cec2-4fc6-aab8-f2fdd1d59bae
keywords:
- Media Player Windows Media. imageSourceWidth
topic_type:
- apiref
api_name:
- Media.imageSourceWidth
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff2a3fef7b74a3d033b058f0afd1f6eece007bd7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329921"
---
# <a name="mediaimagesourcewidth"></a>Media. imageSourceWidth

La proprietà **imageSourceWidth** recupera la larghezza dell'elemento multimediale corrente in pixel.

## <a name="syntax"></a>Sintassi

*Player*. *currentMedia*. **imageSourceWidth**

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un **numero** di sola lettura (**Long**).

## <a name="remarks"></a>Commenti

Se l'elemento multimediale non è quello corrente, questa proprietà restituisce zero.

Per recuperare il valore di questa proprietà, è necessario l'accesso in lettura alla libreria. Per altre informazioni, vedere [accesso alla libreria](library-access.md).

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene usato il *supporto*. **imageSourceWidth** per visualizzare la dimensione dell'immagine, in pixel, dell' **elemento multimediale corrente. Le informazioni vengono stampate in un elemento TEXTAREA HTML denominato VideoSize. L'oggetto Player** è stato creato con ID = "Player".


```JScript
<!-- Create an event handler to refresh the information when the current media changes. -->
<SCRIPT LANGUAGE = "JScript"  FOR = "Player"  EVENT = OpenStateChange(NewState)>

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

 

 





