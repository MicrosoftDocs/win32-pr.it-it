---
title: WM_CAP_FILE_GET_CAPTURE_FILE messaggio (Vfw.h)
description: Il messaggio WM \_ CAP FILE GET CAPTURE FILE restituisce il nome del file di acquisizione \_ \_ \_ \_ corrente. È possibile inviare questo messaggio in modo esplicito o usando la macro capFileGetCaptureFile.
ms.assetid: 86ce2904-834d-449f-9ef8-5a158c55bbaa
keywords:
- WM_CAP_FILE_GET_CAPTURE_FILE messaggio Windows Multimediali
topic_type:
- apiref
api_name:
- WM_CAP_FILE_GET_CAPTURE_FILE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 462f919458078129f6756782c2fde5322b3cd814c3108cb0ba8ee24e2f54c022
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118135319"
---
# <a name="wm_cap_file_get_capture_file-message"></a>MESSAGGIO \_ WM CAP FILE GET CAPTURE \_ \_ \_ \_ FILE

Il **messaggio WM CAP FILE GET CAPTURE \_ \_ \_ \_ \_ FILE** restituisce il nome del file di acquisizione corrente. È possibile inviare questo messaggio in modo esplicito o usando la macro [**capFileGetCaptureFile.**](/windows/desktop/api/Vfw/nf-vfw-capfilegetcapturefile)


```C++
WM_CAP_FILE_GET_CAPTURE_FILE 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*
</dt> <dd>

Dimensione, in byte, del buffer definito dall'applicazione a cui fa riferimento **szName**.

</dd> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*Szname*
</dt> <dd>

Puntatore a un buffer definito dall'applicazione utilizzato per restituire il nome del file di acquisizione come stringa con terminazione Null.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE se** l'operazione ha esito positivo o FALSE **in** caso contrario.

## <a name="remarks"></a>Commenti

Il nome file di acquisizione predefinito è C: \\CAPTURE.AVI.

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

 

 





