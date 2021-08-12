---
title: WM_CAP_DRIVER_CONNECT messaggio (Vfw.h)
description: Il messaggio WM \_ CAP DRIVER CONNECT connette una finestra di acquisizione a un driver di \_ \_ acquisizione. È possibile inviare questo messaggio in modo esplicito o usando la macro capDriverConnect.
ms.assetid: 8804bb3c-d06c-4ddc-b116-3d292205a52d
keywords:
- WM_CAP_DRIVER_CONNECT messaggio Windows Multimediali
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
ms.openlocfilehash: c8b0e54d496302488db653505321778bcd22546bd2ed9b2180aa0e15cb6969f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118622630"
---
# <a name="wm_cap_driver_connect-message"></a>Messaggio \_ WM CAP DRIVER \_ \_ CONNECT

Il **messaggio WM CAP DRIVER \_ \_ \_ CONNECT** connette una finestra di acquisizione a un driver di acquisizione. È possibile inviare questo messaggio in modo esplicito o usando la macro [**capDriverConnect.**](/windows/desktop/api/Vfw/nf-vfw-capdriverconnect)


```C++
WM_CAP_DRIVER_CONNECT 
wParam = (WPARAM) (iIndex); 
lParam = 0L; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*Iindex*
</dt> <dd>

Indice del driver di acquisizione. L'indice può variare da 0 a 9.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE** se ha esito positivo **o FALSE** se il driver di acquisizione specificato non può essere connesso alla finestra di acquisizione.

## <a name="remarks"></a>Commenti

La connessione di un driver di acquisizione a una finestra di acquisizione disconnette automaticamente qualsiasi driver di acquisizione connesso in precedenza.

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

 

 





