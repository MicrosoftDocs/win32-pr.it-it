---
description: Controlla la cache quando viene scaricato un provider di proprietà.
ms.assetid: 8fc7de7a-889c-4d53-97ea-a676879de1d3
ms.tgt_platform: multiple
title: __PropertyProviderCacheControl classe
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
ms.openlocfilehash: 33edad107859328e9a81a6c77c3c02e29e2ee3aebbbe411ee20fb438e51517a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118110539"
---
# <a name="__propertyprovidercachecontrol-class"></a>\_\_Classe PropertyProviderCacheControl

La **\_ \_ classe PropertyProviderCacheControl** controlla la cache quando viene scaricato un provider di proprietà. Questa classe esiste solo nello spazio dei \\ nomi radice.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class __PropertyProviderCacheControl
{
  datetime ClearAfter;
};
```

## <a name="members"></a>Members

La **\_ \_ classe PropertyProviderCacheControl** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **\_ \_ classe PropertyProviderCacheControl** ha queste proprietà.

<dl> <dt>

**ClearAfter**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Intervallo di tempo dopo il rilascio di un provider di proprietà da parte di WMI. L'ora è nel formato intervallo.

</dd> </dl>

## <a name="remarks"></a>Commenti

La **\_ \_ classe PropertyProviderCacheControl** è derivata da [**\_ \_ CacheControl.**](--cachecontrol.md) Per altre informazioni, vedere [Scaricamento di un provider.](unloading-a-provider.md)

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

 

 




