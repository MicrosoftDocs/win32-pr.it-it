---
description: Questa classe è la classe padre per gli eventi di configurazione hardware. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 720c2366-bd68-4895-bfaf-74aa9b64ba4a
title: Classe SystemConfig
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3332d396005deb2fb811d101a99827544ebc6df0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885872"
---
# <a name="systemconfig-class"></a>Classe SystemConfig

Questa classe è la classe padre per gli eventi di configurazione hardware.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Guid("{01853a65-418f-4f36-aefc-dc0f1d2fd235}"), EventVersion(2)]
class SystemConfig : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Members

La classe **SystemConfig** non definisce membri.

## <a name="remarks"></a>Commenti

Questi eventi forniscono la configurazione hardware del computer. Diversamente dagli altri eventi del logger di kernel NT, la sessione kernel genera automaticamente gli eventi di configurazione hardware. questi eventi non vengono abilitati all'avvio della sessione del logger del kernel NT.

Per gli eventi di configurazione hardware in Windows XP, vedere la classe [HWConfig](hwconfig.md) .

I consumer di traccia degli eventi possono implementare un'elaborazione speciale per gli eventi di configurazione hardware chiamando la funzione [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e specificando [**EventTraceConfigGuid**](nt-kernel-logger-constants.md) come parametro *pGuid* . Usare i tipi di eventi seguenti per identificare l'evento di configurazione hardware effettivo quando si utilizzano gli eventi.



| Tipo di evento                                                                      | Descrizione                                                                                                                                                                         |
|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Evento \_ Tipo di traccia \_ \_ \_ CPU di configurazione**(il valore del tipo di evento è 10)<br/>          | Evento di configurazione della CPU. Le classi MOF della [**\_ CPU SystemConfig**](systemconfig-cpu.md) definiscono i dati degli eventi per questo evento.                                                       |
| **Evento \_ Tipo di traccia \_ \_ config \_ IDECHANNEL**(il valore del tipo di evento è 23)<br/>   | Evento di configurazione del canale IDE primario e secondario. La classe MOF delle classi MOF [**SystemConfig \_ IDEChannel**](systemconfig-idechannel.md) definisce i dati dell'evento per questo evento. |
| **Evento \_ \_ \_ \_ IRQ Config del tipo di traccia**(il valore del tipo di evento è 21)<br/>          | Evento di richiesta di interrupt (IRQ). La classe MOF di [**SystemConfig \_ IRQ**](systemconfig-irq.md) Classis definisce i dati dell'evento per questo evento.                                       |
| **Evento \_ Tipo di traccia \_ \_ config \_ disco logico**(il valore del tipo di evento è 12)<br/>  | Evento configurazione disco logico. La classe MOF delle classi MOF [**SystemConfig \_ LogDisk**](systemconfig-logdisk.md) definisce i dati dell'evento per questo evento.                            |
| **Evento \_ Tipo di traccia \_ \_ config \_ NetInfo**(il valore del tipo di evento è 17)<br/>      | Evento Iformation di rete. La classe MOF di [**\_ rete SystemConfig**](systemconfig-network.md) definisce i dati dell'evento per questo evento.                                                |
| **Evento \_ \_ \_ \_ Scheda** di interfaccia di rete di tipo traccia (valore del tipo di evento 13)<br/>          | Evento di configurazione NIC. Le classi MOF di [**\_ NIC SystemConfig**](systemconfig-nic.md) definiscono i dati degli eventi per questo evento.                                                       |
| **Evento \_ Tipo di traccia \_ \_ config \_ PHYSICALDISK**(il valore del tipo di evento è 11)<br/> | Evento di configurazione del disco fisico. Le classi MOF [**SystemConfig \_ PhyDisk**](systemconfig-phydisk.md) definiscono i dati degli eventi per questo evento.                                     |
| **Evento \_ Configurazione del tipo di traccia \_ \_ \_ PNP**(il valore del tipo di evento è 22)<br/>          | Evento plug and Play. La classe MOF [**SystemConfig \_ PNP**](systemconfig-pnp.md) classi MOF definisce i dati dell'evento per questo evento.                                                 |
| **Evento \_ Configurazione del tipo di traccia \_ \_ \_ Power**(il valore del tipo di evento è 16)<br/>        | Evento di configurazione risparmio energia. La classe [**SystemConfig di \_ Power**](systemconfig-power.md) MOF definisce i dati dell'evento per questo evento.                                                   |
| **Evento \_ \_Servizi di \_ configurazione \_ del tipo di traccia**(il valore del tipo di evento è 15)<br/>     | Evento di configurazione dei servizi. La classe MOF dei [**\_ Servizi SystemConfig**](systemconfig-services.md) definisce i dati dell'evento per questo evento.                                          |
| **Evento \_ Tipo di traccia \_ \_ \_ video di configurazione**(il valore del tipo di evento è 14)<br/>        | Evento di configurazione della scheda grafica. La classe MOF [**\_ video SystemConfig**](systemconfig-video.md) definisce i dati dell'evento per questo evento.                                        |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_SYSTEMTRACE MSNT**](msnt-systemtrace.md)
</dt> <dt>

[**\_CPU SystemConfig**](systemconfig-cpu.md)
</dt> <dt>

[**\_IDEChannel SystemConfig**](systemconfig-idechannel.md)
</dt> <dt>

[**\_IRQ SystemConfig**](systemconfig-irq.md)
</dt> <dt>

[**\_LogDisk SystemConfig**](systemconfig-logdisk.md)
</dt> <dt>

[**\_Rete SystemConfig**](systemconfig-network.md)
</dt> <dt>

[**Scheda di interfaccia di rete SystemConfig \_**](systemconfig-nic.md)
</dt> <dt>

[**\_PhyDisk SystemConfig**](systemconfig-phydisk.md)
</dt> <dt>

[**SystemConfig \_ PNP**](systemconfig-pnp.md)
</dt> <dt>

[**\_Power SystemConfig**](systemconfig-power.md)
</dt> <dt>

[**\_Servizi SystemConfig**](systemconfig-services.md)
</dt> <dt>

[**Video di SystemConfig \_**](systemconfig-video.md)
</dt> <dt>

[**SystemConfig \_ V0**](systemconfig-v0.md)
</dt> </dl>

 

 
