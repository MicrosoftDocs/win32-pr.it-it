---
title: WM_CAP_FILE_SET_CAPTURE_FILE messaggio (Vfw.h)
description: Il messaggio WM \_ CAP FILE SET CAPTURE FILE indica il file usato per \_ \_ \_ \_ l'acquisizione video. È possibile inviare questo messaggio in modo esplicito o tramite la macro capFileSetCaptureFile.
ms.assetid: d96e498b-6322-4d48-a5d7-156e95f23740
keywords:
- WM_CAP_FILE_SET_CAPTURE_FILE messaggio Windows Multimediali
topic_type:
- apiref
api_name:
- WM_CAP_FILE_SET_CAPTURE_FILE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9435a7f0790c8ffe88f6b7ea6228bb2f442b23f5dcb15e2722e59b75c671588
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687021"
---
# <a name="wm_cap_file_set_capture_file-message"></a>Messaggio \_ WM CAP FILE SET CAPTURE \_ \_ \_ \_ FILE

Il **messaggio WM CAP FILE SET CAPTURE \_ \_ \_ \_ \_ FILE** indica il file usato per l'acquisizione video. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**capFileSetCaptureFile.**](/windows/desktop/api/Vfw/nf-vfw-capfilesetcapturefile)


```C++
WM_CAP_FILE_SET_CAPTURE_FILE 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*Szname*
</dt> <dd>

Puntatore alla stringa con terminazione Null che contiene il nome del file di acquisizione da usare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE se** l'operazione ha esito positivo o **FALSE** se il nome file non è valido o se è in corso l'acquisizione di un singolo frame o di streaming.

## <a name="remarks"></a>Commenti

Questo messaggio archivia il nome file in una struttura interna. Non crea, alloca o apre il file specificato. Il nome file di acquisizione predefinito è C: \\CAPTURE.AVI.

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

 

 





