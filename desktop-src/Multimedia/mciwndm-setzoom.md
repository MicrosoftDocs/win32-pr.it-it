---
title: Messaggio di MCIWNDM_SETZOOM (VFW. h)
description: Il \_ messaggio MCIWNDM di Zoom ridimensiona un'immagine video in base a un fattore di zoom. Questo Marco regola le dimensioni di una finestra MCIWnd mantenendo le proporzioni costanti. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro MCIWndSetZoom.
ms.assetid: c899b678-5ba7-4f0a-9ef9-c5370b3b4ea8
keywords:
- MCIWNDM_SETZOOM messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_SETZOOM
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80ecb513735c4e62266892e8ad55c7bf5daca151
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475515"
---
# <a name="mciwndm_setzoom-message"></a>MCIWNDM- \_ messaggio di zoom

Il messaggio **MCIWNDM di \_ Zoom** ridimensiona un'immagine video in base a un fattore di zoom. Questo Marco regola le dimensioni di una finestra MCIWnd mantenendo le proporzioni costanti. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndSetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetzoom) .


```C++
MCIWNDM_SETZOOM 
wParam = 0; 
lParam = (LPARAM) (UINT) iZoom; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="iZoom"></span><span id="izoom"></span><span id="IZOOM"></span>*iZoom*
</dt> <dd>

Fattore di zoom espresso come percentuale dell'immagine originale. Specificare 100 per visualizzare l'immagine alla dimensione creata, 200 per visualizzare l'immagine al doppio delle dimensioni normali o 50 per visualizzare l'immagine a metà delle dimensioni normali.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce alcun valore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MCIWndSetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetzoom)
</dt> </dl>

 

 





