---
title: Metodo LogFiles.Add
description: Aggiunge un file di log alla raccolta.
ms.assetid: f6b671ea-9620-49a7-8b0c-0c8e1d9819b0
keywords:
- Metodo Add SysMon
- Metodo Add SysMon , classe LogFiles
- Metodo SysMon , Add della classe LogFiles
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
ms.openlocfilehash: af01c5c7a1bbe16826457d7e1f8700df01876827c522a36db41f6c3843101d6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118882336"
---
# <a name="logfilesadd-method"></a>Metodo LogFiles.Add

Aggiunge un file di log alla raccolta.

## <a name="syntax"></a>Sintassi


```VB
LogFiles.Add( _
  ByVal pathname As String _
) As LogFileItem
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pathname* \[ Pollici\]
</dt> <dd>

Percorso del file di log. È possibile specificare il percorso come percorso assoluto, relativo o UNC. L'estensione del file di log deve essere .csv, tsv o blg.

</dd> </dl>

## <a name="remarks"></a>Commenti

È necessario usare lo strumento Logman.exe o lo snap-in MMC Perfmon.msc per generare i file di log aggiunti a questa raccolta. Per Perfmon.msc, i log dei contatori si trovano **in Avvisi e registri di prestazioni**. Per informazioni dettagliate sull'Logman.exe o Perfmon.msc, cercare logman o utilizzo delle prestazioni, **rispettivamente, nella** Guida e supporto tecnico .

**Prima di Windows Vista:** Non è possibile aggiungere file di log alla raccolta [**di file**](systemmonitor-logfiles.md) di log se il valore di [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) è impostato suDataSourceTypeConstants.sys [**monLogFiles**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants). Impostare innanzitutto **SystemMonitor.DataSourceType** su **DataSourceTypeConstants.sysmonNullDataSource**, aggiungere i file di log e i contatori e quindi **impostare SystemMonitor.DataSourceType** suDataSourceTypeConstants.sys **monLogFiles**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[LogFiles](logfiles.md)
</dt> <dt>

[**LogFileItem**](logfileitem.md)
</dt> <dt>

[**LogFiles**](systemmonitor-logfiles.md)
</dt> </dl>

 

 





