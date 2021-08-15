---
title: WM_CAP_DRIVER_GET_NAME messaggio (Vfw.h)
description: Il messaggio WM \_ CAP DRIVER GET NAME restituisce il nome del driver di acquisizione connesso alla finestra di \_ \_ \_ acquisizione. È possibile inviare questo messaggio in modo esplicito o usando la macro capDriverGetName.
ms.assetid: 84cecaf1-e0ff-424f-8c10-8bfe5cc2e7ea
keywords:
- WM_CAP_DRIVER_GET_NAME messaggio Windows Multimediali
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
ms.openlocfilehash: 0dc44efae992f2967cb069c0866fbb7f9febed51ea73f94853a1b017bc57a068
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118369682"
---
# <a name="wm_cap_driver_get_name-message"></a>Messaggio GET NAME del DRIVER WM \_ CAP \_ \_ \_

Il **messaggio WM CAP DRIVER GET \_ \_ \_ \_ NAME** restituisce il nome del driver di acquisizione connesso alla finestra di acquisizione. È possibile inviare questo messaggio in modo esplicito o usando la macro [**capDriverGetName.**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetname)


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

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*Szname*
</dt> <dd>

Puntatore a un buffer definito dall'applicazione utilizzato per restituire il nome del dispositivo come stringa con terminazione Null.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE se** l'operazione ha esito positivo o **FALSE** se la finestra di acquisizione non è connessa a un driver di acquisizione.

## <a name="remarks"></a>Commenti

Il nome è una stringa di testo recuperata dall'area delle risorse del driver. Le applicazioni devono allocare circa 80 byte per questa stringa. Se il driver non contiene una risorsa nome, viene restituito il nome completo del percorso del driver elencato nel Registro di sistema o nel file SYSTEM.INI file.

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

 

 





