---
title: MCIWNDM_GETSTYLES messaggio (Vfw.h)
description: Il messaggio MCIWNDM GETSTYLES recupera i flag che specificano gli stili di finestra \_ MCIWnd correnti usati da una finestra. È possibile inviare questo messaggio in modo esplicito o tramite la macro MCIWndGetStyles.
ms.assetid: cd34ba05-47cb-488e-a6c6-4ec1c0d25de8
keywords:
- MCIWNDM_GETSTYLES messaggio Windows Multimediali
topic_type:
- apiref
api_name:
- MCIWNDM_GETSTYLES
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 036bd687c5d7828fade23994b9141488354added5ee38d38bafc9c5ce22a954c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119783291"
---
# <a name="mciwndm_getstyles-message"></a>Messaggio MCIWNDM \_ GETSTYLES

Il **messaggio MCIWNDM \_ GETSTYLES** recupera i flag che specificano gli stili di finestra MCIWnd correnti usati da una finestra. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**MCIWndGetStyles.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstyles)


```C++
MCIWNDM_GETSTYLES 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valore restituito

Restituisce un valore che rappresenta gli stili correnti della finestra MCIWnd. Il valore restituito è l'operatore OR bit per bit degli stili della finestra MCIWnd (flag MCIWNDF).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MCIWndGetStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstyles)
</dt> </dl>

 

 





