---
description: Controlla quando viene scaricato un provider di classi o istanze.
ms.assetid: 4cbeb820-8a65-4fab-97f1-2a973b2a4310
ms.tgt_platform: multiple
title: Classe __ObjectProviderCacheControl
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ObjectProviderCacheControl
- Root.__ObjectProviderCacheControl.ClearAfter
api_type:
- Schema
api_location:
- Root
ms.openlocfilehash: 53cfaa69afead4f436879f128a4d42e50d36fe67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317583"
---
# <a name="__objectprovidercachecontrol-class"></a>\_\_Classe ObjectProviderCacheControl

La classe di sistema **\_ \_ ObjectProviderCacheControl** controlla quando viene scaricato un provider di classi o istanze. Si trova solo nello \\ spazio dei nomi radice.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[singleton]
class __ObjectProviderCacheControl : __CacheControl
{
  datetime ClearAfter;
};
```

## <a name="members"></a>Members

La classe **\_ \_ ObjectProviderCacheControl** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **\_ \_ ObjectProviderCacheControl** dispone di queste proprietà.

<dl> <dt>

**ClearAfter**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Intervallo di tempo dopo il quale WMI rilascia un'istanza, una classe o un provider di metodi. L'ora è in [Formato intervallo](interval-format.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **\_ \_ ObjectProviderCacheControl** deriva da [**\_ \_ CacheControl**](--cachecontrol.md). Per ulteriori informazioni sull'utilizzo di questa classe, vedere [scaricamento di un provider](unloading-a-provider.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |
| Spazio dei nomi<br/>                | Radice<br/>                |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_\_CacheControl**](/windows/desktop/WmiSdk/--cachecontrol)
</dt> <dt>

[Classi di sistema WMI](wmi-system-classes.md)
</dt> <dt>

[Ricezione di eventi in qualsiasi momento](receiving-events-at-all-times.md)
</dt> </dl>

 

