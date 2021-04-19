---
description: Utilizzato per determinare quando WMI rilascia un puntatore IWbemUnboundObjectSink per i provider di consumer di eventi.
ms.assetid: f7b14efc-a2f7-4e99-8ec8-5b5af0743139
ms.tgt_platform: multiple
title: Classe __EventSinkCacheControl
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
ms.openlocfilehash: 9d20e64fed1ee6ba5622d5e6a342a60485f53d36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317598"
---
# <a name="__eventsinkcachecontrol-class"></a>\_\_Classe EventSinkCacheControl

La classe di sistema **\_ \_ EventSinkCacheControl** viene utilizzata per determinare quando WMI rilascia un puntatore [**IWbemUnboundObjectSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemunboundobjectsink) del provider di consumer di eventi. La classe **\_ \_ EventSinkCacheControl** è una classe singleton. Si trova solo nello \\ spazio dei nomi radice.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[singleton]
class __EventSinkCacheControl : CacheControl
{
  datetime ClearAfter;
};
```

## <a name="members"></a>Members

La classe **\_ \_ EventSinkCacheControl** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **\_ \_ EventSinkCacheControl** dispone di queste proprietà.

<dl> <dt>

**ClearAfter**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Intervallo di tempo dopo il quale WMI rilascia un provider di eventi. L'intervallo specificato per scaricare il provider può richiedere fino a due volte. L'ora è in [Formato intervallo](interval-format.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **\_ \_ EventSinkCacheControl** deriva da [**\_ \_ CacheControl**](--cachecontrol.md). Per ulteriori informazioni sull'utilizzo di questa classe, vedere [scaricamento di un provider](unloading-a-provider.md).

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

 

 




