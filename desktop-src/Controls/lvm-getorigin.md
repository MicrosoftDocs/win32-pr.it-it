---
title: Messaggio LVM_GETORIGIN (COMmctrl. h)
description: Recupera l'origine della visualizzazione corrente per un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro ListView getOrigin.
ms.assetid: 913c8339-fbe4-43c8-a997-5a972920dc3b
keywords:
- Controlli di Windows Message LVM_GETORIGIN
topic_type:
- apiref
api_name:
- LVM_GETORIGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8af42f3d616aa609d6b9e41d3991adb9d68eb24e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120982"
---
# <a name="lvm_getorigin-message"></a>\_Messaggio GETORIGIN LVM

Recupera l'origine della visualizzazione corrente per un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**ListView \_ getOrigin**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getorigin) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura di [**punti**](/previous-versions//dd162805(v=vs.85)) che riceve l'origine della visualizzazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se ha esito positivo o **false** se la visualizzazione corrente è elenco o visualizzazione report.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

