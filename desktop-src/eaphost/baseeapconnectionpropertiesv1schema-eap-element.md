---
title: Elemento EAP (proprietà di connessione)
description: Informazioni sull'elemento EAP. Questo elemento acquisisce il tipo di metodo selezionato e la configurazione specifica del metodo. | Elemento EAP (proprietà di connessione)
ms.assetid: 4e9f3869-257e-4b03-93f6-2eec94eaacee
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
ms.openlocfilehash: c39812d00ecf9a1183eb81fc03b09b146d751f0e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321336"
---
# <a name="eap-element-connection-properties"></a>Elemento EAP (proprietà di connessione)

L'elemento **EAP** acquisisce il tipo di metodo selezionato e la configurazione specifica del metodo.

``` syntax
<xs:element name="Eap
          
        "
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

[Schema baseeapconnectionpropertiesv1](baseeapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





