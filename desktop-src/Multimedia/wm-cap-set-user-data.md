---
title: WM_CAP_SET_USER_DATA messaggio (Vfw.h)
description: Il messaggio WM \_ CAP SET USER DATA associa un valore di dati LONG \_ \_ \_ \_ PTR a una finestra di acquisizione. È possibile inviare questo messaggio in modo esplicito o tramite la macro capSetUserData.
ms.assetid: 067502e3-f009-4cf2-b612-4a0b64624416
keywords:
- WM_CAP_SET_USER_DATA messaggio Windows Multimediali
topic_type:
- apiref
api_name:
- WM_CAP_SET_USER_DATA
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea5b4a192b774572ea374b08d4a4128389281e44ee00614806841b0b007d978b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119803551"
---
# <a name="wm_cap_set_user_data-message"></a>Messaggio \_ WM CAP SET USER \_ \_ \_ DATA

Il **messaggio WM CAP SET USER \_ \_ \_ \_ DATA** associa un **valore di dati LONG \_ PTR** a una finestra di acquisizione. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**capSetUserData.**](/windows/desktop/api/Vfw/nf-vfw-capsetuserdata)


```C++
WM_CAP_SET_USER_DATA 
wParam = (WPARAM) 0; 
lParam = (LPARAM)lUser; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lUser"></span><span id="luser"></span><span id="LUSER"></span>*lUser*
</dt> <dd>

Valore dei dati da associare a una finestra di acquisizione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE se** l'operazione ha esito positivo o **FALSE** se è in corso l'acquisizione del flusso.

## <a name="remarks"></a>Commenti

In genere questo messaggio viene usato per puntare a un blocco di dati associato a una finestra di acquisizione.

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

 

 





