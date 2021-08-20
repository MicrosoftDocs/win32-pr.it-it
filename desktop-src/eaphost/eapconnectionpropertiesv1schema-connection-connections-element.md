---
title: Elemento Connection (Connections)
description: Definisce ogni impostazione di configurazione e la associa a un nome. L'elemento Connection è facoltativo.
ms.assetid: 913263ab-0e0e-4213-947b-7bca9ba0697e
keywords:
- Elemento Connection EAPHost
topic_type:
- apiref
api_name:
- Connection
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6948675f7910c46cb2b5db4285ce0df795fa057f275ce29b7f4c664b14c4ce1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118498371"
---
# <a name="connection-connections-element"></a>Elemento Connection (Connections)

**L'elemento Connection (Connections)** definisce ogni impostazione di configurazione e la associa a un nome. **L'elemento Connection** è facoltativo.

``` syntax
<xs:element name="Connection">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="Name"
                type="string"
             />
            <xs:element
                maxOccurs="unbounded"
                ref="Eap"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

**L'elemento Connection** è definito dall'elemento [**Connections.**](eapconnectionpropertiesv1schema-connections-element.md)

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                 | Tipo   | Descrizione                                                                                                             |
|-------------------------------------------------------------------------|--------|-------------------------------------------------------------------------------------------------------------------------|
| [**Eap**](baseeapconnectionpropertiesv1schema-eap-element.md)          |        | Identifica l'elemento di configurazione EAP.<br/>                                                                    |
| [**Nome**](eapconnectionpropertiesv1schema-name-connection-element.md) | string | Acquisisce il nome della connessione definita, assistendo nell'identificazione di più connessioni. <br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**Connessioni**](eapconnectionpropertiesv1schema-connections-element.md)
</dt> <dt>

**Possibile elemento padre immediato nell'istanza dello schema**
</dt> <dt>

[**Connessioni**](eapconnectionpropertiesv1schema-connections-element.md)
</dt> <dt>

[EAPHost e schema legacy](eaphost-schemas.md)
</dt> <dt>

[Schema eapconnectionpropertiesv1](eapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





