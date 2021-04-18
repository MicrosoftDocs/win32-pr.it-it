---
title: Messaggio RB_SETBKCOLOR (COMmctrl. h)
description: Imposta il colore di sfondo predefinito del controllo Rebar.
ms.assetid: 450a1e16-24f6-4f86-8e46-14009da05efc
keywords:
- Controlli di Windows Message RB_SETBKCOLOR
topic_type:
- apiref
api_name:
- RB_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa9365de2d790b1f28b1330c038b69d30b208143
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301836"
---
# <a name="rb_setbkcolor-message"></a>\_Messaggio SETBKCOLOR RB

Imposta il colore di sfondo predefinito del controllo Rebar.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Valore [**COLORREF**](/windows/desktop/gdi/colorref) che rappresenta il nuovo colore di sfondo predefinito.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore [**COLORREF**](/windows/desktop/gdi/colorref) che rappresenta il colore di sfondo predefinito precedente.

## <a name="remarks"></a>Commenti

Il colore di sfondo predefinito del controllo Rebar viene utilizzato per creare lo sfondo in un controllo Rebar e tutte le bande aggiunte dopo l'invio del messaggio. Il colore di sfondo predefinito per una particolare banda può essere sottoposto a override quando si aggiunge o si modifica una banda impostando il \_ flag RBBIM Colors in **fmask** e impostando **clrBack** nella struttura [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) .

Quando gli stili di visualizzazione sono abilitati, questo messaggio non ha alcun effetto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**RB \_ GETBKCOLOR**](rb-getbkcolor.md)
</dt> </dl>

 

