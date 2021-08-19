---
description: Notifica a un'applicazione quando un IME selezionato richiede una stringa per la riconversione. L'applicazione riceve questo comando tramite il messaggio WM \_ IME \_ REQUEST con le impostazioni dei parametri, come illustrato di seguito.
ms.assetid: 82ef20b5-bdfa-4bde-abb4-3d14ae35c116
title: IMR_RECONVERTSTRING codice di notifica (Imm.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0dfc2b188a2873af3ec7004ffaac65a3cce0b4257c1428dfe4abfcba9d2b2aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118948758"
---
# <a name="imr_reconvertstring-notification-code"></a>Codice di notifica \_ IMR RECONVERTSTRING

Notifica a un'applicazione quando un IME selezionato richiede una stringa per la riconversione. L'applicazione riceve questo comando tramite il messaggio [**WM \_ IME \_ REQUEST**](wm-ime-request.md) con le impostazioni dei parametri, come illustrato di seguito.


```C++
LRESULT IMR_RECONVERTSTRING
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*Wparam*
</dt> <dd>

Impostare su IMR \_ RECONVERTSTRING.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Puntatore a un buffer contenente la struttura e le stringhe [**RECONVERTSTRING.**](/windows/win32/api/imm/ns-imm-reconvertstring)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce la struttura della stringa di riconversione corrente. Se *lParam è* impostato su **NULL,** l'applicazione restituisce le dimensioni del buffer necessario per contenere la struttura. Il comando restituisce 0 se non ha esito positivo.

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

 

 




