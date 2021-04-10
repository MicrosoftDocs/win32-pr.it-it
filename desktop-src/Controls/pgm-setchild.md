---
title: Messaggio PGM_SETCHILD (COMmctrl. h)
description: Imposta la finestra contenuta per il controllo pager.
ms.assetid: 717e6720-aa42-4ecd-9520-4618a04dc28d
keywords:
- Controlli di Windows Message PGM_SETCHILD
topic_type:
- apiref
api_name:
- PGM_SETCHILD
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c934c3c5688ac79b5c5ce67aef68e28ad3627ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119582"
---
# <a name="pgm_setchild-message"></a>\_Messaggio del messaggio PGM

Imposta la finestra contenuta per il controllo pager. Questo messaggio non modificherà l'elemento padre della finestra contenuta; assegna un handle di finestra al controllo pager per lo scorrimento. Nella maggior parte dei casi, la finestra contenuta sarà una finestra figlio. In tal caso, la finestra contenuta deve essere un elemento figlio del controllo pager. È possibile inviare questo messaggio in modo esplicito o utilizzare la macro [**pager \_ figlio**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setchild) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Handle per la finestra da contenere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito non viene utilizzato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





