---
description: Notifica a un'applicazione quando l'IME selezionato necessita della stringa convertita dall'applicazione. L'applicazione riceve questo comando tramite il \_ \_ messaggio di richiesta IME WM con i parametri impostati come illustrato di seguito.
ms.assetid: 1a007bed-15e5-4400-9d2f-32e37e1765d2
title: Codice di notifica IMR_DOCUMENTFEED (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc4fe46f95b7ad17ba7bb7850ec3fb9ca980519f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227416"
---
# <a name="imr_documentfeed-notification-code"></a>\_Codice di notifica DOCUMENTFEED di IMR

Notifica a un'applicazione quando l'IME selezionato necessita della stringa convertita dall'applicazione. L'applicazione riceve questo comando tramite il messaggio di [**\_ \_ richiesta IME WM**](wm-ime-request.md) con i parametri impostati come illustrato di seguito.


```C++
LRESULT IMR_DOCUMENTFEED
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Impostare su IMR \_ DOCUMENTFEED.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Puntatore a un buffer per contenere la struttura [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce la struttura della stringa di riconversione corrente. Se *lParam* è impostato su **null**, l'applicazione restituisce la dimensione richiesta per il buffer in cui deve essere contenuta la struttura. Se l'operazione non riesce, il comando restituisce 0.

## <a name="remarks"></a>Commenti

L'IME memorizza nella cache le stringhe convertite per una maggiore accuratezza della conversione. Una limitazione della memorizzazione nella cache dell'IME è la perdita della stringa convertita nei casi seguenti:

-   La posizione del punto di inserimento per l'applicazione viene spostata da una chiave, ad esempio una chiave del cursore.
-   La posizione del punto di inserimento per l'applicazione viene spostata dal mouse.
-   Viene aperto un nuovo documento.

Con il comando **IMR \_ DOCUMENTFEED** , l'IME può aggiornare le stringhe memorizzate nella cache in qualsiasi momento. L'uso di questo comando migliora l'accuratezza della conversione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                 |
| Intestazione<br/>                   | <dl> <dt>Imm. h (Includi Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Gestione metodo di input](input-method-manager.md)
</dt> <dt>

[Comandi di input Method Manager](input-method-manager-commands.md)
</dt> <dt>

[**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring)
</dt> <dt>

[**\_richiesta IME \_ WM**](wm-ime-request.md)
</dt> </dl>

 

 




