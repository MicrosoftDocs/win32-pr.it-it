---
title: Messaggio PSM_ISDIALOGMESSAGE (Prsht. h)
description: Passa un messaggio a una finestra di dialogo della finestra delle proprietà e indica se la finestra di dialogo ha elaborato il messaggio. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro PropSheet IsDialogMessage.
ms.assetid: 7629c3f8-0b10-4585-8a95-9309c75b3ebb
keywords:
- Controlli di Windows Message PSM_ISDIALOGMESSAGE
topic_type:
- apiref
api_name:
- PSM_ISDIALOGMESSAGE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b753fc849d76e3ac5071dd85bdd94950460fbb10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873889"
---
# <a name="psm_isdialogmessage-message"></a>\_Messaggio ISDIALOGMESSAGE di PSM

Passa un messaggio a una finestra di dialogo della finestra delle proprietà e indica se la finestra di dialogo ha elaborato il messaggio. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**PropSheet \_ IsDialogMessage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_isdialogmessage) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura di [**messaggi**](/windows/win32/api/winuser/ns-winuser-msg) contenente il messaggio da verificare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se il messaggio è stato elaborato oppure **false** se il messaggio non è stato elaborato.

## <a name="remarks"></a>Commenti

Il ciclo di messaggi deve usare il messaggio **PSM \_ ISDIALOGMESSAGE** con finestre delle proprietà non modali per passare i messaggi alla finestra di dialogo della finestra delle proprietà. Nei sistemi che supportano Unicode, utilizzare le versioni Unicode delle funzioni [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) e [**PeekMessage**](/windows/desktop/api/winuser/nf-winuser-peekmessagea) (**GetMessageW** e **PeekMessageW**) per recuperare i messaggi.

Se il valore restituito indica che il messaggio è stato elaborato, non deve essere passato alla funzione [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) o [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) .

> [!Note]  
> Questo messaggio non è supportato quando si usa lo stile della procedura guidata Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta)
</dt> </dl>

 

