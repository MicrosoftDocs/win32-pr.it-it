---
title: MCIWNDM_SETZOOM messaggio (Vfw.h)
description: Il messaggio MCIWNDM \_ SETZOOM ridimensiona un'immagine video in base a un fattore di zoom. Questa proprietà regola le dimensioni di una finestra MCIWnd mantenendo proporzioni costanti. È possibile inviare questo messaggio in modo esplicito o tramite la macro MCIWndSetZoom.
ms.assetid: c899b678-5ba7-4f0a-9ef9-c5370b3b4ea8
keywords:
- MCIWNDM_SETZOOM messaggio Windows Multimediali
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
ms.openlocfilehash: fbcdd40206332df442bbae32975b0d888bbe39bc377a189d40e215888e4a6d0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807581"
---
# <a name="mciwndm_setzoom-message"></a>Messaggio MCIWNDM \_ SETZOOM

Il **messaggio MCIWNDM \_ SETZOOM** ridimensiona un'immagine video in base a un fattore di zoom. Questa proprietà regola le dimensioni di una finestra MCIWnd mantenendo proporzioni costanti. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**MCIWndSetZoom.**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetzoom)


```C++
MCIWNDM_SETZOOM 
wParam = 0; 
lParam = (LPARAM) (UINT) iZoom; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="iZoom"></span><span id="izoom"></span><span id="IZOOM"></span>*Izoom*
</dt> <dd>

Fattore di zoom espresso come percentuale dell'immagine originale. Specificare 100 per visualizzare l'immagine con le dimensioni di creazione, 200 per visualizzare l'immagine al doppio delle dimensioni normali o 50 per visualizzare l'immagine a metà delle dimensioni normali.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce un valore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MCIWndSetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetzoom)
</dt> </dl>

 

 





