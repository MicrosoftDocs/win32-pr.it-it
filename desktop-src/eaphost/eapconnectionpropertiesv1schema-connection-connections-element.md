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
ms.openlocfilehash: 5aabc29a7fe5122a7f7571750b97ebccb38158d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301770"
---
# <a name="connection-connections-element"></a>Elemento Connection (Connections)

L'elemento **Connection (Connections)** definisce ogni impostazione di configurazione e la associa a un nome. L'elemento **Connection** è facoltativo.

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

L'elemento **Connection** è definito dall'elemento [**Connections**](eapconnectionpropertiesv1schema-connections-element.md) .

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                 | Tipo   | Descrizione                                                                                                             |
|-------------------------------------------------------------------------|--------|-------------------------------------------------------------------------------------------------------------------------|
| [**EAP**](baseeapconnectionpropertiesv1schema-eap-element.md)          |        | Identifica l'elemento di configurazione EAP.<br/>                                                                    |
| [**Nome**](eapconnectionpropertiesv1schema-name-connection-element.md) | string | Acquisisce il nome della connessione da definire, per facilitare l'identificazione di più connessioni. <br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



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

 

 





