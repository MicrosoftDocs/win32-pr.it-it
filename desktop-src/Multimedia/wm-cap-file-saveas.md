---
title: WM_CAP_FILE_SAVEAS messaggio (Vfw.h)
description: Il messaggio WM \_ CAP \_ FILE \_ SAVEAS copia il contenuto del file di acquisizione in un altro file. È possibile inviare questo messaggio in modo esplicito o tramite la macro capFileSaveAs.
ms.assetid: fab37bee-3160-4ebc-b58f-46021ed49b55
keywords:
- WM_CAP_FILE_SAVEAS messaggio Windows Multimediali
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
ms.openlocfilehash: a200b8e73d81072961ec4e6aa7c8e1dd989bf2d8c3e0480c75908a8761ee93b1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687011"
---
# <a name="wm_cap_file_saveas-message"></a>Messaggio \_ WM CAP FILE \_ \_ SAVEAS

Il **messaggio WM CAP FILE \_ \_ \_ SAVEAS** copia il contenuto del file di acquisizione in un altro file. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**capFileSaveAs.**](/windows/desktop/api/Vfw/nf-vfw-capfilesaveas)


```C++
WM_CAP_FILE_SAVEAS 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*Szname*
</dt> <dd>

Puntatore alla stringa con terminazione Null contenente il nome del file di destinazione utilizzato per copiare il file.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo o FALSE **in** caso contrario.

Se si verifica un errore e viene impostata una funzione di callback di errore usando il messaggio DI ERRORE [**CALLBACK \_ SET \_ \_ SET \_ WM,**](wm-cap-set-callback-error.md) viene chiamata la funzione di callback dell'errore.

## <a name="remarks"></a>Commenti

Questo messaggio non modifica il nome o il contenuto del file di acquisizione corrente.

Se l'operazione di copia non riesce a causa di un errore di disco pieno, il file di destinazione viene eliminato automaticamente.

In genere, un file di acquisizione viene preallocato per il segmento di acquisizione più grande previsto e solo una parte di esso può essere usata per acquisire i dati. Questo messaggio copia solo la parte del file contenente i dati di acquisizione.

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

 

 





