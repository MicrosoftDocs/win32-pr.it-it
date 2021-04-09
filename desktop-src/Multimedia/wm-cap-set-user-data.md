---
title: Messaggio di WM_CAP_SET_USER_DATA (VFW. h)
description: Il \_ messaggio WM Cap \_ set \_ User \_ Data associa un \_ valore di dati ptr lungo a una finestra di acquisizione. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro capSetUserData.
ms.assetid: 067502e3-f009-4cf2-b612-4a0b64624416
keywords:
- WM_CAP_SET_USER_DATA messaggi multimediali di Windows
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
ms.openlocfilehash: 542b8e49f740bfc265824947237841dede1f6065
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121390"
---
# <a name="wm_cap_set_user_data-message"></a>\_Messaggio di \_ \_ dati utente \_ per l'impostazione di WM Cap

Il messaggio **WM \_ Cap \_ set \_ User \_ Data** associa un valore di dati **\_ ptr lungo** a una finestra di acquisizione. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capSetUserData**](/windows/desktop/api/Vfw/nf-vfw-capsetuserdata) .


```C++
WM_CAP_SET_USER_DATA 
wParam = (WPARAM) 0; 
lParam = (LPARAM)lUser; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lUser"></span><span id="luser"></span><span id="LUSER"></span>*lUser*
</dt> <dd>

Valore di dati da associare a una finestra di acquisizione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione è riuscita o **false** se è in corso l'acquisizione di flussi.

## <a name="remarks"></a>Commenti

In genere questo messaggio viene usato per puntare a un blocco di dati associato a una finestra di acquisizione.

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

 

 





