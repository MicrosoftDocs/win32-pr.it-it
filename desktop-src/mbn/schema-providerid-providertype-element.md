---
description: Specifica l'ID provider della rete cellulare.
ms.assetid: 5528dfec-eb1b-4af3-8d7d-03b458e5ae75
title: Elemento ProviderID (providerType)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ProviderID
api_type:
- Schema
ms.openlocfilehash: b40ac5abab2abf850d927c21f0de66ad419987f594f28dffcd380ead7f982d63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959791"
---
# <a name="providerid-providertype-element"></a>Elemento ProviderID (providerType)

**L'elemento ProviderID (providerType)** specifica l'ID provider della rete cellulare.

L'elemento è una sequenza di cifre con un massimo di 6 cifre.

Questo elemento è obbligatorio all'interno [**dell'elemento Provider.**](schema-provider-dataroamingpartners-element.md)

``` syntax
<xs:element name="ProviderID"
    type="providerType"
 />
```

**L'elemento ProviderID** è definito dal [**tipo complesso providerType.**](schema-providertype-complextype.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop \| app UWP\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**Providertype**](schema-providertype-complextype.md)
</dt> <dt>

**Possibile elemento padre immediato nell'istanza dello schema**
</dt> <dt>

[**Provider (DataRoamingPartners)**](schema-provider-dataroamingpartners-element.md)
</dt> </dl>

 

 




