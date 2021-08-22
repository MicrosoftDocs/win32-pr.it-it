---
title: PSM_APPLY messaggio (Prsht.h)
description: Simula la selezione del pulsante Applica, a indicare che una o più pagine sono state modificate e che le modifiche devono essere convalidate e registrate.
ms.assetid: 2948fb66-ad77-4552-88b6-455418515e4c
keywords:
- PSM_APPLY dei controlli Windows messaggio
topic_type:
- apiref
api_name:
- PSM_APPLY
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f753eb2465ec835f467493bdbd83d10b8ba174b11c83abffcb91d20f8beba002
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544161"
---
# <a name="psm_apply-message"></a>Messaggio PSM \_ APPLY

Simula la selezione del **pulsante** Applica, a indicare che una o più pagine sono state modificate e che le modifiche devono essere convalidate e registrate.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE se** tutte le pagine hanno applicato correttamente le modifiche oppure FALSE in caso **contrario.**

## <a name="remarks"></a>Commenti

La finestra delle proprietà invia il [codice di notifica \_ PSN KILLACTIVE](psn-killactive.md) alla pagina corrente. Se la pagina corrente restituisce **FALSE,** la finestra delle proprietà invia il codice di notifica [PSN \_ APPLY](psn-apply.md) a tutte le pagine attive. È possibile inviare il messaggio PSM APPLY in modo \_ esplicito o tramite la macro [**PropSheet \_ Apply.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_apply)

> [!Note]  
> Questo messaggio non è supportato quando si usa lo stile della procedura guidata Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

 





