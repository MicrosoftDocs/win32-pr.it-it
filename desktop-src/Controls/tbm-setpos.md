---
title: TBM_SETPOS messaggio (Commctrl.h)
description: 'TBM_SETPOS messaggio: imposta la posizione logica corrente del dispositivo di scorrimento in un trackbar.'
ms.assetid: df6c4e5d-2847-419d-82b5-334d53bb6ba1
keywords:
- TBM_SETPOS dei messaggi Windows controllo
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
ms.openlocfilehash: 3ccd1cb35f8cde672c51baafe5623291e5449f90aa118eb36cb12152fe155385
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078045"
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

Nuova posizione logica del dispositivo di scorrimento. Le posizioni logiche valide sono i valori interi nell'intervallo tra le posizioni minime e massime del dispositivo di scorrimento del trackbar. Se questo valore non rientra nell'intervallo massimo e minimo del controllo, la posizione viene impostata sul valore massimo o minimo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





