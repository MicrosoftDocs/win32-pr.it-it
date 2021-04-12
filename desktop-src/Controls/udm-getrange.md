---
title: Messaggio UDM_GETRANGE (COMmctrl. h)
description: Recupera le posizioni minime e massime (intervallo) per un controllo di scorrimento.
ms.assetid: fd42538a-8d96-4a9c-a1db-07c3e9afef84
keywords:
- Controlli di Windows Message UDM_GETRANGE
topic_type:
- apiref
api_name:
- UDM_GETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6fd8467ad4494bea92a4c1f9a68d675ef1471f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104225244"
---
# <a name="udm_getrange-message"></a>UDM \_ messaggio GETrange

Recupera le posizioni minime e massime (intervallo) per un controllo di scorrimento.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è un valore a 32 bit che contiene le posizioni minime e massime. [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) è la posizione massima per il controllo e [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) è la posizione minima.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

