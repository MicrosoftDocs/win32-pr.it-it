---
title: Elemento Connections
description: Informazioni sull'elemento Connections. Questo elemento raccoglie e contiene zero o più elementi Connection.
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
ms.openlocfilehash: 62635d09030875a4f17deefa1aec05432df5662369eb483894f1a8cef4bbaf5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118498219"
---
# <a name="connections-element"></a>Elemento Connections

**L'elemento Connections** raccoglie e contiene zero o più [**elementi Connection.**](eapconnectionpropertiesv1schema-connection-connections-element.md)

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
| [**Eap**](baseeapconnectionpropertiesv1schema-eap-element.md)                       |        | Identifica l'elemento di configurazione EAP.<br/>                                                                                                                                       |
| [**Connessione**](eapconnectionpropertiesv1schema-connection-connections-element.md) |        | Definisce ogni impostazione di configurazione e la associa a un nome. [**L'elemento Connection**](eapconnectionpropertiesv1schema-connection-connections-element.md) è facoltativo.<br/> |
| [**Nome**](eapconnectionpropertiesv1schema-name-connection-element.md)              | string | Acquisisce il nome della connessione da definire, assistendo nell'identificazione di più connessioni.<br/>                                                                     |



## <a name="remarks"></a>Commenti

**L'elemento** Connections non viene usato con i metodi legacy tramite le API EAPHost.

## <a name="requirements"></a>Requisiti



| Ruolo | Versione minima supportata del sistema operativo |
|------|------------------------------|
| Client<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Schema EAPHost e legacy](eaphost-schemas.md)
</dt> <dt>

[Schema eapconnectionpropertiesv1](eapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





