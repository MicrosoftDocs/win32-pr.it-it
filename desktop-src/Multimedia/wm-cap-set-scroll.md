---
title: WM_CAP_SET_SCROLL messaggio (Vfw.h)
description: Il messaggio WM \_ CAP SET SCROLL definisce la parte del \_ \_ fotogramma video da visualizzare nella finestra di acquisizione.
ms.assetid: 545605e4-6b1f-403a-a3ab-0fd6750ae776
keywords:
- WM_CAP_SET_SCROLL messaggio Windows Multimediali
topic_type:
- apiref
api_name:
- WM_CAP_SET_SCROLL
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 352d65c2ad8e80622f7ff50cca0a8f7d6e523d53ae002a2325327a634b97c931
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134985"
---
# <a name="wm_cap_set_scroll-message"></a>Messaggio WM \_ CAP \_ SET \_ SCROLL

Il **messaggio WM CAP SET \_ \_ \_ SCROLL** definisce la parte del fotogramma video da visualizzare nella finestra di acquisizione. Questo messaggio imposta l'angolo superiore sinistro dell'area client della finestra di acquisizione alle coordinate di un pixel specificato all'interno del fotogramma video. È possibile inviare questo messaggio in modo esplicito o usando la macro [**capSetScrollPos.**](/windows/desktop/api/Vfw/nf-vfw-capsetscrollpos)


```C++
WM_CAP_SET_SCROLL 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPPOINT) (lpP); 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lpP"></span><span id="lpp"></span><span id="LPP"></span>*Lpp*
</dt> <dd>

Indirizzo per contenere la posizione di scorrimento desiderata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE se** l'operazione ha esito positivo o FALSE **in** caso contrario.

## <a name="remarks"></a>Commenti

La posizione di scorrimento influisce sull'immagine sia in modalità di anteprima che di sovrapposizione.

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

 

 





