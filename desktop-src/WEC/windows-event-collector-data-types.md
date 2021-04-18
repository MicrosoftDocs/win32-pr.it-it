---
title: Tipi di dati dell'agente di raccolta eventi Windows (Evcoll. h)
description: I tipi di dati per l'agente di raccolta eventi di Windows vengono utilizzati come tipi di variabile oggetto sottoscrizione evento, tipi di parametri di funzione e tipi restituiti di funzione.
ms.assetid: b78bdaf8-e034-40fe-acf8-632313e4fd94
ms.tgt_platform: multiple
keywords:
- EC_HANDLE
- EC_OBJECT_ARRAY_PROPERTY_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ccec141317644aa091eac44033b87b9e4495ddc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106300921"
---
# <a name="windows-event-collector-data-types"></a>Tipi di dati dell'agente di raccolta eventi Windows

I tipi di dati per l'agente di raccolta eventi di Windows vengono utilizzati come tipi di variabile oggetto sottoscrizione evento, tipi di parametri di funzione e tipi restituiti di funzione.


```C++
typedef HANDLE EC_HANDLE;
typedef HANDLE EC_OBJECT_ARRAY_PROPERTY_HANDLE;
```



<dl> <dt>

**\_handle EC**
</dt> <dd>

Handle per un oggetto sottoscrizione. Utilizzato per rappresentare una sottoscrizione dell'agente di raccolta eventi.

</dd> <dt>

**\_ \_ \_ Handle proprietà matrice di oggetti EC \_**
</dt> <dd>

Handle per una matrice di valori di proprietà per le origini eventi di una sottoscrizione. L'handle di matrice viene restituito dal metodo [**EcGetSubscriptionProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionproperty) quando il valore **EcSubscriptionEventSources** viene passato nel parametro *PropertyId* .

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                            |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Evcoll. h</dt> </dl> |



 

 





