---
description: Annulla la registrazione di una barra delle app rimuovendo la barra dall'elenco interno del sistema. Il sistema non invia più messaggi di notifica alla barra delle app o impedisce ad altre applicazioni di usare l'area dello schermo usata dalla barra delle app.
title: ABM_REMOVE messaggio (Shellapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3da73a52-3dbb-4133-a9bd-86540e1c4154
api_name:
- ABM_REMOVE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c32fd2c7a12fc8146a01d3722b31b46bad01f61b526397806a5121b7381b069e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117861708"
---
# <a name="abm_remove-message"></a>Messaggio REMOVE \_ ABM

Annulla la registrazione di una barra delle app rimuovendo la barra dall'elenco interno del sistema. Il sistema non invia più messaggi di notifica alla barra delle app o impedisce ad altre applicazioni di usare l'area dello schermo usata dalla barra delle app.


```C++
                SHAppBarMessage(ABM_REMOVE, pabd); 
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pabd* 
</dt> <dd>

Puntatore a una [**struttura APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) che contiene l'handle per la barra dell'app di cui annullare la registrazione. È necessario specificare i **membri cbSize** **e hWnd** quando si invia questo messaggio. tutti gli altri membri vengono ignorati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce sempre **TRUE.**

## <a name="remarks"></a>Commenti

Questo messaggio fa sì che il sistema invii il messaggio di notifica [**\_ POSCHANGED ABN**](abn-poschanged.md) a tutte le barre delle app.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Shellapi.h</dt> </dl> |



 

 




