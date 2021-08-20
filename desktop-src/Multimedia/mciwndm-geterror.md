---
title: MCIWNDM_GETERROR messaggio (Vfw.h)
description: Il messaggio MCIWNDM \_ GETERROR recupera l'ultimo errore MCI rilevato. È possibile inviare questo messaggio in modo esplicito o tramite la macro MCIWndGetError.
ms.assetid: f110a9b3-5b05-4bf0-85d1-b49ce7396222
keywords:
- MCIWNDM_GETERROR messaggio Windows Multimediali
topic_type:
- apiref
api_name:
- MCIWNDM_GETERROR
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b748aec6cf686ecf47baf8deae621514e620971f5e1da667f8e4f0aae708ab80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118137722"
---
# <a name="mciwndm_geterror-message"></a>Messaggio MCIWNDM \_ GETERROR

Il **messaggio MCIWNDM \_ GETERROR** recupera l'ultimo errore MCI rilevato. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**MCIWndGetError.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgeterror)


```C++
MCIWNDM_GETERROR 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPVOID) lp; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="len"></span><span id="LEN"></span>*Len*
</dt> <dd>

Dimensione, in byte, del buffer degli errori.

</dd> <dt>

<span id="lp"></span><span id="LP"></span>*Lp*
</dt> <dd>

Puntatore a un buffer definito dall'applicazione utilizzato per restituire la stringa di errore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il valore di errore intero in caso di esito positivo.

## <a name="remarks"></a>Commenti

Se *lp* è un puntatore valido, nel buffer viene restituita una stringa con terminazione Null corrispondente all'errore. Se la stringa di errore è più lunga del buffer, MCIWnd la tronca.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MCIWndGetError**](/windows/desktop/api/Vfw/nf-vfw-mciwndgeterror)
</dt> </dl>

 

 





