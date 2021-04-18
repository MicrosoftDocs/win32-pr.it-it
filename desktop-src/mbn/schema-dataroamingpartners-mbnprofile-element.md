---
description: Specifica l'elenco dei provider di rete preferiti al momento del roaming.
ms.assetid: 5873fcd7-8e89-4edd-8dc5-f43675919c55
title: Elemento DataRoamingPartners (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DataRoamingPartners
api_type:
- Schema
ms.openlocfilehash: 7f721abd608dd241c399f16eee90369ebcf19594
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307541"
---
# <a name="dataroamingpartners-mbnprofile-element"></a>Elemento DataRoamingPartners (MBNProfile)

L'elemento **DataRoamingPartners (MBNProfile)** specifica l'elenco dei provider di rete preferiti al momento del roaming.

Il servizio Mobile Broadband usa questo elemento per selezionare la rete preferita da fornire durante il roaming.

L'elemento ha l'elemento figlio seguente che deve essere definito almeno una volta, ma può essere definito più volte.

-   [**Provider**](schema-provider-dataroamingpartners-element.md)

Questo elemento può avere un massimo di un'occorrenza.

Questo elemento è facoltativo.

``` syntax
<xs:element name="DataRoamingPartners">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="Provider"
                type="providerType"
                maxOccurs="unbounded"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

L'elemento **DataRoamingPartners** è definito dall'elemento [**MBNProfile**](schema-mbnprofile-element.md) .

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                         | Tipo                                                    | Descrizione                                            |
|-----------------------------------------------------------------|---------------------------------------------------------|--------------------------------------------------------|
| [**Provider**](schema-provider-dataroamingpartners-element.md) | [**providerType**](schema-providertype-complextype.md) | Nome e ID del provider di una rete cellulare.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 7 \[ \| UWP\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**MBNProfile**](schema-mbnprofile-element.md)
</dt> <dt>

**Possibile elemento padre immediato nell'istanza dello schema**
</dt> <dt>

[**MBNProfile**](schema-mbnprofile-element.md)
</dt> </dl>

 

 




