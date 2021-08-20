---
description: 'SystemConfig_Services: questa classe è la classe del tipo di evento per gli eventi di configurazione del servizio.'
ms.assetid: 7cba9992-d154-44b8-87d8-b46a8438f607
title: SystemConfig_Services classe
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
ms.openlocfilehash: 80d0bfdc324f55bd8b697dfd63f9c2cf5c847ca3e3c931842b886c00adbc6aac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119383451"
---
# <a name="systemconfig_services-class"></a>Classe SystemConfig \_ Services

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

La **classe SystemConfig \_ Services** include questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe SystemConfig \_ Services** dispone di queste proprietà.

<dl> <dt>

**DisplayName**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (5), **StringTermination("NullTerminated")**, **Format("w")**
</dt> </dl>

Nome visualizzato del servizio. Il nome viene mantenuto senza distinzione tra maiuscole e minuscole in Gestione controllo servizi. Tuttavia, i nomi visualizzati vengono sempre confrontati senza distinzione tra maiuscole e minuscole.

</dd> <dt>

**Processid**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (1), **Format("x")**
</dt> </dl>

Identificatore del processo in cui viene eseguito il servizio.

</dd> <dt>

**ProcessName**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (6), **StringTermination("NullTerminated")**, **Format("w")**
</dt> </dl>

Nome del processo in cui viene eseguito il servizio.

</dd> <dt>

**Servicename**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (4), **StringTermination("NullTerminated")**, **Format("w")**
</dt> </dl>

Identificatore univoco del servizio. L'identificatore fornisce un'indicazione della funzionalità fornita dal servizio.

</dd> <dt>

**ServiceState**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (2), **Format("x")**
</dt> </dl>

Stato corrente del servizio. Per i valori possibili, vedere **il membro dwCurrentState** di **SERVICE STATUS \_ \_ PROCESS.**

</dd> <dt>

**SubProcessTag**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (3), **Format("x")**
</dt> </dl>

Identifica il servizio.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SystemConfig**](systemconfig.md)
</dt> </dl>

 

 




