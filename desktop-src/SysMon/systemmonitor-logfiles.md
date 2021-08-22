---
title: SystemMonitor.LogFiles - proprietà
description: Raccolta di uno o più file di log da utilizzare come origine dei valori dei contatori visualizzati in Monitoraggio di sistema.
ms.assetid: 6e9e7205-3516-404d-b67d-777e484900da
keywords:
- Proprietà LogFiles SysMon
- Proprietà LogFiles SysMon , oggetto SystemMonitor
- Oggetto SystemMonitor SysMon , proprietà LogFiles
topic_type:
- apiref
api_name:
- SystemMonitor.LogFiles
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bed0ea39809d3dfe40ebcedf2fbf2105833af836c12b95ffdfe442d3956d52a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118882181"
---
# <a name="systemmonitorlogfiles-property"></a>SystemMonitor.LogFiles - proprietà

Raccolta di uno o più file di log da utilizzare come origine dei valori dei contatori visualizzati in Monitoraggio di sistema.

## <a name="syntax"></a>Sintassi


```VB
Property LogFiles As ILogFiles
```



## <a name="property-value"></a>Valore proprietà

Raccolta di [**oggetti LogFileItem**](logfileitem.md) che specificano i file di log utilizzati come origine dati per il grafo.

## <a name="remarks"></a>Commenti

Per aggiungere o rimuovere un file di log dalla raccolta di file di log, il valore di [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) non deve essere impostato su sysmonLogFiles.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> <dt>

[**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md)
</dt> <dt>

[**SystemMonitor.LogViewStart**](systemmonitor-logviewstart.md)
</dt> <dt>

[**SystemMonitor.LogViewStop**](systemmonitor-logviewstop.md)
</dt> <dt>

[**SystemMonitor.SqlLogSetName**](systemmonitor-sqllogsetname.md)
</dt> </dl>

 

 





