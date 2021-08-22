---
title: WM_CAP_SET_CALLBACK_WAVESTREAM messaggio (Vfw.h)
description: Il messaggio WM \_ CAP \_ SET CALLBACK \_ \_ WAVESTREAM imposta una funzione di callback nell'applicazione.
ms.assetid: f2554cbb-73de-4f76-b785-6c18c82c2992
keywords:
- WM_CAP_SET_CALLBACK_WAVESTREAM messaggio Windows Multimediali
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
ms.openlocfilehash: 3e4a8ef585a3ceb35aa07fe4e31c5819ce3e56d20b0bfd2d6c5f588fc25c335b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118622520"
---
# <a name="wm_cap_set_callback_wavestream-message"></a>Messaggio \_ \_ \_ WAVESTREAM DI CALLBACK WM CAP SET \_

Il **messaggio WM CAP SET CALLBACK \_ \_ \_ \_ WAVESTREAM** imposta una funzione di callback nell'applicazione. AVICap chiama questa procedura durante l'acquisizione di streaming quando diventa disponibile un nuovo buffer audio. È possibile inviare questo messaggio in modo esplicito o usando la macro [**capSetCallbackOnWaveStream.**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonwavestream)


```C++
WM_CAP_SET_CALLBACK_WAVESTREAM 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*
</dt> <dd>

Puntatore alla funzione di callback del flusso d'onda, di [**tipo capWaveStreamCallback.**](/windows/desktop/api/Vfw/nc-vfw-capwavecallback) Specificare **NULL per** questo parametro per disabilitare una funzione di callback del flusso audio installata in precedenza.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE se** l'operazione ha esito positivo o **FALSE** se è in corso un'acquisizione di flusso o una sessione di acquisizione a frame singolo.

## <a name="remarks"></a>Commenti

La finestra di acquisizione chiama la procedura prima di scrivere il buffer audio su disco. In questo modo le applicazioni possono modificare il buffer audio, se necessario.

Se si usa una funzione di callback del flusso audio, è necessario installare la funzione prima di avviare la sessione di acquisizione e deve rimanere abilitata per la durata della sessione. Può essere disabilitato al termine dell'acquisizione di streaming.

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

 

 





