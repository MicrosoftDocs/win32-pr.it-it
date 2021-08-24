---
title: PSM_CHANGED messaggio (Prsht.h)
description: Informa una finestra delle proprietà che le informazioni in una pagina sono state modificate. È possibile inviare questo messaggio in modo esplicito o tramite la macro PropSheet \_ Changed.
ms.assetid: b092969f-31dc-4e3c-9100-d15f1bdd5aa5
keywords:
- PSM_CHANGED controlli di Windows messaggio
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
ms.openlocfilehash: 2002801d21e4e89a6ccf762b9c9932671b210217a950f5494fb736feda35d32e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826021"
---
# <a name="psm_changed-message"></a>PSM \_ CHANGED message

Informa una finestra delle proprietà che le informazioni in una pagina sono state modificate. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**PropSheet \_ Changed.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_changed)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per la pagina modificata.

</dd> <dt>

*lParam* 
</dt> <dd>

Deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

La finestra delle proprietà abiliterà **il pulsante** Applica.

> [!Note]  
> Questo messaggio non è supportato quando si usa lo stile della procedura guidata Aero ([**PSH \_ ACROBATWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

 





