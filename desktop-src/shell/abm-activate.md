---
description: Notifica al sistema che è stata attivata una barra delle app. Un'appbar deve chiamare questo messaggio in risposta al messaggio WM \_ ACTIVATE.
ms.assetid: 16011302-7c2d-4c34-9953-51cceb96e4b3
title: ABM_ACTIVATE messaggio (Shellapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 224f04a88a1e69a1a67fc08c6018d33af2bcdbc6f34ff9fbd00d1dd76f82ce5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118461134"
---
# <a name="abm_activate-message"></a>Messaggio ABM \_ ACTIVATE

Notifica al sistema che è stata attivata una barra delle app. Un'appbar deve chiamare questo messaggio in risposta al [**messaggio WM \_ ACTIVATE.**](/windows/desktop/inputdev/wm-activate)


```C++

SHAppBarMessage(ABM_ACTIVATE, pabd); 

            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pabd* 
</dt> <dd>

Puntatore a una [**struttura APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) che identifica la barra dell'app da attivare. È necessario specificare i **membri cbSize** **e hWnd** quando si invia questo messaggio. tutti gli altri membri vengono ignorati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce sempre **TRUE.**

## <a name="remarks"></a>Commenti

Questo messaggio viene ignorato se il **membro hWnd** della struttura a cui punta *pabd* identifica una barra dell'app con rilevamento automatico. Il sistema imposta automaticamente l'ordine z per la visualizzazione automatica delle barre delle app.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Shellapi.h</dt> </dl> |



 

