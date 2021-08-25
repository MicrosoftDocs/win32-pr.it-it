---
title: ICM_ABOUT messaggio (Vfw.h)
description: Il ICM INFORMAZIONI su invia una notifica a un driver di compressione video per visualizzare la relativa finestra di dialogo Informazioni su o esegue una query su un driver di compressione video per determinare se è disponibile \_ una finestra di dialogo Informazioni su . È possibile inviare questo messaggio in modo esplicito o tramite la macro ICAbout.
ms.assetid: 6eca69a3-0463-48e6-befb-5003b7515e7d
keywords:
- ICM_ABOUT di messaggi Windows multimediali
topic_type:
- apiref
api_name:
- ICM_ABOUT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bf47ff93ef1986d805b2cb37697fdf4d86876c5552fe6aeffb00ff172673018
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119785071"
---
# <a name="icm_about-message"></a>\_ICM Messaggio ABOUT

Il **ICM \_ ABOUT** invia una notifica a un driver di compressione video per visualizzare la finestra di dialogo Informazioni su o esegue una query su un driver di compressione video per determinare se è disponibile una finestra di dialogo Informazioni su . È possibile inviare questo messaggio in modo esplicito o tramite la macro [**ICAbout.**](/windows/desktop/api/Vfw/nf-vfw-icabout)


```C++
ICM_ABOUT 
wParam = (DWORD_PTR) (UINT_PTR) hwnd; 
lParam = 0; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="hwnd"></span><span id="HWND"></span>*Hwnd*
</dt> <dd>

Handle per la finestra padre della finestra di dialogo visualizzata. È anche possibile determinare se un driver dispone di una finestra di dialogo Informazioni su specificando -1 in questo parametro, come nella macro [**ICQueryAbout.**](/windows/desktop/api/Vfw/nf-vfw-icqueryabout) Il driver restituisce ICERR OK se ha una finestra di dialogo Informazioni su \_ o ICERR \_ UNSUPPORTED in caso contrario.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce ICERR OK se il driver supporta questo messaggio o \_ ICERR \_ UNSUPPORTED in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Gestione compressione video](video-compression-manager.md)
</dt> <dt>

[Messaggi di compressione video](video-compression-messages.md)
</dt> </dl>

 

 





