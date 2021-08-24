---
title: ICM_SET_STATUS_PROC messaggio (Vfw.h)
description: Il ICM SET STATUS PROC fornisce una funzione di callback di stato \_ con lo stato di \_ \_ un'operazione di lunga durata.
ms.assetid: a1bcd840-b94b-487e-91d6-67411a8a3a2d
keywords:
- ICM_SET_STATUS_PROC messaggio Windows Multimediali
topic_type:
- apiref
api_name:
- ICM_SET_STATUS_PROC
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c02019bb6375aa18fd37ba34d2603839b37291d58822858b0b9cabc01e47d7b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678341"
---
# <a name="icm_set_status_proc-message"></a>\_ICM Messaggio SET \_ STATUS \_ PROC

Il **ICM SET STATUS \_ \_ \_ PROC** fornisce una funzione di callback di stato con lo stato di un'operazione di lunga durata.


```C++
ICM_SET_STATUS_PROC 
wParam = (DWORD_PTR)icsetstatusProc; 
lParam = sizeof(ICSETSTATUSPROC); 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="icsetstatusProc"></span><span id="icsetstatusproc"></span><span id="ICSETSTATUSPROC"></span>*icsetstatusProc*
</dt> <dd>

Puntatore a [**una struttura ICSETSTATUSPROC.**](/windows/desktop/api/Vfw/ns-vfw-icsetstatusproc)

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Dimensioni, in byte, di **ICSETSTATUSPROC.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce ICERR \_ OK in caso di esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

Il supporto di questo messaggio è facoltativo ma fortemente consigliato se la compressione o la decompressione richiede più di un decimo di secondo circa.

Un'applicazione può inviare questo messaggio periodicamente a una funzione di callback di stato durante operazioni di lunga durata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Gestione compressione video](video-compression-manager.md)
</dt> <dt>

[Messaggi di compressione video](video-compression-messages.md)
</dt> </dl>

 

 





