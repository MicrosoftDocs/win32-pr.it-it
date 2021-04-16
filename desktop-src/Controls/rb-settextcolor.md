---
title: Messaggio RB_SETTEXTCOLOR (COMmctrl. h)
description: Imposta il colore del testo predefinito del controllo Rebar.
ms.assetid: 85f120bd-39aa-43f8-a794-3bb4f3fe1cd4
keywords:
- Controlli di Windows Message RB_SETTEXTCOLOR
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
ms.openlocfilehash: 68311572927f2e8dac623c697ac366d37d7ab5fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477860"
---
# <a name="rb_settextcolor-message"></a>\_Messaggio SETTEXTCOLOR RB

Imposta il colore del testo predefinito del controllo Rebar.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Valore [**COLORREF**](/windows/desktop/gdi/colorref) che rappresenta il nuovo colore del testo predefinito.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore [**COLORREF**](/windows/desktop/gdi/colorref) che rappresenta il colore del testo predefinito precedente.

## <a name="remarks"></a>Commenti

Il colore del testo predefinito del controllo Rebar viene utilizzato per creare il testo in un controllo Rebar e tutte le bande aggiunte dopo l'invio del messaggio. Il colore del testo predefinito per una particolare banda può essere sottoposto a override quando si aggiunge o si modifica una banda impostando il \_ flag RBBIM Colors in **fmask** e impostando **clrBack** nella struttura [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**RB \_ GETTEXTCOLOR**](rb-gettextcolor.md)
</dt> </dl>

 

