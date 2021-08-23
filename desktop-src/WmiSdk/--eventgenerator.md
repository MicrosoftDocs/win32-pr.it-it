---
description: Funge da classe padre per le classi che controllano la generazione di eventi, ad esempio gli eventi timer.
ms.assetid: 381b06e7-2857-4932-9f52-f1d62efa8b79
ms.tgt_platform: multiple
title: __EventGenerator classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventGenerator
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 0033bef55915865ba1945c9f17705ed40cd0d3db4cd572efd13cdadf99d4bbab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119732903"
---
# <a name="__eventgenerator-class"></a>\_\_Classe EventGenerator

La **\_ \_ classe di sistema EventGenerator** è una classe di base astratta che funge da classe padre per le classi che controllano la generazione di eventi, ad esempio gli [eventi timer.](receiving-a-timed-or-repeating-event.md)

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[abstract]
class __EventGenerator : __IndicationRelated
{
};
```

## <a name="members"></a>Members

La **\_ \_ classe EventGenerator** non definisce membri.

## <a name="remarks"></a>Commenti

La **\_ \_ classe EventGenerator** è derivata da [**\_ \_ IndicationRelated,**](--indicationrelated.md)che non dispone di proprietà.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |
| Spazio dei nomi<br/>                | Tutti gli spazi dei nomi WMI<br/>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_\_IndicationRelated**](/windows/desktop/WmiSdk/--indicationrelated)
</dt> <dt>

[Classi di sistema WMI](wmi-system-classes.md)
</dt> </dl>

 

