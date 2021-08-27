---
title: TBM_GETPAGESIZE messaggio (Commctrl.h)
description: Recupera il numero di posizioni logiche in cui il dispositivo di scorrimento del trackbar si sposta in risposta all'input da tastiera, ad esempio i tasti o , o l'input del mouse, ad esempio i clic nel canale del trackbar.
ms.assetid: f0c5feac-2723-440e-96c0-dac37b0531ed
keywords:
- TBM_GETPAGESIZE controlli Windows messaggio
topic_type:
- apiref
api_name:
- TBM_GETPAGESIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1aa3ef3412fd00c18972b62d4d868ff1dbc97cb4787693b3746281b4884706e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046501"
---
# <a name="tbm_getpagesize-message"></a>Messaggio \_ GETPAGESIZE TBM

Recupera il numero di posizioni logiche in cui il dispositivo di scorrimento del trackbar si sposta in risposta all'input da tastiera, ad esempio i tasti o , o l'input del mouse, ad esempio i clic nel canale del trackbar. Le posizioni logiche sono gli incrementi di interi nell'intervallo tra le posizioni minime e massime del dispositivo di scorrimento del trackbar.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore a 32 bit che specifica le dimensioni della pagina per il trackbar.

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

[**TBM \_ SETPAGESIZE**](tbm-setpagesize.md)
</dt> </dl>

 

 





