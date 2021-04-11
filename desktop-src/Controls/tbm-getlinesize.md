---
title: Messaggio TBM_GETLINESIZE (COMmctrl. h)
description: Recupera il numero di posizioni logiche spostate dal dispositivo di scorrimento del TrackBar in risposta all'input da tastiera dei tasti di direzione, ad esempio i tasti o. Le posizioni logiche sono gli incrementi interi nell'intervallo compreso tra minimo e massimo per le posizioni del dispositivo di scorrimento.
ms.assetid: b596060a-5bac-4b31-82f3-ee4744a9779c
keywords:
- Controlli di Windows Message TBM_GETLINESIZE
topic_type:
- apiref
api_name:
- TBM_GETLINESIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86eb103f34461e545f5a9f56148c48364d880dbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964996"
---
# <a name="tbm_getlinesize-message"></a>\_Messaggio GETLINESIZE TBM

Recupera il numero di posizioni logiche spostate dal dispositivo di scorrimento del TrackBar in risposta all'input da tastiera dei tasti di direzione, ad esempio i tasti o. Le posizioni logiche sono gli incrementi interi nell'intervallo compreso tra minimo e massimo per le posizioni del dispositivo di scorrimento.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore a 32 bit che specifica le dimensioni della riga per il TrackBar.

## <a name="remarks"></a>Commenti

L'impostazione predefinita per le dimensioni della riga è 1.

TrackBar invia anche un messaggio [**WM \_ HSCROLL**](wm-hscroll.md) o [**WM \_ VSCROLL**](wm-vscroll.md) con i \_ \_ codici di notifica TB e TB LINEDOWN alla finestra padre quando l'utente preme i tasti di direzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





