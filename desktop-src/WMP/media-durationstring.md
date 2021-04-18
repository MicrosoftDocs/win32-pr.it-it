---
title: Media. durationString
description: La proprietà durationString recupera un valore stringa che indica la durata dell'elemento multimediale corrente nel formato HH MM SS.
ms.assetid: dfcb4c2e-c62c-4c3e-a9f4-fd147fb5b28c
keywords:
- Media Player Windows Media. durationString
topic_type:
- apiref
api_name:
- Media.durationString
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f1bbb89716ab1d06b176754396611ab22980659
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331384"
---
# <a name="mediadurationstring"></a>Media. durationString

La proprietà **durationstring** recupera un valore **stringa** che indica la durata dell'elemento multimediale corrente nel formato HH: mm: SS.

## <a name="syntax"></a>Sintassi

*Player*. *currentMedia*. **durationstring**

## <a name="possible-values"></a>Valori possibili

Questa proprietà è una **stringa** di sola lettura.

## <a name="remarks"></a>Commenti

Se questa proprietà viene utilizzata con un elemento multimediale diverso da quello specificato in *Player*. **currentMedia**, non può contenere un valore valido. Se la lunghezza dell'elemento multimediale è inferiore a un'ora, la parte HH: del valore restituito viene omessa.

Per recuperare il valore di questa proprietà, è necessario l'accesso in lettura alla libreria. Per altre informazioni, vedere [accesso alla libreria](library-access.md).

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene usato il *supporto*. **durationstring** per visualizzare la durata dell'elemento multimediale corrente come testo formattato. Un elemento DIV HTML denominato MediaInfo Visualizza le informazioni sulla durata. L'oggetto **Player** è stato creato con ID = "Player".


```JScript
<!-- Create an event handler to update the display when
 the current media item changes. -->
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = OpenStateChange(NewState)>

// Test whether the new media item is open.
if (NewState == 13){

   // Write the formatted duration string to the DIV region.
   MediaInfo.innerHTML = "Duration: " + Player.currentMedia.durationString;
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

[**Media. durata**](media-duration.md)
</dt> <dt>

[**Player. currentMedia**](player-currentmedia.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





