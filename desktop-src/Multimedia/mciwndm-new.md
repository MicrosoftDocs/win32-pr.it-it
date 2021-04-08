---
title: Messaggio di MCIWNDM_NEW (VFW. h)
description: Il \_ nuovo messaggio MCIWNDM crea un nuovo file per il dispositivo MCI corrente. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro MCIWndNew.
ms.assetid: 18b2340d-8303-415a-867f-bd346034db2a
keywords:
- MCIWNDM_NEW messaggi multimediali di Windows
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
ms.openlocfilehash: 293323cd0404da45e648024b35b7f96ef60fea61
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741162"
---
# <a name="mciwndm_new-message"></a>MCIWNDM \_ nuovo messaggio

Il **\_ nuovo messaggio MCIWNDM** crea un nuovo file per il dispositivo MCI corrente. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndNew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew) .


```C++
MCIWNDM_NEW 
wParam = 0; 
lParam = (LPARAM) (LPVOID) lp; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lp"></span><span id="LP"></span>*LP*
</dt> <dd>

Puntatore a un buffer contenente il nome del dispositivo MCI che utilizzerà il file.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MCIWndNew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew)
</dt> </dl>

 

 





