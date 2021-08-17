---
description: 'Classe SystemConfig: questa classe è la classe padre per gli eventi di configurazione hardware. La sintassi seguente è semplificata dal codice MOF.'
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
ms.openlocfilehash: 4f409887f70989c65475c8b854b4b610c9ffa6c122edc25e87b5ebdc8dbc9180
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069641"
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

La **classe SystemConfig** non definisce membri.

## <a name="remarks"></a>Commenti

Questi eventi forniscono la configurazione hardware del computer. A differenza di altri eventi del logger del kernel NT, la sessione del kernel genera automaticamente eventi di configurazione hardware. questi eventi non vengono abilitati all'avvio della sessione del logger del kernel NT.

Per gli eventi di configurazione hardware Windows XP, vedere la [classe HWConfig.](hwconfig.md)

I consumer di traccia eventi possono implementare un'elaborazione speciale per gli eventi di configurazione hardware chiamando la [**funzione SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e specificando [**EventTraceConfigGuid**](nt-kernel-logger-constants.md) come *parametro pGuid.* Usare i tipi di evento seguenti per identificare l'evento di configurazione hardware effettivo durante l'utilizzo degli eventi.



| Tipo di evento                                                                      | Descrizione                                                                                                                                                                         |
|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EVENTO \_ TRACE \_ TYPE \_ CONFIG \_ CPU**(il valore del tipo di evento è 10)<br/>          | Evento di configurazione della CPU. Le [**classi MOF \_ della CPU SystemConfig**](systemconfig-cpu.md) definiscono i dati degli eventi per questo evento.                                                       |
| **EVENTO \_ TRACE \_ TYPE \_ CONFIG \_ IDECHANNEL**(il valore del tipo di evento è 23)<br/>   | Evento di configurazione del canale IDE primario e secondario. La classe MOF classi MOF [**SYSTEMConfig \_ IDEChannel**](systemconfig-idechannel.md) definisce i dati dell'evento per questo evento. |
| **EVENTO \_ TRACE \_ TYPE \_ CONFIG \_ IRQ**(il valore del tipo di evento è 21)<br/>          | Evento di richiesta di interruzione (IRQ). La classe MOF delle classi MOF [**systemConfig \_ IRQ**](systemconfig-irq.md) definisce i dati dell'evento per questo evento.                                       |
| **EVENTO \_ TRACE \_ TYPE \_ CONFIG \_ LOGICALDISK**(il valore del tipo di evento è 12)<br/>  | Evento di configurazione del disco logico. La classe MOF delle classi MOF [**SystemConfig \_ LogDisk**](systemconfig-logdisk.md) definisce i dati degli eventi per questo evento.                            |
| **EVENTO \_ TRACE \_ TYPE \_ CONFIG \_ NETINFO**(il valore del tipo di evento è 17)<br/>      | Evento di iformazione di rete. La [**classe MOF \_ di**](systemconfig-network.md) rete SystemConfig definisce i dati dell'evento.                                                |
| **EVENTO \_ SCHEDA \_ DI INTERFACCIA DI \_ \_ RETE DI TRACE TYPE CONFIG**(il valore del tipo di evento è 13)<br/>          | Evento di configurazione della scheda di interfaccia di rete. Le [**classi MOF \_ della scheda**](systemconfig-nic.md) di interfaccia di rete SystemConfig definiscono i dati dell'evento.                                                       |
| **EVENTO \_ TRACE \_ TYPE \_ CONFIG \_ PHYSICALDISK**(il valore del tipo di evento è 11)<br/> | Evento di configurazione del disco fisico. Le [**classi MOF \_ SystemConfig PhyDisk**](systemconfig-phydisk.md) definiscono i dati dell'evento.                                     |
| **EVENTO \_ TRACE \_ TYPE \_ CONFIG \_ PNP**(il valore del tipo di evento è 22)<br/>          | Evento Plug and Play. La classe MOF delle classi MOF [**\_ SystemConfig PNP**](systemconfig-pnp.md) definisce i dati dell'evento.                                                 |
| **EVENTO \_ TRACE \_ TYPE \_ CONFIG \_ POWER**(il valore del tipo di evento è 16)<br/>        | Evento di configurazione dell'alimentazione. La [**classe SystemConfig \_ Power**](systemconfig-power.md) MOF definisce i dati dell'evento.                                                   |
| **EVENTO \_ TRACE \_ TYPE \_ CONFIG \_ SERVICES**(il valore del tipo di evento è 15)<br/>     | Evento di configurazione dei servizi. La [**classe MOF di SystemConfig \_ Services**](systemconfig-services.md) definisce i dati dell'evento.                                          |
| **EVENTO \_ TRACE \_ TYPE \_ CONFIG \_ VIDEO**(il valore del tipo di evento è 14)<br/>        | Evento di configurazione dell'adattatore grafico. La [**classe MOF \_ SystemConfig Video**](systemconfig-video.md) definisce i dati dell'evento.                                        |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MSNT \_ SystemTrace**](msnt-systemtrace.md)
</dt> <dt>

[**SystemConfig \_ CPU**](systemconfig-cpu.md)
</dt> <dt>

[**SystemConfig \_ IDEChannel**](systemconfig-idechannel.md)
</dt> <dt>

[**SystemConfig \_ IRQ**](systemconfig-irq.md)
</dt> <dt>

[**SystemConfig \_ LogDisk**](systemconfig-logdisk.md)
</dt> <dt>

[**Rete \_ SystemConfig**](systemconfig-network.md)
</dt> <dt>

[**Scheda di interfaccia di rete SystemConfig \_**](systemconfig-nic.md)
</dt> <dt>

[**SystemConfig \_ PhyDisk**](systemconfig-phydisk.md)
</dt> <dt>

[**SystemConfig \_ PNP**](systemconfig-pnp.md)
</dt> <dt>

[**SystemConfig \_ Power**](systemconfig-power.md)
</dt> <dt>

[**Servizi \_ SystemConfig**](systemconfig-services.md)
</dt> <dt>

[**Video di \_ SystemConfig**](systemconfig-video.md)
</dt> <dt>

[**SystemConfig \_ V0**](systemconfig-v0.md)
</dt> </dl>

 

 
