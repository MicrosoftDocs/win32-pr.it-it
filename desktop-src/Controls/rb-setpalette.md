---
title: Messaggio RB_SETPALETTE (COMmctrl. h)
description: Imposta la tavolozza corrente del controllo Rebar.
ms.assetid: 85f0726a-21fd-41b3-aa52-6a0a0c1947fa
keywords:
- Controlli di Windows Message RB_SETPALETTE
topic_type:
- apiref
api_name:
- RB_SETPALETTE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7ee47985c05bcd8a857620e7fe501bddf53bdec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964549"
---
# <a name="rb_setpalette-message"></a>\_Messaggio della tavolozza RB

Imposta la tavolozza corrente del controllo Rebar.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Oggetto **HPALETTE** che specifica la nuova tavolozza che il controllo Rebar utilizzerà.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **HPALETTE** che specifica la tavolozza precedente del controllo Rebar.

## <a name="remarks"></a>Commenti

È responsabilità dell'applicazione che invia questo messaggio per eliminare il **HPALETTE** passato in questo messaggio (vedere [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)). Il controllo Rebar non eliminerà un set di **HPALETTE** con questo messaggio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_tavolozza RB**](rb-getpalette.md)
</dt> </dl>

 

