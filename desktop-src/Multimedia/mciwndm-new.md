---
title: MCIWNDM_NEW messaggio (Vfw.h)
description: Il messaggio MCIWNDM \_ NEW crea un nuovo file per il dispositivo MCI corrente. È possibile inviare questo messaggio in modo esplicito o tramite la macro MCIWndNew.
ms.assetid: 18b2340d-8303-415a-867f-bd346034db2a
keywords:
- MCIWNDM_NEW messaggio Windows Multimediali
topic_type:
- apiref
api_name:
- MCIWNDM_NEW
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bca9c03aff08c07f3ab1d8337547de776aeab5c6623a34ddaa71bfada0bca4f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119783081"
---
# <a name="mciwndm_new-message"></a>MESSAGGIO NUOVO MCIWNDM \_

Il **messaggio MCIWNDM \_ NEW** crea un nuovo file per il dispositivo MCI corrente. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**MCIWndNew.**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew)


```C++
MCIWNDM_NEW 
wParam = 0; 
lParam = (LPARAM) (LPVOID) lp; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lp"></span><span id="LP"></span>*Lp*
</dt> <dd>

Puntatore a un buffer contenente il nome del dispositivo MCI che userà il file.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MCIWndNew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew)
</dt> </dl>

 

 





