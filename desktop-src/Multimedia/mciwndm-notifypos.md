---
title: MCIWNDM_NOTIFYPOS messaggio (Vfw.h)
description: Il messaggio NOTIFYPOS MCIWNDM notifica alla finestra padre \_ di un'applicazione che la posizione della finestra è stata modificata.
ms.assetid: ccc8903b-ad79-495a-8003-20e120ad28ff
keywords:
- MCIWNDM_NOTIFYPOS messaggio Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_NOTIFYPOS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d55d3b14ffb6a42e0c41cb820e066eee5c419b069e0d92ad614ffb51d577b963
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119429000"
---
# <a name="mciwndm_notifypos-message"></a>Messaggio NOTIFYPOS MCIWNDM \_

Il **messaggio \_ NOTIFYPOS MCIWNDM** notifica alla finestra padre di un'applicazione che la posizione della finestra è stata modificata.


```C++
MCIWNDM_NOTIFYPOS 
wParam = (WPARAM) (HWND) hwnd; 
lParam = (LPARAM) (LONG) pos; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="hwnd"></span><span id="HWND"></span>*Hwnd*
</dt> <dd>

Handle per la finestra MCIWnd.

</dd> <dt>

<span id="pos"></span><span id="POS"></span>*Pos*
</dt> <dd>

Descrive la nuova posizione.

</dd> </dl>

## <a name="remarks"></a>Commenti

È possibile abilitare la notifica delle modifiche nella posizione di una finestra MCIWnd specificando lo stile della finestra MCIWNDF \_ NOTIFYPOS.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



 

 





