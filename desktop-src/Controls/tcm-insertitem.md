---
title: TCM_INSERTITEM messaggio (Commctrl.h)
description: Inserisce una nuova scheda in un controllo Struttura a schede. È possibile inviare questo messaggio in modo esplicito o tramite la \_ macro InsertItem tabCtrl.
ms.assetid: e547c49a-699c-4137-8680-20391d138d54
keywords:
- TCM_INSERTITEM dei messaggi Windows controlli
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
ms.openlocfilehash: a7c3c17714218562d7ddc82497a7ef27e131e30a2ff04daf36970dfbcf5cc354
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829102"
---
# <a name="tcm_insertitem-message"></a>Messaggio INSERTITEM di TCM \_

Inserisce una nuova scheda in un controllo Struttura a schede. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**\_ InsertItem tabCtrl.**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_insertitem)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice della nuova scheda.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) che specifica gli attributi della scheda. I **membri dwState** **e dwStateMask** di questa struttura vengono ignorati da questo messaggio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'indice della nuova scheda in caso di esito positivo oppure -1 in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **Gestione controllo servizi \_ INSERTITEMW** (Unicode) e **TCM \_ INSERTITEMA** (ANSI)<br/>             |



 

 





