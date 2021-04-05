---
title: Messaggio RBN_AUTOBREAK (COMmctrl. h)
description: Notifica all'elemento padre di un controllo Rebar che verrà visualizzata un'interruzioni nella barra. L'elemento padre determina se eseguire l'interruzioni. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: b7a63027-6cfa-4d5a-9ea6-fdd8b4fb6864
keywords:
- Controlli di Windows Message RBN_AUTOBREAK
topic_type:
- apiref
api_name:
- RBN_AUTOBREAK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d614277d89578cb66e528ba16656ed55681ebbcf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874566"
---
# <a name="rbn_autobreak-message"></a>\_Messaggio di AUTOBREAK RBN

Notifica all'elemento padre di un controllo [Rebar](rebar-controls.md) che verrà visualizzata un'interruzioni nella barra. L'elemento padre determina se eseguire l'interruzioni. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
RBN_AUTOBREAK

    pnmRebarAutoBreak = (LPNMREBARAUTOBREAK) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMREBARAUTOBREAK**](/windows/win32/api/commctrl/ns-commctrl-nmrebarautobreak) contenente informazioni sul codice di notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito per questa notifica non viene utilizzato.

## <a name="remarks"></a>Commenti

Il valore nel membro **fAutoBreak** della struttura [**NMREBARAUTOBREAK**](/windows/win32/api/commctrl/ns-commctrl-nmrebarautobreak) indica se deve verificarsi un'interruzioni nel controllo Rebar.

Per usare questo codice di notifica, specificare Comctl32.dll versione 6 nel manifesto. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





