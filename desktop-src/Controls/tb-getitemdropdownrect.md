---
title: TB_GETITEMDROPDOWNRECT messaggio (Commctrl.h)
description: Ottiene il rettangolo di delimitazione della finestra a discesa per un elemento della barra degli strumenti con stile BTNS \_ DROPDOWN.
ms.assetid: 4b59c96b-8d75-44c1-b771-c1d62502a2c2
keywords:
- TB_GETITEMDROPDOWNRECT dei messaggi Windows controllo
topic_type:
- apiref
api_name:
- TB_GETITEMDROPDOWNRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecd2dfc8a48ff735bfb8bcc99bc0baf36555eee9d995c3f453a95ea2910948a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119918701"
---
# <a name="tb_getitemdropdownrect-message"></a>TB \_ GETITEMDROPDOWNRECT message

Ottiene il rettangolo di delimitazione della finestra a discesa per un elemento della barra degli strumenti con stile [**BTNS \_ DROPDOWN.**](toolbar-control-and-button-styles.md)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ Pollici\]
</dt> <dd>

Indice in base zero dell'elemento del controllo barra degli strumenti per il quale recuperare il rettangolo di delimitazione.

</dd> <dt>

*lParam* \[ in, out\]
</dt> <dd>Puntatore a una struttura <a href="/previous-versions//dd162897(v=vs.85)">**RECT**</a> per ricevere le informazioni sul rettangolo di delimitazione. Il mittente del messaggio è responsabile dell'allocazione di questa struttura. Le coordinate restituite nella struttura **RECT** sono espresse come coordinate client.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce sempre un valore diverso da zero.

## <a name="remarks"></a>Commenti

L'elemento deve avere lo [**stile BTNS \_ DROPDOWN.**](toolbar-control-and-button-styles.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

