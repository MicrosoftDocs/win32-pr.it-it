---
title: WM_CAP_GET_SEQUENCE_SETUP messaggio (Vfw.h)
description: Il messaggio WM \_ CAP GET SEQUENCE SETUP recupera le impostazioni correnti dei parametri di acquisizione del \_ \_ \_ flusso. È possibile inviare questo messaggio in modo esplicito o usando la macro capCaptureGetSetup.
ms.assetid: 2220c92a-1994-4f15-9730-1cf01972dda6
keywords:
- WM_CAP_GET_SEQUENCE_SETUP messaggio Windows Multimediali
topic_type:
- apiref
api_name:
- WM_CAP_GET_SEQUENCE_SETUP
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55122a98846f23c609eb371ab5698198729c39e967d7953295850b61764459af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118369539"
---
# <a name="wm_cap_get_sequence_setup-message"></a>Messaggio \_ WM CAP GET SEQUENCE \_ \_ \_ SETUP

Il **messaggio WM CAP GET SEQUENCE \_ \_ \_ \_ SETUP** recupera le impostazioni correnti dei parametri di acquisizione del flusso. È possibile inviare questo messaggio in modo esplicito o usando la macro [**capCaptureGetSetup.**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup)


```C++
WM_CAP_GET_SEQUENCE_SETUP 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPCAPTUREPARMS) (s); 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*
</dt> <dd>

Dimensione, in byte, della struttura a cui fa riferimento **s**.

</dd> <dt>

<span id="s"></span><span id="S"></span>*s*
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

 

 





