---
title: Messaggio LVM_GETCOLUMNWIDTH (COMmctrl. h)
description: Ottiene la larghezza di una colonna in un report o in una visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro GetColumnWidth di ListView.
ms.assetid: 06e8ec36-3bc5-4516-ac29-17c36fb6d962
keywords:
- Controlli di Windows Message LVM_GETCOLUMNWIDTH
topic_type:
- apiref
api_name:
- LVM_GETCOLUMNWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0577e7cb2a589c432d4b5ca62f640de61d67dc75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119006"
---
# <a name="lvm_getcolumnwidth-message"></a>\_Messaggio GETCOLUMNWIDTH LVM

Ottiene la larghezza di una colonna in un report o in una visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ GetColumnWidth di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcolumnwidth) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice della colonna. Questo parametro viene ignorato in visualizzazione elenco.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce la larghezza della colonna in caso di esito positivo; in caso contrario, zero. Se questo messaggio viene inviato a un controllo di visualizzazione elenco con lo stile del [**\_ report LVS**](list-view-window-styles.md) e la colonna specificata non esiste, il valore restituito non è definito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





