---
title: Media.markerCount
description: La proprietà markerCount recupera il numero di marcatori nell'elemento multimediale.
ms.assetid: 48313395-b225-4008-b0e8-82fa22d6aaef
keywords:
- Media.markerCount Windows Media Player
topic_type:
- apiref
api_name:
- Media.markerCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00206991f81c6a445648a063a37bcc45bf91f647b60317772478142eefd1b20e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123351"
---
# <a name="mediamarkercount"></a>Media.markerCount

La **proprietà markerCount** recupera il numero di marcatori nell'elemento multimediale.

## <a name="syntax"></a>Sintassi

*lettore*. *currentMedia.* **markerCount**

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un numero di sola **lettura** (**long**) che specifica il numero di marcatori nel file.

## <a name="remarks"></a>Commenti

Questa proprietà restituisce zero se un file non contiene marcatori o se l'elemento multimediale non corrisponde a *Player.* **currentMedia.**

I numeri dei marcatori iniziano da 1.

Per recuperare il valore di questa proprietà, è necessario l'accesso in lettura alla libreria. Per altre informazioni, vedere [Accesso alla libreria.](library-access.md)

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene utilizzato *Media*. **markerCount** per recuperare il numero di marcatori nell'elemento multimediale corrente. Tale valore viene quindi usato come limite superiore per una struttura di ciclo, che scorre l'elenco dei marcatori per recuperare il nome di ogni marcatore. Un elemento HTML TEXTAREA denominato MNAMES visualizza i nomi dei marcatori nell'elemento multimediale corrente. **L'oggetto Player** è stato creato con ID = "Player".


```JScript
// Get the number of markers in the current media item.
var mcount = Player.currentMedia.markerCount;

// Verify that at least one marker exists in the current media item.
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

 

 





