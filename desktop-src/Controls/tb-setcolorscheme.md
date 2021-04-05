---
title: Messaggio TB_SETCOLORSCHEME (COMmctrl. h)
description: Imposta le informazioni sulla combinazione di colori per il controllo Toolbar.
ms.assetid: 96cf6464-b760-46af-910f-984e41dbfca5
keywords:
- Controlli di Windows Message TB_SETCOLORSCHEME
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
ms.openlocfilehash: 0b4ed278ea31dfa156dcc8a64afdb98a2ae3b938
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874493"
---
# <a name="tb_setcolorscheme-message"></a>TB \_ SETCOLORSCHEME messaggio

Imposta le informazioni sulla combinazione di colori per il controllo Toolbar.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**ColorScheme**](/windows/win32/api/commctrl/ns-commctrl-colorscheme) che contiene le informazioni sulla combinazione di colori.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito per questo messaggio non viene utilizzato.

## <a name="remarks"></a>Commenti

Il controllo toolbar utilizza le informazioni sulla combinazione di colori quando si disegnano gli elementi 3D nel controllo.

Quando gli stili di visualizzazione sono abilitati, questo messaggio non ha alcun effetto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TB \_ GETCOLORSCHEME**](tb-getcolorscheme.md)
</dt> </dl>

 

 





