---
description: Specifica il nome e il tipo di una rete wireless.
ms.assetid: 839afae0-b8e1-489f-8811-19a82c173627
title: Tipo complesso networkItemType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkItemType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 5db7c5fc4d9b5227d9cd29c5e2dfc69da6fad139
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317119"
---
# <a name="networkitemtype-complex-type"></a>Tipo complesso networkItemType

Il tipo complesso networkItemType specifica il nome e il tipo di una rete wireless.

``` syntax
<xs:complexType name="networkItemType">
    <xs:sequence>
        <xs:element name="networkName"
            type="networkNameType"
         />
        <xs:element name="networkType"
            type="networkTypeType"
         />
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                      | Tipo                                                                    | Descrizione                                                   |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------|---------------------------------------------------------------|
| [**networkName**](wlan-policyschema-networkname-networkitemtype-element.md) | [**networkNameType**](wlan-policyschema-networknametype-simpletype.md) | Identificatore del set di servizi (SSID) della rete. <br/> |
| [**networkType**](wlan-policyschema-networktype-networkitemtype-element.md) | [**networkTypeType**](wlan-policyschema-networktypetype-simpletype.md) | Tipo di rete. <br/>                                 |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 




