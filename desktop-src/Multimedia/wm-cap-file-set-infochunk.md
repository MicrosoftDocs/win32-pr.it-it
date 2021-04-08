---
title: Messaggio di WM_CAP_FILE_SET_INFOCHUNK (VFW. h)
description: Il \_ \_ \_ set di file di WM Cap \_ imposta INFOCHUNK e cancella i blocchi di informazioni.
ms.assetid: 67d11a05-a2b4-45d2-ba66-83a198745303
keywords:
- WM_CAP_FILE_SET_INFOCHUNK messaggi multimediali di Windows
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
ms.openlocfilehash: 067ba00563a5ca511f13b23615fc4542090ba397
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047890"
---
# <a name="wm_cap_file_set_infochunk-message"></a>\_ \_ \_ Messaggio INFOCHUNK set di file WM Cap \_

Il **set di file di WM \_ Cap imposta \_ \_ \_ INFOCHUNK** e cancella i blocchi di informazioni. I blocchi di informazioni possono essere inseriti in un file AVI durante l'acquisizione per incorporare stringhe di testo o dati personalizzati. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capFileSetInfoChunk**](/windows/desktop/api/Vfw/nf-vfw-capfilesetinfochunk) .


```C++
WM_CAP_FILE_SET_INFOCHUNK 
wParam = (WPARAM)0; 
lParam = (LPARAM) (LPCAPINFOCHUNK) (lpInfoChunk); 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lpInfoChunk"></span><span id="lpinfochunk"></span><span id="LPINFOCHUNK"></span>*lpInfoChunk*
</dt> <dd>

Puntatore a una struttura [**CAPINFOCHUNK**](/windows/win32/api/vfw/ns-vfw-capinfochunk) che definisce il blocco di informazioni da creare o eliminare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione è riuscita o **false** in caso contrario.

Se si verifica un errore e viene impostata una funzione di callback di errore utilizzando il messaggio di errore di richiamata di [**WM \_ Cap \_ set \_ \_**](wm-cap-set-callback-error.md) , viene chiamata la funzione di callback dell'errore.

## <a name="remarks"></a>Commenti

È possibile aggiungere più blocchi di informazioni registrate a un file AVI. Dopo aver impostato un blocco di informazioni, questo continua a essere aggiunto ai file di acquisizione successivi fino alla cancellazione della voce o alla cancellazione di tutte le voci del blocco di informazioni. Per cancellare una singola voce, specificare il blocco Information nel membro **fccInfoID** e **null** nel membro **lpData** della struttura [**CAPINFOCHUNK**](/windows/win32/api/vfw/ns-vfw-capinfochunk) . Per cancellare tutte le voci, specificare **null** in **fccInfoID**.

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

 

 





