---
title: LVM_GETTOPINDEX messaggio (Commctrl.h)
description: Recupera l'indice dell'elemento visibile in primo piano nella visualizzazione elenco o report. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro ListView GetTopIndex.
ms.assetid: vs|controls|~\controls\listview\messages\lvm_gettopindex.htm
keywords:
- LVM_GETTOPINDEX controlli di Windows messaggio
topic_type:
- apiref
api_name:
- LVM_GETTOPINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6434aa2c7382a4a4d54fc3a76edd5eb4b70ccae858b8d9fcf41547590a8bc69c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119920041"
---
# <a name="lvm_gettopindex-message"></a>Messaggio LVM \_ GETTOPINDEX

Recupera l'indice dell'elemento visibile in primo piano nella visualizzazione elenco o report. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ ListView GetTopIndex.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettopindex)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'indice dell'elemento in caso di esito positivo. Restituisce zero se il controllo visualizzazione elenco si trova nella visualizzazione icona o icona piccola o se il controllo visualizzazione elenco si trova nella visualizzazione dettagli con i gruppi abilitati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





