---
description: Identifica il nome del provider Home per la SIM o il dispositivo specificato.
ms.assetid: 05d65091-5a1d-427a-8f51-1e1b9d189571
title: Elemento HomeProviderName (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HomeProviderName
api_type:
- Schema
ms.openlocfilehash: 1868be18dc7acf9d5146f987658feb006714fbcc3db35883007afd01c308609e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035829"
---
# <a name="homeprovidername-mbnprofile-element"></a>Elemento HomeProviderName (MBNProfile)

**L'elemento HomeProviderName (MBNProfile)** identifica il nome del provider Home per la SIM o il dispositivo specificato.

Questo elemento è facoltativo e viene impostato dal servizio Mobile Broadband per uso interno. Un'applicazione non deve impostare questo campo durante la creazione o l'aggiornamento di un profilo.

``` syntax
<xs:element name="HomeProviderName"
    type="providerNameType"
 />
```

**L'elemento HomeProviderName** è definito dall'elemento [**MBNProfile.**](schema-mbnprofile-element.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop app \| UWP\]<br/> |
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

 

 




