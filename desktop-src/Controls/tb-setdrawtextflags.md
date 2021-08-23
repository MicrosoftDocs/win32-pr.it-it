---
title: TB_SETDRAWTEXTFLAGS messaggio (Commctrl.h)
description: Imposta i flag di disegno del testo per la barra degli strumenti.
ms.assetid: b088af32-ea8a-4304-89f1-a7cec5497f85
keywords:
- TB_SETDRAWTEXTFLAGS di controllo Windows messaggio
topic_type:
- apiref
api_name:
- TB_SETDRAWTEXTFLAGS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 849bbb0e661c9e8afe246894d2d2f59d99d15a3f096ad2295a7018cf3df26ca4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119543881"
---
# <a name="tb_setdrawtextflags-message"></a>TB \_ SETDRAWTEXTFLAGS message

Imposta i flag di disegno del testo per la barra degli strumenti.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Uno o più flag \_ DT, specificati in [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext), che indicano quali bit in *lParam* verranno usati durante il disegno del testo.

</dd> <dt>

*lParam* 
</dt> <dd>

Uno o più flag \_ DT, specificati in [**DrawText,**](/windows/desktop/api/winuser/nf-winuser-drawtext)che indicano come verrà disegnato il testo del pulsante. Questo valore verrà passato alla funzione **DrawText** quando viene disegnato il testo del pulsante.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce i flag di disegno del testo precedenti.

## <a name="remarks"></a>Commenti

Il *parametro wParam* consente di specificare quali flag verranno usati durante il disegno del testo, anche se questi flag sono disattivati. Ad esempio, se non si vuole usare il flag DT CENTER durante il disegno del testo, aggiungere il flag DT CENTER a wParam e non specificare il \_ \_ flag DT CENTER in  \_ *lParam*. Ciò impedisce al controllo di passare il flag DT \_ CENTER alla [**funzione DrawText.**](/windows/desktop/api/winuser/nf-winuser-drawtext)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

