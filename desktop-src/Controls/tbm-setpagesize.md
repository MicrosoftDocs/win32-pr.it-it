---
title: TBM_SETPAGESIZE messaggio (Commctrl.h)
description: Imposta il numero di posizioni logiche in cui il dispositivo di scorrimento del trackbar si sposta in risposta all'input da tastiera, ad esempio i tasti o , o l'input del mouse, ad esempio i clic nel canale del trackbar.
ms.assetid: 34edb868-4b6b-4b3f-b315-3ce39346b134
keywords:
- TBM_SETPAGESIZE controlli di Windows messaggio
topic_type:
- apiref
api_name:
- TBM_SETPAGESIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87cf41547a996e9726002101998ea859b7dbc6cc3e7ed3f87927fdae8bdadd2f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046101"
---
# <a name="tbm_setpagesize-message"></a>TBM \_ SETPAGESIZE message

Imposta il numero di posizioni logiche in cui il dispositivo di scorrimento del trackbar si sposta in risposta all'input da tastiera, ad esempio i tasti o , o l'input del mouse, ad esempio i clic nel canale del trackbar. Le posizioni logiche sono gli incrementi di interi nell'intervallo tra le posizioni minime e massime del dispositivo di scorrimento del trackbar.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Nuove dimensioni di pagina.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore a 32 bit che specifica le dimensioni della pagina precedente.

## <a name="remarks"></a>Commenti

Il trackbar invia anche un messaggio [**WM \_ HSCROLL**](wm-hscroll.md) o [**WM \_ VSCROLL**](wm-vscroll.md) con i codici di notifica TB PAGEUP e TB PAGEDOWN alla relativa finestra padre quando riceve l'input da tastiera o mouse che scorre la \_ \_ pagina.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TBM \_ GETPAGESIZE**](tbm-getpagesize.md)
</dt> </dl>

 

 





