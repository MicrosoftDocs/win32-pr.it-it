---
title: Elemento EAP (proprietà User)
description: Informazioni sull'elemento EAP. Questo elemento acquisisce il tipo di metodo selezionato e la configurazione specifica del metodo. | Elemento EAP (proprietà User)
ms.assetid: 4adef133-1d18-444a-baa3-5419b8cbe298
keywords:
- EAPHost (elemento EAP)
topic_type:
- apiref
api_name:
- Eap
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 23f00b5162ddb42efd9fae759bab1ea47efc04dc
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321690"
---
# <a name="eap-element-user-property"></a>Elemento EAP (proprietà User)

L'elemento **EAP** acquisisce il tipo di metodo selezionato e la configurazione specifica del metodo.

``` syntax
<xs:element name="Eap"
    type="BaseEapParameters"
 />
```

## <a name="remarks"></a>Commenti

Il metodo può definire gli elementi costitutivi all'interno dell'elemento **EAP** . Il metodo esegue inoltre la convalida dello schema sugli elementi in **EAP**.

## <a name="requirements"></a>Requisiti



| Ruolo | Versione minima del sistema operativo supportata |
|------|------------------------------|
| Client<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[EAPHost e schema legacy](eaphost-schemas.md)
</dt> <dt>

[Schema baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





