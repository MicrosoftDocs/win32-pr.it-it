---
title: Messaggio HDM_INSERTITEM (COMmctrl. h)
description: Inserisce un nuovo elemento in un controllo intestazione. È possibile inviare questo messaggio in modo esplicito o usare la macro dell'intestazione \_ InsertItem.
ms.assetid: aececf32-090d-4cd4-a239-4435a322f72e
keywords:
- Controlli di Windows Message HDM_INSERTITEM
topic_type:
- apiref
api_name:
- HDM_INSERTITEM
- HDM_INSERTITEMA
- HDM_INSERTITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9cabf86fea79fd437b3e9fb7e32890b3ba1a780
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476817"
---
# <a name="hdm_insertitem-message"></a>\_Messaggio HDM INSERTITEM

Inserisce un nuovo elemento in un controllo intestazione. È possibile inviare questo messaggio in modo esplicito o usare la macro dell' [**intestazione \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_insertitem) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice dell'elemento dopo il quale deve essere inserito il nuovo elemento. Il nuovo elemento viene inserito alla fine del controllo intestazione se *wParam* è maggiore o uguale al numero di elementi nel controllo. Se *wParam* è zero, il nuovo elemento viene inserito all'inizio del controllo intestazione.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) che contiene informazioni sul nuovo elemento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'indice del nuovo elemento, se ha esito positivo, oppure-1 in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **HDM \_ INSERTITEMW** (Unicode) e **HDM \_ INSERTITEMA** (ANSI)<br/>             |



 

 





