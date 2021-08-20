---
title: MCIWNDM_SETACTIVETIMER messaggio (Vfw.h)
description: Il messaggio MCIWNDM SETACTIVETIMER imposta il periodo di aggiornamento usato da MCIWnd per aggiornare il trackbar nella finestra MCIWnd, aggiornare le informazioni sulla posizione visualizzate nella barra del titolo della finestra e inviare messaggi di notifica alla finestra padre quando la \_ finestra MCIWnd è attiva. È possibile inviare questo messaggio in modo esplicito o tramite la macro MCIWndSetActiveTimer.
ms.assetid: a30c0091-d9bb-44a3-a7b0-d1be30adcd9c
keywords:
- MCIWNDM_SETACTIVETIMER messaggio Windows Multimediali
topic_type:
- apiref
api_name:
- MCIWNDM_SETACTIVETIMER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08ca1da5729566bd8838c399276b0a082b6702f378dacf026010a0b648dba1a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117985801"
---
# <a name="mciwndm_setactivetimer-message"></a>Messaggio MCIWNDM \_ SETACTIVETIMER

Il **messaggio MCIWNDM \_ SETACTIVETIMER** imposta il periodo di aggiornamento usato da MCIWnd per aggiornare il trackbar nella finestra MCIWnd, aggiornare le informazioni sulla posizione visualizzate nella barra del titolo della finestra e inviare messaggi di notifica alla finestra padre quando la finestra MCIWnd è attiva. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**MCIWndSetActiveTimer.**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetactivetimer)


```C++
MCIWNDM_SETACTIVETIMER 
wParam = (WPARAM) (UINT) active; 
lParam = 0L; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="active"></span><span id="ACTIVE"></span>*Attivo*
</dt> <dd>

Periodo di aggiornamento, espresso in millisecondi. Il valore predefinito è 500 millisecondi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce un valore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MCIWndSetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetactivetimer)
</dt> </dl>

 

 





