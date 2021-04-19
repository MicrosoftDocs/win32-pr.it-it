---
title: Media. getmarkname, metodo
description: Il metodo getmarkname Recupera il nome del marcatore in corrispondenza dell'indice specificato.
ms.assetid: 142438b7-88d1-4523-829f-52dafbf0a7a6
keywords:
- Metodo getmarkname Media Player Windows
- Metodo getmarkname Media Player Windows, classe media
- Media class Media Player Windows, metodo getmarkname
topic_type:
- apiref
api_name:
- Media.getMarkerName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69b923408432f76525b2dcf8cab046703fb76f80
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332545"
---
# <a name="mediagetmarkername-method"></a>Media. getmarkname, metodo

Il metodo **Getmarkname** Recupera il nome del marcatore in corrispondenza dell'indice specificato.

## <a name="syntax"></a>Sintassi


```JScript
strRetVal = Media.getMarkerName(
  markerNum
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*markerNum* \[ in\]
</dt> <dd>

**Numero** (**Long**) che specifica un indice del marcatore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce una **stringa**.

## <a name="remarks"></a>Commenti

Questo metodo restituisce **null** se il marcatore specificato non esiste.

Alcuni elementi multimediali digitali non contengono marcatori. Usare **markerCount** per verificare il numero di marcatori presenti nella clip corrente.

I numeri di indice del marcatore iniziano da 1.

Per usare questo metodo, è necessario l'accesso in lettura alla libreria. Per altre informazioni, vedere [accesso alla libreria](library-access.md).

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene usato il *supporto*. **Getmarkername** per inserire un elemento textarea HTML denominato MNAMES con i nomi dei marcatori nell'elemento multimediale corrente. L'oggetto **Player** è stato creato con ID = "Player".


```JScript
// Get the number of markers in the current media item.
var mcount = Player.currentMedia.markerCount;

// Verify that at least one marker exists in the current media.
if (mcount > 0){

// Loop through the marker list.
for (var i = 1; i < mcount + 1; i++){

   // Print the marker name to the text area.
   MNAMES.value += Player.currentMedia.getMarkerName(i);
   MNAMES.value += "\n";
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

[**Media. getMarkerTime**](media-getmarkertime.md)
</dt> <dt>

[**Media. markerCount**](media-markercount.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





