---
title: Messaggio RB_GETBARINFO (COMmctrl. h)
description: Recupera le informazioni sul controllo Rebar e sull'elenco di immagini utilizzate.
ms.assetid: d3d56b95-7540-4e45-bb2e-b9d41cfcca0d
keywords:
- Controlli di Windows Message RB_GETBARINFO
topic_type:
- apiref
api_name:
- RB_GETBARINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d224c7c826bad0d5d6ae76ce5a4c2266632fa8a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048549"
---
# <a name="rb_getbarinfo-message"></a>\_Messaggio GETBARINFO RB

Recupera le informazioni sul controllo Rebar e sull'elenco di immagini utilizzate.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**REBARINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarinfo) che riceverà le informazioni sul controllo Rebar. Prima di inviare questo messaggio, è necessario impostare il membro **cbSize** della struttura su **sizeof**(REBARINFO).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





