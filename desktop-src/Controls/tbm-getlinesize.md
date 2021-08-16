---
title: TBM_GETLINESIZE messaggio (Commctrl.h)
description: Recupera il numero di posizioni logiche che il dispositivo di scorrimento del trackbar sposta in risposta all'input della tastiera dai tasti di direzione, ad esempio i tasti o . Le posizioni logiche sono gli incrementi interi nell'intervallo di posizioni del dispositivo di scorrimento minimo/massimo del trackbar.
ms.assetid: b596060a-5bac-4b31-82f3-ee4744a9779c
keywords:
- TBM_GETLINESIZE dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- TBM_GETLINESIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e6db69efda8a6836f8c366092871cbb6b54261021a69c80e2bb14abcd88d967
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046561"
---
# <a name="tbm_getlinesize-message"></a>Messaggio \_ GETLINESIZE TBM

Recupera il numero di posizioni logiche che il dispositivo di scorrimento del trackbar sposta in risposta all'input della tastiera dai tasti di direzione, ad esempio i tasti o . Le posizioni logiche sono gli incrementi interi nell'intervallo di posizioni del dispositivo di scorrimento minimo/massimo del trackbar.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore a 32 bit che specifica le dimensioni della linea per il trackbar.

## <a name="remarks"></a>Commenti

L'impostazione predefinita per le dimensioni della linea è 1.

Il trackbar invia anche un messaggio [**WM \_ HSCROLL**](wm-hscroll.md) o [**WM \_ VSCROLL**](wm-vscroll.md) con i codici di notifica TB LINEUP e TB LINEDOWN alla finestra padre quando l'utente preme \_ i tasti di \_ direzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





