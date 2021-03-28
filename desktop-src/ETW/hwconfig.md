---
description: La classe HWConfig è la classe padre per gli eventi di configurazione hardware in Windows XP. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 47f062c0-fdf0-4beb-906d-257571324de9
title: Classe HWConfig
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HWConfig
api_type:
- NA
api_location: ''
ms.openlocfilehash: cfb194e09701dbc52b00279b624877f09ffac24b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885562"
---
# <a name="hwconfig-class"></a>Classe HWConfig

La classe **HWConfig** è la classe padre per gli eventi di configurazione hardware in Windows XP.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Guid("{01853a65-418f-4f36-aefc-dc0f1d2fd235}")]
class HWConfig : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Members

La classe **HWConfig** non definisce membri.

## <a name="remarks"></a>Commenti

Questi eventi forniscono la configurazione hardware del computer. Diversamente dagli altri eventi del logger di kernel NT, la sessione kernel genera automaticamente gli eventi di configurazione hardware. questi eventi non vengono abilitati all'avvio della sessione del logger del kernel NT.

**Windows 2000:** Non supportato.

Per gli eventi di configurazione hardware in Windows Vista e Windows Server 2003, vedere la classe [SystemConfig](systemconfig.md) .

I consumer di traccia degli eventi possono implementare un'elaborazione speciale per gli eventi di configurazione hardware chiamando la funzione [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e specificando [**EventTraceConfigGuid**](nt-kernel-logger-constants.md) come parametro *pGuid* . Usare i tipi di eventi seguenti per identificare l'evento di configurazione hardware effettivo quando si utilizzano gli eventi.



| Tipo di evento                                                                      | Descrizione                                                                                                                                      |
|---------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| **Evento \_ Tipo di traccia \_ \_ \_ CPU di configurazione**(il valore del tipo di evento è 10)<br/>          | Evento di configurazione della CPU. Le classi MOF della [**\_ CPU HWConfig**](hwconfig-cpu.md) definiscono i dati degli eventi per questo evento.                            |
| **Evento \_ Tipo di traccia \_ \_ config \_ disco logico**(il valore del tipo di evento è 12)<br/>  | Evento configurazione disco logico. La classe MOF delle classi MOF [**HWConfig \_ LogDisk**](hwconfig-logdisk.md) definisce i dati dell'evento per questo evento. |
| **Evento \_ \_ \_ \_ Scheda** di interfaccia di rete di tipo traccia (valore del tipo di evento 13)<br/>          | Evento di configurazione NIC. Le classi MOF di [**\_ NIC HWConfig**](hwconfig-nic.md) definiscono i dati degli eventi per questo evento.                            |
| **Evento \_ Tipo di traccia \_ \_ config \_ PHYSICALDISK**(il valore del tipo di evento è 11)<br/> | Evento di configurazione del disco fisico. Le classi MOF [**HWConfig \_ PhyDisk**](hwconfig-phydisk.md) definiscono i dati degli eventi per questo evento.          |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_SYSTEMTRACE MSNT**](msnt-systemtrace.md)
</dt> <dt>

[**\_CPU HWConfig**](hwconfig-cpu.md)
</dt> <dt>

[**\_LogDisk HWConfig**](hwconfig-logdisk.md)
</dt> <dt>

[**Scheda di interfaccia di rete HWConfig \_**](hwconfig-nic.md)
</dt> <dt>

[**\_PhyDisk HWConfig**](hwconfig-phydisk.md)
</dt> </dl>

 

 
