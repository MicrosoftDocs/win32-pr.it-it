---
title: Messaggio di MCIWNDM_GETERROR (VFW. h)
description: Il \_ messaggio MCIWNDM GetError recupera l'ultimo errore MCI rilevato. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro MCIWndGetError.
ms.assetid: f110a9b3-5b05-4bf0-85d1-b49ce7396222
keywords:
- MCIWNDM_GETERROR messaggi multimediali di Windows
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
ms.openlocfilehash: 5c2977bb079351824b48da21f4ba3cc2dc5afe7e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873422"
---
# <a name="mciwndm_geterror-message"></a>\_Messaggio GETERROR MCIWNDM

Il messaggio **MCIWNDM \_ GetError** recupera l'ultimo errore MCI rilevato. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndGetError**](/windows/desktop/api/Vfw/nf-vfw-mciwndgeterror) .


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

<span id="lp"></span><span id="LP"></span>*LP*
</dt> <dd>

Puntatore a un buffer definito dall'applicazione utilizzato per restituire la stringa di errore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il valore di errore integer in caso di esito positivo.

## <a name="remarks"></a>Commenti

Se *LP* è un puntatore valido, nel buffer viene restituita una stringa con terminazione null corrispondente all'errore. Se la stringa di errore è più lunga del buffer, MCIWnd lo tronca.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MCIWndGetError**](/windows/desktop/api/Vfw/nf-vfw-mciwndgeterror)
</dt> </dl>

 

 





