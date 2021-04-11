---
description: Identifica il nome e l'ID del provider per una rete cellulare.
ms.assetid: 007ecad9-23a3-4352-b3e2-c22d0f3f449d
title: Elemento provider (DataRoamingPartners)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Provider
api_type:
- Schema
ms.openlocfilehash: b5b36c973bf44175b90e25fd2a141fed3624d8b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129010"
---
# <a name="provider-dataroamingpartners-element"></a>Elemento provider (DataRoamingPartners)

L'elemento **provider (DataRoamingPartners)** identifica il nome e l'ID provider per una rete cellulare.

Questo elemento ha gli elementi figlio seguenti.

-   [**ProviderID**](schema-providerid-providertype-element.md)
-   [**ProviderName**](schema-providername-providertype-element.md)

Questo elemento può essere definito più volte all'interno dell'elemento [**DataRoamingPartners**](schema-dataroamingpartners-mbnprofile-element.md) . Deve essere definito almeno una volta.

``` syntax
<xs:element name="Provider"
    type="providerType"
 />
```

L'elemento **provider** è definito dall'elemento [**DataRoamingPartners**](schema-dataroamingpartners-mbnprofile-element.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 7 \[ \| UWP\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**DataRoamingPartners**](schema-dataroamingpartners-mbnprofile-element.md)
</dt> <dt>

**Possibile elemento padre immediato nell'istanza dello schema**
</dt> <dt>

[**DataRoamingPartners (MBNProfile)**](schema-dataroamingpartners-mbnprofile-element.md)
</dt> </dl>

 

 




