---
description: Indica alla finestra IME di visualizzare la finestra di stato. Per inviare questo comando, l'applicazione usa il messaggio WM \_ IME \_ CONTROL con le impostazioni dei parametri illustrate di seguito.
ms.assetid: 8c422592-ef59-4030-b684-81e4e552c6b0
title: IMC_OPENSTATUSWINDOW comando (Imm.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 263640a3f104c9abf72a7eb5b33bce6ff3813ca40645c18b179b9b31a95fdda9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107291"
---
# <a name="imc_openstatuswindow-command"></a>Comando IMC \_ OPENSTATUSWINDOW

Indica alla finestra IME di visualizzare la finestra di stato. Per inviare questo comando, l'applicazione usa il [**messaggio WM \_ IME \_ CONTROL**](wm-ime-control.md) con le impostazioni dei parametri illustrate di seguito.


```C++
LRESULT IMC_OPENSTATUSWINDOW
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*Wparam*
</dt> <dd>

Impostare su IMC \_ OPENSTATUSWINDOW.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Non usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo oppure un valore diverso da zero in caso contrario.

## <a name="remarks"></a>Commenti

Questo comando viene ignorato se il sistema operativo non è in modalità mostra stato IME. L'utente può impostare o deselezionare la modalità mostra stato IME dalla barra delle applicazioni.

Se la finestra di stato è già visualizzata, questo comando non esegue alcuna operazione. Anche se l'applicazione può inviare questo comando alla finestra IME, l'applicazione non riceve il comando [**IMN \_ OPENSTATUSWINDOW**](imn-openstatuswindow.md) corrispondente.

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

 

 




