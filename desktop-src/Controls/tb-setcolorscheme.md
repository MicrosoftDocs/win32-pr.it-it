---
title: TB_SETCOLORSCHEME messaggio (Commctrl.h)
description: Imposta le informazioni sulla combinazione colori per il controllo barra degli strumenti.
ms.assetid: 96cf6464-b760-46af-910f-984e41dbfca5
keywords:
- TB_SETCOLORSCHEME di controllo Windows messaggio
topic_type:
- apiref
api_name:
- TB_SETCOLORSCHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58c6a07c186fd3f5a521719ba0f75f8e468c3868d8ebfaa0595679d48b45089f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118167501"
---
# <a name="tb_setcolorscheme-message"></a>TB \_ SETCOLORSCHEME message

Imposta le informazioni sulla combinazione colori per il controllo barra degli strumenti.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura COLORSCHEME**](/windows/win32/api/commctrl/ns-commctrl-colorscheme) che contiene le informazioni sulla combinazione di colori.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito per questo messaggio non viene utilizzato.

## <a name="remarks"></a>Commenti

Il controllo barra degli strumenti usa le informazioni sulla combinazione di colori quando si disegnano gli elementi 3D nel controllo.

Quando gli stili di visualizzazione sono abilitati, questo messaggio non ha alcun effetto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TB \_ GETCOLORSCHEME**](tb-getcolorscheme.md)
</dt> </dl>

 

 





