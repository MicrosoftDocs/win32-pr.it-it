---
description: Notifica a un'applicazione quando viene aggiornato il tipo di carattere del contesto di input. L'applicazione riceve questo comando tramite il \_ \_ messaggio di notifica dell'IME WM con le impostazioni dei parametri, come illustrato di seguito.
ms.assetid: 946bee83-91af-4647-9b22-96d42466352c
title: Codice di notifica IMN_SETCOMPOSITIONFONT (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8373954e80e420004b347bf1b40021c86ddbb876
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317150"
---
# <a name="imn_setcompositionfont-notification-code"></a>\_Codice di notifica SETCOMPOSITIONFONT di IMN

Notifica a un'applicazione quando viene aggiornato il tipo di carattere del contesto di input. L'applicazione riceve questo comando tramite il messaggio di [**\_ \_ notifica dell'IME WM**](wm-ime-notify.md) con le impostazioni dei parametri, come illustrato di seguito.


```C++
IMN_SETCOMPOSITIONFONT
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Impostare su IMN \_ SETCOMPOSITIONFONT.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Non usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo comando non restituisce alcun valore.

## <a name="remarks"></a>Commenti

L'applicazione può ottenere informazioni sul tipo di carattere tramite la funzione [**ImmGetCompositionFont**](/windows/desktop/api/Imm/nf-imm-immgetcompositionfonta) . La finestra IME utilizza successivamente il tipo di carattere per creare la stringa di composizione.

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

[**ImmGetCompositionFont**](/windows/desktop/api/Imm/nf-imm-immgetcompositionfonta)
</dt> <dt>

[**\_notifica IME \_ WM**](wm-ime-notify.md)
</dt> </dl>

 

 




