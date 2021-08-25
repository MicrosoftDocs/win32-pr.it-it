---
title: PSM_ISDIALOGMESSAGE messaggio (Prsht.h)
description: Passa un messaggio a una finestra di dialogo della finestra delle proprietà e indica se la finestra di dialogo ha elaborato il messaggio. È possibile inviare questo messaggio in modo esplicito o tramite la macro PropSheet \_ IsDialogMessage.
ms.assetid: 7629c3f8-0b10-4585-8a95-9309c75b3ebb
keywords:
- PSM_ISDIALOGMESSAGE di controllo Windows messaggio
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
ms.openlocfilehash: 12f28d63e5586d3b083282db4e029551ce4e61d0ef997e36e3e874e9f032095b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088681"
---
# <a name="psm_isdialogmessage-message"></a>Messaggio PSM \_ ISDIALOGMESSAGE

Passa un messaggio a una finestra di dialogo della finestra delle proprietà e indica se la finestra di dialogo ha elaborato il messaggio. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**PropSheet \_ IsDialogMessage.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_isdialogmessage)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura MSG**](/windows/win32/api/winuser/ns-winuser-msg) che contiene il messaggio da controllare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE** se il messaggio è stato elaborato oppure **FALSE** se il messaggio non è stato elaborato.

## <a name="remarks"></a>Commenti

Il ciclo di messaggi deve usare il **messaggio PSM \_ ISDIALOGMESSAGE** con finestre delle proprietà non modali per passare messaggi alla finestra di dialogo della finestra delle proprietà. Nei sistemi che supportano Unicode, usare le versioni Unicode delle [**funzioni GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) e [**PeekMessage**](/windows/desktop/api/winuser/nf-winuser-peekmessagea) (**GetMessageW** e **PeekMessageW**) per recuperare i messaggi.

Se il valore restituito indica che il messaggio è stato elaborato, non deve essere passato alla funzione [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) [**o DispatchMessage.**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage)

> [!Note]  
> Questo messaggio non è supportato quando si usa lo stile della procedura guidata Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Propertysheets**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta)
</dt> </dl>

 

