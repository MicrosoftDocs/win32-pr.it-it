---
title: Messaggio DTM_GETMCFONT (COMmctrl. h)
description: Ottiene il tipo di carattere attualmente utilizzato dal controllo Calendar Month del controllo di selezione data e ora (DTP). È possibile inviare questo messaggio in modo esplicito o usare la \_ macro DateTime GetMonthCalFont.
ms.assetid: 6687a1dc-6f6d-4684-80b2-f726b08d2f3a
keywords:
- Controlli di Windows Message DTM_GETMCFONT
topic_type:
- apiref
api_name:
- DTM_GETMCFONT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d799d5dbbe5e3a4cdf7eede871f9aeac451d17a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874369"
---
# <a name="dtm_getmcfont-message"></a>\_Messaggio GETMCFONT DTM

Ottiene il tipo di carattere attualmente utilizzato dal controllo Calendar Month del controllo di selezione data e ora (DTP). È possibile inviare questo messaggio in modo esplicito o usare la macro [**DateTime \_ GetMonthCalFont**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalfont) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore HFONT che rappresenta l'handle per il tipo di carattere corrente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





