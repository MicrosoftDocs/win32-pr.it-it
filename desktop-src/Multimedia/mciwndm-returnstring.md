---
title: MCIWNDM_RETURNSTRING messaggio (Vfw.h)
description: Il messaggio RETURNSTRING MCIWNDM recupera la risposta al comando stringa MCI più \_ recente inviato a un dispositivo MCI.
ms.assetid: 36a5222c-a63c-4b8c-ad0c-a00477e95b96
keywords:
- MCIWNDM_RETURNSTRING messaggio Windows Multimediali
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
ms.openlocfilehash: d2ea9624c70245c67f0f6a78af68bf291ae3ce60ba65ae2cd273008bbc914ec2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118137658"
---
# <a name="mciwndm_returnstring-message"></a>Messaggio RETURNSTRING MCIWNDM \_

Il **messaggio \_ RETURNSTRING MCIWNDM** recupera la risposta al comando stringa MCI più recente inviato a un dispositivo MCI. Le informazioni nella risposta vengono fornite come stringa con terminazione Null. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**MCIWndReturnString.**](/windows/desktop/api/Vfw/nf-vfw-mciwndreturnstring)


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

<span id="lp"></span><span id="LP"></span>*Lp*
</dt> <dd>

Puntatore a un buffer definito dall'applicazione per contenere la stringa con terminazione Null.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un intero corrispondente alla stringa MCI.

## <a name="remarks"></a>Commenti

Se la stringa con terminazione Null è più lunga del buffer, la stringa viene troncata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MCIWndReturnString**](/windows/desktop/api/Vfw/nf-vfw-mciwndreturnstring)
</dt> </dl>

 

 





