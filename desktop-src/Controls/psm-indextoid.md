---
title: PSM_INDEXTOID messaggio (Prsht.h)
description: Accetta l'indice di una pagina della finestra delle proprietà e restituisce il relativo ID risorsa. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro PropSheet IndexToId.
ms.assetid: c153675a-360f-4916-aa0b-500636dd9022
keywords:
- PSM_INDEXTOID di controllo Windows messaggio
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
ms.openlocfilehash: bc7a26cd97d324ae9bb4cfee85df00387c59293c7de8817b67da5605a207f07f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985721"
---
# <a name="psm_indextoid-message"></a>Messaggio \_ INDEXTOID PSM

Accetta l'indice di una pagina della finestra delle proprietà e restituisce il relativo ID risorsa. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ PropSheet IndexToId.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextoid)

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

Restituisce l'ID risorsa della pagina della finestra delle proprietà specificata da *wParam* in caso di esito positivo. In caso contrario, restituisce zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

 





