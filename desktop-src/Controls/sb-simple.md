---
title: Messaggio SB_SIMPLE (COMmctrl. h)
description: Specifica se una finestra di stato Visualizza testo semplice o Visualizza tutte le parti della finestra impostate da un messaggio precedente della \_ parte SB.
ms.assetid: 457209cb-67d4-4a9f-8d18-75aa5eb9ca1d
keywords:
- Controlli di Windows Message SB_SIMPLE
topic_type:
- apiref
api_name:
- SB_SIMPLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f7a462a917c86531cd70f5f5c8ea60bf448ff6f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120694"
---
# <a name="sb_simple-message"></a>\_Messaggio semplice SB

Specifica se una finestra di stato Visualizza testo semplice o Visualizza tutte le parti della finestra impostate da un messaggio precedente della [**\_ parte SB**](sb-setparts.md) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Flag tipo di visualizzazione. Se questo parametro è **true**, nella finestra viene visualizzato un testo semplice. Se è **false**, vengono visualizzate più parti.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito non viene utilizzato.

## <a name="remarks"></a>Commenti

Se la finestra di stato viene modificata da non semplice a semplice o viceversa, la finestra viene immediatamente ridisegnato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





