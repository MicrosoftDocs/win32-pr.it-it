---
title: Messaggio PSM_INDEXTOID (Prsht. h)
description: Accetta l'indice di una pagina della finestra delle proprietà e restituisce il relativo ID di risorsa. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro IndexToId di PropSheet.
ms.assetid: c153675a-360f-4916-aa0b-500636dd9022
keywords:
- Controlli di Windows Message PSM_INDEXTOID
topic_type:
- apiref
api_name:
- PSM_INDEXTOID
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 643861ecb6dc11d949483defc282d6d65648bdca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048517"
---
# <a name="psm_indextoid-message"></a>\_Messaggio INDEXTOID di PSM

Accetta l'indice di una pagina della finestra delle proprietà e restituisce il relativo ID di risorsa. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ IndexToId di PropSheet**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextoid) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero della pagina.

</dd> <dt>

*lParam* 
</dt> <dd>

Deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'ID risorsa della pagina della finestra delle proprietà specificata da *wParam* se ha esito positivo. In caso contrario, restituisce zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





