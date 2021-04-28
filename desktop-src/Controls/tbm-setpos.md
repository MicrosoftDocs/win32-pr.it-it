---
title: TBM_SETPOS messaggio (Commctrl.h)
description: 'TBM_SETPOS: imposta la posizione logica corrente del dispositivo di scorrimento in un trackbar.'
ms.assetid: df6c4e5d-2847-419d-82b5-334d53bb6ba1
keywords:
- TBM_SETPOS di windows del messaggio
topic_type:
- apiref
api_name:
- TBM_SETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f10e05a677119f18489d0eb9eebc4528d3ad115
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085869"
---
# <a name="tbm_setpos-message"></a>Messaggio \_ SETPOS TBM

Imposta la posizione logica corrente del dispositivo di scorrimento in un trackbar.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Flag di ridisegno. Se questo parametro è **TRUE,** il messaggio ridisegna il controllo con il dispositivo di scorrimento nella posizione specificata da *lParam*. Se questo parametro è **FALSE,** il messaggio non ridisegna il dispositivo di scorrimento nella nuova posizione. Si noti che il messaggio imposta il valore della posizione del dispositivo di scorrimento (come restituito dal messaggio [**\_ GETPOS TBM)**](tbm-getpos.md) indipendentemente dal *parametro wParam.*

</dd> <dt>

*lParam* 
</dt> <dd>

Nuova posizione logica del dispositivo di scorrimento. Le posizioni logiche valide sono i valori interi nell'intervallo di posizioni del dispositivo di scorrimento minimo e massimo del trackbar. Se questo valore non rientra nell'intervallo massimo e minimo del controllo, la posizione viene impostata sul valore massimo o minimo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows Vista \[\]<br/>                                        |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





