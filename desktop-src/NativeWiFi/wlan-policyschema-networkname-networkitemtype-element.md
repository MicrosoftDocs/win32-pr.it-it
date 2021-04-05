---
description: Specifica l'identificatore del set di servizi (SSID) di una rete wireless.
ms.assetid: 103808f2-9e5f-4605-b42a-337a13455294
title: Elemento NetworkName (networkItemType)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkName
api_type:
- Schema
api_location: ''
ms.openlocfilehash: da635c392a29419e7b151cc2c4fb080ff7d3fca9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884553"
---
# <a name="networkname-networkitemtype-element"></a>Elemento NetworkName (networkItemType)

L'elemento NetworkName (networkItemType) specifica l'identificatore del set di servizi (SSID) di una rete wireless.

``` syntax
<xs:element name="networkName"
    type="networkNameType"
 />
```

L'elemento **NetworkName** è definito dal tipo complesso [**networkItemType**](wlan-policyschema-networkitemtype-complextype.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**networkItemType**](wlan-policyschema-networkitemtype-complextype.md)
</dt> <dt>

**Possibili elementi padre immediati nell'istanza dello schema**
</dt> <dt>

[**rete (Consenti)**](wlan-policyschema-network-allowlist-element.md)
</dt> <dt>

[**rete (blocco)**](wlan-policyschema-network-blocklist-element.md)
</dt> </dl>

 

 




