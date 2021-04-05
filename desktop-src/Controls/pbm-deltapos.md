---
title: Messaggio PBM_DELTAPOS (COMmctrl. h)
description: Sposta in avanti la posizione corrente di un indicatore di stato in base a un incremento specificato e ridisegnato la barra per riflettere la nuova posizione.
ms.assetid: 92c89434-d50b-45e7-b686-42e9297518b9
keywords:
- Controlli di Windows Message PBM_DELTAPOS
topic_type:
- apiref
api_name:
- PBM_DELTAPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19d0c36bbfdf5a812c8a7ffb2b2cdda6720fb757
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048555"
---
# <a name="pbm_deltapos-message"></a>\_Messaggio DELTAPOS PBM

Sposta in avanti la posizione corrente di un indicatore di stato in base a un incremento specificato e ridisegnato la barra per riflettere la nuova posizione.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Quantità per far avanzare la posizione.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce la posizione precedente.

## <a name="remarks"></a>Commenti

Se l'incremento restituisce un valore non compreso nell'intervallo del controllo, la posizione viene impostata sul limite più vicino.

Il comportamento di questo messaggio non è definito se viene inviato a un controllo con stile di [**\_ selezione PBS**](progress-bar-control-styles.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





