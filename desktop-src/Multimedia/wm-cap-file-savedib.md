---
title: WM_CAP_FILE_SAVEDIB messaggio (Vfw.h)
description: Il messaggio WM \_ CAP \_ FILE \_ SAVEDIB copia il frame corrente in un file DIB. È possibile inviare questo messaggio in modo esplicito o tramite la macro capFileSaveDIB.
ms.assetid: bf6d343b-9236-4e68-bbda-2ed6e197a5cb
keywords:
- WM_CAP_FILE_SAVEDIB messaggio Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_FILE_SAVEDIB
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66d6dd9b8675e1fb8625349afc4b3f86347d71d605407d5c99fbca291ade744d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119803811"
---
# <a name="wm_cap_file_savedib-message"></a>Messaggio \_ WM CAP FILE \_ \_ SAVEDIB

Il **messaggio WM CAP FILE \_ \_ \_ SAVEDIB** copia il frame corrente in un file DIB. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**capFileSaveDIB.**](/windows/desktop/api/Vfw/nf-vfw-capfilesavedib)


```C++
WM_CAP_FILE_SAVEDIB 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*Szname*
</dt> <dd>

Puntatore alla stringa con terminazione Null che contiene il nome del file DIB di destinazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo o FALSE **in** caso contrario.

Se si verifica un errore e viene impostata una funzione di callback di errore usando il messaggio DI ERRORE [**CALLBACK \_ SET \_ \_ SET \_ WM,**](wm-cap-set-callback-error.md) viene chiamata la funzione di callback dell'errore.

## <a name="remarks"></a>Commenti

Se il driver di acquisizione fornisce frame in un formato compresso, questa chiamata tenta di decomprimere il frame prima di scrivere il file.

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

 

 





