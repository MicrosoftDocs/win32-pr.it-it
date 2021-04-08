---
title: Messaggio TBM_SETPOS (COMmctrl. h)
description: Imposta la posizione logica corrente del dispositivo di scorrimento in un TrackBar.
ms.assetid: df6c4e5d-2847-419d-82b5-334d53bb6ba1
keywords:
- Controlli di Windows Message TBM_SETPOS
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
ms.openlocfilehash: e8e8da6e8e231a26b216ca8f9314d59474384857
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964967"
---
# <a name="tbm_setpos-message"></a>\_Messaggio SETPOS TBM

Imposta la posizione logica corrente del dispositivo di scorrimento in un TrackBar.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Ridisegni flag. Se questo parametro è **true**, il messaggio riestrae il controllo con il dispositivo di scorrimento in corrispondenza della posizione specificata da *lParam*. Se questo parametro è **false**, il messaggio non ridisegnato il dispositivo di scorrimento nella nuova posizione. Si noti che il messaggio imposta il valore della posizione del dispositivo di scorrimento (restituito dal messaggio [**TBM \_ GETPOS**](tbm-getpos.md) ) indipendentemente dal parametro *wParam* .

</dd> <dt>

*lParam* 
</dt> <dd>

Nuova posizione logica del dispositivo di scorrimento. Le posizioni logiche valide sono i valori integer nell'intervallo compreso tra le posizioni minime e massime del dispositivo di scorrimento. Se questo valore non è compreso nell'intervallo massimo e minimo del controllo, la posizione viene impostata sul valore massimo o minimo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





