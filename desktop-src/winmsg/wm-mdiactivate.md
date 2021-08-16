---
description: Un'applicazione invia il messaggio WM MDIACTIVATE a una finestra client dell'interfaccia a documenti multipli per indicare alla finestra client di attivare un'altra \_ finestra figlio MDI.
ms.assetid: c5de18b5-fac3-4e55-9eca-3b6672df0e7b
title: WM_MDIACTIVATE messaggio (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e8b71e0f3755d76ecb44d60eecbd3b92c124aa59339a6fbf59a098b1eeb274f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931271"
---
# <a name="wm_mdiactivate-message"></a>Messaggio \_ WM MDIACTIVATE

Un'applicazione invia il messaggio **\_ WM MDIACTIVATE** a una finestra client dell'interfaccia a documenti multipli per indicare alla finestra client di attivare un'altra finestra figlio MDI.


```C++
#define WM_MDIACTIVATE                  0x0222
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per la finestra figlio MDI da attivare.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **LRESULT**

Se un'applicazione invia questo messaggio a una finestra del client MDI, il valore restituito è zero.

Una finestra figlio MDI deve restituire zero se elabora questo messaggio.

## <a name="remarks"></a>Commenti

Quando la finestra client elabora questo messaggio, invia **WM \_ MDIACTIVATE** alla finestra figlio in fase di disattivazione e alla finestra figlio da attivare. I parametri del messaggio ricevuti da una finestra figlio MDI sono i seguenti:

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*Wparam*
</dt> <dd>

Handle per la finestra figlio MDI in fase di disattivazione.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Handle per la finestra figlio MDI da attivare.

</dd> </dl>

Una finestra figlio MDI viene attivata indipendentemente dalla finestra cornice MDI. Quando la finestra cornice diventa attiva, l'ultima finestra figlio attivata tramite il messaggio **WM \_ MDIACTIVATE** riceve il messaggio [**WM \_ NCACTIVATE**](wm-ncactivate.md) per disegnare una cornice della finestra attiva e una barra del titolo. La finestra figlio non riceve un altro messaggio **WM \_ MDIACTIVATE.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**WM \_ MDIGETACTIVE**](wm-mdigetactive.md)
</dt> <dt>

[**WM \_ MDINEXT**](wm-mdinext.md)
</dt> <dt>

[**WM \_ NCACTIVATE**](wm-ncactivate.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Interfaccia a documenti multipli](multiple-document-interface.md)
</dt> </dl>

 

 




