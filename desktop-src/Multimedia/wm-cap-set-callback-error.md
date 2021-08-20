---
title: WM_CAP_SET_CALLBACK_ERROR messaggio (Vfw.h)
description: Il messaggio WM \_ CAP SET CALLBACK ERROR imposta una funzione di callback degli errori \_ \_ \_ nell'applicazione client. AVICap chiama questa procedura quando si verificano errori. È possibile inviare questo messaggio in modo esplicito o usando la macro capSetCallbackOnError.
ms.assetid: 4eb57515-9b5a-466c-bbaa-fdee3bca19db
keywords:
- WM_CAP_SET_CALLBACK_ERROR messaggio Windows Multimediali
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
ms.openlocfilehash: f2b631a66923fc614e1486405b1c8e64f152c0f0dd21c8abec292548c546d17b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118135103"
---
# <a name="wm_cap_set_callback_error-message"></a>MESSAGGIO \_ DI ERRORE DI CALLBACK DI WM CAP \_ SET \_ \_

Il **messaggio WM CAP SET CALLBACK \_ \_ \_ \_ ERROR** imposta una funzione di callback degli errori nell'applicazione client. AVICap chiama questa procedura quando si verificano errori. È possibile inviare questo messaggio in modo esplicito o usando la macro [**capSetCallbackOnError.**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonerror)


```C++
WM_CAP_SET_CALLBACK_ERROR 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*
</dt> <dd>

Puntatore alla funzione di callback di errore di [**tipo capErrorCallback.**](/windows/desktop/api/Vfw/nc-vfw-caperrorcallbacka) Specificare **NULL per** questo parametro per disabilitare una funzione di callback degli errori installata in precedenza.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE se** l'operazione ha esito positivo o **FALSE** se è in corso un'acquisizione di flusso o una sessione di acquisizione a frame singolo.

## <a name="remarks"></a>Commenti

Le applicazioni possono facoltativamente impostare una funzione di callback degli errori. Se impostato, AVICap chiama la procedura di errore nelle situazioni seguenti:

-   Disco pieno.
-   Una finestra di acquisizione non può essere connessa a un driver di acquisizione.
-   Non è possibile aprire un dispositivo audio waveform.
-   Il numero di frame eliminati durante l'acquisizione supera la percentuale specificata.
-   I frame non possono essere acquisiti a causa di problemi di interruzione della sincronizzazione verticale.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Acquisizione video](video-capture.md)
</dt> <dt>

[Messaggi di acquisizione video](video-capture-messages.md)
</dt> </dl>

 

 





