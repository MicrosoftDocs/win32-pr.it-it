---
title: WM_CAP_FILE_SET_INFOCHUNK messaggio (Vfw.h)
description: Il messaggio WM \_ CAP \_ FILE SET \_ \_ INFOCHUNK imposta e cancella i blocchi di informazioni.
ms.assetid: 67d11a05-a2b4-45d2-ba66-83a198745303
keywords:
- WM_CAP_FILE_SET_INFOCHUNK messaggio Windows Multimediali
topic_type:
- apiref
api_name:
- WM_CAP_FILE_SET_INFOCHUNK
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06d64f88a87af63e5afc513e0e2cf2df53d64570bec099a2f8f2846d781fc0b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119892071"
---
# <a name="wm_cap_file_set_infochunk-message"></a>Messaggio WM \_ CAP \_ FILE SET \_ \_ INFOCHUNK

Il **messaggio WM CAP FILE SET \_ \_ \_ \_ INFOCHUNK** imposta e cancella i blocchi di informazioni. I blocchi di informazioni possono essere inseriti in un file AVI durante l'acquisizione per incorporare stringhe di testo o dati personalizzati. È possibile inviare questo messaggio in modo esplicito o usando la macro [**capFileSetInfoChunk.**](/windows/desktop/api/Vfw/nf-vfw-capfilesetinfochunk)


```C++
WM_CAP_FILE_SET_INFOCHUNK 
wParam = (WPARAM)0; 
lParam = (LPARAM) (LPCAPINFOCHUNK) (lpInfoChunk); 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lpInfoChunk"></span><span id="lpinfochunk"></span><span id="LPINFOCHUNK"></span>*lpInfoChunk*
</dt> <dd>

Puntatore a [**una struttura CAPINFOCHUNK**](/windows/win32/api/vfw/ns-vfw-capinfochunk) che definisce il blocco di informazioni da creare o eliminare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE se** l'operazione ha esito positivo o FALSE **in** caso contrario.

Se si verifica un errore e viene impostata una funzione di callback degli errori usando il messaggio [**WM CAP SET CALLBACK \_ \_ \_ \_ ERROR,**](wm-cap-set-callback-error.md) viene chiamata la funzione di callback degli errori.

## <a name="remarks"></a>Commenti

È possibile aggiungere più blocchi di informazioni registrati a un file AVI. Dopo l'impostazione, un blocco di informazioni continua ad essere aggiunto ai file di acquisizione successivi fino a quando la voce non viene cancellata o non vengono cancellate tutte le voci del blocco di informazioni. Per cancellare una singola voce, specificare il blocco di informazioni nel membro **fccInfoID** e **NULL** nel membro **lpData** della [**struttura CAPINFOCHUNK.**](/windows/win32/api/vfw/ns-vfw-capinfochunk) Per cancellare tutte le voci, specificare **NULL** in **fccInfoID**.

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

 

 





