---
title: Messaggio di WM_CAP_SET_CALLBACK_ERROR (VFW. h)
description: Il \_ \_ \_ messaggio di errore del set di richiamata di WM Cap \_ imposta una funzione di callback di errore nell'applicazione client. AVICap chiama questa procedura quando si verificano errori. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro capSetCallbackOnError.
ms.assetid: 4eb57515-9b5a-466c-bbaa-fdee3bca19db
keywords:
- WM_CAP_SET_CALLBACK_ERROR messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_ERROR
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40f50d62112d71f78196a17b958dc7d3d10702e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477248"
---
# <a name="wm_cap_set_callback_error-message"></a>\_Messaggio di \_ errore di callback del set di estremità WM \_ \_

Il messaggio di **\_ errore del set di \_ \_ richiamata \_ di WM Cap** imposta una funzione di callback di errore nell'applicazione client. AVICap chiama questa procedura quando si verificano errori. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capSetCallbackOnError**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonerror) .


```C++
WM_CAP_SET_CALLBACK_ERROR 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*
</dt> <dd>

Puntatore alla funzione di callback di errore, di tipo [**capErrorCallback**](/windows/desktop/api/Vfw/nc-vfw-caperrorcallbacka). Specificare **null** per questo parametro per disabilitare una funzione di callback degli errori installata in precedenza.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito **positivo o negativo** se è in corso l'acquisizione di flussi o una sessione di acquisizione a singolo frame.

## <a name="remarks"></a>Commenti

Le applicazioni possono facoltativamente impostare una funzione di callback degli errori. Se impostata, AVICap chiama la procedura di errore nelle situazioni seguenti:

-   Disco pieno.
-   Una finestra di acquisizione non può essere connessa a un driver di acquisizione.
-   Non è possibile aprire un dispositivo audio waveform.
-   Il numero di frame eliminati durante l'acquisizione supera la percentuale specificata.
-   Impossibile acquisire i frame a causa di problemi di interrupt della sincronizzazione verticale.

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

 

 





