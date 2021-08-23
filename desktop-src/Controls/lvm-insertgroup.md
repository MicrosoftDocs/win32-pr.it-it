---
title: LVM_INSERTGROUP messaggio (Commctrl.h)
description: Inserisce un gruppo in un controllo di visualizzazione elenco.
ms.assetid: d43e21bc-e212-42dd-af88-48813d40cd50
keywords:
- LVM_INSERTGROUP di controllo Windows messaggio
topic_type:
- apiref
api_name:
- LVM_INSERTGROUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f31504226663b0df91e0297ed29abf784ff239dfcee5f323e8617f73dff65acc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019249"
---
# <a name="lvm_insertgroup-message"></a>Messaggio LVM \_ INSERTGROUP

Inserisce un gruppo in un controllo di visualizzazione elenco.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Indice in cui aggiungere il gruppo. Se è -1, il gruppo viene aggiunto alla fine dell'elenco.</dd> <dt>

*lParam* 
</dt> <dd>Puntatore a <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroup">**una struttura LVGROUP**</a> che contiene il gruppo da aggiungere.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'indice dell'elemento a cui è stato aggiunto il gruppo oppure -1 se l'operazione non è riuscita.

## <a name="remarks"></a>Commenti

Per attivare la modalità gruppo, chiamare [**LVM \_ ENABLEGROUPVIEW**](lvm-enablegroupview.md) o [**ListView \_ EnableGroupView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_enablegroupview).

Non è possibile inserire un gruppo in un controllo list-view vuoto.

Assicurarsi di impostare **iGroupId** negli elementi a cui è stato aggiunto il gruppo. In caso [**contrario, dopo l'elaborazione del messaggio LVM \_ ENABLEGROUPVIEW**](lvm-enablegroupview.md) **con TRUE,** il controllo listview non mostrerà alcun elemento.

> [!Note]  
> Per usare questo messaggio, è necessario fornire un manifesto che specifica Comclt32 versione 6.0. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





