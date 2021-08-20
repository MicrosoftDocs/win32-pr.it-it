---
title: PBM_SETRANGE messaggio (Commctrl.h)
description: Imposta i valori minimo e massimo per un indicatore di stato e ridisegna l'indicatore per riflettere il nuovo intervallo.
ms.assetid: 251eb8c5-bedc-4e2c-90c2-e1626cb00420
keywords:
- PBM_SETRANGE di controllo Windows messaggio
topic_type:
- apiref
api_name:
- PBM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb5dca4e4be30b50627d8583a67801dc5cb246ef65e9cd267e6d7b3ee3ed7869
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118170198"
---
# <a name="pbm_setrange-message"></a>Messaggio \_ SETRANGE PBM

Imposta i valori minimo e massimo per un indicatore di stato e ridisegna l'indicatore per riflettere il nuovo intervallo.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

LOWORD [**specifica**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) il valore minimo dell'intervallo e [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica il valore di intervallo massimo. Il valore minimo dell'intervallo non deve essere negativo. Per impostazione predefinita, il valore minimo è zero. Il valore dell'intervallo massimo deve essere maggiore del valore minimo dell'intervallo. Per impostazione predefinita, il valore massimo dell'intervallo è 100.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce i valori dell'intervallo precedente in caso di esito positivo oppure zero in caso contrario. [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifica il valore minimo precedente e [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica il valore massimo precedente.

## <a name="remarks"></a>Commenti

Se non si impostano i valori di intervallo, il sistema imposta il valore minimo su 0 e il valore massimo su 100. Poiché questo messaggio esprime l'intervallo come intero senza segno a 16 bit, può estendersi da 0 a 65.535. Il valore minimo nell'intervallo può essere compreso tra 0 e 65.535. Analogamente, il valore massimo può essere compreso tra 0 e 65.535.

Per impostare un intervallo più ampio, chiamare [**PBM \_ SETRANGE32.**](pbm-setrange32.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**PBM \_ GETRANGE**](pbm-getrange.md)
</dt> <dt>

[**PBM \_ SETRANGE32**](pbm-setrange32.md)
</dt> </dl>

 

