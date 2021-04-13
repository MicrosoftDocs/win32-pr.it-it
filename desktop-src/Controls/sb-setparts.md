---
title: Messaggio SB_SETPARTS (COMmctrl. h)
description: Imposta il numero di parti in una finestra di stato e la coordinata del bordo destro di ogni parte.
ms.assetid: e29e8b09-c018-4ea4-8b47-6f3713113427
keywords:
- Controlli di Windows Message SB_SETPARTS
topic_type:
- apiref
api_name:
- SB_SETPARTS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 062058fa3778cd0394cadd9d76b363a0353ffb2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518436"
---
# <a name="sb_setparts-message"></a>\_Messaggio di SEparazione SB

Imposta il numero di parti in una finestra di stato e la coordinata del bordo destro di ogni parte.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Numero di parti da impostare (non può essere maggiore di 256).

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una matrice di interi. Il numero di elementi è specificato in *wParam*. Ogni elemento specifica la posizione, in coordinate client, del bordo destro della parte corrispondente. Se un elemento è-1, il bordo destro della parte corrispondente si estende al bordo della finestra.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





