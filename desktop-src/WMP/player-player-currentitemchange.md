---
title: Evento Player. CurrentItemChange
description: L'evento CurrentItemChange si verifica quando viene modificato Controls. currentItem.
ms.assetid: e6f68aeb-d7e7-460b-adc9-647f28c678a1
keywords:
- Media Player di Windows Event CurrentItemChange
- Windows Event CurrentItemChange Media Player, classe Player
- Classe Player Windows Media Player, evento CurrentItemChange
topic_type:
- apiref
api_name:
- Player.CurrentItemChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4c425184bf4b338177ec892ed5362c085dd8cb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332677"
---
# <a name="playercurrentitemchange-event"></a>Evento Player. CurrentItemChange

L'evento **CurrentItemChange** si verifica quando i *controlli*. **CurrentItem** modifiche.

## <a name="syntax"></a>Sintassi


```JScript
Player.CurrentItemChange()
```



## <a name="parameters"></a>Parametri

Questo evento non contiene parametri.

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene illustrato un gestore eventi per il *lettore*. evento **currentItemChange** . L'oggetto **Player** è stato creato con ID = "Player".


```JScript
<!-- Create an HTML text box to display the media item name. -->
<INPUT TYPE="TEXT" NAME="MEDIA">

<!-- Create an event handler. -->
<SCRIPT LANGUAGE = "JScript"  FOR = Player EVENT = currentItemChange()>

   // Display the name of the new media item.
   MEDIA.value = Player.currentMedia.name;

</SCRIPT>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Controls. currentItem**](controls-currentitem.md)
</dt> <dt>

[**Oggetto Player**](player-object.md)
</dt> </dl>

 

 





