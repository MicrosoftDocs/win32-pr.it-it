---
title: Messaggio PSM_REBOOTSYSTEM (Prsht. h)
description: Indica che è necessario riavviare il sistema per rendere effettive le modifiche. È possibile inviare il \_ messaggio PSM REBOOTSYSTEM in modo esplicito o usando la \_ macro PropSheet REBOOTSYSTEM.
ms.assetid: 461fce3c-183a-4b9b-8eab-ed2838d9f866
keywords:
- Controlli di Windows Message PSM_REBOOTSYSTEM
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
ms.openlocfilehash: 14f5018dc3845d699561740ccd9cbb0a9c793f15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476060"
---
# <a name="psm_rebootsystem-message"></a>\_Messaggio REBOOTSYSTEM di PSM

Indica che è necessario riavviare il sistema per rendere effettive le modifiche. È possibile inviare il messaggio **PSM \_ REBOOTSYSTEM** in modo esplicito o usando la macro [**PropSheet \_ REBOOTSYSTEM**](/windows/desktop/api/Prsht/nf-prsht-propsheet_rebootsystem) .

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

Un'applicazione deve inviare questo messaggio solo in risposta al messaggio di notifica [PSN \_ Apply](psn-apply.md) o [PSN \_ KILLACTIVE](psn-killactive.md) .

Questo messaggio fa in modo che la funzione [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) restituisca il \_ valore ID PSREBOOTSYSTEM, ma solo se l'utente fa clic sul pulsante **OK** per chiudere la finestra delle proprietà. È responsabilità dell'applicazione riavviare il sistema, operazione che può essere eseguita tramite la funzione [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) .

Questo messaggio sostituisce tutti i messaggi di [**PSM \_ RESTARTWINDOWS**](psm-restartwindows.md) che lo precedono o lo seguono.

> [!Note]  
> Questo messaggio non è supportato quando si usa lo stile della procedura guidata Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

