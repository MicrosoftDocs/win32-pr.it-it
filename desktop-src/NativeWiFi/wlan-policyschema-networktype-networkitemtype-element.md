---
description: Specifica un tipo di rete.
ms.assetid: fe3044ab-6e93-48f8-b8cb-fdf984987232
title: Elemento networkType (networkItemType)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: c63b8afdaf699fde6871c198a8235772c59da1ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317114"
---
# <a name="networktype-networkitemtype-element"></a>Elemento networkType (networkItemType)

L'elemento networkType (networkItemType) specifica un tipo di rete. Esistono due tipi di reti: reti di infrastruttura (SSE) e reti ad hoc (IBSS).

``` syntax
<xs:element name="networkType"
    type="networkTypeType"
 />
```

L'elemento **networkType** è definito dal tipo complesso [**networkItemType**](wlan-policyschema-networkitemtype-complextype.md) .

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

 

 




