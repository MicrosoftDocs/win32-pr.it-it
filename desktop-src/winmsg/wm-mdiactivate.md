---
description: Un'applicazione invia il \_ messaggio WM MDIACTIVATE a una finestra del client di interfaccia a documenti multipli (MDI) per indicare alla finestra client di attivare una finestra figlio MDI diversa.
ms.assetid: c5de18b5-fac3-4e55-9eca-3b6672df0e7b
title: Messaggio WM_MDIACTIVATE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b240c41d3b7127a5d69b855f3a5587e194b02d96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312375"
---
# <a name="wm_mdiactivate-message"></a>\_Messaggio MDIACTIVATE WM

Un'applicazione invia il messaggio **WM \_ MDIACTIVATE** a una finestra del client di interfaccia a documenti multipli (MDI) per indicare alla finestra client di attivare una finestra figlio MDI diversa.


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

Quando la finestra client elabora questo messaggio, invia **WM \_ MDIACTIVATE** alla finestra figlio in fase di disattivazione e alla finestra figlio attivata. I parametri del messaggio ricevuti da una finestra figlio MDI sono i seguenti:

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Handle per la finestra figlio MDI da disattivare.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Handle per la finestra figlio MDI attivata.

</dd> </dl>

Una finestra figlio MDI viene attivata indipendentemente dalla finestra cornice MDI. Quando la finestra cornice diventa attiva, la finestra figlio abilitata per l'ultima volta con il messaggio **WM \_ MDIACTIVATE** riceve il messaggio [**WM \_ NCACTIVATE**](wm-ncactivate.md) per creare una cornice e una barra del titolo attive; la finestra figlio non riceve un altro messaggio **WM \_ MDIACTIVATE** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**\_MDIGETACTIVE WM**](wm-mdigetactive.md)
</dt> <dt>

[**\_MDINEXT WM**](wm-mdinext.md)
</dt> <dt>

[**\_NCACTIVATE WM**](wm-ncactivate.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Interfaccia a documenti multipli](multiple-document-interface.md)
</dt> </dl>

 

 




