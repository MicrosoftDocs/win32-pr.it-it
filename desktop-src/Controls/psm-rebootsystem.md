---
title: PSM_REBOOTSYSTEM messaggio (Prsht.h)
description: Indica che il sistema deve essere riavviato per l'applicazione delle modifiche. È possibile inviare il messaggio PSM REBOOTSYSTEM in modo \_ esplicito o tramite la macro PropSheet \_ RebootSystem.
ms.assetid: 461fce3c-183a-4b9b-8eab-ed2838d9f866
keywords:
- PSM_REBOOTSYSTEM dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- PSM_REBOOTSYSTEM
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfcfebc931d1dbf01ab053fa2723bdcf361c4be5ef1443b9131115e2300770cc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088631"
---
# <a name="psm_rebootsystem-message"></a>Messaggio PSM \_ REBOOTSYSTEM

Indica che il sistema deve essere riavviato per l'applicazione delle modifiche. È possibile inviare il **messaggio PSM \_ REBOOTSYSTEM** in modo esplicito o tramite la macro [**PropSheet \_ RebootSystem.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_rebootsystem)

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

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Un'applicazione deve inviare questo messaggio solo in risposta al messaggio di notifica [PSN \_ APPLY](psn-apply.md) o [PSN \_ KILLACTIVE.](psn-killactive.md)

Questo messaggio fa in modo che la funzione [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) restituirà il valore \_ ID PSREBOOTSYSTEM, ma solo se l'utente fa clic sul **pulsante OK** per chiudere la finestra delle proprietà. È responsabilità dell'applicazione riavviare il sistema, operazione che può essere eseguita usando la [**funzione ExitWindowsEx.**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex)

Questo messaggio sostituisce tutti i messaggi [**\_ RESTARTWINDOWS PSM**](psm-restartwindows.md) che lo precedono o seguono.

> [!Note]  
> Questo messaggio non è supportato quando si usa lo stile della procedura guidata Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

