---
title: Messaggio IPM_SETFOCUS (COMmctrl. h)
description: Imposta lo stato attivo della tastiera sul campo specificato nel controllo degli indirizzi IP. Tutto il testo in tale campo verrà selezionato.
ms.assetid: 4b975eb2-85e1-4e33-a803-99b48d2ff5e8
keywords:
- Controlli di Windows Message IPM_SETFOCUS
topic_type:
- apiref
api_name:
- IPM_SETFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d713e0a8b7eb838a2db5c4738c801d4fb76b782
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120291"
---
# <a name="ipm_setfocus-message"></a>\_Messaggio di DISattivazione IPM

Imposta lo stato attivo della tastiera sul campo specificato nel controllo degli indirizzi IP. Tutto il testo in tale campo verrà selezionato.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice di campo in base zero in cui impostare lo stato attivo. Se questo valore è maggiore del numero di campi, lo stato attivo è impostato sul primo campo vuoto. Se tutti i campi non sono vuoti, lo stato attivo è impostato sul primo campo.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito non viene utilizzato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





