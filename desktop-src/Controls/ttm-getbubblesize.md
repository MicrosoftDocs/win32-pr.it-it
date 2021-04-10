---
title: Messaggio TTM_GETBUBBLESIZE (COMmctrl. h)
description: Restituisce la larghezza e l'altezza di un controllo ToolTip.
ms.assetid: 6afb971e-f05d-4b7a-b63d-3672bfcc32dc
keywords:
- Controlli di Windows Message TTM_GETBUBBLESIZE
topic_type:
- apiref
api_name:
- TTM_GETBUBBLESIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48b48bda0f795473cb48303e88bbf3c1c35df7cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119818"
---
# <a name="ttm_getbubblesize-message"></a>\_Messaggio TTM GETBUBBLESIZE

Restituisce la larghezza e l'altezza di un controllo ToolTip.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore alla struttura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) della descrizione comando.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce la larghezza della descrizione comando nella parola bassa e l'altezza della parola alta se ha esito positivo. In caso contrario, restituisce **false**.

## <a name="remarks"></a>Commenti

Se i \_ flag di traccia ttf e i \_ flag assoluti ttf sono impostati nel membro **uFlags** della struttura ToolTip [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) , questo messaggio può essere usato per facilitare la posizione esatta della descrizione comando.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





