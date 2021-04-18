---
title: Connections-elemento
description: Informazioni sull'elemento Connections. Questo elemento raccoglie e contiene zero o più elementi di connessione.
ms.assetid: 2c199338-892f-4d8c-bf33-4a19f362de3e
keywords:
- Elemento Connections EAPHost
topic_type:
- apiref
api_name:
- Connections
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6cdb23c9f1a6130e2fe77061286e8a0657c3e2f5
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300465"
---
# <a name="connections-element"></a>Connections-elemento

L'elemento **Connections** raccoglie e contiene zero o più elementi [**Connection**](eapconnectionpropertiesv1schema-connection-connections-element.md) .

``` syntax
<xs:element name="Connections">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="Connection"
                minOccurs="0"
                maxOccurs="unbounded"
            >
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
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                              | Tipo   | Descrizione                                                                                                                                                                                |
|--------------------------------------------------------------------------------------|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EAP**](baseeapconnectionpropertiesv1schema-eap-element.md)                       |        | Identifica l'elemento di configurazione EAP.<br/>                                                                                                                                       |
| [**Connessioni**](eapconnectionpropertiesv1schema-connection-connections-element.md) |        | Definisce ogni impostazione di configurazione e la associa a un nome. L'elemento [**Connection**](eapconnectionpropertiesv1schema-connection-connections-element.md) è facoltativo.<br/> |
| [**Nome**](eapconnectionpropertiesv1schema-name-connection-element.md)              | string | Acquisisce il nome della connessione da definire, per facilitare l'identificazione di più connessioni.<br/>                                                                     |



## <a name="remarks"></a>Commenti

L'elemento **Connections** non viene usato con i metodi legacy tramite le API EAPHost.

## <a name="requirements"></a>Requisiti



| Ruolo | Versione minima del sistema operativo supportata |
|------|------------------------------|
| Client<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[EAPHost e schema legacy](eaphost-schemas.md)
</dt> <dt>

[Schema eapconnectionpropertiesv1](eapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





