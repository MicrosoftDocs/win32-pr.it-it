---
title: Messaggio di MCIWNDM_GETSTYLES (VFW. h)
description: Il \_ messaggio MCIWNDM GETstyles recupera i flag che specificano gli stili correnti della finestra MCIWnd usati da una finestra. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro MCIWndGetStyles.
ms.assetid: cd34ba05-47cb-488e-a6c6-4ec1c0d25de8
keywords:
- MCIWNDM_GETSTYLES messaggi multimediali di Windows
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
ms.openlocfilehash: 983e37291977edf2473c2b603cd5b40792fb7989
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302508"
---
# <a name="mciwndm_getstyles-message"></a>\_Messaggio GETstyles MCIWNDM

Il messaggio **MCIWNDM \_ GetStyles** recupera i flag che specificano gli stili correnti della finestra MCIWnd usati da una finestra. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndGetStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstyles) .


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
| Intestazione<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MCIWndGetStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstyles)
</dt> </dl>

 

 





