---
title: Messaggio di WM_CAP_SET_CALLBACK_STATUS (VFW. h)
description: Il \_ \_ \_ \_ messaggio di stato del callback di WM Cap imposta una funzione di callback dello stato nell'applicazione. AVICap chiama questa procedura ogni volta che lo stato della finestra di acquisizione cambia. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro capSetCallbackOnStatus.
ms.assetid: 451ba9f9-7bfb-4c57-af6c-d5f691f39618
keywords:
- WM_CAP_SET_CALLBACK_STATUS messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_STATUS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 493893a51d51b1ce61d43ff54461bb71c08a9f6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475491"
---
# <a name="wm_cap_set_callback_status-message"></a>Messaggio di stato del callback di WM \_ Cap \_ set \_ \_

Il messaggio di **\_ stato del \_ \_ callback \_ di WM Cap** imposta una funzione di callback dello stato nell'applicazione. AVICap chiama questa procedura ogni volta che lo stato della finestra di acquisizione cambia. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capSetCallbackOnStatus**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonstatus) .


```C++
WM_CAP_SET_CALLBACK_STATUS 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*
</dt> <dd>

Puntatore alla funzione di callback dello stato di tipo [**capStatusCallback**](/windows/desktop/api/Vfw/nc-vfw-capstatuscallbacka). Specificare **null** per questo parametro per disabilitare una funzione di callback dello stato installata in precedenza.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito **positivo o negativo** se è in corso l'acquisizione di flussi o una sessione di acquisizione a singolo frame.

## <a name="remarks"></a>Commenti

Le applicazioni possono facoltativamente impostare una funzione di callback dello stato. Se impostata, AVICap chiama questa procedura nelle situazioni seguenti:

-   Una sessione di acquisizione è stata completata.
-   Un driver di acquisizione è riuscito a connettersi a una finestra di acquisizione.
-   Viene creata una tavolozza ottimale.
-   Il numero di frame acquisiti viene segnalato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Acquisizione video](video-capture.md)
</dt> <dt>

[Messaggi di acquisizione video](video-capture-messages.md)
</dt> </dl>

 

 





