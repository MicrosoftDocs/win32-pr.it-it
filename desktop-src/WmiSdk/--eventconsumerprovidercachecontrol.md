---
description: Determina quando WMI deve rilasciare un provider di consumer di eventi.
ms.assetid: 93246826-8070-4e05-96f0-f773041ed1d4
ms.tgt_platform: multiple
title: Classe __EventConsumerProviderCacheControl
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventConsumerProviderCacheControl
- Root.__EventConsumerProviderCacheControl.ClearAfter
api_type:
- Schema
api_location:
- Root
ms.openlocfilehash: f769427c77f6efdf9a521a63f7334d5d27416c04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319324"
---
# <a name="__eventconsumerprovidercachecontrol-class"></a>\_\_Classe EventConsumerProviderCacheControl

La classe di sistema **\_ \_ EventConsumerProviderCacheControl** determina quando WMI deve rilasciare un provider di consumer di eventi. La classe **\_ \_ EventConsumerProviderCacheControl** è una classe singleton. Si trova solo nello \\ spazio dei nomi radice.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[singleton]
class __EventConsumerProviderCacheControl : CacheControl
{
  datetime ClearAfter;
};
```

## <a name="members"></a>Members

La classe **\_ \_ EventConsumerProviderCacheControl** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **\_ \_ EventConsumerProviderCacheControl** dispone di queste proprietà.

<dl> <dt>

**ClearAfter**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Intervallo di tempo dopo il quale WMI rilascia un provider di consumer di eventi. L'intervallo specificato per lo scaricamento del provider potrebbe richiedere fino al doppio. L'ora è in [Formato intervallo](interval-format.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **\_ \_ EventConsumerProviderCacheControl** deriva da [**\_ \_ CacheControl**](--cachecontrol.md). Per ulteriori informazioni sull'utilizzo di questa classe, vedere [scaricamento di un provider](unloading-a-provider.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |
| Spazio dei nomi<br/>                | Radice<br/>                |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Classi di sistema WMI](wmi-system-classes.md)
</dt> </dl>

 

 




