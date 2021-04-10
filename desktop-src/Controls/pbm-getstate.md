---
title: Messaggio PBM_GETSTATE (COMmctrl. h)
description: Ottiene lo stato dell'indicatore di stato.
ms.assetid: ff240160-7db6-4711-8d4e-25a77dfba118
keywords:
- Controlli di Windows Message PBM_GETSTATE
topic_type:
- apiref
api_name:
- PBM_GETSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07d4f7029fca46a046545efd1cea8e0eab99c757
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964565"
---
# <a name="pbm_getstate-message"></a>\_Messaggio GETstate di PBM

Ottiene lo stato dell'indicatore di stato.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce lo stato corrente dell'indicatore di stato. Uno dei valori seguenti.



| Codice restituito                                                                                 | Descrizione             |
|---------------------------------------------------------------------------------------------|-------------------------|
| <dl> <dt>**PBST \_ normale**</dt> </dl> | Operazione in corso.<br/> |
| <dl> <dt>**\_errore PBST**</dt> </dl>  | Errore.<br/>       |
| <dl> <dt>**PBST \_ sospeso**</dt> </dl> | (sospeso)<br/>      |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





