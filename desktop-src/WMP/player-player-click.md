---
title: Evento Player.Click
description: L'evento Click si verifica quando l'utente fa clic su un pulsante del mouse.
ms.assetid: c2d5fab9-9b53-4d0c-a001-8cbf4430e713
keywords:
- Evento Click Windows Media Player
- Evento Click Windows Media Player , classe Player
- Classe player Windows Media Player, evento Click
topic_type:
- apiref
api_name:
- Player.Click
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b60e6368c6ccb70d0bc87c9fc2d1d99770b4fa36dfe957365d48a2e26c00a163
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995931"
---
# <a name="playerclick-event"></a>Evento Player.Click

**L'evento Click** si verifica quando l'utente fa clic su un pulsante del mouse.

## <a name="syntax"></a>Sintassi


```JScript
Player.Click(
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

**Numero** (**int**) che specifica un campo di bit con bit corrispondenti al pulsante sinistro (bit 0), al pulsante destro (bit 1) e al pulsante centrale (bit 2). Questi bit corrispondono rispettivamente ai valori 1, 2 e 4. Viene impostato solo uno dei bit , che indica il pulsante che ha causato l'evento.

</dd> <dt>

*nShiftState* 
</dt> <dd>

**Numero** (**int**) che specifica un campo di bit con i bit meno significativi corrispondenti al tasto MAIUSC (bit 0), al tasto CTRL (bit 1) e al tasto ALT (bit 2). Questi bit corrispondono rispettivamente ai valori 1, 2 e 4. L'argomento shift indica lo stato di queste chiavi. È possibile impostare alcuni, tutti o nessuno dei bit, a indicare che vengono premuti alcuni, tutti o nessuno dei tasti.

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

Il valore dei parametri dell'evento viene specificato da Windows Media Player e può essere accessibile o passato a un metodo in un file JScript importato usando il nome del parametro specificato. Questo nome di parametro deve essere digitato esattamente come illustrato, inclusa l'maiuscola.

**Windows Media Player 10 Mobile:** Questo evento non è supportato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player serie 9 o successiva.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Player**](player-object.md)
</dt> </dl>

 

 





