---
title: Messaggio TBM_GETPAGESIZE (COMmctrl. h)
description: Recupera il numero di posizioni logiche spostate dal dispositivo di scorrimento di TrackBar in risposta all'input da tastiera, ad esempio le chiavi o o l'input del mouse, ad esempio i clic nel canale del TrackBar.
ms.assetid: f0c5feac-2723-440e-96c0-dac37b0531ed
keywords:
- Controlli di Windows Message TBM_GETPAGESIZE
topic_type:
- apiref
api_name:
- TBM_GETPAGESIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac58c0b935b468cf8af565fba2db67c88418ee4f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119822"
---
# <a name="tbm_getpagesize-message"></a>\_Messaggio GETPAGESIZE TBM

Recupera il numero di posizioni logiche spostate dal dispositivo di scorrimento di TrackBar in risposta all'input da tastiera, ad esempio le chiavi o o l'input del mouse, ad esempio i clic nel canale del TrackBar. Le posizioni logiche sono gli incrementi interi nell'intervallo compreso tra minimo e massimo per le posizioni del dispositivo di scorrimento.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore a 32 bit che specifica le dimensioni di pagina per il TrackBar.

## <a name="remarks"></a>Commenti

TrackBar invia anche un messaggio [**WM \_ HSCROLL**](wm-hscroll.md) o [**WM \_ VSCROLL**](wm-vscroll.md) con i \_ codici di notifica TB PAGEUP e TB \_ PGGIÙ alla finestra padre quando riceve l'input della tastiera o del mouse che scorre la pagina.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**sepagesize TBM \_**](tbm-setpagesize.md)
</dt> </dl>

 

 





