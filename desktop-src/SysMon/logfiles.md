---
title: Oggetto LogFiles (Isysmon.h)
description: Utilizzare questa classe per gestire una raccolta di uno o più file di log contenenti i dati dei contatori delle prestazioni. Per recuperare questo oggetto, chiamare SystemMonitor.LogFiles.
ms.assetid: 1af475c5-ed0c-49b4-a558-13eb8758a986
keywords:
- Oggetto LogFiles SysMon
- Oggetto LogFiles SysMon , descritto
topic_type:
- apiref
api_name:
- LogFiles
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75a0890acdf656c807ae3bcb275012bd56a4711a114547f750f04fd8d875fc68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118883149"
---
# <a name="logfiles-object"></a>Oggetto LogFiles

Utilizzare questa classe per gestire una raccolta di uno o più file di log contenenti i dati dei contatori delle prestazioni.

Per recuperare questo oggetto, chiamare [**SystemMonitor.LogFiles**](systemmonitor-logfiles.md).

## <a name="members"></a>Membri

**L'oggetto LogFiles** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'oggetto LogFiles** dispone di questi metodi.



| Metodo                                          | Descrizione                                                                           |
|:------------------------------------------------|:--------------------------------------------------------------------------------------|
| [**Aggiungere**](systemmonitor-logfiles-add.md)       | Aggiunge [**un'istanza di LogFileItem**](logfileitem.md) alla raccolta.<br/>      |
| [**Rimuovi**](systemmonitor-logfiles-remove.md) | Rimuove [**un'istanza di LogFileItem**](logfileitem.md) dalla raccolta.<br/> |



 

### <a name="properties"></a>Proprietà

**L'oggetto LogFiles** ha queste proprietà.



| Proprietà                                                 | Descrizione                                                                                         |
|:---------------------------------------------------------|:----------------------------------------------------------------------------------------------------|
| [**Conteggio**](systemmonitor-logfiles-count.md)<br/> | Recupera il numero di [**istanze di LogFileItem**](logfileitem.md) nella raccolta.<br/>  |
| [**Elemento**](systemmonitor-logfiles-item.md)<br/>   | Recupera [**l'istanza di LogFileItem**](logfileitem.md) specificata dalla raccolta.<br/> |



 

## <a name="remarks"></a>Commenti

Per fare in modo che SYSMON visualizza i contatori delle prestazioni da un file di log, impostare [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) [**suDataSourceTypeConstants.sysmonLogFiles**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants). Dopo aver aggiunto i file di log alla raccolta, utilizzare la raccolta [**Counters**](counters.md) per specificare i dati dei contatori che si desidera leggere dai file di log. Si noti che se **SystemMonitor.DataSourceType** è impostato su **DataSourceTypeConstants.sysmonLogFiles**, SYSMON ricampionerà i file di log ogni volta che si aggiunge un file di log o un contatore alle rispettive raccolte.

**Prima di Windows Vista:** Non è possibile aggiungere file di log alla raccolta [**di file**](systemmonitor-logfiles.md) di log se il valore di [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) è impostato suDataSourceTypeConstants.sys [**monLogFiles**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants). Impostare prima di tutto **SystemMonitor.DataSourceType** su **DataSourceTypeConstants.sysmonNullDataSource**, aggiungere i file di log e i contatori e quindi impostare **SystemMonitor.DataSourceType** su **DataSourceTypeConstants.sysmonLogFiles**.

Le [**proprietà SystemMonitor.LogViewStart**](systemmonitor-logviewstart.md) e [**SystemMonitor.LogViewStop**](systemmonitor-logviewstop.md) specificano l'intervallo di valori campionati dai file di log al grafico. SYSMON rappresenta solo una visualizzazione dei dati del file di log(la visualizzazione grafico non scorre come quando si esegue il grafico dell'attività corrente del computer). Se i dati campionati superano quello che può essere visualizzato in una singola visualizzazione grafico, SYSMON comprime i dati campionati (ogni punto grafico rappresenta la media di più valori campionati) per adattare tutti i dati campionati dai file di log nel grafico.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Isysmon.h</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



 

 





