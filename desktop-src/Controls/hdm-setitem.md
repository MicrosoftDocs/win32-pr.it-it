---
title: Messaggio HDM_SETITEM (COMmctrl. h)
description: Imposta gli attributi dell'elemento specificato in un controllo intestazione. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro elemento intestazione.
ms.assetid: c8f0d526-3ebe-48c5-8aea-ea3703e2d983
keywords:
- Controlli di Windows Message HDM_SETITEM
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
ms.openlocfilehash: 71b03a05b909cf8c7887edd2031f5346c419f1cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478268"
---
# <a name="hdm_setitem-message"></a>HDM- \_ messaggio di elemento

Imposta gli attributi dell'elemento specificato in un controllo intestazione. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ elemento intestazione**](/windows/desktop/api/Commctrl/nf-commctrl-header_setitem) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice corrente dell'elemento i cui attributi devono essere modificati.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) che contiene informazioni sull'elemento. Quando viene inviato questo messaggio, è necessario impostare il membro **mask** della struttura per indicare gli attributi da impostare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero in caso di esito positivo o zero.

## <a name="remarks"></a>Commenti

La struttura [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) che supporta questo messaggio supporta le informazioni sull'ordine degli elementi e sull'elenco di immagini. Usando questi membri, è possibile controllare l'ordine in cui vengono visualizzati gli elementi e specificare le immagini da visualizzare con gli elementi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **HDM \_ SETITEMW** (Unicode) e **HDM \_ setitema** (ANSI)<br/>                   |



 

 





