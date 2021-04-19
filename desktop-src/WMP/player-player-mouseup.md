---
title: Evento Player. MouseUp
description: L'evento MouseUp si verifica quando l'utente rilascia un pulsante del mouse. | Evento Player. MouseUp
ms.assetid: 0f209fc4-2aad-46b1-84ba-2bfbecbe2930
keywords:
- Finestre eventi MouseUp Media Player
- Evento MouseUp Windows Media Player, classe Player
- Classe Player Windows Media Player, evento MouseUp
topic_type:
- apiref
api_name:
- Player.MouseUp
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50883ed8e5ea5696bd3aef1c5170959814de3026
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326466"
---
# <a name="playermouseup-event"></a>Evento Player. MouseUp

L'evento **MouseUp** si verifica quando l'utente rilascia un pulsante del mouse.

## <a name="syntax"></a>Sintassi


```JScript
Player.MouseUp(
  nButton,
  nShiftState,
  fX,
  fY
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Npulsante* 
</dt> <dd>

**Number** (**int**) che specifica un bit con bit corrispondenti al pulsante sinistro (bit 0), al pulsante destro (bit 1) e al pulsante centrale (bit 2). Questi bit corrispondono rispettivamente ai valori 1, 2 e 4. Viene impostato solo uno dei bit, che indica il pulsante che ha causato l'evento.

</dd> <dt>

*nShiftState* 
</dt> <dd>

**Number** (**int**) che specifica un bit con i bit meno significativi che corrispondono al tasto MAIUSC (bit 0), il tasto Ctrl (bit 1) e il tasto Alt (bit 2). Questi bit corrispondono rispettivamente ai valori 1, 2 e 4. L'argomento Shift indica lo stato di queste chiavi. È possibile impostare some, all o nessuno dei bit, a indicare che vengono premuti alcuni, tutti o nessuno dei tasti.

</dd> <dt>

*fX* 
</dt> <dd>

**Numero** (**Long**) che specifica la coordinata x del puntatore del mouse rispetto all'angolo superiore sinistro del controllo.

</dd> <dt>

*fY* 
</dt> <dd>

**Numero** (**Long**) che specifica la coordinata y del puntatore del mouse rispetto all'angolo superiore sinistro del controllo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Il valore dei parametri evento viene specificato da Windows Media Player ed è possibile accedervi o passarli a un metodo in un file JScript importato usando il nome del parametro specificato. Questo nome di parametro deve essere digitato esattamente come illustrato, incluse le maiuscole.

**Windows Media Player 10 Mobile:** Questo evento non è supportato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Player**](player-object.md)
</dt> </dl>

 

 





