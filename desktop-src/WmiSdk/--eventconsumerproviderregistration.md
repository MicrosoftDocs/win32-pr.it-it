---
description: Registra i provider di consumer di eventi con WMI.
ms.assetid: 31ff43dc-dc70-4ba0-866f-37445912f837
ms.tgt_platform: multiple
title: Classe __EventConsumerProviderRegistration
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
ms.openlocfilehash: 38552519221018735c3c7543d9a1f3f2d4b680e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884001"
---
# <a name="__eventconsumerproviderregistration-class"></a>\_\_Classe EventConsumerProviderRegistration

La classe di sistema **\_ \_ EventConsumerProviderRegistration** registra i provider di consumer di eventi con WMI.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class __EventConsumerProviderRegistration : __ProviderRegistration
{
  string         ConsumerClassNames[];
  __Provider REF provider;
};
```

## <a name="members"></a>Members

La classe **\_ \_ EventConsumerProviderRegistration** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **\_ \_ EventConsumerProviderRegistration** dispone di queste proprietà.

<dl> <dt>

**ConsumerClassNames**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Matrice di nomi delle classi di consumer logiche supportate dal provider di consumer di eventi.

</dd> <dt>

**provider**
</dt> <dd> <dl> <dt>

Tipo di dati: **\_ \_ provider**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percorso dell'oggetto per il provider. Questa proprietà viene ereditata da [**\_ \_ ProviderRegistration**](--providerregistration.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **\_ \_ EventConsumerProviderRegistration** deriva da [**\_ \_ ProviderRegistration**](--providerregistration.md).

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

 

