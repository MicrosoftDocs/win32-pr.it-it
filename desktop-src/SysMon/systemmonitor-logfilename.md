---
title: Proprietà SystemMonitor. LogFilename
description: Recupera o imposta il nome di un file di log da utilizzare come origine dei valori del contatore visualizzati nel monitor di sistema.
ms.assetid: a93d1c98-4875-4d8e-940c-4443d1e585e6
keywords:
- Proprietà LogFilename SysMon
- Proprietà LogFilename SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, proprietà LogFilename
topic_type:
- apiref
api_name:
- SystemMonitor.LogFileName
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf9d6168f416d1bdab47a4c2952ac60ee7e67397
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400647"
---
# <a name="systemmonitorlogfilename-property"></a>Proprietà SystemMonitor. LogFilename

Recupera o imposta il nome di un file di log da utilizzare come origine dei valori del contatore visualizzati nel monitor di sistema.

> [!Note]  
> Questa proprietà è stata resa obsoleta dalla proprietà [**LogFiles**](systemmonitor-logfiles.md) .

 

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```VB
Property LogFileName As String
```



## <a name="property-value"></a>Valore proprietà

Percorso del file di log. È possibile specificare un percorso assoluto, relativo o UNC. L'estensione del nome del file di log deve essere CSV, TSV o.

## <a name="exceptions"></a>Eccezioni



| Tipo di eccezione                                  | Condizione                                                              |
|-------------------------------------------------|------------------------------------------------------------------------|
| **System. Runtime. InteropServices. COMException** | Impossibile trovare il file specificato. Il valore ERR. Number è 0xC0000BD1. |
| **System. ArgumentException**                    | Non è possibile specificare una stringa vuota.                                    |



 

## <a name="remarks"></a>Commenti

Questa proprietà restituisce il nome del file di log dal primo membro della raccolta [**LogFiles**](systemmonitor-logfiles.md) .

L'impostazione di questa proprietà avrà esito negativo se la raccolta [**LogFiles**](systemmonitor-logfiles.md) contiene uno o più membri.

È necessario utilizzare lo strumento Logman.exe o lo snap-in MMC Perfmon. msc per generare i file di log aggiunti a questa raccolta. Per PerfMon. msc, i registri dei contatori si trovano in **avvisi e registri di prestazioni**. Per informazioni dettagliate sull'utilizzo di Logman.exe o Perfmon. msc, cercare rispettivamente logman o using performance in **Help and Support Center**.

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
</dt> </dl>

 

 





