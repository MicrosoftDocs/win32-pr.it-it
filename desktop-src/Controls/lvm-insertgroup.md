---
title: Messaggio LVM_INSERTGROUP (COMmctrl. h)
description: Inserisce un gruppo in un controllo visualizzazione elenco.
ms.assetid: d43e21bc-e212-42dd-af88-48813d40cd50
keywords:
- Controlli di Windows Message LVM_INSERTGROUP
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
ms.openlocfilehash: 94dbae780f7de26a5c791477e1a7321794054056
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302287"
---
# <a name="lvm_insertgroup-message"></a>\_Messaggio INSERTGROUP LVM

Inserisce un gruppo in un controllo visualizzazione elenco.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Indice in cui deve essere aggiunto il gruppo. Se è-1, il gruppo viene aggiunto alla fine dell'elenco.</dd> <dt>

*lParam* 
</dt> <dd>Puntatore a una struttura <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroup">**LVGROUP**</a> contenente il gruppo da aggiungere.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'indice dell'elemento a cui è stato aggiunto il gruppo oppure-1 se l'operazione non è riuscita.

## <a name="remarks"></a>Commenti

Per attivare la modalità gruppo, chiamare [**LVM \_ ENABLEGROUPVIEW**](lvm-enablegroupview.md) o [**ListView \_ ENABLEGROUPVIEW**](/windows/desktop/api/Commctrl/nf-commctrl-listview_enablegroupview).

Non è possibile inserire un gruppo in un controllo visualizzazione elenco vuoto.

Assicurarsi di impostare **iGroupId** negli elementi a cui è stato aggiunto il gruppo. In caso contrario, dopo l'elaborazione del messaggio [**LVM \_ ENABLEGROUPVIEW**](lvm-enablegroupview.md) con **true** , il controllo ListView non visualizzerà alcun elemento.

> [!Note]  
> Per usare questo messaggio, è necessario fornire un manifesto che specifichi la versione 6,0 di Comclt32. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





