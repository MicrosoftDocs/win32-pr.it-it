---
title: Tipo complesso BaseEapMethodUserCredentials
description: Informazioni sul tipo complesso BaseEapMethodUserCredentials. Questo tipo è un elemento segnaposto per i dati delle credenziali del metodo.
ms.assetid: ebbf813d-657a-4ff2-acf2-c18ce694b564
keywords:
- Tipo complesso BaseEapMethodUserCredentials EAPHost
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
ms.openlocfilehash: 8102f095ca7d4b1ada6db3c21fbe55e73a98ed6d06d2d6b99032f1a21a344527
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120094421"
---
# <a name="baseeapmethodusercredentials-complex-type"></a>Tipo complesso BaseEapMethodUserCredentials

Il **tipo complesso BaseEapMethodUserCredentials** è un elemento segnaposto per i dati delle credenziali del metodo.

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

Il metodo EAP esegue la convalida dello schema sul contenuto di **BaseEapMethodUserCredentials.**

## <a name="requirements"></a>Requisiti



| Ruolo | Versione minima supportata del sistema operativo |
|------|------------------------------|
| Client<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[EAPHost e schema legacy](eaphost-schemas.md)
</dt> <dt>

[Schema baseeapmethodusercredentials](baseeapmethodusercredentialsschema-schema.md)
</dt> </dl>

 

 





