---
description: La classe HWConfig è la classe padre per gli eventi di configurazione hardware Windows XP. La sintassi seguente è semplificata dal codice MOF.
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
ms.openlocfilehash: e1d4b8f69784729ffe5d51f3068b03fc0b4154182b2d05f2896e4556a05f7eba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118394681"
---
# <a name="hwconfig-class"></a>Classe HWConfig

La **classe HWConfig** è la classe padre per gli eventi di configurazione hardware Windows XP.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Guid("{01853a65-418f-4f36-aefc-dc0f1d2fd235}")]
class HWConfig : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Members

La **classe HWConfig** non definisce membri.

## <a name="remarks"></a>Commenti

Questi eventi forniscono la configurazione hardware del computer. A differenza di altri eventi del logger del kernel NT, la sessione del kernel genera automaticamente eventi di configurazione hardware. Questi eventi non vengono abilitati all'avvio della sessione del logger del kernel NT.

**Windows 2000:** Non supportato.

Per gli eventi di configurazione hardware Windows Vista e Windows Server 2003, vedere la [classe SystemConfig.](systemconfig.md)

I consumer di traccia eventi possono implementare un'elaborazione speciale per gli eventi di configurazione hardware chiamando la [**funzione SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e specificando [**EventTraceConfigGuid**](nt-kernel-logger-constants.md) come *parametro pGuid.* Usare i tipi di evento seguenti per identificare l'evento di configurazione hardware effettivo quando si utilizzano gli eventi.



| Tipo di evento                                                                      | Descrizione                                                                                                                                      |
|---------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| **EVENTO \_ TRACE \_ TYPE \_ CONFIG \_ CPU**(il valore del tipo di evento è 10)<br/>          | Evento di configurazione della CPU. Le [**classi MOF \_ della CPU HWConfig**](hwconfig-cpu.md) definiscono i dati dell'evento.                            |
| **EVENTO \_ TRACE \_ TYPE \_ CONFIG \_ LOGICALDISK**(il valore del tipo di evento è 12)<br/>  | Evento di configurazione del disco logico. La classe MOF delle classi MOF [**HWConfig \_ LogDisk**](hwconfig-logdisk.md) definisce i dati dell'evento per questo evento. |
| **EVENTO \_ SCHEDA \_ DI INTERFACCIA DI \_ \_ RETE TRACE TYPE CONFIG**(il valore del tipo di evento è 13)<br/>          | Evento di configurazione della scheda di interfaccia di rete. Le [**classi MOF \_ della scheda**](hwconfig-nic.md) di interfaccia di rete HWConfig definiscono i dati dell'evento.                            |
| **EVENTO \_ TRACE \_ TYPE \_ CONFIG \_ PHYSICALDISK**(il valore del tipo di evento è 11)<br/> | Evento di configurazione del disco fisico. Le [**classi MOF \_ HWConfig PhyDisk**](hwconfig-phydisk.md) definiscono i dati dell'evento per questo evento.          |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MSNT \_ SystemTrace**](msnt-systemtrace.md)
</dt> <dt>

[**HWConfig \_ CPU**](hwconfig-cpu.md)
</dt> <dt>

[**HWConfig \_ LogDisk**](hwconfig-logdisk.md)
</dt> <dt>

[**Scheda di interfaccia di rete HWConfig \_**](hwconfig-nic.md)
</dt> <dt>

[**HWConfig \_ PhyDisk**](hwconfig-phydisk.md)
</dt> </dl>

 

 
