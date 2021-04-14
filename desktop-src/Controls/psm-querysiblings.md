---
title: Messaggio PSM_QUERYSIBLINGS (Prsht. h)
description: Inviato a una finestra delle proprietà che quindi inoltra il messaggio a ognuna delle relative pagine. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro PropSheet QuerySiblings.
ms.assetid: 96f48847-b7b8-4d6f-8bde-ada915b7c962
keywords:
- Controlli di Windows Message PSM_QUERYSIBLINGS
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
ms.openlocfilehash: ea5943fefa906475e34d1cc7acc7f8a86cd99252
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517967"
---
# <a name="psm_querysiblings-message"></a>\_Messaggio QUERYSIBLINGS di PSM

Inviato a una finestra delle proprietà che quindi inoltra il messaggio a ognuna delle relative pagine. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**PropSheet \_ QuerySiblings**](/windows/desktop/api/Prsht/nf-prsht-propsheet_querysiblings) .

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
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





