---
description: 'SystemConfig_V0_Services: questa classe è la classe del tipo di evento per gli eventi di configurazione del servizio.'
ms.assetid: 1e6c2061-f1a2-4253-a0c4-4b45b2feceda
title: SystemConfig_V0_Services classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_Services
- SystemConfig_V0_Services.ServiceName
- SystemConfig_V0_Services.DisplayName
- SystemConfig_V0_Services.ProcessName
- SystemConfig_V0_Services.ProcessId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 5cfe3bfd4509a02eeafcb014f9265f810e4cb942e87b67390dbd1cbf841f7295
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118393790"
---
# <a name="systemconfig_v0_services-class"></a>Classe SystemConfig \_ V0 \_ Services

Questa classe è la classe del tipo di evento per gli eventi di configurazione del servizio.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[EventType(15), EventTypeName("Services")]
class SystemConfig_V0_Services : SystemConfig_V0
{
  char16 ServiceName[];
  char16 DisplayName[];
  char16 ProcessName[];
  uint32 ProcessId;
};
```

## <a name="members"></a>Members

La **classe SystemConfig \_ V0 \_ Services** include questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe SystemConfig \_ V0 \_ Services** dispone di queste proprietà.

<dl> <dt>

**DisplayName**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice char16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (2), **Max** (256)
</dt> </dl>

Nome visualizzato del servizio. Il nome viene mantenuto senza distinzione tra maiuscole e minuscole in Gestione controllo servizi. Tuttavia, i nomi visualizzati vengono sempre confrontati senza distinzione tra maiuscole e minuscole.

</dd> <dt>

**Processid**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (4)
</dt> </dl>

Identificatore del processo in cui viene eseguito il servizio.

</dd> <dt>

**ProcessName**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice char16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (3), **Max** (34)
</dt> </dl>

Nome del processo in cui viene eseguito il servizio.

</dd> <dt>

**Servicename**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice char16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (1), **Max** (34)
</dt> </dl>

Identificatore univoco del servizio. L'identificatore fornisce un'indicazione della funzionalità fornita dal servizio.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                            |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SystemConfig \_ V0**](systemconfig-v0.md)
</dt> </dl>

 

 




