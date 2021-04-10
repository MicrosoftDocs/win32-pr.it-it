---
title: Messaggio di WM_CAP_FILE_SET_CAPTURE_FILE (VFW. h)
description: Il file \_ \_ \_ di acquisizione del set di file di WM Cap è \_ \_ il file usato per l'acquisizione video. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro capFileSetCaptureFile.
ms.assetid: d96e498b-6322-4d48-a5d7-156e95f23740
keywords:
- WM_CAP_FILE_SET_CAPTURE_FILE messaggi multimediali di Windows
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
ms.openlocfilehash: 12b3f59edfc9bf01f6bd2af3b9028f8e3315e2de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963738"
---
# <a name="wm_cap_file_set_capture_file-message"></a>\_ \_ \_ \_ Messaggio file di acquisizione del set di file di WM Cap \_

Il file di acquisizione del set di file di **WM \_ Cap \_ \_ \_ \_** è il file usato per l'acquisizione video. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capFileSetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilesetcapturefile) .


```C++
WM_CAP_FILE_SET_CAPTURE_FILE 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*
</dt> <dd>

Puntatore alla stringa con terminazione null che contiene il nome del file di acquisizione da utilizzare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito **positivo o negativo** se il nome del file non è valido o se è in corso l'acquisizione di un flusso o un singolo frame.

## <a name="remarks"></a>Commenti

Questo messaggio archivia il nome del file in una struttura interna. Non crea, alloca o apre il file specificato. Il nome file di acquisizione predefinito è C: \\CAPTURE.AVI.

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

 

 





