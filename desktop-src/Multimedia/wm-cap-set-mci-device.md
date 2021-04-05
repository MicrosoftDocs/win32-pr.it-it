---
title: Messaggio di WM_CAP_SET_MCI_DEVICE (VFW. h)
description: Il \_ messaggio del dispositivo WM Cap \_ set \_ MCI \_ specifica il nome del dispositivo video MCI da usare per l'acquisizione dei dati. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro capSetMCIDeviceName.
ms.assetid: 83fdf567-ceb2-45aa-8529-433a5c64ac0a
keywords:
- WM_CAP_SET_MCI_DEVICE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WM_CAP_SET_MCI_DEVICE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86187f3357bf72866e05b497332454c10bcd2fd3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740055"
---
# <a name="wm_cap_set_mci_device-message"></a>Messaggio di set di WM \_ Cap \_ set \_ MCI \_

Il messaggio del **\_ dispositivo WM Cap \_ set \_ MCI \_** specifica il nome del dispositivo video MCI da usare per l'acquisizione dei dati. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capSetMCIDeviceName**](/windows/desktop/api/Vfw/nf-vfw-capsetmcidevicename) .


```C++
WM_CAP_SET_MCI_DEVICE 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*
</dt> <dd>

Puntatore a una stringa con terminazione null che contiene il nome del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione è riuscita o **false** in caso contrario.

## <a name="remarks"></a>Commenti

Questo messaggio archivia il nome del dispositivo MCI in una struttura interna. Non apre né accede al dispositivo. Il nome del dispositivo predefinito è **null**.

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

 

 





