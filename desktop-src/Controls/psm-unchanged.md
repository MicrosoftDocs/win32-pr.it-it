---
title: Messaggio PSM_UNCHANGED (Prsht. h)
description: Informa una finestra delle proprietà che le informazioni in una pagina sono state ripristinate allo stato salvato in precedenza. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro PropSheet non modificata.
ms.assetid: 61c15dec-40d0-4720-a117-4eed765c8819
keywords:
- Controlli di Windows Message PSM_UNCHANGED
topic_type:
- apiref
api_name:
- PSM_UNCHANGED
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eb1d6216f94afd610bb49710a3e84b4c21a673f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104225234"
---
# <a name="psm_unchanged-message"></a>PSM \_ messaggio non modificato

Informa una finestra delle proprietà che le informazioni in una pagina sono state ripristinate allo stato salvato in precedenza. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**PropSheet non \_ modificata**](/windows/desktop/api/Prsht/nf-prsht-propsheet_unchanged) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per la pagina che ha ripristinato lo stato salvato in precedenza.

</dd> <dt>

*lParam* 
</dt> <dd>

Deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

La finestra delle proprietà Disabilita il pulsante **applica** se nessuna altra pagina ha registrato modifiche con la finestra delle proprietà.

> [!Note]  
> Questo messaggio non è supportato quando si usa lo stile della procedura guidata Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





