---
description: Questa classe è la classe padre per gli eventi di configurazione hardware. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 9da1a7ec-89b5-462b-a336-544e4b7adf96
title: Classe SystemConfig_V0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0
api_type:
- NA
api_location: ''
ms.openlocfilehash: 92d77d1ad3effdd2bf22a7df8112187b27666238
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880894"
---
# <a name="systemconfig_v0-class"></a>\_Classe SystemConfig V0

Questa classe è la classe padre per gli eventi di configurazione hardware.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Guid("{01853a65-418f-4f36-aefc-dc0f1d2fd235}"), EventVersion(0)]
class SystemConfig_V0 : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Members

La classe **SystemConfig \_ V0** non definisce membri.

## <a name="remarks"></a>Commenti

Per gli eventi di configurazione hardware in Windows XP, vedere la classe [**HWConfig**](hwconfig.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_SYSTEMTRACE MSNT**](msnt-systemtrace.md)
</dt> <dt>

[**SystemConfig**](systemconfig.md)
</dt> <dt>

[**\_CPU SystemConfig V0 \_**](systemconfig-v0-cpu.md)
</dt> <dt>

[**SystemConfig \_ V0 \_ LogDisk**](systemconfig-v0-logdisk.md)
</dt> <dt>

[**Scheda di interfaccia di rete SystemConfig \_ V0 \_**](systemconfig-v0-nic.md)
</dt> <dt>

[**SystemConfig \_ V0 \_ PhyDisk**](systemconfig-v0-phydisk.md)
</dt> <dt>

[**\_Potenza SystemConfig V0 \_**](systemconfig-v0-power.md)
</dt> <dt>

[**\_Servizi SystemConfig V0 \_**](systemconfig-v0-services.md)
</dt> <dt>

[**\_Video SystemConfig V0 \_**](systemconfig-v0-video.md)
</dt> </dl>

 

 




