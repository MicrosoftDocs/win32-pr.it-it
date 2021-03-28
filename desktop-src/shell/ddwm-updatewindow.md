---
description: Indica a una finestra rilascia immagine di eseguire l'aggiornamento usando le nuove informazioni DROPDESCRIPTION.
title: Messaggio DDWM_UPDATEWINDOW
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3b74f2e1-8121-4b7c-8d7a-b449cda529da
api_name:
- DDWM_UPDATEWINDOW
api_type:
- NA
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2bff0e007c735fcf202aaf16cf304eb4ff5358f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977311"
---
# <a name="ddwm_updatewindow-message"></a>\_Messaggio DDWM UPDATEWINDOW

Indica a una finestra rilascia immagine di eseguire l'aggiornamento usando le nuove informazioni [**DROPDESCRIPTION**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

Non usato.

</dd> <dt>

*lParam* \[ in\]
</dt> <dd>

Non usato.

</dd> </dl>

## <a name="remarks"></a>Commenti

DDWM \_ UPDATEWINDOW è definito come \_ utente WM + 3.

Quando lo stato di un'operazione di eliminazione cambia, ad esempio in risposta a un tasto di modifica,[**IDropTarget::D ragover**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover) restituisce un nuovo valore [**DropEffect**](../com/dropeffect-constants.md) (questo valore di **DropEffect** può essere ricevuto anche tramite [**IDropSource:: GiveFeedback**](/windows/win32/api/oleidl/nf-oleidl-idropsource-givefeedback)). In risposta, l'applicazione aggiorna la struttura [**DROPDESCRIPTION**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription) della destinazione di rilascio con un nuovo valore [**DROPIMAGETYPE**](/windows/desktop/api/shlobj_core/ne-shlobj_core-dropimagetype) che indica la decorazione da applicare all'oggetto visivo della finestra di trascinamento. ad esempio, un'indicazione che indica che il file viene copiato anziché spostato o che l'oggetto non può essere eliminato in tale posizione. Tuttavia, gli oggetti visivi non vengono aggiornati finché l'oggetto riceve un messaggio **DDWM \_ UPDATEWINDOW** .

Il formato degli Appunti di [DragWindow](clipboard.md) fornisce l' **HWND** della finestra di trascinamento del destinatario al mittente del messaggio **\_ UPDATEWINDOW DDWM** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 
