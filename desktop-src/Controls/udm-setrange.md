---
title: Messaggio UDM_SETRANGE (COMmctrl. h)
description: Imposta le posizioni minime e massime (intervallo) per un controllo di scorrimento.
ms.assetid: 81875528-86cc-419a-a07c-f4f98baf1462
keywords:
- Controlli di Windows Message UDM_SETRANGE
topic_type:
- apiref
api_name:
- UDM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb32a72ca8ca5182e87e2c0346cbc44ab25300e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048543"
---
# <a name="udm_setrange-message"></a>\_Messaggio SEtrange UDM

Imposta le posizioni minime e massime (intervallo) per un controllo di scorrimento.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) è un valore **short** che specifica la posizione massima per il controllo di scorrimento e [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) è un valore **short** che specifica la posizione minima. La posizione non può essere maggiore del \_ valore MaxVal di UD o minore del \_ valore MINVAL di UD. Inoltre, la differenza tra le due posizioni non può superare il \_ MaxVal UD.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

La posizione massima può essere minore della posizione minima. Facendo clic sul pulsante freccia su viene spostata la posizione corrente più vicina alla posizione massima e facendo clic sul pulsante freccia giù si sposta verso la posizione minima.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MAKELPARAM**](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> <dt>

[**\_SEtrange UDM**](udm-setrange.md)
</dt> </dl>

 

