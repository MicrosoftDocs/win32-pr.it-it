---
title: Messaggio di WM_CAP_GET_VIDEOFORMAT (VFW. h)
description: Il \_ messaggio WM Cap \_ get \_ VIDEOFORMAT recupera una copia del formato video in uso o le dimensioni necessarie per il formato video. È possibile inviare questo messaggio in modo esplicito o usando le macro capGetVideoFormat e capGetVideoFormatSize.
ms.assetid: ac72dfdb-fe1a-4007-bdce-41e5e67d076a
keywords:
- WM_CAP_GET_VIDEOFORMAT messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WM_CAP_GET_VIDEOFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 072d71366efee550b037d4a20388817954937854
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964187"
---
# <a name="wm_cap_get_videoformat-message"></a>\_ \_ \_ Messaggio VIDEOFORMAT di WM Cap

Il messaggio **WM \_ Cap \_ get \_ VIDEOFORMAT** recupera una copia del formato video in uso o le dimensioni necessarie per il formato video. È possibile inviare questo messaggio in modo esplicito o usando le macro [**capGetVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformat) e [**capGetVideoFormatSize**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformatsize) .


```C++
WM_CAP_GET_VIDEOFORMAT 
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

Puntatore a una struttura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) . È anche possibile specificare **null** per recuperare il numero di byte necessari.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce la dimensione, in byte, del formato video o zero se la finestra di acquisizione non è connessa a un driver di acquisizione. Per i formati video che richiedono una tavolozza, viene restituita anche la tavolozza corrente.

## <a name="remarks"></a>Commenti

Poiché i formati video compressi variano in requisiti di dimensioni, le applicazioni devono prima recuperare le dimensioni, quindi allocare memoria e infine richiedere i dati in formato video.

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

 

