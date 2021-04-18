---
description: Utilizzato per registrare i provider di eventi con Strumentazione gestione Windows (WMI).
ms.assetid: d87f61a8-5549-4f33-ba67-31b5d72b5282
ms.tgt_platform: multiple
title: Classe __EventProviderRegistration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventProviderRegistration
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: caaad1b4ab03cfc1b43e4239b9144d3ceeade82f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314606"
---
# <a name="__eventproviderregistration-class"></a>\_\_Classe EventProviderRegistration

La classe di sistema **\_ \_ EventProviderRegistration** viene utilizzata per registrare i provider di eventi con Strumentazione gestione Windows (WMI).

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class __EventProviderRegistration : __ProviderRegistration
{
  string         EventQueryList[];
  __Provider REF provider;
};
```

## <a name="members"></a>Members

La classe **\_ \_ EventProviderRegistration** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **\_ \_ EventProviderRegistration** dispone di queste proprietà.

<dl> <dt>

**EventQueryList**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Una o più query WQL (Strumentazione gestione Windows Query Language) che descrivono gli eventi supportati dal provider di eventi.

</dd> <dt>

**provider**
</dt> <dd> <dl> <dt>

Tipo di dati: **\_ \_ provider**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percorso dell'oggetto per il provider di eventi. Questa proprietà viene ereditata da [**\_ \_ ProviderRegistration**](--providerregistration.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

Solo gli amministratori possono registrare o eliminare un provider di eventi creando un'istanza di [**\_ \_ Win32Provider**](--win32provider.md) e [**\_ \_ EventProviderRegistration**](--eventconsumerproviderregistration.md). La classe **\_ \_ EventProviderRegistration** deriva da [**\_ \_ ProviderRegistration**](--providerregistration.md).

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

[Registrazione di un provider di eventi](registering-an-event-provider.md)
</dt> <dt>

[Scrittura di un provider di eventi](writing-an-event-provider.md)
</dt> </dl>

 

