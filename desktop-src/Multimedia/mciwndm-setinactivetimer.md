---
title: Messaggio di MCIWNDM_SETINACTIVETIMER (VFW. h)
description: Il \_ messaggio MCIWNDM SETINACTIVETIMER imposta il periodo di aggiornamento usato da MCIWnd per aggiornare il controllo TrackBar nella finestra MCIWnd, aggiornare le informazioni sulla posizione visualizzate nella barra del titolo della finestra e inviare messaggi di notifica alla finestra padre quando la finestra MCIWnd è inattiva. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro MCIWndSetInactiveTimer.
ms.assetid: 8900c372-0493-4a63-a027-ef6ecf8f8254
keywords:
- MCIWNDM_SETINACTIVETIMER messaggi multimediali di Windows
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
ms.openlocfilehash: ba4504d84b254dfb67616568f5f97bba8e3bc2e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518250"
---
# <a name="mciwndm_setinactivetimer-message"></a>\_Messaggio MCIWNDM SETINACTIVETIMER

Il messaggio **MCIWNDM \_ SETINACTIVETIMER** imposta il periodo di aggiornamento usato da MCIWnd per aggiornare il controllo TrackBar nella finestra MCIWnd, aggiornare le informazioni sulla posizione visualizzate nella barra del titolo della finestra e inviare messaggi di notifica alla finestra padre quando la finestra MCIWnd è inattiva. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndSetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetinactivetimer) .


```C++
MCIWNDM_SETINACTIVETIMER 
wParam = (WPARAM) (UINT) inactive; 
lParam = 0; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="inactive"></span><span id="INACTIVE"></span>*inattivo*
</dt> <dd>

Periodo di aggiornamento, in millisecondi. Il valore predefinito è 2000 millisecondi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce alcun valore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MCIWndSetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetinactivetimer)
</dt> </dl>

 

 





