---
title: Tipo complesso BaseEapMethodUserCredentials
description: Informazioni sul tipo complesso BaseEapMethodUserCredentials. Questo tipo è un elemento segnaposto per i dati delle credenziali del metodo.
ms.assetid: ebbf813d-657a-4ff2-acf2-c18ce694b564
keywords:
- BaseEapMethodUserCredentials di tipo complesso EAPHost
topic_type:
- apiref
api_name:
- BaseEapMethodUserCredentials
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 37bc7a91a5d90cde6cba1af12bb0a4784ee21c7f
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730178"
---
# <a name="baseeapmethodusercredentials-complex-type"></a>Tipo complesso BaseEapMethodUserCredentials

Il tipo complesso **BaseEapMethodUserCredentials** è un elemento segnaposto per i dati delle credenziali del metodo.

``` syntax
<xs:complexType name="BaseEapMethodUserCredentials">
    <xs:sequence>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##any"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="remarks"></a>Commenti

Il metodo EAP esegue la convalida dello schema sul contenuto di **BaseEapMethodUserCredentials**.

## <a name="requirements"></a>Requisiti



| Ruolo | Versione minima del sistema operativo supportata |
|------|------------------------------|
| Client<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[EAPHost e schema legacy](eaphost-schemas.md)
</dt> <dt>

[Schema baseeapmethodusercredentials](baseeapmethodusercredentialsschema-schema.md)
</dt> </dl>

 

 





