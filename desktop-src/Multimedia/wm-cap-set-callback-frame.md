---
title: WM_CAP_SET_CALLBACK_FRAME messaggio (Vfw.h)
description: Il messaggio WM \_ CAP SET CALLBACK FRAME imposta una funzione di callback di anteprima \_ \_ \_ nell'applicazione. AVICap chiama questa procedura quando la finestra di acquisizione acquisisce i frame di anteprima. È possibile inviare questo messaggio in modo esplicito o usando la macro capSetCallbackOnFrame.
ms.assetid: 3882e6f6-c48c-4e50-9697-cbdf5b9342a5
keywords:
- WM_CAP_SET_CALLBACK_FRAME di messaggi Windows multimediali
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_FRAME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f85321483639135db31750cacf76cc5f0dc4ad42e96474efa1dc17ac84ba4a79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118369509"
---
# <a name="wm_cap_set_callback_frame-message"></a>Messaggio WM \_ CAP \_ SET CALLBACK \_ \_ FRAME

Il **messaggio WM CAP SET CALLBACK \_ \_ \_ \_ FRAME** imposta una funzione di callback di anteprima nell'applicazione. AVICap chiama questa procedura quando la finestra di acquisizione acquisisce i frame di anteprima. È possibile inviare questo messaggio in modo esplicito o usando la macro [**capSetCallbackOnFrame.**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonframe)


```C++
WM_CAP_SET_CALLBACK_FRAME 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*
</dt> <dd>

Puntatore alla funzione di callback di anteprima, di [**tipo capVideoStreamCallback.**](/windows/desktop/api/Vfw/nc-vfw-capvideocallback) Specificare **NULL per** questo parametro per disabilitare una funzione di callback installata in precedenza.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE se** l'operazione ha esito positivo o **FALSE** se è in corso un'acquisizione di flusso o una sessione di acquisizione a frame singolo.

## <a name="remarks"></a>Commenti

La finestra di acquisizione chiama la funzione di callback prima di visualizzare i frame di anteprima. In questo modo un'applicazione può modificare il frame, se necessario. Questa funzione di callback non viene usata durante l'acquisizione di video in streaming.

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

 

 





