---
description: Questa classe è la classe del tipo di evento per gli eventi di configurazione del servizio.
ms.assetid: 1e6c2061-f1a2-4253-a0c4-4b45b2feceda
title: Classe SystemConfig_V0_Services
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
ms.openlocfilehash: 6c061c6a0c4cbb3e807bcb3418155b1194fcfa28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349321"
---
# <a name="systemconfig_v0_services-class"></a>\_ \_ Classe dei servizi SystemConfig V0

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

La classe dei **\_ \_ Servizi SystemConfig V0** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ \_ dei servizi SystemConfig V0** dispone di queste proprietà.

<dl> <dt>

**DisplayName**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **Char16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (2), **Max** (256)
</dt> </dl>

Nome visualizzato del servizio. Il nome viene mantenuto con la distinzione tra maiuscole e minuscole in Gestione controllo servizi. Tuttavia, i nomi visualizzati vengono sempre confrontati senza distinzione tra maiuscole e minuscole.

</dd> <dt>

**ProcessId**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (4)
</dt> </dl>

Identificatore del processo in cui viene eseguito il servizio.

</dd> <dt>

**ProcessName**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **Char16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (3), **Max** (34)
</dt> </dl>

Nome del processo in cui viene eseguito il servizio.

</dd> <dt>

**ServiceName**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **Char16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (1), **Max** (34)
</dt> </dl>

Identificatore univoco del servizio. L'identificatore fornisce un'indicazione delle funzionalità fornite dal servizio.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SystemConfig \_ V0**](systemconfig-v0.md)
</dt> </dl>

 

 




