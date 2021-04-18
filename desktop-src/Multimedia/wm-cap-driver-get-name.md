---
title: Messaggio di WM_CAP_DRIVER_GET_NAME (VFW. h)
description: Il \_ messaggio WM Cap \_ driver \_ get \_ Name restituisce il nome del driver di acquisizione connesso alla finestra di acquisizione. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro capDriverGetName.
ms.assetid: 84cecaf1-e0ff-424f-8c10-8bfe5cc2e7ea
keywords:
- WM_CAP_DRIVER_GET_NAME messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WM_CAP_DRIVER_GET_NAME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 256b5f7913c83ddd278f3f3a05552b3d81070c73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475857"
---
# <a name="wm_cap_driver_get_name-message"></a>\_Messaggio di \_ \_ nome Get driver WM Cap \_

Il messaggio **WM \_ Cap \_ driver \_ get \_ Name** restituisce il nome del driver di acquisizione connesso alla finestra di acquisizione. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capDriverGetName**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetname) .


```C++
WM_CAP_DRIVER_GET_NAME 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*
</dt> <dd>

Dimensione, in byte, del buffer a cui fa riferimento **szName**.

</dd> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*
</dt> <dd>

Puntatore a un buffer definito dall'applicazione usato per restituire il nome del dispositivo come stringa con terminazione null.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** se la finestra di acquisizione non è connessa a un driver di acquisizione.

## <a name="remarks"></a>Commenti

Il nome è una stringa di testo recuperata dall'area delle risorse del driver. Le applicazioni devono allocare circa 80 byte per questa stringa. Se il driver non contiene una risorsa nome, viene restituito il nome del percorso completo del driver elencato nel registro di sistema o nel file di SYSTEM.INI.

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

 

 





