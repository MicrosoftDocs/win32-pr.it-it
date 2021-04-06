---
title: Messaggio LB_ITEMFROMPOINT (winuser. h)
description: Ottiene l'indice in base zero dell'elemento più vicino al punto specificato in una casella di riepilogo.
ms.assetid: 5739eccb-e708-4ddb-ac97-d3e6c6120842
keywords:
- Controlli di Windows Message LB_ITEMFROMPOINT
topic_type:
- apiref
api_name:
- LB_ITEMFROMPOINT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5c4f06b9de8e6580c81c7faf7ddb8c287a148b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743023"
---
# <a name="lb_itemfrompoint-message"></a>\_Messaggio ITEMFROMPOINT lb

Ottiene l'indice in base zero dell'elemento più vicino al punto specificato in una casella di riepilogo.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifica la coordinata x di un punto, relativa all'angolo superiore sinistro dell'area client della casella di riepilogo.

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica la coordinata y di un punto, relativa all'angolo superiore sinistro dell'area client della casella di riepilogo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito contiene l'indice dell'elemento più vicino in [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)). [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) è zero se il punto specificato si trova nell'area client della casella di riepilogo o uno se è all'esterno dell'area client.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MAKELPARAM**](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> </dl>

 

