---
description: Notifica a un AppBar che lo stato di Nascondi automaticamente o sempre in primo piano della barra delle applicazioni è stato modificato&\# 8212, ovvero l'utente ha selezionato o cancellato l'&\# 0034; Always on top&\# 0034; o &\# 0034; Nascondi automaticamente&\# 0034; casella di controllo nella finestra delle proprietà della barra delle applicazioni.
title: Messaggio ABN_STATECHANGE (Shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: ac2c00a2-ac20-40a5-947e-6b75a2620a0b
api_name:
- ABN_STATECHANGE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 33879fcb5e9435e2245bc3d00a9fab75bf1cbdc5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878778"
---
# <a name="abn_statechange-message"></a>\_Messaggio STATECHANGE di ABN

Notifica a un AppBar che lo stato di Nascondi automaticamente o della barra delle applicazioni è stato modificato, ovvero l'utente ha selezionato o deselezionato la casella di controllo "always on top" o "Nascondi automaticamente" nella finestra delle proprietà della barra delle applicazioni.


```C++
ABN_STATECHANGE 
```



## <a name="parameters"></a>Parametri

Questo messaggio non contiene parametri.

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Un AppBar può utilizzare questo messaggio di notifica per impostare lo stato di conformità a quello della barra delle applicazioni, se lo si desidera.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



 

 




