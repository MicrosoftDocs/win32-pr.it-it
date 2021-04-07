---
title: Messaggio SB_GETICON (COMmctrl. h)
description: Recupera l'icona per una parte in una barra di stato.
ms.assetid: f99508e3-afa8-48fd-b87a-fce41c4410ff
keywords:
- Controlli di Windows Message SB_GETICON
topic_type:
- apiref
api_name:
- SB_GETICON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab86809df54d796b8e83f05f2a2b9041450ce2fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874230"
---
# <a name="sb_geticon-message"></a>\_Messaggio SB GETicon

Recupera l'icona per una parte in una barra di stato.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero della parte che contiene l'icona da recuperare. Se questo parametro è-1, si presuppone che la barra di stato sia una barra di stato in [modalità semplice](status-bars.md) .

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'handle per l'icona in caso di esito positivo; in caso contrario, **null** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





