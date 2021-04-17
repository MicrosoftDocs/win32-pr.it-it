---
description: Notifica a un AppBar quando si è verificato un evento che può influire sulle dimensioni e la posizione di AppBar.
ms.assetid: 1016a362-4d2b-410e-aec9-c1cc8f497778
title: Messaggio ABN_POSCHANGED (Shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24b0a800b1c112cba18fbadbba79a999ec83c77e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977426"
---
# <a name="abn_poschanged-message"></a>\_Messaggio POSCHANGED di ABN

Notifica a un AppBar quando si è verificato un evento che può influire sulle dimensioni e la posizione di AppBar. Gli eventi includono le modifiche apportate alle dimensioni, alla posizione e allo stato di visibilità della barra delle applicazioni, nonché l'aggiunta, la rimozione o il ridimensionamento di un altro AppBar sullo stesso lato dello schermo.


```C++
ABN_POSCHANGED
```



## <a name="parameters"></a>Parametri

Questo messaggio non contiene parametri.

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Un AppBar deve rispondere a questo messaggio di notifica inviando i messaggi [**ABM \_ QUERYPOS**](abm-querypos.md) e [**ABM \_ SETPOS**](abm-setpos.md) . Se la posizione è cambiata, AppBar deve chiamare la funzione [**MoveWindow**](/windows/desktop/api/winuser/nf-winuser-movewindow) per spostarsi alla nuova posizione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



 

