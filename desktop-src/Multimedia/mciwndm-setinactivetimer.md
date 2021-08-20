---
title: MCIWNDM_SETINACTIVETIMER messaggio (Vfw.h)
description: Il messaggio MCIWNDM SETINACTIVETIMER imposta il periodo di aggiornamento usato da MCIWnd per aggiornare il trackbar nella finestra MCIWnd, aggiornare le informazioni sulla posizione visualizzate nella barra del titolo della finestra e inviare messaggi di notifica alla finestra padre quando la \_ finestra MCIWnd è inattiva. È possibile inviare questo messaggio in modo esplicito o tramite la macro MCIWndSetInactiveTimer.
ms.assetid: 8900c372-0493-4a63-a027-ef6ecf8f8254
keywords:
- MCIWNDM_SETINACTIVETIMER messaggio Windows Multimediali
topic_type:
- apiref
api_name:
- MCIWNDM_SETINACTIVETIMER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e4161d52335e050fb8e9bcb702986492b5cd230713fcd15810a71590a92b030
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118137648"
---
# <a name="mciwndm_setinactivetimer-message"></a>Messaggio DI MCIWNDM \_ SETINACTIVETIMER

Il messaggio **MCIWNDM \_ SETINACTIVETIMER** imposta il periodo di aggiornamento usato da MCIWnd per aggiornare il trackbar nella finestra MCIWnd, aggiornare le informazioni sulla posizione visualizzate nella barra del titolo della finestra e inviare messaggi di notifica alla finestra padre quando la finestra MCIWnd è inattiva. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**MCIWndSetInactiveTimer.**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetinactivetimer)


```C++
MCIWNDM_SETINACTIVETIMER 
wParam = (WPARAM) (UINT) inactive; 
lParam = 0; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="inactive"></span><span id="INACTIVE"></span>*Inattivo*
</dt> <dd>

Periodo di aggiornamento, espresso in millisecondi. Il valore predefinito è 2000 millisecondi.

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

[**MCIWndSetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetinactivetimer)
</dt> </dl>

 

 





