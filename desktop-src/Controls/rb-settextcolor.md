---
title: RB_SETTEXTCOLOR messaggio (Commctrl.h)
description: Imposta il colore del testo predefinito di un controllo Rebar.
ms.assetid: 85f120bd-39aa-43f8-a794-3bb4f3fe1cd4
keywords:
- RB_SETTEXTCOLOR dei controlli Windows messaggio
topic_type:
- apiref
api_name:
- RB_SETTEXTCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88458f5a131250dbb261040bf26689356c1ba5446db854839ded05ff287a14ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078615"
---
# <a name="rb_settextcolor-message"></a>Messaggio RB \_ SETTEXTCOLOR

Imposta il colore del testo predefinito di un controllo Rebar.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

[**Valore COLORREF**](/windows/desktop/gdi/colorref) che rappresenta il nuovo colore del testo predefinito.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un [**valore COLORREF**](/windows/desktop/gdi/colorref) che rappresenta il colore del testo predefinito precedente.

## <a name="remarks"></a>Commenti

Il colore del testo predefinito del controllo Rebar viene usato per disegnare il testo in un controllo Rebar e in tutte le bande aggiunte dopo l'invio del messaggio. Il colore del testo predefinito per una determinata banda può essere sostituito quando una banda viene aggiunta o modificata impostando il flag RBBIM \_ COLORS in **fMask** e impostando **clrBack** nella struttura [**REBARBANDINFO.**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**RB \_ GETTEXTCOLOR**](rb-gettextcolor.md)
</dt> </dl>

 

