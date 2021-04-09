---
title: Codice di notifica di NM_NCHITTEST (Rebar) (COMmctrl. h)
description: Inviato da un controllo Rebar quando il controllo riceve un \_ messaggio WM NCHITTEST. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: b345d83e-682d-4067-a783-689d64f9b7bc
keywords:
- NM_NCHITTEST (Rebar) il codice di notifica controlli Windows
topic_type:
- apiref
api_name:
- NM_NCHITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fb4568cad87017d9fff94deb60583ac0b4c1d0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120715"
---
# <a name="nm_nchittest-rebar-notification-code"></a>\_Codice di notifica NCHITTEST (Rebar) Nm

Inviato da un controllo Rebar quando il controllo riceve un messaggio [**WM \_ NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) . Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
NM_NCHITTEST

    lpnmmouse = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) contenente informazioni sul codice di notifica. Il membro **dwItemSpec** contiene l'indice della banda su cui si è verificato il messaggio di hit test e il membro **PT** contiene le coordinate del mouse del messaggio di hit test.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero per consentire al rebar di eseguire l'elaborazione predefinita del messaggio di hit test oppure restituire uno dei valori HT \* documentati in [**WM \_ NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) per eseguire l'override dell'elaborazione dell'hit test predefinita.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

