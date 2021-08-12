---
title: Evento Player.PlayStateChange
description: L'evento PlayStateChange si verifica quando viene apportata una modifica alla proprietà playState.
ms.assetid: d4c4b114-04b6-4079-b6a2-52b336fc6dc1
keywords:
- Eventi PlayStateChange Windows Media Player
- Evento PlayStateChange Windows Media Player , classe Player
- Classe player Windows Media Player, evento PlayStateChange
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
ms.openlocfilehash: 3995f7373984ae9e3b0e24f9f41390154326cfd87bd8589970dc76520c6efd93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118572527"
---
# <a name="playerplaystatechange-event"></a>Evento Player.PlayStateChange

**L'evento PlayStateChange** si verifica quando viene apportata una modifica alla **proprietà playState.**

## <a name="syntax"></a>Sintassi


```JScript
Player.PlayStateChange(
  NewState
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Newstate* 
</dt> <dd>

Numero (**long**) che specifica il nuovo **playState**. Vedere [playState](player-playstate.md) per una tabella dei valori possibili.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Il valore dei parametri dell'evento viene specificato da Windows Media Player ed è accessibile o passato a un metodo in un file JScript importato usando il nome del parametro specificato. Questo nome di parametro deve essere digitato esattamente come illustrato, inclusa l'maiuscola.

Windows Media Player non è garantito che gli stati si verifichino in un ordine specifico. Inoltre, non tutti gli stati si verificano necessariamente durante una sequenza di eventi. Non è consigliabile scrivere codice che si basa sull'ordine di stato.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato un gestore eventi per *player*. **evento playStateChange.** Un elemento di testo HTML, denominato "myText", visualizza il nuovo stato di riproduzione. L'oggetto lettore è stato creato con ID = "Player".


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
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Player**](player-object.md)
</dt> <dt>

[**Player.playState**](player-playstate.md)
</dt> </dl>

 

 





