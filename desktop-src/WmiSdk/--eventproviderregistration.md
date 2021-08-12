---
description: Usato per registrare i provider di eventi Windows Management Instrumentation (WMI).
ms.assetid: d87f61a8-5549-4f33-ba67-31b5d72b5282
ms.tgt_platform: multiple
title: __EventProviderRegistration classe
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
ms.openlocfilehash: ce973f05aec0a1c859598c558ef8c2cc637a8faec22fd1d7f2ad2aaf383bd201
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118557945"
---
# <a name="__eventproviderregistration-class"></a>\_\_Classe EventProviderRegistration

La **\_ \_ classe di sistema EventProviderRegistration** viene usata per registrare i provider di eventi Windows Management Instrumentation (WMI).

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class __EventProviderRegistration : __ProviderRegistration
{
  string         EventQueryList[];
  __Provider REF provider;
};
```

## <a name="members"></a>Members

La **\_ \_ classe EventProviderRegistration** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **\_ \_ classe EventProviderRegistration** ha queste proprietà.

<dl> <dt>

**EventQueryList**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Una o più Windows query WQL (Management Instrumentation Query Language) che descrivono gli eventi supportati dal provider di eventi.

</dd> <dt>

**Provider**
</dt> <dd> <dl> <dt>

Tipo di dati: **\_ \_ Provider**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percorso dell'oggetto al provider di eventi. Questa proprietà viene ereditata da [**\_ \_ ProviderRegistration**](--providerregistration.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

Solo gli amministratori possono registrare o eliminare un provider di eventi creando un'istanza di [**\_ \_ Win32Provider**](--win32provider.md) [**\_ \_ ed EventProviderRegistration**](--eventconsumerproviderregistration.md). La **\_ \_ classe EventProviderRegistration** è derivata da [**\_ \_ ProviderRegistration**](--providerregistration.md).

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

 

