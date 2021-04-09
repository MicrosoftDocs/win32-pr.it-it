---
description: Funge da classe padre per le classi di errore definite dal provider.
ms.assetid: fc2747f5-cfbc-4d61-894d-4585a03dda3f
ms.tgt_platform: multiple
title: Classe __NotifyStatus
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __NotifyStatus
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: f19ef1f6088b5a058f4483f197877358177c81f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759440"
---
# <a name="__notifystatus-class"></a>\_\_Classe NotifyStatus

La classe di sistema astratta **\_ \_ NotifyStatus** funge da classe padre per le classi di errore definite dal provider.

La sintassi seguente è semplificata dal codice Managed Object Format (MF) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[abstract]
class __NotifyStatus
{
  uint32 StatusCode;
};
```

## <a name="members"></a>Members

La classe **\_ \_ NotifyStatus** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **\_ \_ NotifyStatus** dispone di queste proprietà.

<dl> <dt>

**StatusCode**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Contiene un codice di errore o informazioni per un'operazione. Può trattarsi di qualsiasi codice definito dall'utente, ma il valore 0 (zero) è in genere riservato per indicare l'esito positivo.

</dd> </dl>

## <a name="remarks"></a>Commenti

Sebbene la classe **\_ \_ NotifyStatus** possa essere la classe padre per le classi di errore definite dal provider, è consigliabile che i provider derivano invece le classi di errore da [**\_ \_ ExtendedStatus**](--extendedstatus.md) . L'uso di **\_ \_ ExtendedStatus** consente una maggiore standardizzazione delle classi Error.

I provider non devono mai creare direttamente istanze di **\_ \_ NotifyStatus** , perché queste istanze non contengono più informazioni rispetto a un semplice codice restituito.

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

 

 




