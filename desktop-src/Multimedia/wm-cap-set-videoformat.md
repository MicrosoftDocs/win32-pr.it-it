---
title: WM_CAP_SET_VIDEOFORMAT messaggio (Vfw.h)
description: Il messaggio WM \_ CAP \_ SET \_ VIDEOFORMAT imposta il formato dei dati video acquisiti. È possibile inviare questo messaggio in modo esplicito o usando la macro capSetVideoFormat.
ms.assetid: 4f9cf90d-7ccb-4fc7-aad5-3d7e082526be
keywords:
- WM_CAP_SET_VIDEOFORMAT messaggio Windows Multimediali
topic_type:
- apiref
api_name:
- WM_CAP_SET_VIDEOFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c543f613fedf54518579829d6825bd20dc4738ae03cb77f0996f8a58a123cb76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118135017"
---
# <a name="wm_cap_set_videoformat-message"></a>Messaggio WM \_ CAP \_ SET \_ VIDEOFORMAT

Il **messaggio WM CAP SET \_ \_ \_ VIDEOFORMAT** imposta il formato dei dati video acquisiti. È possibile inviare questo messaggio in modo esplicito o usando la macro [**capSetVideoFormat.**](/windows/desktop/api/Vfw/nf-vfw-capsetvideoformat)


```C++
WM_CAP_SET_VIDEOFORMAT 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (psVideoFormat); 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*
</dt> <dd>

Dimensione, in byte, della struttura a cui fa riferimento **s**.

</dd> <dt>

<span id="psVideoFormat"></span><span id="psvideoformat"></span><span id="PSVIDEOFORMAT"></span>*psVideoFormat*
</dt> <dd>

Puntatore a una [**struttura BITMAPINFO.**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE se** l'operazione ha esito positivo o FALSE **in** caso contrario.

## <a name="remarks"></a>Commenti

Poiché i formati video sono specifici del dispositivo, le applicazioni devono controllare il valore restituito da questa funzione per determinare se il formato viene accettato dal driver.

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

 

