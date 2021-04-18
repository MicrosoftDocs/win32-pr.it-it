---
title: Messaggio PSM_CHANGED (Prsht. h)
description: Informa una finestra delle proprietà che le informazioni in una pagina sono state modificate. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro PropSheet modificata.
ms.assetid: b092969f-31dc-4e3c-9100-d15f1bdd5aa5
keywords:
- Controlli di Windows Message PSM_CHANGED
topic_type:
- apiref
api_name:
- PSM_CHANGED
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57f931db5e25f816f7ea164ca5871a4e3e7757a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302201"
---
# <a name="psm_changed-message"></a>PSM- \_ messaggio modificato

Informa una finestra delle proprietà che le informazioni in una pagina sono state modificate. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**PropSheet \_ modificata**](/windows/desktop/api/Prsht/nf-prsht-propsheet_changed) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per la pagina che è stata modificata.

</dd> <dt>

*lParam* 
</dt> <dd>

Deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Nella finestra delle proprietà viene abilitato il pulsante **applica** .

> [!Note]  
> Questo messaggio non è supportato quando si usa lo stile della procedura guidata Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





