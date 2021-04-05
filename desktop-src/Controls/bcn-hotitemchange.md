---
title: Codice di notifica BCN_HOTITEMCHANGE (COMmctrl. h)
description: Notifica al proprietario del controllo Button che il mouse entra o esce dall'area client del controllo Button. Il controllo Button invia questo codice di notifica sotto forma di messaggio di \_ notifica WM.
ms.assetid: 92882e21-b69d-4326-94e9-ae69a0d00a83
keywords:
- Controlli di Windows per il codice di notifica BCN_HOTITEMCHANGE
topic_type:
- apiref
api_name:
- BCN_HOTITEMCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67ba6a7e64e95b45d0883b5adf34b384bccac8c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048204"
---
# <a name="bcn_hotitemchange-notification-code"></a>\_Codice di notifica BCN HOTITEMCHANGE

Notifica al proprietario del controllo Button che il mouse entra o esce dall'area client del controllo Button. Il controllo Button invia questo codice di notifica sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
BCN_HOTITEMCHANGE

    pnmbchotitem = (NMBCHOTITEM*) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMBCHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmbchotitem) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce alcun valore.

## <a name="remarks"></a>Commenti

> [!Note]  
> Per usare questo codice di notifica, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





