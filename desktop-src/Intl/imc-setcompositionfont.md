---
description: Indica a una finestra IME di specificare il tipo di carattere logico da usare per visualizzare i caratteri intermedi nella finestra di composizione. Per inviare questo comando, l'applicazione usa il messaggio WM \_ IME \_ CONTROL con le impostazioni dei parametri illustrate di seguito.
ms.assetid: 17b222e7-bf57-4cdd-8475-d9a8be03ab7f
title: IMC_SETCOMPOSITIONFONT comando (Imm.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ebc9f435371d4ae08b12191419c95fd53c69256064f0e90bb654e75fab922f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118949272"
---
# <a name="imc_setcompositionfont-command"></a>Comando \_ IMC SETCOMPOSITIONFONT

Indica a una finestra IME di specificare il tipo di carattere logico da usare per visualizzare i caratteri intermedi nella finestra di composizione. Per inviare questo comando, l'applicazione usa il [**messaggio WM \_ IME \_ CONTROL**](wm-ime-control.md) con le impostazioni dei parametri illustrate di seguito.


```C++
LRESULT IMC_SETCOMPOSITIONFONT
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*Wparam*
</dt> <dd>

Impostare su IMC \_ SETCOMPOSITIONFONT.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Puntatore a una [**struttura LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) che contiene informazioni sul tipo di carattere logico.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo oppure un valore diverso da zero in caso contrario.

## <a name="remarks"></a>Commenti

Quando si elabora questo comando, la finestra IME modifica il tipo di carattere selezionato corrente nel contesto di input.

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

[**CONTROLLO \_ IME \_ WM**](wm-ime-control.md)
</dt> </dl>

 

 
