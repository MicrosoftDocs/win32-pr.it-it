---
title: HKM_GETHOTKEY messaggio (Commctrl.h)
description: Ottiene il codice del tasto virtuale e i flag di modifica di un tasto di scelta rapida da un controllo tasto di scelta rapida.
ms.assetid: 8b061411-604d-46ea-a082-3eca2d47d992
keywords:
- HKM_GETHOTKEY controlli Windows messaggio
topic_type:
- apiref
api_name:
- HKM_GETHOTKEY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79bfbad1eb5e9a6679a1b3e419a0877e61cd90247ef0cf91b0a30c655f755a57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118672269"
---
# <a name="hkm_gethotkey-message"></a>Messaggio \_ HKM GETHOTKEY

Ottiene il codice del tasto virtuale e i flag di modifica di un tasto di scelta rapida da un controllo tasto di scelta rapida.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il codice del tasto virtuale e i flag di modifica. Il [**LOBYTE**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85)) della [**parola chiave LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) è il codice della chiave virtuale del tasto di scelta rapida. [**L'HIBYTE**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85)) della **parola chiave LOWORD** è il modificatore di tasto che specifica i tasti che definiscono una combinazione di tasti di scelta rapida. I flag di modifica possono essere una combinazione dei valori seguenti.



| Valore            | Significato      |
|------------------|--------------|
| TASTO DI SCELTA \_ RAPIDAF ALT     | ALT (tasto)      |
| CONTROLLO \_ HOTKEYF | Tasto CTRL  |
| HOTKEYF \_ EXT     | Chiave estesa |
| TASTO DI SCELTA \_ RAPIDAF MAIUSC   | MAIUSC    |



 

## <a name="remarks"></a>Commenti

Il valore a 16 bit restituito da questo messaggio può essere usato come parametro *wParam* nel [**messaggio WM \_ SETHOTKEY.**](/windows/desktop/inputdev/wm-sethotkey)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

