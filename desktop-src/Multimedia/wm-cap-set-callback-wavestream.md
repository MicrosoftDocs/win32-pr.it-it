---
title: Messaggio di WM_CAP_SET_CALLBACK_WAVESTREAM (VFW. h)
description: Il \_ messaggio WM Cap \_ set \_ callback \_ WAVESTREAM imposta una funzione di callback nell'applicazione.
ms.assetid: f2554cbb-73de-4f76-b785-6c18c82c2992
keywords:
- WM_CAP_SET_CALLBACK_WAVESTREAM messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_WAVESTREAM
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d36abc7848de082e033cfc25d4f15d90c86cf3b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479055"
---
# <a name="wm_cap_set_callback_wavestream-message"></a>\_ \_ \_ Messaggio WAVESTREAM di richiamata di WM Cap Set \_

Il messaggio **WM \_ Cap \_ set \_ callback \_ WAVESTREAM** imposta una funzione di callback nell'applicazione. AVICap chiama questa procedura durante l'acquisizione del flusso quando diventa disponibile un nuovo buffer audio. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capSetCallbackOnWaveStream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonwavestream) .


```C++
WM_CAP_SET_CALLBACK_WAVESTREAM 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*
</dt> <dd>

Puntatore alla funzione di callback del flusso Wave, di tipo [**capWaveStreamCallback**](/windows/desktop/api/Vfw/nc-vfw-capwavecallback). Specificare **null** per questo parametro per disabilitare una funzione di callback del flusso Wave installata in precedenza.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito **positivo o negativo** se è in corso l'acquisizione di flussi o una sessione di acquisizione a singolo frame.

## <a name="remarks"></a>Commenti

La finestra di acquisizione chiama la procedura prima di scrivere il buffer audio su disco. Ciò consente alle applicazioni di modificare il buffer audio se lo si desidera.

Se viene usata una funzione di callback del flusso Wave, è necessario installarla prima di avviare la sessione di acquisizione e deve rimanere abilitata per la durata della sessione. Può essere disabilitato al termine dell'acquisizione di streaming.

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

 

 





