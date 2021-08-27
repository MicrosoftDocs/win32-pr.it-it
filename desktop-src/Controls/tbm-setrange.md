---
title: TBM_SETRANGE messaggio (Commctrl.h)
description: Imposta l'intervallo di posizioni logiche minime e massime per il dispositivo di scorrimento in un trackbar.
ms.assetid: 9c225742-8e5e-4f47-af8c-8243b6c90c1d
keywords:
- TBM_SETRANGE di controllo Windows messaggio
topic_type:
- apiref
api_name:
- TBM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfcd4bf71cfcbc36e098bc83568bdf519209ec82cc9889b6b5ec3934d349f737
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061141"
---
# <a name="tbm_setrange-message"></a>Messaggio \_ SETRANGE TBM

Imposta l'intervallo di posizioni logiche minime e massime per il dispositivo di scorrimento in un trackbar.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Flag di ridisegno. Se questo parametro è **TRUE,** il trackbar viene ridisegnato dopo l'impostazione dell'intervallo. Se questo parametro è **FALSE,** il messaggio imposta l'intervallo ma non ridisegna il trackbar.

</dd> <dt>

*lParam* 
</dt> <dd>

LOWORD specifica la posizione minima per il dispositivo di scorrimento e [**la parola chiave HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica la posizione massima. [](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Se la posizione corrente del dispositivo di scorrimento non rientra nel nuovo intervallo, il messaggio **\_ TBM SETRANGE** imposta la posizione del dispositivo di scorrimento sul nuovo valore massimo o minimo.

Poiché questo messaggio accetta due valori integer senza segno a 16 bit, l'intervallo massimo che questo messaggio può specificare è compreso tra 0 e 65.535. Per specificare valori di intervallo più grandi, usare [**i messaggi \_ TBM SETRANGEMIN**](tbm-setrangemin.md) e [**TBM \_ SETRANGEMAX.**](tbm-setrangemax.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**TBM \_ SETRANGEMAX**](tbm-setrangemax.md)
</dt> <dt>

[**TBM \_ SETRANGEMIN**](tbm-setrangemin.md)
</dt> </dl>

 

