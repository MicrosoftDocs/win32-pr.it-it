---
description: Specifica l'ID del provider della rete cellulare.
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
ms.openlocfilehash: 750e6c3f4397f710bb1ccbcea0286be68a89e145
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226191"
---
# <a name="providerid-providertype-element"></a>Elemento ProviderID (providerType)

L'elemento **ProviderID (ProviderType)** specifica l'ID del provider della rete cellulare.

L'elemento è una sequenza di cifre con un massimo di 6 cifre.

Questo elemento è obbligatorio nell'elemento [**provider**](schema-provider-dataroamingpartners-element.md) .

``` syntax
<xs:element name="ProviderID"
    type="providerType"
 />
```

L'elemento **ProviderID** è definito dal tipo complesso [**ProviderType**](schema-providertype-complextype.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 7 \[ \| UWP\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**providerType**](schema-providertype-complextype.md)
</dt> <dt>

**Possibile elemento padre immediato nell'istanza dello schema**
</dt> <dt>

[**Provider (DataRoamingPartners)**](schema-provider-dataroamingpartners-element.md)
</dt> </dl>

 

 




