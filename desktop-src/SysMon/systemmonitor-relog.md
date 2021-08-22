---
title: Metodo SystemMonitor.Relog
description: Riloga i dati del contatore in un nuovo file. È inoltre possibile utilizzare questo metodo per specificare un nuovo tipo di file e ridurre il numero di esempi contenuti nel file di log.
ms.assetid: 4439f9ef-99e0-47d4-8f6f-d08afcba672d
keywords:
- Metodo Relog SysMon
- Metodo Relog SysMon , oggetto SystemMonitor
- Oggetto SystemMonitor SysMon , metodo Relog
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
ms.openlocfilehash: 73025a352ba3ec2e9ed113c59a7e04f98084495da834f83bf052c697833dd13f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118881728"
---
# <a name="systemmonitorrelog-method"></a>Metodo SystemMonitor.Relog

Riloga i dati del contatore in un nuovo file. È inoltre possibile utilizzare questo metodo per specificare un nuovo tipo di file e ridurre il numero di esempi contenuti nel file di log.

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

*fileName* \[ Pollici\]
</dt> <dd>

Percorso del file di log. È possibile specificare il percorso come percorso assoluto, relativo o UNC. L'estensione del nome file di log deve essere blg, tsv o .csv. Se non esiste una cartella nel percorso, SYSMON la creerà. Se il file esiste, viene sovrascritto. SYSMON applica gli ACL predefiniti dalla directory padre.

</dd> <dt>

*tipo di file* \[ Pollici\]
</dt> <dd>

Formato dei dati del contatore salvati nel file di log. È possibile specificare [**SysmonFileType.sysmonFileBlg**](/windows/win32/api/isysmon/ne-isysmon-sysmonfiletype), **SysmonFileType.sysmonFileCsv** **o monFileTsvSysmonFileType.sysmonFileTsv**.

</dd> <dt>

*filter* \[ Pollici\]
</dt> <dd>

Numero di esempi dei file di log precedente da salvare nel nuovo file di log. Specificare 1 per salvare ogni esempio dai file vecchi nei nuovi file. Specificare 2 per salvare uno dei due campioni del file precedente. Specificare 3 per salvare uno dei tre campioni del file precedente. e così via.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo usa i file di log contenuti nella raccolta [**SystemMonitor.LogFiles**](systemmonitor-logfiles.md) per registrare nuovamente i dati del contatore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> <dt>

[**SystemMonitor.SaveAs**](systemmonitor-saveas.md)
</dt> </dl>

 

 





