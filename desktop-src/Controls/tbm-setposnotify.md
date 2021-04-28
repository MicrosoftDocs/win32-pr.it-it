---
title: TBM_SETPOSNOTIFY messaggio (Commctrl.h)
description: 'TBM_SETPOSNOTIFY messaggio: imposta la posizione logica corrente del dispositivo di scorrimento in un trackbar.'
ms.assetid: 02f8899a-55b0-46ae-8642-9e534ab4abf5
keywords:
- TBM_SETPOSNOTIFY messaggio Controlli Windows
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
ms.openlocfilehash: 7201f3056ed05e6321ab9d9bd726edc3b4470f0b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104079"
---
# <a name="tbm_setposnotify-message"></a>Messaggio \_ TBM SETPOSNOTIFY

Imposta la posizione logica corrente del dispositivo di scorrimento in un trackbar.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

wParam non viene usato.

</dd> <dt>

*lParam* 
</dt> <dd>

Nuova posizione logica del dispositivo di scorrimento. Le posizioni logiche valide sono i valori interi nell'intervallo tra le posizioni minime e massime del dispositivo di scorrimento del trackbar. Se questo valore non rientra nell'intervallo massimo e minimo del controllo, la posizione viene impostata sul valore massimo o minimo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

La chiamata a **TBM \_ SETPOSNOTIFY** imposta la posizione del dispositivo di scorrimento del trackbar come farebbe [**TBM \_ SETPOS,**](tbm-setpos.md) ma determina anche la notifica del trackbar all'elemento padre di uno spostamento tramite un messaggio [**WM \_ HSCROLL**](wm-hscroll.md) o [**WM \_ VSCROLL.**](wm-vscroll.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows 7 \[\]<br/>                                            |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2008 R2 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





