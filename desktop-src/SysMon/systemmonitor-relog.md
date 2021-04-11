---
title: SystemMonitor. relog, metodo
description: Registra i dati del contatore in un nuovo file. È inoltre possibile utilizzare questo metodo per specificare un nuovo tipo di file e per ridurre il numero di campioni contenuti nel file di log.
ms.assetid: 4439f9ef-99e0-47d4-8f6f-d08afcba672d
keywords:
- Metodo relog SysMon
- Metodo relog SysMon, oggetto SystemMonitor
- Oggetto SystemMonitor SysMon, metodo relog
topic_type:
- apiref
api_name:
- SystemMonitor.Relog
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 109d0a6e44ef73652bd563099929ce601670610b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119523"
---
# <a name="systemmonitorrelog-method"></a>SystemMonitor. relog, metodo

Registra i dati del contatore in un nuovo file. È inoltre possibile utilizzare questo metodo per specificare un nuovo tipo di file e per ridurre il numero di campioni contenuti nel file di log.

## <a name="syntax"></a>Sintassi


```VB
SystemMonitor.Relog( _
  ByVal fileName As String, _
  ByVal fileType As SysmonFileType, _
  ByVal filter As Long _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*nome file* \[ in\]
</dt> <dd>

Percorso del file di log. È possibile specificare il percorso come percorso assoluto, relativo o UNC. L'estensione del nome del file di log deve essere. grosso,. TSV o. csv. Se una cartella nel percorso non esiste, verrà creata da SYSMON. Se il file esiste, il file viene sovrascritto. SYSMON applica gli ACL predefiniti dalla directory padre.

</dd> <dt>

*FileType* \[ in\]
</dt> <dd>

Formato dei dati del contatore salvati nel file di log. È possibile specificare [**SysmonFileType.sysmonFileBlg**](/windows/win32/api/isysmon/ne-isysmon-sysmonfiletype), **SysmonFileType.sysMonFileCsv** o **SysmonFileType.sysmonFileTsv**.

</dd> <dt>

*filtro* \[ di in\]
</dt> <dd>

Numero di campioni dei vecchi file di log da salvare nel nuovo file di log. Specificare 1 per salvare ogni esempio dai file precedenti ai nuovi file. Specificare 2 per salvare uno dei due campioni dal file precedente. Specificare 3 per salvare uno dei tre campioni dal file precedente. e così via.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo utilizza i file di log contenuti nella raccolta [**SystemMonitor. LogFiles**](systemmonitor-logfiles.md) per relog i dati del contatore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> <dt>

[**SystemMonitor. SaveAs**](systemmonitor-saveas.md)
</dt> </dl>

 

 





