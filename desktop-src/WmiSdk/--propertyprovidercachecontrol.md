---
description: Controlla la cache quando viene scaricato un provider di proprietà.
ms.assetid: 8fc7de7a-889c-4d53-97ea-a676879de1d3
ms.tgt_platform: multiple
title: Classe __PropertyProviderCacheControl
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __PropertyProviderCacheControl
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 1d153049a9635b4b77a1ad09ca0ee64835b9bcfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231828"
---
# <a name="__propertyprovidercachecontrol-class"></a>\_\_Classe PropertyProviderCacheControl

La classe **\_ \_ PropertyProviderCacheControl** controlla la cache quando viene scaricato un provider di proprietà. Questa classe esiste solo nello \\ spazio dei nomi radice.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class __PropertyProviderCacheControl
{
  datetime ClearAfter;
};
```

## <a name="members"></a>Members

La classe **\_ \_ PropertyProviderCacheControl** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **\_ \_ PropertyProviderCacheControl** dispone di queste proprietà.

<dl> <dt>

**ClearAfter**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Intervallo di tempo dopo il rilascio di un provider di proprietà da WMI. L'ora è nel formato intervallo.

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **\_ \_ PropertyProviderCacheControl** deriva da [**\_ \_ CacheControl**](--cachecontrol.md). Per ulteriori informazioni, vedere [scaricamento di un provider](unloading-a-provider.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |
| Spazio dei nomi<br/>                | Tutti gli spazi dei nomi WMI<br/>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Classi di sistema WMI](wmi-system-classes.md)
</dt> </dl>

 

 




