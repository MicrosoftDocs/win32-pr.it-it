---
title: Media. markerCount
description: La proprietà markerCount Recupera il numero di marcatori nell'elemento multimediale.
ms.assetid: 48313395-b225-4008-b0e8-82fa22d6aaef
keywords:
- Media Player Windows Media. markerCount
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
ms.openlocfilehash: c97a874211c0c00ebf9f242887d4314ec490b552
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329307"
---
# <a name="mediamarkercount"></a>Media. markerCount

La proprietà **markerCount** Recupera il numero di marcatori nell'elemento multimediale.

## <a name="syntax"></a>Sintassi

*Player*. *currentMedia*. **markerCount**

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un **numero** di sola lettura (**Long**) che specifica il numero di marcatori nel file.

## <a name="remarks"></a>Commenti

Questa proprietà restituisce zero se un file non ha marcatori o se l'elemento multimediale non è uguale a *Player*. **currentMedia**.

I numeri degli indicatori iniziano da 1.

Per recuperare il valore di questa proprietà, è necessario l'accesso in lettura alla libreria. Per altre informazioni, vedere [accesso alla libreria](library-access.md).

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene usato il *supporto*. **markerCount** per recuperare il numero di marcatori nell'elemento multimediale corrente. Tale valore viene quindi utilizzato come limite superiore per una struttura di ciclo, che scorre l'elenco dei marcatori per recuperare ogni nome del marcatore. Un elemento TEXTAREA HTML denominato MNAMES Visualizza i nomi dei marcatori nell'elemento multimediale corrente. L'oggetto **Player** è stato creato con ID = "Player".


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

 

 





