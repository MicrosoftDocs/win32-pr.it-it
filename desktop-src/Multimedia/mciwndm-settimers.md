---
title: Messaggio di MCIWNDM_SETTIMERS (VFW. h)
description: Il \_ messaggio MCIWNDM Timers imposta i periodi di aggiornamento utilizzati da MCIWnd per aggiornare il controllo TrackBar nella finestra MCIWnd, aggiornare le informazioni sulla posizione visualizzate nella barra del titolo della finestra e inviare messaggi di notifica alla finestra padre.
ms.assetid: 06407c67-b620-4f80-9fe9-456cdf3d0666
keywords:
- MCIWNDM_SETTIMERS messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_SETTIMERS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bba3fa2e474a15dc23deb9cdc6d00d148b8cd3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740234"
---
# <a name="mciwndm_settimers-message"></a>MCIWNDM \_ messaggi temporizzati

Il messaggio **MCIWNDM \_ Timers** imposta i periodi di aggiornamento utilizzati da MCIWnd per aggiornare il controllo TrackBar nella finestra MCIWnd, aggiornare le informazioni sulla posizione visualizzate nella barra del titolo della finestra e inviare messaggi di notifica alla finestra padre. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndSetTimers**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimers) .


```C++
MCIWNDM_SETTIMERS 
wParam = (WPARAM) (UINT) active; 
lParam = (LPARAM) (UINT) inactive; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="active"></span><span id="ACTIVE"></span>*Active*
</dt> <dd>

Periodo di aggiornamento utilizzato da MCIWnd quando è la finestra attiva. Il valore predefinito è 500 millisecondi. Lo spazio di archiviazione per questo valore è limitato a 16 bit.

</dd> <dt>

<span id="inactive"></span><span id="INACTIVE"></span>*inattivo*
</dt> <dd>

Periodo di aggiornamento utilizzato da MCIWnd quando si tratta della finestra inattiva. Il valore predefinito è 2000 millisecondi. Lo spazio di archiviazione per questo valore è limitato a 16 bit.

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

[**MCIWndSetTimers**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimers)
</dt> </dl>

 

 





