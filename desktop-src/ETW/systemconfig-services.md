---
description: Questa classe è la classe del tipo di evento per gli eventi di configurazione del servizio.
ms.assetid: 7cba9992-d154-44b8-87d8-b46a8438f607
title: Classe SystemConfig_Services
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_Services
- SystemConfig_Services.ProcessId
- SystemConfig_Services.ServiceState
- SystemConfig_Services.SubProcessTag
- SystemConfig_Services.ServiceName
- SystemConfig_Services.DisplayName
- SystemConfig_Services.ProcessName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 97b4d2a56f2ed739403681875e0be4d9e21481ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977471"
---
# <a name="systemconfig_services-class"></a>\_Classe dei servizi SystemConfig

Questa classe è la classe del tipo di evento per gli eventi di configurazione del servizio.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[EventType(15), EventTypeName("Services")]
class SystemConfig_Services : SystemConfig
{
  uint32 ProcessId;
  uint32 ServiceState;
  uint32 SubProcessTag;
  string ServiceName[];
  string DisplayName[];
  string ProcessName[];
};
```

## <a name="members"></a>Members

La classe dei **\_ Servizi SystemConfig** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ dei servizi SystemConfig** dispone di queste proprietà.

<dl> <dt>

**DisplayName**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (5), **StringTermination ("NullTerminated")**, **Format ("w")**
</dt> </dl>

Nome visualizzato del servizio. Il nome viene mantenuto con la distinzione tra maiuscole e minuscole in Gestione controllo servizi. Tuttavia, i nomi visualizzati vengono sempre confrontati senza distinzione tra maiuscole e minuscole.

</dd> <dt>

**ProcessId**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (1), **Format ("x")**
</dt> </dl>

Identificatore del processo in cui viene eseguito il servizio.

</dd> <dt>

**ProcessName**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (6), **StringTermination ("NullTerminated")**, **Format ("w")**
</dt> </dl>

Nome del processo in cui viene eseguito il servizio.

</dd> <dt>

**ServiceName**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (4), **StringTermination ("NullTerminated")**, **Format ("w")**
</dt> </dl>

Identificatore univoco del servizio. L'identificatore fornisce un'indicazione delle funzionalità fornite dal servizio.

</dd> <dt>

**ServiceState**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (2), **Format ("x")**
</dt> </dl>

Stato corrente del servizio. Per i valori possibili, vedere il membro **dwCurrentState** del **processo di \_ stato \_ del servizio**.

</dd> <dt>

**SubProcessTag**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (3), **Format ("x")**
</dt> </dl>

Identifica il servizio.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SystemConfig**](systemconfig.md)
</dt> </dl>

 

 




