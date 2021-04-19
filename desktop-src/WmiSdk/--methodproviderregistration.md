---
description: Registra i provider di metodi con WMI.
ms.assetid: c5a8ccd3-487e-42a3-bb31-d27da9a711c4
ms.tgt_platform: multiple
title: Classe __MethodProviderRegistration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __MethodProviderRegistration
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: dd59a88c9c0ff7b4b6726b58ce69f879eb3893ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317591"
---
# <a name="__methodproviderregistration-class"></a>\_\_Classe MethodProviderRegistration

La classe di sistema **\_ \_ MethodProviderRegistration** registra i provider di metodi con WMI.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class __MethodProviderRegistration : __ProviderRegistration
{
  __Provider REF provider;
};
```

## <a name="members"></a>Members

La classe **\_ \_ MethodProviderRegistration** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **\_ \_ MethodProviderRegistration** dispone di queste proprietà.

<dl> <dt>

**provider**
</dt> <dd> <dl> <dt>

Tipo di dati: **\_ \_ provider**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Riferimento a un'istanza del [**\_ \_ provider**](--provider.md) che rappresenta il percorso dell'oggetto del provider di metodi. Questa proprietà viene ereditata da [**\_ \_ ProviderRegistration**](--providerregistration.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **\_ \_ MethodProviderRegistration** deriva da [**\_ \_ ProviderRegistration**](--providerregistration.md). Solo gli amministratori possono registrare o eliminare un provider di metodi creando un'istanza di [**\_ \_ Win32Provider**](--win32provider.md) e **\_ \_ MethodProviderRegistration**.

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

[Registrazione di un provider di metodi](registering-a-method-provider.md)
</dt> </dl>

 

