---
description: Classe è la classe base astratta per le classi utilizzate per determinare quando WMI deve rilasciare un oggetto Component Object Model (COM).
ms.assetid: 32631610-8c0e-4f04-b0b2-62e5f8e23ef4
ms.tgt_platform: multiple
title: Classe __CacheControl
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __CacheControl
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: fe5358630a7ac5eb48751135d39c2fd998196bf7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314097"
---
# <a name="__cachecontrol-class"></a>\_\_Classe CacheControl

La classe di sistema **\_ \_ CacheControl** è la classe di base astratta per le classi utilizzate per determinare quando WMI deve rilasciare un oggetto Component Object Model (com). Le istanze di questa classe non vengono mai create. La classe **\_ \_ CacheControl** si trova solo nello spazio dei nomi radice. Per ulteriori informazioni sull'utilizzo di questa classe, vedere [scaricamento di un provider](unloading-a-provider.md).

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[abstract]
class __CacheControl : __SystemClass
{
};
```

## <a name="members"></a>Members

La classe **\_ \_ CacheControl** non definisce membri.

## <a name="remarks"></a>Commenti

La classe **\_ \_ CacheControl** deriva da [**\_ \_ SystemClass**](--systemclass.md).

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

[**\_\_EventConsumerProviderCacheControl**](--eventconsumerprovidercachecontrol.md)
</dt> <dt>

[**\_\_EventProviderCacheControl**](--eventprovidercachecontrol.md)
</dt> <dt>

[**\_\_EventSinkCacheControl**](--eventsinkcachecontrol.md)
</dt> <dt>

[**\_\_ObjectProviderCacheControl**](--objectprovidercachecontrol.md)
</dt> <dt>

[\_\_PropertyProviderCacheControl](--propertyprovidercachecontrol.md)
</dt> <dt>

[Scaricamento di un provider](unloading-a-provider.md)
</dt> </dl>

 

