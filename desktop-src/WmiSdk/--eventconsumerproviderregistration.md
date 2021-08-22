---
description: Registra i provider di consumer di eventi con WMI.
ms.assetid: 31ff43dc-dc70-4ba0-866f-37445912f837
ms.tgt_platform: multiple
title: __EventConsumerProviderRegistration classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventConsumerProviderRegistration
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: bc3acec16b92c375f07836318be0e77c335862aec826c80bb77815865a337a72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118557935"
---
# <a name="__eventconsumerproviderregistration-class"></a>\_\_Classe EventConsumerProviderRegistration

La **\_ \_ classe di sistema EventConsumerProviderRegistration** registra i provider di consumer di eventi con WMI.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class __EventConsumerProviderRegistration : __ProviderRegistration
{
  string         ConsumerClassNames[];
  __Provider REF provider;
};
```

## <a name="members"></a>Members

La **\_ \_ classe EventConsumerProviderRegistration** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **\_ \_ classe EventConsumerProviderRegistration** ha queste proprietà.

<dl> <dt>

**ConsumerClassNames**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Matrice di nomi delle classi consumer logiche supportate dal provider di consumer di eventi.

</dd> <dt>

**Provider**
</dt> <dd> <dl> <dt>

Tipo di dati: **\_ \_ Provider**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percorso dell'oggetto del provider. Questa proprietà viene ereditata da [**\_ \_ ProviderRegistration.**](--providerregistration.md)

</dd> </dl>

## <a name="remarks"></a>Commenti

La **\_ \_ classe EventConsumerProviderRegistration** è derivata da [**\_ \_ ProviderRegistration.**](--providerregistration.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |
| Spazio dei nomi<br/>                | Tutti gli spazi dei nomi WMI<br/>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_\_ProviderRegistration**](/windows/desktop/WmiSdk/--providerregistration)
</dt> <dt>

[Classi di sistema WMI](wmi-system-classes.md)
</dt> <dt>

[Registrazione di un provider di consumer di eventi](registering-an-event-consumer-provider.md)
</dt> <dt>

[Scrittura di un provider di consumer di eventi](writing-an-event-consumer-provider.md)
</dt> </dl>

 

