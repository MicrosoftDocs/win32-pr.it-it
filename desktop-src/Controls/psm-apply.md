---
title: Messaggio PSM_APPLY (Prsht. h)
description: Simula la selezione del pulsante Applica, che indica che una o più pagine sono state modificate ed è necessario convalidare e registrare le modifiche.
ms.assetid: 2948fb66-ad77-4552-88b6-455418515e4c
keywords:
- Controlli di Windows Message PSM_APPLY
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
ms.openlocfilehash: 67d798d4a9a2f780ac81cc84c90a57d0efd4e299
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874257"
---
# <a name="psm_apply-message"></a>\_Messaggio di applicazione PSM

Simula la selezione del pulsante **applica** , che indica che una o più pagine sono state modificate ed è necessario convalidare e registrare le modifiche.

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

Restituisce **true** se tutte le pagine hanno applicato correttamente le modifiche. in caso contrario, **false** .

## <a name="remarks"></a>Commenti

La finestra delle proprietà Invia il codice di notifica [ \_ KILLACTIVE PSN](psn-killactive.md) alla pagina corrente. Se la pagina corrente restituisce **false**, la finestra delle proprietà Invia il codice di notifica di [ \_ applicazione PSN](psn-apply.md) a tutte le pagine attive. È possibile inviare il \_ messaggio di applicazione PSM in modo esplicito o usando la macro [**PropSheet \_ Apply**](/windows/desktop/api/Prsht/nf-prsht-propsheet_apply) .

> [!Note]  
> Questo messaggio non è supportato quando si usa lo stile della procedura guidata Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





