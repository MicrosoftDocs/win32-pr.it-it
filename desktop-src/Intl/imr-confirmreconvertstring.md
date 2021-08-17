---
description: Notifica a un'applicazione quando l'IME deve modificare la struttura RECONVERTSTRING. L'applicazione riceve questo comando tramite il messaggio WM \_ IME \_ REQUEST con le impostazioni dei parametri, come illustrato di seguito.
ms.assetid: 035a7072-d292-4883-bc3e-d1e9ed64d9ec
title: IMR_CONFIRMRECONVERTSTRING di notifica (Imm.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a0fd1c38c7552d09489c51b9acc897f679aa3a218e86bbba222225fcff57e90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118948798"
---
# <a name="imr_confirmreconvertstring-notification-code"></a>Codice di \_ notifica IMR CONFIRMRECONVERTSTRING

Notifica a un'applicazione quando l'IME deve modificare la [**struttura RECONVERTSTRING.**](/windows/win32/api/imm/ns-imm-reconvertstring) L'applicazione riceve questo comando tramite il messaggio [**WM \_ IME \_ REQUEST**](wm-ime-request.md) con le impostazioni dei parametri, come illustrato di seguito.


```C++
LRESULT IMR_CONFIRMRECONVERTSTRING
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*Wparam*
</dt> <dd>

Impostare su IMR \_ CONFIRMRECONVERTSTRING.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Puntatore a [**una struttura RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) dall'IME. Per altre informazioni, vedere la sezione Osservazioni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero se l'applicazione accetta la struttura [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) modificata. In caso contrario, il comando restituisce 0 e l'IME usa la **struttura RECONVERTSTRING** originale.

## <a name="remarks"></a>Commenti

L'applicazione inserisce la [**struttura RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) alla ricezione del [comando IMR \_ RECONVERTSTRING.](imr-reconvertstring.md)

Dopo che l'applicazione ha gestito [IMR \_ RECONVERTSTRING,](imr-reconvertstring.md)l'IME potrebbe modificare o meno la [**struttura RECONVERTSTRING.**](/windows/win32/api/imm/ns-imm-reconvertstring) L'IME invia WM \_ IME \_ REQUEST con **IMR \_ CONFIRMRECONVERTSTRING** per confermare le modifiche alla **struttura RECONVERTSTRING.** Se l'applicazione restituisce **TRUE** per **IMR \_ CONFIRMRECONVERTSTRING,** l'IME genera una nuova stringa di composizione basata sulla struttura **RECONVERTSTRING** per il **comando IMR \_ CONFIRMRECONVERTSTRING.** Se l'applicazione restituisce **FALSE** per **IMR \_ CONFIRMRECONVERTSTRING**, l'IME genera una nuova stringa di composizione basata sulla struttura **RECONVERTSTRING** originale specificata dall'applicazione nel comando IMR \_ RECONVERTSTRING.

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

[IMR \_ RECONVERTSTRING](imr-reconvertstring.md)
</dt> <dt>

[**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring)
</dt> <dt>

[**RICHIESTA \_ IME \_ WM**](wm-ime-request.md)
</dt> </dl>

 

 




