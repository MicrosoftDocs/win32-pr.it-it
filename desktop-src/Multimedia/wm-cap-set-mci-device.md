---
title: WM_CAP_SET_MCI_DEVICE messaggio (Vfw.h)
description: Il messaggio WM CAP SET MCI DEVICE specifica il nome del dispositivo video MCI da usare per \_ \_ acquisire i \_ \_ dati. È possibile inviare questo messaggio in modo esplicito o usando la macro capSetMCIDeviceName.
ms.assetid: 83fdf567-ceb2-45aa-8529-433a5c64ac0a
keywords:
- WM_CAP_SET_MCI_DEVICE messaggio Windows Multimedia
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
ms.openlocfilehash: f2df82b171e2353b51198fcd4a908abb586d981417c3fd14e5a81731975012aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118622180"
---
# <a name="wm_cap_set_mci_device-message"></a>Messaggio \_ WM CAP SET \_ \_ MCI \_ DEVICE

Il **messaggio WM CAP SET \_ \_ \_ MCI \_ DEVICE** specifica il nome del dispositivo video MCI da usare per acquisire i dati. È possibile inviare questo messaggio in modo esplicito o usando la macro [**capSetMCIDeviceName.**](/windows/desktop/api/Vfw/nf-vfw-capsetmcidevicename)


```C++
WM_CAP_SET_MCI_DEVICE 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*Szname*
</dt> <dd>

Puntatore a una stringa con terminazione Null contenente il nome del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo o FALSE **in** caso contrario.

## <a name="remarks"></a>Commenti

Questo messaggio archivia il nome del dispositivo MCI in una struttura interna. Non si apre né si accede al dispositivo. Il nome del dispositivo predefinito è **NULL.**

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

 

 





