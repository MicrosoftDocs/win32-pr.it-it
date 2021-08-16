---
title: Evento Player.MouseMove
description: L'evento MouseMove si verifica quando il puntatore del mouse viene spostato. | Evento Player.MouseMove
ms.assetid: 026928a3-25a6-4e67-837a-df71c05e49ee
keywords:
- Evento MouseMove Windows Media Player
- Classe di evento MouseMove Windows Media Player , Player
- Classe Player Windows Media Player, evento MouseMove
topic_type:
- apiref
api_name:
- Player.MouseMove
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb864e2a8bf686bd39f2d44ba8f5558516d72034f606579a79c76a5d86ab3990
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118338098"
---
# <a name="playermousemove-event"></a>Evento Player.MouseMove

**L'evento MouseMove** si verifica quando il puntatore del mouse viene spostato.

## <a name="syntax"></a>Sintassi


```JScript
Player.MouseMove(
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

**Numero** (**int**) che specifica un campo di bit con bit corrispondenti al pulsante sinistro (bit 0), al pulsante destro (bit 1) e al pulsante centrale (bit 2). Questi bit corrispondono rispettivamente ai valori 1, 2 e 4. Alcuni, tutti o nessuno dei bit possono essere impostati, a indicare che alcuni, tutti o nessuno dei pulsanti sono premuti.

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

 

 





