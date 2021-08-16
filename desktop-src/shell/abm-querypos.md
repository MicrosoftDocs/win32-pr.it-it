---
description: Richiede dimensioni e posizione dello schermo per una barra delle app.
ms.assetid: 061a30fb-a68a-464e-ad8c-0bda672b57d9
title: ABM_QUERYPOS messaggio (Shellapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24f7a5e78b6b040904144a64e1068fea3a3e56c7b42fdfcf314f2ced4bfff9e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118225032"
---
# <a name="abm_querypos-message"></a>Messaggio \_ QUERYPOS ABM

Richiede dimensioni e posizione dello schermo per una barra delle app. Quando viene effettuata la richiesta, il messaggio propone un bordo dello schermo e un rettangolo di delimitazione per la barra dell'app. Il sistema regola il rettangolo di delimitazione in modo che la barra delle applicazioni non interferisca con Windows barra delle applicazioni o altre barre delle applicazioni.


```C++
SHAppBarMessage(ABM_QUERYPOS, pabd); 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pabd* 
</dt> <dd>

Puntatore a una [**struttura APPBARDATA.**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) Il **membro uEdge** specifica un bordo dello schermo e il membro **rc** contiene il rettangolo di delimitazione proposto. Quando la [**funzione SHAppBarMessage**](/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage) viene restituita, **rc** contiene il rettangolo di delimitazione approvato. Quando si invia questo messaggio, è necessario specificare i membri **cbSize**, **hWnd**, **uEdge** **e rc.** tutti gli altri membri vengono ignorati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce sempre **TRUE.**

## <a name="remarks"></a>Commenti

Un'appbar deve inviare questo messaggio prima di inviare il [**messaggio \_ SETPOS ABM.**](abm-setpos.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Shellapi.h</dt> </dl> |



 

 




