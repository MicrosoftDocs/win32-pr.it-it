---
title: Evento Player. PlayStateChange
description: L'evento PlayStateChange si verifica quando viene apportata una modifica alla proprietà riproduzione.
ms.assetid: d4c4b114-04b6-4079-b6a2-52b336fc6dc1
keywords:
- Media Player di Windows Event PlayStateChange
- Windows Event PlayStateChange Media Player, classe Player
- Classe Player Windows Media Player, evento PlayStateChange
topic_type:
- apiref
api_name:
- Player.PlayStateChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e621d8698a5379b0d39a55db141fc0012f6ef969
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326001"
---
# <a name="playerplaystatechange-event"></a>Evento Player. PlayStateChange

L'evento **PlayStateChange** si verifica quando viene apportata una modifica alla proprietà **riproduzione** .

## <a name="syntax"></a>Sintassi


```JScript
Player.PlayStateChange(
  NewState
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*NewState* 
</dt> <dd>

Numero (**Long**) che specifica il nuovo **riproduzione**. Per una tabella dei valori possibili, vedere [riproduzione](player-playstate.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Il valore dei parametri evento viene specificato da Windows Media Player ed è possibile accedervi o passarli a un metodo in un file JScript importato usando il nome del parametro specificato. Questo nome di parametro deve essere digitato esattamente come illustrato, incluse le maiuscole.

Non è garantito che gli Stati di Windows Media Player vengano eseguiti in un ordine particolare. Inoltre, non tutti gli Stati si verificano necessariamente durante una sequenza di eventi. Non è necessario scrivere codice che si basa sull'ordine di stato.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato un gestore eventi per il *lettore*. evento **playStateChange** . Un elemento di testo HTML, denominato "testo", Visualizza il nuovo stato di riproduzione. L'oggetto Player è stato creato con ID = "Player".


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player EVENT = playStateChange(NewState)>

// Test for the player current state, display a message for each.
switch (NewState){
    case 1:
        myText.value = "Stopped";
        break;

    case 2:
        myText.value = "Paused";
        break;

    case 3:
        myText.value = "Playing";
        break;

    // Other cases go here.

    default:
        myText.value = "";
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

[**Oggetto Player**](player-object.md)
</dt> <dt>

[**Player. riproduzione**](player-playstate.md)
</dt> </dl>

 

 





