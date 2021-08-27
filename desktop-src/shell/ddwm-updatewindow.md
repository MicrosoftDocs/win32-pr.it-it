---
description: Indica a una finestra dell'immagine di rilascio di eseguire l'aggiornamento usando le nuove informazioni DROPDESCRIPTION.
title: DDWM_UPDATEWINDOW messaggio
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
ms.openlocfilehash: a17e015d6dff2ae5133f3ce8245c5ead3c3381f8eb5c48e74946fdf9bcb46ad1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032839"
---
# <a name="ddwm_updatewindow-message"></a>Messaggio DDWM \_ UPDATEWINDOW

Indica a una finestra dell'immagine di rilascio di eseguire l'aggiornamento usando le [**nuove informazioni DROPDESCRIPTION.**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ Pollici\]
</dt> <dd>

Non usato.

</dd> <dt>

*lParam* \[ Pollici\]
</dt> <dd>

Non usato.

</dd> </dl>

## <a name="remarks"></a>Commenti

DDWM \_ UPDATEWINDOW è definito come WM \_ USER+3.

Quando lo stato di un'operazione di rilascio cambia, ad esempio in risposta a un tasto di modifica,[**IDropTarget::D ragOver**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover) restituisce un nuovo valore [**DROPEFFECT**](../com/dropeffect-constants.md) (questo **valore DROPEFFECT** può essere ricevuto anche tramite [**IDropSource::GiveFeedback).**](/windows/win32/api/oleidl/nf-oleidl-idropsource-givefeedback) In risposta, l'applicazione aggiorna la struttura [**DROPDESCRIPTION**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription) della destinazione di rilascio con un nuovo [**valore DROPIMAGETYPE**](/windows/desktop/api/shlobj_core/ne-shlobj_core-dropimagetype) che indica la decorazione da applicare all'oggetto visivo della finestra di trascinamento. ad esempio un'indicazione che il file viene copiato anziché spostato o che l'oggetto non può essere eliminato in tale percorso. Tuttavia, gli oggetti visivi non vengono aggiornati fino a quando l'oggetto non riceve un **messaggio \_ UPDATEWINDOW DDWM.**

Il formato degli Appunti [DragWindow](clipboard.md) fornisce **l'HWND** della finestra di trascinamento del destinatario al mittente del messaggio **DDWM \_ UPDATEWINDOW.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



 

 
