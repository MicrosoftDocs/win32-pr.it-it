---
title: Evento Player.CurrentItemChange
description: L'evento CurrentItemChange si verifica quando viene modificato Controls.currentItem.
ms.assetid: e6f68aeb-d7e7-460b-adc9-647f28c678a1
keywords:
- Evento CurrentItemChange Windows Media Player
- Evento CurrentItemChange Windows Media Player , classe Player
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
ms.openlocfilehash: 5ed0ca3c8333c7261c8332bcc124c905c5540f5cdf0dbefe3f34f121eb901cc3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118338126"
---
# <a name="playercurrentitemchange-event"></a>Evento Player.CurrentItemChange

**L'evento CurrentItemChange** si verifica quando *controls*. **modifiche currentItem.**

## <a name="syntax"></a>Sintassi


```JScript
Player.CurrentItemChange()
```



## <a name="parameters"></a>Parametri

Questo evento non ha parametri.

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="examples"></a>Esempio

Nell'JScript seguente viene illustrato un gestore eventi per *player*. **Evento currentItemChange.** **L'oggetto** Player è stato creato con ID = "Player".


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
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Controls.currentItem**](controls-currentitem.md)
</dt> <dt>

[**Oggetto Player**](player-object.md)
</dt> </dl>

 

 





