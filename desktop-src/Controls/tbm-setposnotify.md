---
title: Messaggio TBM_SETPOSNOTIFY (COMmctrl. h)
description: Imposta la posizione logica corrente del dispositivo di scorrimento in un TrackBar.
ms.assetid: 02f8899a-55b0-46ae-8642-9e534ab4abf5
keywords:
- Controlli di Windows Message TBM_SETPOSNOTIFY
topic_type:
- apiref
api_name:
- TBM_SETPOSNOTIFY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 636a2add9f13470a89b312450f1a3dcbc185be2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475911"
---
# <a name="tbm_setposnotify-message"></a>\_Messaggio SETPOSNOTIFY TBM

Imposta la posizione logica corrente del dispositivo di scorrimento in un TrackBar.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

il wParam è inutilizzato.

</dd> <dt>

*lParam* 
</dt> <dd>

Nuova posizione logica del dispositivo di scorrimento. Le posizioni logiche valide sono i valori integer nell'intervallo compreso tra le posizioni minime e massime del dispositivo di scorrimento. Se questo valore non è compreso nell'intervallo massimo e minimo del controllo, la posizione viene impostata sul valore massimo o minimo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

La chiamata a **TBM \_ SETPOSNOTIFY** imposterà la posizione del dispositivo di scorrimento TrackBar, ad esempio [**TBM \_ SETPOS**](tbm-setpos.md) , ma comporterà anche la notifica all'elemento padre di uno spostamento tramite un messaggio [**WM \_ HSCROLL**](wm-hscroll.md) o [**WM \_ VSCROLL**](wm-vscroll.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                            |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





