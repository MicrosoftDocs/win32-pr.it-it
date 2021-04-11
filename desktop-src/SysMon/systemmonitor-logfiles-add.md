---
title: LogFiles. Add (metodo)
description: Aggiunge un file di log alla raccolta.
ms.assetid: f6b671ea-9620-49a7-8b0c-0c8e1d9819b0
keywords:
- Aggiungere il metodo SysMon
- Add Method SysMon, classe LogFiles
- Classe LogFiles SysMon, Add (metodo)
topic_type:
- apiref
api_name:
- LogFiles.Add
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f690670606cd7ee307ba945fc2daabe92953e81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119870"
---
# <a name="logfilesadd-method"></a>LogFiles. Add (metodo)

Aggiunge un file di log alla raccolta.

## <a name="syntax"></a>Sintassi


```VB
LogFiles.Add( _
  ByVal pathname As String _
) As LogFileItem
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*nome percorso* \[ in\]
</dt> <dd>

Percorso del file di log. È possibile specificare il percorso come percorso assoluto, relativo o UNC. L'estensione del nome del file di log deve essere CSV, TSV o.

</dd> </dl>

## <a name="remarks"></a>Commenti

È necessario utilizzare lo strumento Logman.exe o lo snap-in MMC Perfmon. msc per generare i file di log aggiunti a questa raccolta. Per PerfMon. msc, i registri dei contatori si trovano in **avvisi e registri di prestazioni**. Per informazioni dettagliate sull'utilizzo di Logman.exe o Perfmon. msc, cercare rispettivamente logman o using performance in **Help and Support Center**.

**Prima di Windows Vista:** Non è possibile aggiungere file di log alla [**raccolta di file di log**](systemmonitor-logfiles.md) se il valore di [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md) è impostato su [**DataSourceTypeConstants.sysmonLogFiles**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants). Per prima cosa, impostare **SystemMonitor. DataSourceType** su **DataSourceTypeConstants.sysmonNullDataSource**, aggiungere i file di log e i contatori, quindi impostare **SystemMonitor. DataSourceType** su **DataSourceTypeConstants.sysmonLogFiles**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[LogFiles](logfiles.md)
</dt> <dt>

[**LogFileItem**](logfileitem.md)
</dt> <dt>

[**LogFiles**](systemmonitor-logfiles.md)
</dt> </dl>

 

 





