---
title: Oggetto LogFiles (Isysmon.h)
description: Utilizzare questa classe per gestire una raccolta di uno o più file di log che contengono i dati dei contatori delle prestazioni. Per recuperare l'oggetto, chiamare SystemMonitor. LogFiles.
ms.assetid: 1af475c5-ed0c-49b4-a558-13eb8758a986
keywords:
- SysMon oggetto LogFiles
- Oggetti LogFiles SysMon, descritti
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
ms.openlocfilehash: 1ab30de5c371c012e1320950e4a491021bb0b15c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475052"
---
# <a name="logfiles-object"></a>LogFiles (oggetto)

Utilizzare questa classe per gestire una raccolta di uno o più file di log che contengono i dati dei contatori delle prestazioni.

Per recuperare l'oggetto, chiamare [**SystemMonitor. LogFiles**](systemmonitor-logfiles.md).

## <a name="members"></a>Membri

L'oggetto **LogFiles** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

Questi metodi sono disponibili nell'oggetto **LogFiles** .



| Metodo                                          | Descrizione                                                                           |
|:------------------------------------------------|:--------------------------------------------------------------------------------------|
| [**Aggiungere**](systemmonitor-logfiles-add.md)       | Aggiunge un'istanza di [**LogFileItem**](logfileitem.md) alla raccolta.<br/>      |
| [**Rimuovi**](systemmonitor-logfiles-remove.md) | Rimuove un'istanza di [**LogFileItem**](logfileitem.md) dalla raccolta.<br/> |



 

### <a name="properties"></a>Proprietà

L'oggetto **LogFiles** dispone di queste proprietà.



| Proprietà                                                 | Descrizione                                                                                         |
|:---------------------------------------------------------|:----------------------------------------------------------------------------------------------------|
| [**Conteggio**](systemmonitor-logfiles-count.md)<br/> | Recupera il numero di istanze di [**LogFileItem**](logfileitem.md) nell'insieme.<br/>  |
| [**Elemento**](systemmonitor-logfiles-item.md)<br/>   | Recupera l'istanza di [**LogFileItem**](logfileitem.md) specificata dalla raccolta.<br/> |



 

## <a name="remarks"></a>Commenti

Per visualizzare i contatori delle prestazioni di SYSMON da un file di log, impostare [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md) su [**DataSourceTypeConstants.sysmonLogFiles**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants). Dopo l'aggiunta dei file di log alla raccolta, utilizzare la raccolta dei [**contatori**](counters.md) per specificare i dati dei contatori che si desidera leggere dai file di log. Si noti che se **SystemMonitor. DataSourceType** è impostato su **DataSourceTypeConstants.sysmonLogFiles**, Sysmon Ricampiona i file di log ogni volta che si aggiunge un file di log o un contatore alle rispettive raccolte.

**Prima di Windows Vista:** Non è possibile aggiungere file di log alla [**raccolta di file di log**](systemmonitor-logfiles.md) se il valore di [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md) è impostato su [**DataSourceTypeConstants.sysmonLogFiles**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants). Per prima cosa, impostare **SystemMonitor. DataSourceType** su **DataSourceTypeConstants.sysmonNullDataSource**, aggiungere i file di log e i contatori, quindi impostare **SystemMonitor. DataSourceType** su **DataSourceTypeConstants.sysmonLogFiles**.

Le proprietà [**SystemMonitor. LogViewStart**](systemmonitor-logviewstart.md) e [**SystemMonitor. LogViewStop**](systemmonitor-logviewstop.md) specificano l'intervallo di valori campionati dai file di log a Graph. SYSMON disegna un solo valore di visualizzazione dei dati dal file di log (la visualizzazione del grafico non scorre come quando si crea un grafico dell'attività corrente del computer). Se i dati campionati superano quelli che possono essere visualizzati in una singola visualizzazione grafico, SYSMON comprime i dati campionati (ogni punto grafico rappresenta la media di più valori campionati) per adattarsi a tutti i dati campionati dei file di log nel grafico.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Isysmon. h</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



 

 





