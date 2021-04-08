---
title: Messaggio TB_GETITEMDROPDOWNRECT (COMmctrl. h)
description: Ottiene il rettangolo di delimitazione della finestra a discesa per un elemento della barra degli strumenti con stile \_ elenco a discesa BTNS.
ms.assetid: 4b59c96b-8d75-44c1-b771-c1d62502a2c2
keywords:
- Controlli di Windows Message TB_GETITEMDROPDOWNRECT
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
ms.openlocfilehash: dbcbcef725b0ade0bfc776200fa5b191618d2ccb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047987"
---
# <a name="tb_getitemdropdownrect-message"></a>TB \_ GETITEMDROPDOWNRECT messaggio

Ottiene il rettangolo di delimitazione della finestra a discesa per un elemento della barra degli strumenti con stile [**\_ elenco a discesa BTNS**](toolbar-control-and-button-styles.md).

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

Indice in base zero dell'elemento di controllo della barra degli strumenti per il quale recuperare il rettangolo di delimitazione.

</dd> <dt>

*lParam* \[ in uscita\]
</dt> <dd>Puntatore a una struttura <a href="/previous-versions//dd162897(v=vs.85)">**Rect**</a> per ricevere le informazioni sul rettangolo di delimitazione. Il mittente del messaggio è responsabile dell'allocazione della struttura. Le coordinate restituite nella struttura **Rect** sono espresse come coordinate client.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce sempre un valore diverso da zero.

## <a name="remarks"></a>Commenti

L'elemento deve avere lo stile a [**\_ discesa BTNS**](toolbar-control-and-button-styles.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

