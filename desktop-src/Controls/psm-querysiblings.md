---
title: PSM_QUERYSIBLINGS messaggio (Prsht.h)
description: Inviato a una finestra delle proprietà, che inoltra quindi il messaggio a ognuna delle relative pagine. È possibile inviare questo messaggio in modo esplicito o tramite la \_ macro PropSheet QuerySiblings.
ms.assetid: 96f48847-b7b8-4d6f-8bde-ada915b7c962
keywords:
- PSM_QUERYSIBLINGS di controllo Windows messaggio
topic_type:
- apiref
api_name:
- PSM_QUERYSIBLINGS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c270a3c7a667894f7821f6c0c169115846b6ddc2492648f5f9d75a0c85d21d04
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088651"
---
# <a name="psm_querysiblings-message"></a>Messaggio \_ QUERYSIBLINGS PSM

Inviato a una finestra delle proprietà, che inoltra quindi il messaggio a ognuna delle relative pagine. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**\_ PropSheet QuerySiblings.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_querysiblings)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Primo parametro definito dall'applicazione.

</dd> <dt>

*lParam* 
</dt> <dd>

Secondo parametro definito dall'applicazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il valore diverso da zero da una pagina nella finestra delle proprietà oppure zero se nessuna pagina restituisce un valore diverso da zero.

## <a name="remarks"></a>Commenti

Se una pagina restituisce un valore diverso da zero, la finestra delle proprietà non invia il messaggio alle pagine successive.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

 





