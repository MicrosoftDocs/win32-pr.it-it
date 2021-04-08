---
title: Messaggio di MCIWNDM_RETURNSTRING (VFW. h)
description: Il \_ messaggio MCIWNDM RETURNSTRING recupera la risposta al comando di stringa MCI più recente inviato a un dispositivo MCI.
ms.assetid: 36a5222c-a63c-4b8c-ad0c-a00477e95b96
keywords:
- MCIWNDM_RETURNSTRING messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_RETURNSTRING
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b99307bd7d61a70db594d0a696cceccd6d246a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048336"
---
# <a name="mciwndm_returnstring-message"></a>\_Messaggio MCIWNDM RETURNSTRING

Il messaggio **MCIWNDM \_ RETURNSTRING** recupera la risposta al comando di stringa MCI più recente inviato a un dispositivo MCI. Le informazioni nella risposta vengono fornite come stringa con terminazione null. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndReturnString**](/windows/desktop/api/Vfw/nf-vfw-mciwndreturnstring) .


```C++
MCIWNDM_RETURNSTRING 
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

Puntatore a un buffer definito dall'applicazione per contenere la stringa con terminazione null.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un Integer che corrisponde alla stringa MCI.

## <a name="remarks"></a>Commenti

Se la stringa con terminazione null è più lunga del buffer, la stringa viene troncata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MCIWndReturnString**](/windows/desktop/api/Vfw/nf-vfw-mciwndreturnstring)
</dt> </dl>

 

 





