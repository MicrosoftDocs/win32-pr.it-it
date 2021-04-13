---
title: Messaggio di MCIWNDM_GETDEVICE (VFW. h)
description: Il \_ messaggio MCIWNDM GetDevice Recupera il nome del dispositivo MCI attualmente aperto. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro MCIWndGetDevice.
ms.assetid: e69a73a6-a927-4536-98c7-ee7d5b16668a
keywords:
- MCIWNDM_GETDEVICE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_GETDEVICE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32664508a577db9d5a077e3cb4fd00aab34fbdf3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475533"
---
# <a name="mciwndm_getdevice-message"></a>\_Messaggio GETDEVICE MCIWNDM

Il messaggio **MCIWNDM \_ GetDevice** Recupera il nome del dispositivo MCI attualmente aperto. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndGetDevice**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdevice) .


```C++
MCIWNDM_GETDEVICE 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPVOID) lp; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="len"></span><span id="LEN"></span>*Len*
</dt> <dd>

Dimensione, in byte, del buffer.

</dd> <dt>

<span id="lp"></span><span id="LP"></span>*LP*
</dt> <dd>

Puntatore a un buffer definito dall'applicazione per restituire il nome del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un valore diverso da zero.

## <a name="remarks"></a>Commenti

Se la stringa con terminazione null che contiene il nome del dispositivo è più lunga del buffer, MCIWnd lo tronca.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



 

 





