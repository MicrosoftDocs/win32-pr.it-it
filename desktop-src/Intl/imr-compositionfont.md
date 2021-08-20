---
description: Notifica a un'applicazione quando un IME selezionato necessita di informazioni sul tipo di carattere usato dalla finestra di composizione. L'applicazione riceve questo comando tramite il messaggio WM \_ IME \_ REQUEST con parametri, come illustrato di seguito.
ms.assetid: 46bb71ee-8dc9-4ef0-bc4e-59866c122bf7
title: IMR_COMPOSITIONFONT codice di notifica (Imm.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e241605358a0b6781a5725e4d0cfabc23b06a89f8e2bc041e9556434b6c5816f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117810098"
---
# <a name="imr_compositionfont-notification-code"></a>Codice di notifica IMR \_ COMPOSITIONFONT

Notifica a un'applicazione quando un IME selezionato necessita di informazioni sul tipo di carattere usato dalla finestra di composizione. L'applicazione riceve questo comando tramite il [**messaggio WM \_ IME \_ REQUEST**](wm-ime-request.md) con parametri, come illustrato di seguito.


```C++
LRESULT IMR_COMPOSITIONFONT
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*Wparam*
</dt> <dd>

Impostare su IMR \_ COMPOSITIONFONT.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Puntatore a un buffer contenente una [**struttura LOGFONT.**](/windows/win32/api/wingdi/ns-wingdi-logfonta) L'applicazione inserisce i valori per la finestra di composizione corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero se l'applicazione compila la [**struttura LOGFONT.**](/windows/win32/api/wingdi/ns-wingdi-logfonta) In caso contrario, il comando restituisce 0.

## <a name="remarks"></a>Commenti

Questo comando può essere inviato dall'IME a una finestra che ha cancellato il flag ISC SHOWUICOMPOSITIONWINDOW nel gestore messaggi \_ [**WM \_ IME \_ SETCONTEXT.**](wm-ime-setcontext.md)

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

[**RICHIESTA \_ IME \_ WM**](wm-ime-request.md)
</dt> <dt>

[**WM \_ IME \_ SETCONTEXT**](wm-ime-setcontext.md)
</dt> </dl>

 

 
