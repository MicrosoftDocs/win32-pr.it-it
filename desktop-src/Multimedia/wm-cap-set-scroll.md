---
title: Messaggio di WM_CAP_SET_SCROLL (VFW. h)
description: Il messaggio di scorrimento di WM \_ Cap \_ set \_ definisce la parte del fotogramma video da visualizzare nella finestra di acquisizione.
ms.assetid: 545605e4-6b1f-403a-a3ab-0fd6750ae776
keywords:
- WM_CAP_SET_SCROLL messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WM_CAP_SET_SCROLL
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 812b76bdcad166b9f766957032f232293d4083c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479054"
---
# <a name="wm_cap_set_scroll-message"></a>\_Messaggio di \_ scorrimento set di estremità WM \_

Il messaggio di **scorrimento di WM \_ Cap \_ set \_** definisce la parte del fotogramma video da visualizzare nella finestra di acquisizione. Questo messaggio imposta l'angolo superiore sinistro dell'area client della finestra di acquisizione sulle coordinate di un pixel specificato all'interno del frame del video. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capSetScrollPos**](/windows/desktop/api/Vfw/nf-vfw-capsetscrollpos) .


```C++
WM_CAP_SET_SCROLL 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPPOINT) (lpP); 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lpP"></span><span id="lpp"></span><span id="LPP"></span>*lpP*
</dt> <dd>

Indirizzo per contenere la posizione di scorrimento desiderata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione è riuscita o **false** in caso contrario.

## <a name="remarks"></a>Commenti

La posizione di scorrimento influiscono sull'immagine nelle modalità anteprima e sovrapposizione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Acquisizione video](video-capture.md)
</dt> <dt>

[Messaggi di acquisizione video](video-capture-messages.md)
</dt> </dl>

 

 





