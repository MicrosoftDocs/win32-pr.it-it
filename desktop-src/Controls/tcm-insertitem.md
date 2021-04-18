---
title: Messaggio TCM_INSERTITEM (COMmctrl. h)
description: Inserisce una nuova scheda in un controllo struttura a schede. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro TabCtrl InsertItem.
ms.assetid: e547c49a-699c-4137-8680-20391d138d54
keywords:
- Controlli di Windows Message TCM_INSERTITEM
topic_type:
- apiref
api_name:
- TCM_INSERTITEM
- TCM_INSERTITEMA
- TCM_INSERTITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58002006944a221571e37c37d25259d0aaa74fc4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302360"
---
# <a name="tcm_insertitem-message"></a>\_Messaggio INSERTITEM INSERTITEM

Inserisce una nuova scheda in un controllo struttura a schede. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**TabCtrl \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_insertitem) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice della nuova scheda.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) che specifica gli attributi della scheda. I membri **dwState** e **dwStateMask** di questa struttura vengono ignorati da questo messaggio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'indice della nuova scheda se ha esito positivo oppure-1 in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TCM \_ INSERTITEMW** (Unicode) e **TCM \_ INSERTITEMA** (ANSI)<br/>             |



 

 





