---
title: Costanti dell'agente di raccolta eventi Windows (Evcoll. h)
description: Windows Event Collector SDK contiene le costanti seguenti.
ms.assetid: 2ba862f9-6849-43b3-8914-e18ede1d63c0
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- EC_VARIANT_TYPE_MASK
- EC_VARIANT_TYPE_ARRAY
- EC_READ_ACCESS
- EC_WRITE_ACCESS
- EC_OPEN_ALWAYS
- EC_CREATE_NEW
- EC_OPEN_EXISTING
api_location:
- Evcoll.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf6e7e99186e2148bf6ec3400aadf760a79a2331
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739743"
---
# <a name="windows-event-collector-constants"></a>Costanti dell'agente di raccolta eventi Windows

Windows Event Collector SDK contiene le costanti seguenti.

<dl> <dt>

<span id="EC_VARIANT_TYPE_MASK"></span><span id="ec_variant_type_mask"></span>**\_maschera di \_ tipo \_ variante EC**
</dt> <dd> <dl> <dt>

0x7F
</dt> <dt>



Utilizzato per mascherare il bit della matrice dalla proprietà **Type** di una [**\_ variante EC**](/windows/desktop/api/Evcoll/ns-evcoll-ec_variant) per estrarre il tipo del valore Variant.


</dt> </dl> </dd> <dt>

<span id="EC_VARIANT_TYPE_ARRAY"></span><span id="ec_variant_type_array"></span>**\_matrice di \_ tipi \_ Variant EC**
</dt> <dd> <dl> <dt>

128 (0x80)
</dt> <dt>



Quando questo bit viene impostato nella proprietà **Type** di una [**\_ variante EC**](/windows/desktop/api/Evcoll/ns-evcoll-ec_variant), la variante contiene un puntatore a una matrice di valori, anziché il valore stesso.


</dt> </dl> </dd> <dt>

<span id="EC_READ_ACCESS"></span><span id="ec_read_access"></span>**\_accesso in lettura EC \_**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Autorizzazione di controllo di accesso in lettura che consente di leggere le informazioni dall'agente di raccolta eventi.


</dt> </dl> </dd> <dt>

<span id="EC_WRITE_ACCESS"></span><span id="ec_write_access"></span>**\_accesso in scrittura EC \_**
</dt> <dd> <dl> <dt>

2
</dt> <dt>



Autorizzazione di controllo di accesso in scrittura che consente la scrittura di informazioni nell'agente di raccolta eventi.


</dt> </dl> </dd> <dt>

<span id="EC_OPEN_ALWAYS"></span><span id="ec_open_always"></span>**EC \_ aperto \_ sempre**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



Apre una sottoscrizione esistente o crea la sottoscrizione, se non esiste. Utilizzato dal metodo [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) .


</dt> </dl> </dd> <dt>

<span id="EC_CREATE_NEW"></span><span id="ec_create_new"></span>**EC \_ Crea \_ nuovo**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Flag passato alla funzione [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) che specifica che deve essere creata una nuova sottoscrizione.


</dt> </dl> </dd> <dt>

<span id="EC_OPEN_EXISTING"></span><span id="ec_open_existing"></span>**EC \_ aperto \_ esistente**
</dt> <dd> <dl> <dt>

2
</dt> <dt>



Flag passato alla funzione [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) che specifica che deve essere aperta una sottoscrizione esistente.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                            |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Evcoll. h</dt> </dl> |



 

 





