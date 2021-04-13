---
title: Messaggio di WM_CAP_FILE_SAVEAS (VFW. h)
description: Il \_ \_ messaggio SaveAs del file WM Cap \_ copia il contenuto del file di acquisizione in un altro file. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro capFileSaveAs.
ms.assetid: fab37bee-3160-4ebc-b58f-46021ed49b55
keywords:
- WM_CAP_FILE_SAVEAS messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WM_CAP_FILE_SAVEAS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aca099fefab7ca0f4ef391b1b65e89938a947a01
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400424"
---
# <a name="wm_cap_file_saveas-message"></a>\_ \_ Messaggio SaveAs file di WM Cap \_

Il **messaggio \_ \_ \_ SaveAs del file WM Cap** copia il contenuto del file di acquisizione in un altro file. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capFileSaveAs**](/windows/desktop/api/Vfw/nf-vfw-capfilesaveas) .


```C++
WM_CAP_FILE_SAVEAS 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*
</dt> <dd>

Puntatore alla stringa con terminazione null che contiene il nome del file di destinazione utilizzato per copiare il file.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione è riuscita o **false** in caso contrario.

Se si verifica un errore e viene impostata una funzione di callback di errore utilizzando il messaggio di errore di richiamata di [**WM \_ Cap \_ set \_ \_**](wm-cap-set-callback-error.md) , viene chiamata la funzione di callback dell'errore.

## <a name="remarks"></a>Commenti

Questo messaggio non modifica il nome o il contenuto del file di acquisizione corrente.

Se l'operazione di copia ha esito negativo a causa di un errore del disco completo, il file di destinazione viene eliminato automaticamente.

In genere, un file di acquisizione è preallocato per il segmento di acquisizione più grande previsto e solo una parte di esso potrebbe essere usato per acquisire i dati. Questo messaggio copia solo la parte del file che contiene i dati di acquisizione.

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

 

 





