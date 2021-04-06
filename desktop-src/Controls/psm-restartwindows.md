---
title: Messaggio PSM_RESTARTWINDOWS (Prsht. h)
description: Indica che è necessario riavviare Windows per rendere effettive le modifiche.
ms.assetid: 5bf634ee-7408-45df-adb6-c5b947f6c47b
keywords:
- Controlli di Windows Message PSM_RESTARTWINDOWS
topic_type:
- apiref
api_name:
- PSM_RESTARTWINDOWS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb12126ae0a2b9187a941ccc1aff53186a0cda7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873653"
---
# <a name="psm_restartwindows-message"></a>\_Messaggio RESTARTWINDOWS di PSM

Indica che è necessario riavviare Windows per rendere effettive le modifiche.

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

Un'applicazione deve inviare questo messaggio solo in risposta al codice di notifica [PSN \_ Apply](psn-apply.md) o [PSN \_ KILLACTIVE](psn-killactive.md) . È possibile inviare il messaggio **PSM \_ RESTARTWINDOWS** in modo esplicito o usando la macro [**PropSheet \_ RESTARTWINDOWS**](/windows/desktop/api/Prsht/nf-prsht-propsheet_restartwindows) .

Questo messaggio fa in modo che la funzione [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) restituisca il \_ valore ID PSRESTARTWINDOWS, ma solo se l'utente fa clic sul pulsante **OK** per chiudere la finestra delle proprietà. È responsabilità dell'applicazione riavviare Windows, operazione che può essere eseguita tramite la funzione [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) .

> [!Note]  
> Questo messaggio non è supportato quando si usa lo stile della procedura guidata Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

