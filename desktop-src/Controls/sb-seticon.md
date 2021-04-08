---
title: Messaggio SB_SETICON (COMmctrl. h)
description: Imposta l'icona di una parte in una barra di stato.
ms.assetid: d8528cd1-54d2-44ba-b0d6-29111f75616a
keywords:
- Controlli di Windows Message SB_SETICON
topic_type:
- apiref
api_name:
- SB_SETICON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f720c414238eb89cf98bf0556ebabffefceae4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874225"
---
# <a name="sb_seticon-message"></a>\_Messaggio dell'icona SB

Imposta l'icona di una parte in una barra di stato.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero della parte che riceverà l'icona. Se questo parametro è-1, si presuppone che la barra di stato sia una barra di stato semplice.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per l'icona da impostare. Se questo valore è **null**, l'icona viene rimossa dalla parte.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.

## <a name="remarks"></a>Commenti

La barra di stato non eliminerà l'icona. È responsabilità dell'applicazione chiamante tenere traccia ed eliminare eventuali icone.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





