---
title: ClosedCaption.captioningID
description: La proprietà captioningID specifica o Recupera il nome dell'elemento che visualizza la didascalia.
ms.assetid: 99d4aae3-485f-4c86-9130-101b1ca968e9
keywords:
- Media Player Windows ClosedCaption. captioningID
topic_type:
- apiref
api_name:
- ClosedCaption.captioningID
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faadae626dd5ac0314c4140e3f9d82ab645ef9b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106323908"
---
# <a name="closedcaptioncaptioningid"></a>ClosedCaption.captioningID

La proprietà **captioningID** specifica o Recupera il nome dell'elemento che visualizza la didascalia.

``` syntax
player.closedCaption.captioningID
```

## <a name="possible-values"></a>Valori possibili

Questa proprietà è una **stringa** di lettura/scrittura.

## <a name="remarks"></a>Commenti

Il nome dell'elemento specificato può essere qualsiasi elemento HTML nella pagina Web, purché supporti l'attributo innerHTML. Se la pagina Web contiene più frame, il nome dell'elemento può fare riferimento solo a un elemento nello stesso frame del controllo lettore.

**Windows Media Player 10 Mobile:** Questa proprietà è di sola lettura e restituisce sempre una stringa vuota.

## <a name="examples"></a>Esempio

Nell'esempio Microsoft JScript seguente viene usato *ClosedCaption*. **captioningID** per scegliere l'area di una pagina Web utilizzata per visualizzare le didascalie. Sono stati creati due elementi DIV HTML con ID = CC1 e ID = CC2, rispettivamente. L'oggetto **Player** è stato creato con ID = "Player".


```JScript
<!-- Create two HTML BUTTON elements to allow the user to choose a display region. -->
<INPUT TYPE = "BUTTON"  NAME = "SET1"  VALUE = "Move Caption to CC1"
       OnClick = "
           /* Clear the caption text from the other DIV */
           CC2.innerHTML = 'This is the CC2 DIV';

           /* Show the captions in the DIV named CC1. */ 
           Player.ClosedCaption.captioningID = 'CC1';
          ">

<INPUT TYPE = "BUTTON" NAME = "SET2" VALUE = "Move Caption to CC2"
       OnClick = "
           /* Clear the caption text from the other DIV */
           CC1.innerHTML = 'This is the CC1 DIV';

           /* Show the captions in the DIV named CC2. */
           Player.ClosedCaption.captioningID = 'CC2';
          ">

```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Aggiunta di didascalie chiuse a file multimediali digitali**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Oggetto ClosedCaption**](closedcaption-object.md)
</dt> </dl>

 

 





