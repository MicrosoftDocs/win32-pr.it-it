---
title: Messaggio di WM_CAP_DRIVER_CONNECT (VFW. h)
description: Il \_ \_ messaggio connessione driver WM Cap \_ connette una finestra di acquisizione a un driver di acquisizione. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro capDriverConnect.
ms.assetid: 8804bb3c-d06c-4ddc-b116-3d292205a52d
keywords:
- WM_CAP_DRIVER_CONNECT messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WM_CAP_DRIVER_CONNECT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d73fdeb89968926429f7225912e3d1b3b348e287
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400530"
---
# <a name="wm_cap_driver_connect-message"></a>\_Messaggio di \_ connessione driver WM Cap \_

Il **messaggio \_ \_ \_ connessione driver WM Cap** connette una finestra di acquisizione a un driver di acquisizione. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capDriverConnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverconnect) .


```C++
WM_CAP_DRIVER_CONNECT 
wParam = (WPARAM) (iIndex); 
lParam = 0L; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*
</dt> <dd>

Indice del driver di acquisizione. L'indice può variare da 0 a 9.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** se il driver di acquisizione specificato non può essere connesso alla finestra di acquisizione.

## <a name="remarks"></a>Commenti

La connessione di un driver di acquisizione a una finestra di acquisizione disconnette automaticamente qualsiasi driver di acquisizione connesso in precedenza.

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

 

 





