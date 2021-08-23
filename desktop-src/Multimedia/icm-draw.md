---
title: ICM_DRAW messaggio (Vfw.h)
description: Il ICM DRAW notifica a un driver di rendering di decomprimere un frame di dati e \_ disegnarlo sullo schermo.
ms.assetid: eceb42c6-d91a-45b7-98dc-e0944df3e558
keywords:
- ICM_DRAW messaggio Windows Multimediali
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
ms.openlocfilehash: e44216e523da62e0dde22abed8d88b9b8aacd8f68119a88f3177f45ecd910029
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119784991"
---
# <a name="icm_draw-message"></a>\_ICM Messaggio DRAW

Il **ICM \_ DRAW** notifica a un driver di rendering di decomprimere un frame di dati e disegnarlo sullo schermo.


```C++
ICM_DRAW 
wParam = (DWORD) (LPVOID) &icdraw; 
lParam = sizeof(ICDRAW); 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*Wparam*
</dt> <dd>

Puntatore a [**una struttura ICDRAW.**](/windows/desktop/api/Vfw/ns-vfw-icdraw)

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Dimensioni, in byte, di [**ICDRAW.**](/windows/desktop/api/Vfw/ns-vfw-icdraw)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce ICERR \_ OK in caso di esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

Se il flag ICDRAW UPDATE è impostato nel membro \_ **dwFlags** di [**ICDRAW,**](/windows/desktop/api/Vfw/ns-vfw-icdraw)l'area dello schermo usata per il disegno non è valida e deve essere aggiornata. L'estensione dell'aggiornamento dipende dal contenuto del **membro lpData.**

Se **lpData** è **NULL,** il driver deve aggiornare l'intero rettangolo di destinazione con l'immagine corrente. Se il driver mantiene una copia dell'immagine in un buffer fuori schermo, questo messaggio potrebbe non riuscire. Se **lpData** non è **NULL,** il driver deve disegnare i dati e assicurarsi che l'intera destinazione sia aggiornata.

Se il flag ICDRAW HURRYUP è impostato \_ in **dwFlags**, l'applicazione chiamante vuole che il driver proceda il più rapidamente possibile, probabilmente non aggiornando nemmeno lo schermo.

Se il flag PREROLL di ICDRAW è impostato \_ in **dwFlags,** questo fotogramma video è informazioni preliminari e non deve essere visualizzato, se possibile. Ad esempio, se la riproduzione deve iniziare dal fotogramma 10 e il fotogramma 0 è il fotogramma chiave precedente più vicino, i fotogrammi da 0 a 9 avranno preroll ICDRAW \_ impostato.

Se si vuole che il driver decomprime i dati in un buffer, inviare il ICM [**\_ messaggio DECOMPRESS.**](icm-decompress.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Gestione compressione video](video-compression-manager.md)
</dt> <dt>

[Messaggi di compressione video](video-compression-messages.md)
</dt> </dl>

 

 





