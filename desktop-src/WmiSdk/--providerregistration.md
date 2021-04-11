---
description: Funge da classe padre per le classi di registrazione per diversi tipi di provider.
ms.assetid: 1e5d95cb-0961-4be8-b80a-37b598c9ccfe
ms.tgt_platform: multiple
title: Classe __ProviderRegistration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ProviderRegistration
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 7359f3d5cdcfb2447b724fd6d369a1029d8fcd4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131771"
---
# <a name="__providerregistration-class"></a>\_\_Classe ProviderRegistration

La classe di sistema astratta **\_ \_ ProviderRegistration** funge da classe padre per le classi di registrazione per diversi tipi di provider.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[abstract]
class __ProviderRegistration : __SystemClass
{
  __Provider REF provider;
};
```

## <a name="members"></a>Members

La classe **\_ \_ ProviderRegistration** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **\_ \_ ProviderRegistration** dispone di queste proprietà.

<dl> <dt>

**provider**
</dt> <dd> <dl> <dt>

Tipo di dati: **\_ \_ provider**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Riferimento a un'istanza del [**\_ \_ provider**](--provider.md) che rappresenta il percorso dell'oggetto al provider.

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **\_ \_ ProviderRegistration** deriva da [**\_ \_ SystemClass**](--systemclass.md), che non dispone di proprietà.

Le istanze della classe di sistema **\_ \_ ProviderRegistration** non vengono mai create. Le classi utilizzate dai provider per creare istanze per la registrazione derivano direttamente o indirettamente da questa classe. Tali classi sono:

[**\_\_ClassProviderRegistration**](--classproviderregistration.md)

[**\_\_EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md)

[**\_\_EventProviderRegistration**](--eventproviderregistration.md)

[**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md)

[**\_\_MethodProviderRegistration**](--methodproviderregistration.md)

[**\_\_ObjectProviderRegistration**](--objectproviderregistration.md)

[**\_\_PropertyProviderRegistration**](--propertyproviderregistration.md)

Solo gli amministratori possono registrare o eliminare un provider creando un'istanza di [**\_ \_ Win32Provider**](--win32provider.md) e registrando tale provider.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |
| Spazio dei nomi<br/>                | Tutti gli spazi dei nomi WMI<br/>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_\_SystemClass**](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[Classi di sistema WMI](wmi-system-classes.md)
</dt> <dt>

[Registrazione di un provider](registering-a-provider.md)
</dt> </dl>

 

