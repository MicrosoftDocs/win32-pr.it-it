---
description: Indica a una finestra IME di recuperare il tipo di carattere logico usato per visualizzare i caratteri intermedi nella finestra di composizione. Per inviare questo comando, l'applicazione usa il messaggio WM \_ IME \_ CONTROL con le impostazioni dei parametri illustrate di seguito.
ms.assetid: 43db70b6-f8bc-4241-9096-5d91fd1e332b
title: IMC_GETCOMPOSITIONFONT comando (Imm.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ebf26592f2fd000f864685bd79d71b189fc24d695941691fe2e01d48132d00d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068101"
---
# <a name="imc_getcompositionfont-command"></a>Comando IMC \_ GETCOMPOSITIONFONT

Indica a una finestra IME di recuperare il tipo di carattere logico usato per visualizzare i caratteri intermedi nella finestra di composizione. Per inviare questo comando, l'applicazione usa il [**messaggio WM \_ IME \_ CONTROL**](wm-ime-control.md) con le impostazioni dei parametri illustrate di seguito.


```C++
LRESULT IMC_GETCOMPOSITIONFONT
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*Wparam*
</dt> <dd>

Impostare su IMC \_ GETCOMPOSITIONFONT.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Puntatore a [**una struttura LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) che riceve informazioni sul tipo di carattere logico.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo oppure un valore diverso da zero in caso contrario.

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
</dt> </dl>

 

 
