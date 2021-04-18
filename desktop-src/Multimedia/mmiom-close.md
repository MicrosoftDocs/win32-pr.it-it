---
title: Messaggio MMIOM_CLOSE (mmsystem. h)
description: Il \_ messaggio MMIOM Close viene inviato a una routine di i/O dalla funzione mmioClose per richiedere che un file venga chiuso.
ms.assetid: 9d0dad5b-fd0a-4948-a4cf-9d138e353c76
keywords:
- MMIOM_CLOSE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MMIOM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7863698b99bcead8bc22e6194d213bbc663d5ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519294"
---
# <a name="mmiom_close-message"></a>\_Messaggio di chiusura MMIOM

Il messaggio **MMIOM \_ Close** viene inviato a una routine di i/O dalla funzione [**mmioClose**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) per richiedere che un file venga chiuso.


```C++
MMIOM_CLOSE 
lParam1 = (LPARAM) lCloseFlags 
lParam2 = reserved 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lCloseFlags"></span><span id="lcloseflags"></span><span id="LCLOSEFLAGS"></span>*lCloseFlags*
</dt> <dd>

Flag contenuti nel parametro **wFlags** di **mmioClose**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero se il file è stato chiuso correttamente o un errore in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Mmsystem. h (include Windows. h)</dt> </dl> |



 

