---
title: Windows Costanti dell'agente di raccolta eventi (Evcoll.h)
description: Il Windows Event Collector SDK contiene le costanti seguenti.
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
ms.openlocfilehash: 8d168ecb16c293c524c4dffcb16aee7db2924e23219e42d402939ab26b4bbecf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120005981"
---
# <a name="windows-event-collector-constants"></a>Windows Costanti dell'agente di raccolta eventi

Il Windows Event Collector SDK contiene le costanti seguenti.

<dl> <dt>

<span id="EC_VARIANT_TYPE_MASK"></span><span id="ec_variant_type_mask"></span>**EC \_ VARIANT \_ TYPE \_ MASK**
</dt> <dd> <dl> <dt>

0x7f
</dt> <dt>



Usato per mascherare il bit di matrice dalla **proprietà Type** di un elemento [**EC \_ VARIANT**](/windows/desktop/api/Evcoll/ns-evcoll-ec_variant) per estrarre il tipo del valore variant.


</dt> </dl> </dd> <dt>

<span id="EC_VARIANT_TYPE_ARRAY"></span><span id="ec_variant_type_array"></span>**EC \_ VARIANT \_ TYPE \_ ARRAY**
</dt> <dd> <dl> <dt>

128 (0x80)
</dt> <dt>



Quando questo bit è impostato nella proprietà **Type** di [**un'istruzione EC \_ VARIANT,**](/windows/desktop/api/Evcoll/ns-evcoll-ec_variant)la variante contiene un puntatore a una matrice di valori, anziché il valore stesso.


</dt> </dl> </dd> <dt>

<span id="EC_READ_ACCESS"></span><span id="ec_read_access"></span>**EC \_ READ \_ ACCESS**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Autorizzazione di controllo di accesso in lettura che consente la lettura delle informazioni dall'agente di raccolta eventi.


</dt> </dl> </dd> <dt>

<span id="EC_WRITE_ACCESS"></span><span id="ec_write_access"></span>**EC \_ WRITE \_ ACCESS**
</dt> <dd> <dl> <dt>

2
</dt> <dt>



Autorizzazione di controllo di accesso in scrittura che consente di scrivere informazioni nell'agente di raccolta eventi.


</dt> </dl> </dd> <dt>

<span id="EC_OPEN_ALWAYS"></span><span id="ec_open_always"></span>**EC \_ OPEN \_ ALWAYS**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



Apre una sottoscrizione esistente o crea la sottoscrizione se non esiste. Usato dal [**metodo EcOpenSubscription.**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription)


</dt> </dl> </dd> <dt>

<span id="EC_CREATE_NEW"></span><span id="ec_create_new"></span>**EC \_ CREATE \_ NEW**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Flag passato alla funzione [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) che specifica che deve essere creata una nuova sottoscrizione.


</dt> </dl> </dd> <dt>

<span id="EC_OPEN_EXISTING"></span><span id="ec_open_existing"></span>**EC \_ OPEN \_ EXISTING**
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
| Intestazione<br/>                   | <dl> <dt>Evcoll.h</dt> </dl> |



 

 





