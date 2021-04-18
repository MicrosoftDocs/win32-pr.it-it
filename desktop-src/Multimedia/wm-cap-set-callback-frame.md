---
title: Messaggio di WM_CAP_SET_CALLBACK_FRAME (VFW. h)
description: Il \_ messaggio WM Cap \_ set \_ callback \_ frame imposta una funzione di callback di anteprima nell'applicazione. AVICap chiama questa procedura quando la finestra di acquisizione acquisisce i frame di anteprima. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro capSetCallbackOnFrame.
ms.assetid: 3882e6f6-c48c-4e50-9697-cbdf5b9342a5
keywords:
- WM_CAP_SET_CALLBACK_FRAME messaggi multimediali di Windows
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
ms.openlocfilehash: b91c2f30ac0875e2f45592d3aa7e0a3ce9c296b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301815"
---
# <a name="wm_cap_set_callback_frame-message"></a>Messaggio del frame di callback di WM \_ Cap \_ set \_ \_

Il messaggio **WM \_ Cap \_ set \_ callback \_ frame** imposta una funzione di callback di anteprima nell'applicazione. AVICap chiama questa procedura quando la finestra di acquisizione acquisisce i frame di anteprima. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capSetCallbackOnFrame**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonframe) .


```C++
WM_CAP_SET_CALLBACK_FRAME 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*
</dt> <dd>

Puntatore alla funzione di callback di anteprima, di tipo [**capVideoStreamCallback**](/windows/desktop/api/Vfw/nc-vfw-capvideocallback). Specificare **null** per questo parametro per disabilitare una funzione di callback installata in precedenza.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito **positivo o negativo** se è in corso l'acquisizione di flussi o una sessione di acquisizione a singolo frame.

## <a name="remarks"></a>Commenti

La finestra di acquisizione chiama la funzione di callback prima di visualizzare i frame di anteprima. Questo consente a un'applicazione di modificare il frame se lo si desidera. Questa funzione di callback non viene usata durante l'acquisizione video di streaming.

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

 

 





