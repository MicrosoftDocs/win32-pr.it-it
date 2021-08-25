---
description: Un'applicazione invia il messaggio WM MDIDESTROY a una finestra client dell'interfaccia a documenti multipli \_ (MDI) per chiudere una finestra figlio MDI.
ms.assetid: b415393d-a5c2-4b70-af18-0dc7b3939a47
title: WM_MDIDESTROY messaggio (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 232514831defe3c65cdce66a5e1c7348ad4f80508eb01615572b7aa5b7d8e9c0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119772061"
---
# <a name="wm_mdidestroy-message"></a>Messaggio \_ WM MDIDESTROY

Un'applicazione invia **il \_ messaggio WM MDIDESTROY** a una finestra client dell'interfaccia a documenti multipli (MDI) per chiudere una finestra figlio MDI.


```C++
#define WM_MDIDESTROY                   0x0221
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per la finestra figlio MDI da chiudere.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **zero**

Questo messaggio restituisce sempre zero.

## <a name="remarks"></a>Commenti

Questo messaggio rimuove il titolo della finestra figlio MDI dalla finestra cornice MDI e disattiva la finestra figlio. Un'applicazione deve usare questo messaggio per chiudere tutte le finestre figlio MDI.

Se una finestra del client MDI riceve un messaggio che modifica l'attivazione delle finestre figlio e la finestra figlio MDI attiva è ingrandita, il sistema ripristina la finestra figlio attiva e ingrandisce la finestra figlio appena attivata.

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

[**WM \_ MDICREATE**](wm-mdicreate.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Interfaccia a documenti multipli](multiple-document-interface.md)
</dt> </dl>

 

 




