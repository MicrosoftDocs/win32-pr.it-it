---
description: Notifica a un'applicazione quando l'IME selezionato richiede la stringa convertita dall'applicazione. L'applicazione riceve questo comando tramite il messaggio WM \_ IME \_ REQUEST con i parametri impostati come illustrato di seguito.
ms.assetid: 1a007bed-15e5-4400-9d2f-32e37e1765d2
title: IMR_DOCUMENTFEED di notifica (Imm.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbef4c83d35fa02e2c879d76b9520df6d01588c07cb725b13e66888e9dd27722
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118948778"
---
# <a name="imr_documentfeed-notification-code"></a>ImR DOCUMENTFEED notification code (Codice \_ di notifica IMR DOCUMENTFEED)

Notifica a un'applicazione quando l'IME selezionato richiede la stringa convertita dall'applicazione. L'applicazione riceve questo comando tramite il messaggio [**WM \_ IME \_ REQUEST**](wm-ime-request.md) con i parametri impostati come illustrato di seguito.


```C++
LRESULT IMR_DOCUMENTFEED
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*Wparam*
</dt> <dd>

Impostare su IMR \_ DOCUMENTFEED.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Puntatore a un buffer per contenere la [**struttura RECONVERTSTRING.**](/windows/win32/api/imm/ns-imm-reconvertstring)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce la struttura della stringa di riconversione corrente. Se *lParam è* impostato su **NULL,** l'applicazione restituisce le dimensioni necessarie per il buffer per contenere la struttura. Il comando restituisce 0 se non ha esito positivo.

## <a name="remarks"></a>Commenti

L'IME memorizza nella cache le stringhe convertite per una maggiore accuratezza della conversione. Una limitazione della memorizzazione nella cache dell'IME è la perdita della stringa convertita nelle circostanze seguenti:

-   La posizione del cursore per l'applicazione viene spostata da un tasto, ad esempio un tasto di cursore.
-   La posizione del cursore per l'applicazione viene spostata dal mouse.
-   Viene aperto un nuovo documento.

Con il **comando IMR \_ DOCUMENTFEED,** l'IME può aggiornare le stringhe memorizzate nella cache in qualsiasi momento. L'uso di questo comando migliora l'accuratezza della conversione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                 |
| Intestazione<br/>                   | <dl> <dt>Imm.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Gestione metodi di input](input-method-manager.md)
</dt> <dt>

[Comandi di Gestione metodi di input](input-method-manager-commands.md)
</dt> <dt>

[**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring)
</dt> <dt>

[**RICHIESTA \_ IME \_ WM**](wm-ime-request.md)
</dt> </dl>

 

 




