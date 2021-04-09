---
title: Messaggio TCM_SETITEM (COMmctrl. h)
description: Imposta alcuni o tutti gli attributi di una scheda. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro TabCtrl.
ms.assetid: 1d9c6607-d8ec-4644-a714-22bc2677aa78
keywords:
- Controlli di Windows Message TCM_SETITEM
topic_type:
- apiref
api_name:
- TCM_SETITEM
- TCM_SETITEMA
- TCM_SETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee86cd0737c3c50c89a97d3881e2cdfd3850f481
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739887"
---
# <a name="tcm_setitem-message"></a>\_Messaggio SEtitem (TCM)

Imposta alcuni o tutti gli attributi di una scheda. È possibile inviare questo messaggio in modo esplicito o utilizzando [**la \_ macro TabCtrl**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitem) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice dell'elemento.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) che contiene gli attributi del nuovo elemento. Il membro **mask** specifica gli attributi da impostare. Se il membro **mask** specifica il \_ valore di testo TCIF, il membro **pszText** è l'indirizzo di una stringa con terminazione null e il membro **cchTextMax** viene ignorato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TCM \_ SETITEMW** (Unicode) e **TCM \_ seitema** (ANSI)<br/>                   |



 

 





