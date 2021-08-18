---
title: Evento Player.DoubleClick
description: L'evento DoubleClick si verifica quando l'utente fa doppio clic su un pulsante del mouse.
ms.assetid: e2055cff-e4b0-49e3-a93a-7084789b6842
keywords:
- Evento DoubleClick Windows Media Player
- Evento DoubleClick Windows Media Player , classe Player
- Classe player Windows Media Player , evento DoubleClick
topic_type:
- apiref
api_name:
- Player.DoubleClick
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67a8e6a21c46a8b1c5d7960d70233e38333f9ff2052826bb68d573d4b2f0cd15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995921"
---
# <a name="playerdoubleclick-event"></a>Evento Player.DoubleClick

**L'evento DoubleClick** si verifica quando l'utente fa doppio clic su un pulsante del mouse.

## <a name="syntax"></a>Sintassi


```JScript
Player.DoubleClick(
  nButton,
  nShiftState,
  fX,
  fY
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*nButton* 
</dt> <dd>

**Numero** (**int**) che specifica un campo di bit con bit corrispondenti al pulsante sinistro (bit 0), al pulsante destro (bit 1) e al pulsante centrale (bit 2). Questi bit corrispondono rispettivamente ai valori 1, 2 e 4. Viene impostato solo uno dei bit, che indica il pulsante che ha causato l'evento.

</dd> <dt>

*nShiftState* 
</dt> <dd>

**Numero** (**int**) che specifica un campo di bit con i bit meno significativi corrispondenti al tasto MAIUSC (bit 0), al tasto CTRL (bit 1) e al tasto ALT (bit 2). Questi bit corrispondono rispettivamente ai valori 1, 2 e 4. L'argomento shift indica lo stato di queste chiavi. Alcuni, tutti o nessuno dei bit possono essere impostati, a indicare che alcuni, tutti o nessuno dei tasti vengono premuti.

</dd> <dt>

*Fx* 
</dt> <dd>

**Numero** (**long**) che specifica la coordinata x del puntatore del mouse rispetto all'angolo superiore sinistro del controllo.

</dd> <dt>

*Fy* 
</dt> <dd>

**Numero** (**long**) che specifica la coordinata y del puntatore del mouse rispetto all'angolo superiore sinistro del controllo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Il valore dei parametri dell'evento viene specificato da Windows Media Player ed è accessibile o passato a un metodo in un file JScript importato usando il nome del parametro specificato. Questo nome di parametro deve essere digitato esattamente come illustrato, inclusa l'maiuscola.

**Windows Media Player 10 Mobile:** Questo evento non è supportato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player serie 9 o successive.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Player**](player-object.md)
</dt> </dl>

 

 





