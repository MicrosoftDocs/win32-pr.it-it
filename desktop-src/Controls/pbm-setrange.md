---
title: Messaggio PBM_SETRANGE (COMmctrl. h)
description: Imposta i valori minimo e massimo per un indicatore di stato e ridisegnato la barra in modo da riflettere il nuovo intervallo.
ms.assetid: 251eb8c5-bedc-4e2c-90c2-e1626cb00420
keywords:
- Controlli di Windows Message PBM_SETRANGE
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
ms.openlocfilehash: e9e588170c80378082eab7e419e9425e716b8caf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874157"
---
# <a name="pbm_setrange-message"></a>\_Messaggio SEtrange PBM

Imposta i valori minimo e massimo per un indicatore di stato e ridisegnato la barra in modo da riflettere il nuovo intervallo.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifica il valore di intervallo minimo e [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica il valore di intervallo massimo. Il valore minimo dell'intervallo non deve essere negativo. Per impostazione predefinita, il valore minimo è zero. Il valore di intervallo massimo deve essere maggiore del valore di intervallo minimo. Per impostazione predefinita, il valore di intervallo massimo è 100.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce i valori di intervallo precedenti se l'operazione ha esito positivo oppure zero in caso contrario. [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifica il valore minimo precedente e [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica il valore massimo precedente.

## <a name="remarks"></a>Commenti

Se non si impostano i valori di intervallo, il sistema imposta il valore minimo su 0 e il valore massimo su 100. Poiché questo messaggio esprime l'intervallo come Unsigned Integer a 16 bit, può estendersi da 0 a 65.535. Il valore minimo nell'intervallo può essere compreso tra 0 e 65.535. Analogamente, il valore massimo può essere compreso tra 0 e 65.535.

Per impostare un intervallo più ampio, chiamare [**PBM \_ SETRANGE32**](pbm-setrange32.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**GetRange PBM \_**](pbm-getrange.md)
</dt> <dt>

[**\_SETRANGE32 PBM**](pbm-setrange32.md)
</dt> </dl>

 

