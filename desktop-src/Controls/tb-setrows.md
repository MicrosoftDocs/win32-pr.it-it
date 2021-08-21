---
title: TB_SETROWS messaggio (Commctrl.h)
description: Imposta il numero di righe di pulsanti in una barra degli strumenti.
ms.assetid: d8ea7b80-d23e-4593-8eb1-d23808173fc9
keywords:
- TB_SETROWS dei controlli Windows messaggio
topic_type:
- apiref
api_name:
- TB_SETROWS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2c0e95d6f0f19c2b1c9b76cf22a37da0086987b22fe144603cdb2afa8a1ad83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119293641"
---
# <a name="tb_setrows-message"></a>TB \_ SETROWS message

Imposta il numero di righe di pulsanti in una barra degli strumenti.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

LoWORD [**specifica**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) il numero di righe richieste. Il numero minimo di righe è uno e il numero massimo di righe è uguale al numero di pulsanti nella barra degli strumenti.

[**HIWORD è**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) un **valore BOOL** che indica se creare più righe di quelle richieste quando il sistema non è in grado di creare il numero di righe specificato da *wParam*. Se **TRUE,** il sistema crea più righe. Se **FALSE,** il sistema crea meno righe.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura RECT**](/previous-versions//dd162897(v=vs.85)) che riceve il rettangolo di delimitazione della barra degli strumenti dopo l'impostazione delle righe.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Poiché il sistema non suddivide i gruppi di pulsanti quando si imposta il numero di righe, il numero di righe risultante potrebbe essere diverso dal numero richiesto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

