---
title: Messaggio di ICM_DRAW (VFW. h)
description: Il \_ messaggio di progetto ICM notifica a un driver di rendering di decomprimere un frame di dati e di trascinarlo sullo schermo.
ms.assetid: eceb42c6-d91a-45b7-98dc-e0944df3e558
keywords:
- ICM_DRAW messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_DRAW
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0840c6df2c69f4d3e45600cf8599c214b36200a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741170"
---
# <a name="icm_draw-message"></a>\_Messaggio di progetto ICM

Il messaggio di **\_ progetto ICM** notifica a un driver di rendering di decomprimere un frame di dati e di trascinarlo sullo schermo.


```C++
ICM_DRAW 
wParam = (DWORD) (LPVOID) &icdraw; 
lParam = sizeof(ICDRAW); 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Puntatore a una struttura [**ICDRAW**](/windows/desktop/api/Vfw/ns-vfw-icdraw) .

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Dimensioni, in byte, di [**ICDRAW**](/windows/desktop/api/Vfw/ns-vfw-icdraw).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce ICERR \_ OK se ha esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

Se il \_ flag di aggiornamento ICDRAW è impostato nel membro **DwFlags** di [**ICDRAW**](/windows/desktop/api/Vfw/ns-vfw-icdraw), l'area dello schermo utilizzata per il disegno non è valida e deve essere aggiornata. La portata dell'aggiornamento dipende dal contenuto del membro **lpData** .

Se **lpData** è **null**, il driver deve aggiornare l'intero rettangolo di destinazione con l'immagine corrente. Se il driver mantiene una copia dell'immagine in un buffer fuori schermo, questo messaggio può avere esito negativo. Se **lpData** non è **null**, il driver deve creare i dati e assicurarsi che venga aggiornata l'intera destinazione.

Se il \_ flag sbrigati di ICDRAW è impostato in **dwFlags**, l'applicazione chiamante desidera che il driver proceda il più rapidamente possibile, eventualmente non aggiornando neanche la schermata.

Se il \_ flag di pre-registrazione ICDRAW è impostato in **dwFlags**, questo fotogramma video è costituito da informazioni preliminari e non deve essere visualizzato se possibile. Se ad esempio Play prevede l'avvio dal frame 10 e frame 0 è il fotogramma chiave precedente più vicino, i frame da 0 a 9 avranno ICDRAW \_ preroll set.

Se si desidera che il driver decomprimere i dati in un buffer, inviare il messaggio di [**\_ decompressione ICM**](icm-decompress.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Gestione compressione video](video-compression-manager.md)
</dt> <dt>

[Messaggi di compressione video](video-compression-messages.md)
</dt> </dl>

 

 





