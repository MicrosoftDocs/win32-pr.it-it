---
title: WM_CAP_GET_STATUS messaggio (Vfw.h)
description: Il messaggio WM \_ CAP GET STATUS recupera lo stato della finestra di \_ \_ acquisizione. È possibile inviare questo messaggio in modo esplicito o usando la macro capGetStatus.
ms.assetid: 31349599-a52c-45ba-8f08-91008773f317
keywords:
- WM_CAP_GET_STATUS messaggio Windows Multimediali
topic_type:
- apiref
api_name:
- WM_CAP_GET_STATUS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 805befc3f83c79b157e040004dcf382dccaf07b240b3b846892b8fb035f826ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118135157"
---
# <a name="wm_cap_get_status-message"></a>Messaggio \_ DI STATO GET \_ CAP WM \_

Il **messaggio WM CAP GET \_ \_ \_ STATUS** recupera lo stato della finestra di acquisizione. È possibile inviare questo messaggio in modo esplicito o usando la macro [**capGetStatus.**](/windows/desktop/api/Vfw/nf-vfw-capgetstatus)


```C++
WM_CAP_GET_STATUS 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPCAPSTATUS) (s); 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*
</dt> <dd>

Dimensione, in byte, della struttura a cui fa riferimento **s**.

</dd> <dt>

<span id="s"></span><span id="S"></span>*s*
</dt> <dd>

Puntatore a una [**struttura CAPSTATUS.**](/windows/win32/api/vfw/ns-vfw-capstatus)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE se** l'operazione ha esito positivo o **FALSE** se la finestra di acquisizione non è connessa a un driver di acquisizione.

## <a name="remarks"></a>Commenti

La [**struttura CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) contiene lo stato corrente della finestra di acquisizione. Poiché questo stato è dinamico e cambia in risposta a vari messaggi, l'applicazione deve inizializzare questa struttura dopo l'invio del messaggio [**WM \_ CAP \_ DLG \_ VIDEOFORMAT**](wm-cap-dlg-videoformat.md) (o l'uso della macro [**capDlgVideoFormat)**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideoformat) e ogni volta che è necessario abilitare le voci di menu o determinare lo stato effettivo della finestra.

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

 

 





