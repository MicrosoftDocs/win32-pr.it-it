---
title: Media. getMarkerTime, metodo
description: Il metodo getMarkerTime recupera l'ora del marcatore in corrispondenza dell'indice specificato.
ms.assetid: c3e6bead-2831-4d84-9d13-dcb865efe472
keywords:
- Metodo getMarkerTime Windows Media Player
- Metodo getMarkerTime Windows Media Player, classe media
- Media class Media Player Windows, metodo getMarkerTime
topic_type:
- apiref
api_name:
- Media.getMarkerTime
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4398f89055a1996acb3f921d33c7675e52100ddd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331865"
---
# <a name="mediagetmarkertime-method"></a>Media. getMarkerTime, metodo

Il metodo **getMarkerTime** recupera l'ora del marcatore in corrispondenza dell'indice specificato.

## <a name="syntax"></a>Sintassi


```JScript
retVal = Media.getMarkerTime(
  markerNum
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*markerNum* \[ in\]
</dt> <dd>

**Numero** (**Long**) che specifica l'indice del marcatore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un **numero** (**Double**) che specifica la posizione del marcatore in secondi dall'inizio della clip.

## <a name="remarks"></a>Commenti

Questo metodo restituisce **null** se il marcatore specificato non esiste.

Alcuni elementi multimediali digitali non contengono marcatori. Usare **markerCount** per verificare il numero di marcatori presenti nella clip corrente.

I numeri di indice del marcatore iniziano da 1.

Per usare questo metodo, è necessario l'accesso in lettura alla libreria. Per altre informazioni, vedere [accesso alla libreria](library-access.md).

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene usato il *supporto*. **getMarkerTime** per inserire un elemento textarea HTML denominato MTIMES con la posizione di ogni marcatore. L'oggetto **Player** è stato creato con ID = "Player".


```JScript
// Get the number of markers in the current media item.
var mcount = Player.currentMedia.markerCount;

// Verify that at least one marker exists in the current media item.
if (mcount > 0){

// Loop through the marker list.
for (var i = 1;i < mcount + 1; i++){

   // Print the message to the text area.
   MTIMES.value += "Marker number " + i + " occurs at ";
   MTIMES.value += Player.currentMedia.getMarkerTime(i);
   MTIMES.value += " second(s).";
   MTIMES.value += "\n";
}

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

[**Media. getmarkname**](media-getmarkername.md)
</dt> <dt>

[**Media. markerCount**](media-markercount.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





