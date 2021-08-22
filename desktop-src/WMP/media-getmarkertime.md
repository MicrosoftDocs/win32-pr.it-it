---
title: Metodo Media.getMarkerTime
description: Il metodo getMarkerTime recupera l'ora del marcatore in corrispondenza dell'indice specificato.
ms.assetid: c3e6bead-2831-4d84-9d13-dcb865efe472
keywords:
- Metodo getMarkerTime Windows Media Player
- Metodo getMarkerTime Windows Media Player classe Media
- Classe media Windows Media Player metodo , getMarkerTime
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
ms.openlocfilehash: 0f90d1382302e4a053a6dee4dac911d2cc0c0aa67066469c8143f6f38b3bd889
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119508411"
---
# <a name="mediagetmarkertime-method"></a>Metodo Media.getMarkerTime

Il **metodo getMarkerTime** recupera l'ora del marcatore in corrispondenza dell'indice specificato.

## <a name="syntax"></a>Sintassi


```JScript
retVal = Media.getMarkerTime(
  markerNum
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*markerNum* \[ Pollici\]
</dt> <dd>

**Numero** (**long**) che specifica l'indice del marcatore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un **valore Number** (**double**) che specifica la posizione del marcatore in secondi dall'inizio del clip.

## <a name="remarks"></a>Commenti

Questo metodo restituisce **NULL se** il marcatore specificato non esiste.

Alcuni elementi multimediali digitali non contengono marcatori. Usare **markerCount** per scoprire quanti marcatori sono presenti nel clip corrente.

I numeri di indice dei marcatori iniziano da 1.

Per usare questo metodo, è necessario l'accesso in lettura alla libreria. Per altre informazioni, vedere [Accesso alla libreria](library-access.md).

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene utilizzato *Media*. **getMarkerTime per** riempire un elemento TEXTAREA HTML denominato MTIMES con la posizione di ogni marcatore. **L'oggetto** Player è stato creato con ID = "Player".


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
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto multimediale**](media-object.md)
</dt> <dt>

[**Media.getMarkerName**](media-getmarkername.md)
</dt> <dt>

[**Media.markerCount**](media-markercount.md)
</dt> <dt>

[**Impostazioni.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Impostazioni.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





