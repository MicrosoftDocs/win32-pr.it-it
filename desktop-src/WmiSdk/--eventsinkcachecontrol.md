---
description: Utilizzato per determinare quando WMI rilascia un puntatore IWbemUnboundObjectSink dei provider di consumer di eventi.
ms.assetid: f7b14efc-a2f7-4e99-8ec8-5b5af0743139
ms.tgt_platform: multiple
title: __EventSinkCacheControl classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventSinkCacheControl
- Root.__EventSinkCacheControl.ClearAfter
api_type:
- Schema
api_location:
- Root
ms.openlocfilehash: dc73e2cb740486ad08172c10233f4865709a87d9f1122f399002133687744094
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118557915"
---
# <a name="__eventsinkcachecontrol-class"></a>\_\_Classe EventSinkCacheControl

La **\_ \_ classe di sistema EventSinkCacheControl** viene usata per determinare quando WMI rilascia il puntatore [**IWbemUnboundObjectSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemunboundobjectsink) di un provider di consumer di eventi. La **\_ \_ classe EventSinkCacheControl** è una classe singleton. Si trova solo nello spazio dei \\ nomi radice.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[singleton]
class __EventSinkCacheControl : CacheControl
{
  datetime ClearAfter;
};
```

## <a name="members"></a>Members

La **\_ \_ classe EventSinkCacheControl** include i tipi di membri seguenti:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **\_ \_ classe EventSinkCacheControl** ha queste proprietà.

<dl> <dt>

**ClearAfter**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Intervallo di tempo dopo il quale WMI rilascia un provider di eventi. Lo scaricamento del provider può richiedere fino al doppio dell'intervallo specificato. L'ora è nel [formato intervallo](interval-format.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

La **\_ \_ classe EventSinkCacheControl** è derivata da [**\_ \_ CacheControl.**](--cachecontrol.md) Per altre informazioni sull'uso di questa classe, vedere [Scaricamento di un provider.](unloading-a-provider.md)

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

 

 




