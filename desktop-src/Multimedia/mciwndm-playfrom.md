---
title: Messaggio di MCIWNDM_PLAYFROM (VFW. h)
description: Il \_ messaggio MCIWNDM PLAYFROM riproduce il contenuto di un dispositivo MCI dal percorso specificato alla fine del contenuto o fino a quando un altro comando interrompe la riproduzione. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro MCIWndPlayFrom.
ms.assetid: 1c47f8eb-2a1b-4671-a9f8-fd6d59a5c7c6
keywords:
- MCIWNDM_PLAYFROM messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_PLAYFROM
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c0fa1b3f4b3359e1609b3ba12009fe5879c304a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963872"
---
# <a name="mciwndm_playfrom-message"></a>\_Messaggio MCIWNDM PLAYFROM

Il messaggio **MCIWNDM \_ PLAYFROM** riproduce il contenuto di un dispositivo MCI dal percorso specificato alla fine del contenuto o fino a quando un altro comando interrompe la riproduzione. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndPlayFrom**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom) .


```C++
MCIWNDM_PLAYFROM 
wParam = 0; 
lParam = (LPARAM) (LONG) lPos; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lPos"></span><span id="lpos"></span><span id="LPOS"></span>*lPos*
</dt> <dd>

Posizione iniziale. Le unità per la posizione iniziale dipendono dal formato dell'ora corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="remarks"></a>Commenti

È anche possibile specificare una posizione iniziale e finale per la riproduzione usando la macro [**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MCIWndPlayFrom**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom)
</dt> <dt>

[**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto)
</dt> </dl>

 

 





