---
title: TBM_SETPOSNOTIFY messaggio (Commctrl.h)
description: 'TBM_SETPOSNOTIFY: imposta la posizione logica corrente del dispositivo di scorrimento in un trackbar.'
ms.assetid: 02f8899a-55b0-46ae-8642-9e534ab4abf5
keywords:
- TBM_SETPOSNOTIFY controlli Windows messaggio
topic_type:
- apiref
api_name:
- TBM_SETPOSNOTIFY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 677ab818524614f89d16ae851376d8776a4ccca3ef7798d4ac90aa6d36962ca2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046081"
---
# <a name="tbm_setposnotify-message"></a>TBM \_ SETPOSNOTIFY message

Imposta la posizione logica corrente del dispositivo di scorrimento in un trackbar.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

wParam non è usato.

</dd> <dt>

*lParam* 
</dt> <dd>

Nuova posizione logica del dispositivo di scorrimento. Le posizioni logiche valide sono i valori interi nell'intervallo tra le posizioni del dispositivo di scorrimento minimo e massimo del trackbar. Se questo valore non rientra nell'intervallo massimo e minimo del controllo, la posizione viene impostata sul valore massimo o minimo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

La chiamata a **\_ TBM SETPOSNOTIFY** imposta la posizione del dispositivo di scorrimento del trackbar come [**TBM \_ SETPOS,**](tbm-setpos.md) ma fa sì che il trackbar invii una notifica all'elemento padre di uno spostamento tramite un messaggio [**WM \_ HSCROLL**](wm-hscroll.md) o [**WM \_ VSCROLL.**](wm-vscroll.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                            |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





