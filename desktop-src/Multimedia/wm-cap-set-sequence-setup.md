---
title: WM_CAP_SET_SEQUENCE_SETUP messaggio (Vfw.h)
description: Il messaggio WM \_ CAP SET SEQUENCE SETUP imposta i parametri di configurazione usati con \_ \_ \_ l'acquisizione del flusso. È possibile inviare questo messaggio in modo esplicito o tramite la macro capCaptureSetSetup.
ms.assetid: ba9adb26-6627-469b-a836-f4f277ddb7c4
keywords:
- WM_CAP_SET_SEQUENCE_SETUP messaggio Windows Multimediali
topic_type:
- apiref
api_name:
- WM_CAP_SET_SEQUENCE_SETUP
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4632b62bd208339798c0e26dda835c66c01f9257d7c4ac19157f78def3cd603
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117800192"
---
# <a name="wm_cap_set_sequence_setup-message"></a>Messaggio \_ WM CAP SET SEQUENCE \_ \_ \_ SETUP

Il **messaggio WM CAP SET SEQUENCE \_ \_ \_ \_ SETUP** imposta i parametri di configurazione usati con l'acquisizione del flusso. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**capCaptureSetSetup.**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup)


```C++
WM_CAP_SET_SEQUENCE_SETUP 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPCAPTUREPARMS) (psCapParms); 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*
</dt> <dd>

Dimensione, in byte, della struttura a cui fa riferimento **s**.

</dd> <dt>

<span id="psCapParms"></span><span id="pscapparms"></span><span id="PSCAPPARMS"></span>*psCapParms*
</dt> <dd>

Puntatore a [**una struttura CAPTUREPARMS.**](/windows/win32/api/vfw/ns-vfw-captureparms)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo o FALSE **in** caso contrario.

## <a name="remarks"></a>Commenti

Per informazioni sui parametri usati per controllare l'acquisizione del flusso, vedere la [**struttura CAPTUREPARMS.**](/windows/win32/api/vfw/ns-vfw-captureparms)

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

 

 





