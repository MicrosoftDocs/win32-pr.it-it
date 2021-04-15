---
title: Messaggio TBM_GETTIC (COMmctrl. h)
description: Recupera la posizione logica di un segno di graduazione in un TrackBar. La posizione logica può essere uno qualsiasi dei valori integer nell'intervallo compreso tra le posizioni minime e massime del dispositivo di scorrimento.
ms.assetid: 9d70c860-de97-4579-bb10-e9e9db7f1784
keywords:
- Controlli di Windows Message TBM_GETTIC
topic_type:
- apiref
api_name:
- TBM_GETTIC
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d534d5100e20cc544c31fca2fc9e49cda3bd976
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476798"
---
# <a name="tbm_gettic-message"></a>\_Messaggio Getter TBM

Recupera la posizione logica di un segno di graduazione in un TrackBar. La posizione logica può essere uno qualsiasi dei valori integer nell'intervallo compreso tra le posizioni minime e massime del dispositivo di scorrimento.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero che identifica un segno di graduazione. Gli indici validi sono compresi nell'intervallo da zero a due minori rispetto al conteggio restituito dal messaggio [**TBM \_ GETNUMTICS**](tbm-getnumtics.md) .

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce la posizione logica del segno di graduazione specificato oppure-1 se *wParam* non specifica un indice valido.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





