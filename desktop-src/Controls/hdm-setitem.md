---
title: HDM_SETITEM messaggio (Commctrl.h)
description: Imposta gli attributi dell'elemento specificato in un controllo intestazione. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro Header SetItem.
ms.assetid: c8f0d526-3ebe-48c5-8aea-ea3703e2d983
keywords:
- HDM_SETITEM di controllo Windows messaggio
topic_type:
- apiref
api_name:
- HDM_SETITEM
- HDM_SETITEMA
- HDM_SETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd0e2709a1b40bd4a564498cd0ae0b5d4e11861066aa9b0951815f92ee1c295f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118171066"
---
# <a name="hdm_setitem-message"></a>Messaggio \_ SETITEM HDM

Imposta gli attributi dell'elemento specificato in un controllo intestazione. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ Header SetItem.**](/windows/desktop/api/Commctrl/nf-commctrl-header_setitem)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice corrente dell'elemento i cui attributi devono essere modificati.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) che contiene informazioni sull'elemento. Quando viene inviato questo messaggio, il **membro mask** della struttura deve essere impostato per indicare gli attributi da impostare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero in caso di esito positivo oppure zero in caso contrario.

## <a name="remarks"></a>Commenti

La [**struttura HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) che supporta questo messaggio supporta le informazioni sull'ordine degli elementi e sull'elenco di immagini. Usando questi membri, è possibile controllare l'ordine di visualizzazione degli elementi e specificare le immagini da visualizzare con gli elementi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **HDM \_ SETITEMW** (Unicode) e **HDM \_ SETITEMA** (ANSI)<br/>                   |



 

 





