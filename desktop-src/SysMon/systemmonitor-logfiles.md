---
title: Proprietà SystemMonitor. LogFiles
description: Raccolta di uno o più file di log da utilizzare come origine dei valori del contatore visualizzati nel monitor di sistema.
ms.assetid: 6e9e7205-3516-404d-b67d-777e484900da
keywords:
- Proprietà LogFiles SysMon
- Proprietà LogFiles SysMon, oggetto SystemMonitor
- Oggetto SystemMonitor SysMon, Proprietà LogFiles
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
ms.openlocfilehash: c8127433319290b44498b272834923784b714052
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301578"
---
# <a name="systemmonitorlogfiles-property"></a>Proprietà SystemMonitor. LogFiles

Raccolta di uno o più file di log da utilizzare come origine dei valori del contatore visualizzati nel monitor di sistema.

## <a name="syntax"></a>Sintassi


```VB
Property LogFiles As ILogFiles
```



## <a name="property-value"></a>Valore proprietà

Raccolta di oggetti [**LogFileItem**](logfileitem.md) che specificano i file di log utilizzati come origine dati per il grafico.

## <a name="remarks"></a>Commenti

Per aggiungere o rimuovere un file di log dalla raccolta dei file di log, il valore di [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md) non deve essere impostato su sysmonLogFiles.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> <dt>

[**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md)
</dt> <dt>

[**SystemMonitor. LogViewStart**](systemmonitor-logviewstart.md)
</dt> <dt>

[**SystemMonitor. LogViewStop**](systemmonitor-logviewstop.md)
</dt> <dt>

[**SystemMonitor. SqlLogSetName**](systemmonitor-sqllogsetname.md)
</dt> </dl>

 

 





