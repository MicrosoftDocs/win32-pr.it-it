---
title: Messaggio PBM_SETRANGE32 (COMmctrl. h)
description: Imposta i valori minimo e massimo per un indicatore di stato su valori a 32 bit e ridisegnato la barra in modo da riflettere il nuovo intervallo.
ms.assetid: 7958ea14-17b4-4c0e-97ec-b09fa0d36e8b
keywords:
- Controlli di Windows Message PBM_SETRANGE32
topic_type:
- apiref
api_name:
- PBM_SETRANGE32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55fcf91c794ec9ae3880d67f8df947f87fec413d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742530"
---
# <a name="pbm_setrange32-message"></a>\_Messaggio SETRANGE32 PBM

Imposta i valori minimo e massimo per un indicatore di stato su valori a 32 bit e ridisegnato la barra in modo da riflettere il nuovo intervallo.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Valore minimo dell'intervallo. Per impostazione predefinita, il valore minimo è zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Valore massimo dell'intervallo. Questo valore deve essere maggiore di *wParam*. Per impostazione predefinita, il valore massimo è 100.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **DWORD** che include il limite minimo a 16 bit precedente nel relativo [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) e il limite massimo a 16 bit precedente nel [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)). Se gli intervalli precedenti sono valori a 32 bit, il valore restituito è costituito da **LOWORD** s di entrambi i limiti a 32 bit.

## <a name="remarks"></a>Commenti

Per recuperare tutti i valori a 32 bit massimi e Bassi, usare il messaggio [**PBM \_ GetRange**](pbm-getrange.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

