---
title: Messaggio LVM_GETIMAGELIST (COMmctrl. h)
description: Recupera l'handle a un elenco di immagini utilizzato per disegnare elementi della visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro ListView Getimagine.
ms.assetid: dd48d8b5-6dbd-48ab-95c3-0fcf1e8c24f0
keywords:
- Controlli di Windows Message LVM_GETIMAGELIST
topic_type:
- apiref
api_name:
- LVM_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0abc68c5e5dd9a18c3ec203ad7fe3db97a542845
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120286"
---
# <a name="lvm_getimagelist-message"></a>\_Messaggio GETimagine LVM

Recupera l'handle a un elenco di immagini utilizzato per disegnare elementi della visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**ListView \_ getimagine**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getimagelist) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Elenco di immagini da recuperare. Questo parametro può essere uno dei valori seguenti:



| Valore                                                                                                                                                                     | Significato                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <span id="LVSIL_NORMAL"></span><span id="lvsil_normal"></span><dl> <dt>**LVSIL \_ normale**</dt> </dl>                | Elenco immagini con icone grandi.<br/>  |
| <span id="LVSIL_SMALL"></span><span id="lvsil_small"></span><dl> <dt>**LVSIL \_ Small**</dt> </dl>                   | Elenco immagini con icone piccole.<br/>  |
| <span id="LVSIL_STATE"></span><span id="lvsil_state"></span><dl> <dt>**\_stato LVSIL**</dt> </dl>                   | Elenco immagini con immagini di stato.<br/> |
| <span id="LVSIL_GROUPHEADER"></span><span id="lvsil_groupheader"></span><dl> <dt>**\_GROUPHEADER LVSIL**</dt> </dl> | Elenco di immagini per l'intestazione di gruppo.<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'handle per l'elenco di immagini specificato, in caso di esito positivo; in caso contrario, **null** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





