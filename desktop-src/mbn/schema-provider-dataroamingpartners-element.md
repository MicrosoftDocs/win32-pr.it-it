---
description: Identifica il nome e l'ID provider per una rete cellulare.
ms.assetid: 007ecad9-23a3-4352-b3e2-c22d0f3f449d
title: Elemento Provider (DataRoamingPartners)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Provider
api_type:
- Schema
ms.openlocfilehash: d5ce12ddf15ad57071f2717e5801fbd05f8e2925ea474345f7c376bc2445cd02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119347161"
---
# <a name="provider-dataroamingpartners-element"></a>Elemento Provider (DataRoamingPartners)

**L'elemento Provider (DataRoamingPartners)** identifica il nome e l'ID provider per una rete cellulare.

Questo elemento dispone degli elementi figlio seguenti.

-   [**ProviderID**](schema-providerid-providertype-element.md)
-   [**ProviderName**](schema-providername-providertype-element.md)

Questo elemento può essere definito più volte all'interno [**dell'elemento DataRoamingPartners.**](schema-dataroamingpartners-mbnprofile-element.md) Deve essere definito almeno una volta.

``` syntax
<xs:element name="Provider"
    type="providerType"
 />
```

**L'elemento Provider** è definito [**dall'elemento DataRoamingPartners.**](schema-dataroamingpartners-mbnprofile-element.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop app \| UWP\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**DataRoamingPartners**](schema-dataroamingpartners-mbnprofile-element.md)
</dt> <dt>

**Possibile elemento padre diretto nell'istanza dello schema**
</dt> <dt>

[**DataRoamingPartners (MBNProfile)**](schema-dataroamingpartners-mbnprofile-element.md)
</dt> </dl>

 

 




