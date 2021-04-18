---
title: Messaggio TB_CUSTOMIZE (COMmctrl. h)
description: Consente di visualizzare la finestra di dialogo Personalizza barra degli strumenti.
ms.assetid: 45249467-d585-4ffd-8bbe-e39739059c40
keywords:
- Controlli di Windows Message TB_CUSTOMIZE
topic_type:
- apiref
api_name:
- TB_CUSTOMIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dada0ef195e898b7a46487a2d775e46d6af854ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302785"
---
# <a name="tb_customize-message"></a>TB \_ personalizzare il messaggio

Consente di visualizzare la finestra di dialogo **Personalizza barra degli strumenti** .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

> [!Note]  
> La barra degli strumenti deve gestire le notifiche [TBN \_ QUERYINSERT](tbn-queryinsert.md) e [TBN \_ QUERYDELETE](tbn-querydelete.md) per la visualizzazione della finestra di dialogo **Personalizza barra degli strumenti** . Se la barra degli strumenti non gestisce tali notifiche, **TB \_ Customize** non ha alcun effetto.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





