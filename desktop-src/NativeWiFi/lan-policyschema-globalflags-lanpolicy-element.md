---
description: Contiene le impostazioni globali per la configurazione automatica delle reti cablate.
ms.assetid: 172cf15c-cd51-43d4-ae5d-f9460c2a40e2
title: Elemento globalFlags (LANPolicy)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- globalFlags
api_type:
- Schema
api_location: ''
ms.openlocfilehash: bfbfecbc1d60e34a913bb523f5af8c2ab25665fd689976c87725d392f6ea26c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119801131"
---
# <a name="globalflags-lanpolicy-element"></a>Elemento globalFlags (LANPolicy)

L'elemento globalFlags (LANPolicy) contiene le impostazioni globali per la configurazione automatica delle reti cablate.

``` syntax
<xs:element name="globalFlags">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="enableAutoConfig"
                type="boolean"
             />
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

**L'elemento globalFlags** è definito dall'elemento [**LANPolicy.**](lan-policyschema-lanpolicy-element.md)

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                           | Tipo    | Descrizione                                                                                                                                                                          |
|-----------------------------------------------------------------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**enableAutoConfig**](lan-policyschema-enableautoconfig-globalflags-element.md) | boolean | Specifica se i computer usano il servizio di configurazione automatica incorporato per gestire le connessioni alle reti cablate che richiedono l'autenticazione di livello 2, ad esempio 802.1X.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**LANPolicy**](lan-policyschema-lanpolicy-element.md)
</dt> <dt>

**Possibile elemento padre immediato nell'istanza dello schema**
</dt> <dt>

[**LANPolicy**](lan-policyschema-lanpolicy-element.md)
</dt> </dl>

 

 




