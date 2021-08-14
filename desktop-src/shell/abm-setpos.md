---
description: Imposta le dimensioni e la posizione dello schermo di una barra delle app.
ms.assetid: b3c56278-b9a2-4e08-bf98-7b3e4c8bd082
title: ABM_SETPOS messaggio (Shellapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 431bbdc02ed202c94d66b6b93ce43aba0ebd40f1fb7058583f56c027cfc29b70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117861603"
---
# <a name="abm_setpos-message"></a>Messaggio \_ SETPOS ABM

Imposta le dimensioni e la posizione dello schermo di una barra delle app. Il messaggio specifica un bordo dello schermo e il rettangolo di delimitazione per la barra dell'app. Il sistema può regolare il rettangolo di delimitazione in modo che la barra delle applicazioni non interferisca con la barra delle applicazioni Windows o con qualsiasi altra barra delle applicazioni.


```C++
SHAppBarMessage(ABM_SETPOS, pabd); 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pabd* 
</dt> <dd>

Puntatore a una [**struttura APPBARDATA.**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) Il **membro uEdge** specifica un bordo dello schermo e il membro **rc** contiene il rettangolo di delimitazione. Quando la [**funzione SHAppBarMessage**](/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage) viene restituita, **rc** contiene il rettangolo di delimitazione approvato. Quando si invia questo messaggio, è necessario specificare i membri **cbSize**, **hWnd**, **uEdge** **e rc.** tutti gli altri membri vengono ignorati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce sempre **TRUE.**

## <a name="remarks"></a>Commenti

Questo messaggio fa sì che il sistema invii il messaggio di notifica [**ABN \_ POSCHANGED**](abn-poschanged.md) a tutte le barre delle app.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Shellapi.h</dt> </dl> |



 

 




