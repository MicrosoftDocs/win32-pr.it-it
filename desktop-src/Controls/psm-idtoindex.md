---
title: Messaggio PSM_IDTOINDEX (Prsht. h)
description: Accetta l'ID di una pagina della finestra delle proprietà e restituisce il relativo indice in base zero. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro IdToIndex di PropSheet.
ms.assetid: vs|controls|~\controls\propsheet\messages\psm_idtoindex.htm
keywords:
- Controlli di Windows Message PSM_IDTOINDEX
topic_type:
- apiref
api_name:
- PSM_IDTOINDEX
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f098c37ba30e33685abedf9dccd3ffc7c303acb9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120834"
---
# <a name="psm_idtoindex-message"></a>\_Messaggio IDTOINDEX di PSM

Accetta l'ID di una pagina della finestra delle proprietà e restituisce il relativo indice in base zero. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ IdToIndex di PropSheet**](/windows/desktop/api/Prsht/nf-prsht-propsheet_idtoindex) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

ID risorsa della pagina.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'indice in base zero della pagina della finestra delle proprietà specificato da *lParam* se ha esito positivo. In caso contrario, restituisce -1.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





