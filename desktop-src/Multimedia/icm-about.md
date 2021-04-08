---
title: Messaggio di ICM_ABOUT (VFW. h)
description: Il \_ messaggio ICM about invia una notifica a un driver di compressione video per visualizzare la finestra di dialogo informazioni su o esegue una query su un driver di compressione video per determinare se è presente una finestra di dialogo informazioni su. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro ICAbout.
ms.assetid: 6eca69a3-0463-48e6-befb-5003b7515e7d
keywords:
- ICM_ABOUT messaggi multimediali di Windows
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
ms.openlocfilehash: d1e03e88993ba1e345a3ea32a9de7adb2d63abe9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047835"
---
# <a name="icm_about-message"></a>ICM \_ informazioni sul messaggio

Il messaggio **ICM \_ About** invia una notifica a un driver di compressione video per visualizzare la finestra di dialogo informazioni su o esegue una query su un driver di compressione video per determinare se è presente una finestra di dialogo informazioni su. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**ICAbout**](/windows/desktop/api/Vfw/nf-vfw-icabout) .


```C++
ICM_ABOUT 
wParam = (DWORD_PTR) (UINT_PTR) hwnd; 
lParam = 0; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="hwnd"></span><span id="HWND"></span>*HWND*
</dt> <dd>

Handle per la finestra padre della finestra di dialogo visualizzata. È inoltre possibile determinare se un driver dispone di una finestra di dialogo informazioni su, specificando-1 in questo parametro, come nella macro [**ICQueryAbout**](/windows/desktop/api/Vfw/nf-vfw-icqueryabout) . Il driver restituisce ICERR \_ OK se la finestra di dialogo informazioni su o ICERR non è \_ supportata in caso contrario.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce ICERR \_ OK se il driver supporta questo messaggio o ICERR non \_ supportato in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Gestione compressione video](video-compression-manager.md)
</dt> <dt>

[Messaggi di compressione video](video-compression-messages.md)
</dt> </dl>

 

 





