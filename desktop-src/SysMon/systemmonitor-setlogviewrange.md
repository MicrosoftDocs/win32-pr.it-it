---
title: SystemMonitor. SetLogViewRange, metodo
description: Imposta la data di inizio utilizzata per recuperare i valori dei contatori dai file di log.
ms.assetid: ced641d0-cf71-4826-8ff0-c05f20a71aaa
keywords:
- Metodo SetLogViewRange SysMon
- Metodo SetLogViewRange SysMon, oggetto SystemMonitor
- Oggetto SystemMonitor SysMon, metodo SetLogViewRange
topic_type:
- apiref
api_name:
- SystemMonitor.SetLogViewRange
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 534a7dc3bf711832ec99e4202f4f56cc347f336b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400415"
---
# <a name="systemmonitorsetlogviewrange-method"></a>SystemMonitor. SetLogViewRange, metodo

Imposta la data di inizio utilizzata per recuperare i valori dei contatori dai file di log.

## <a name="syntax"></a>Sintassi


```VB
SystemMonitor.SetLogViewRange( _
  ByVal StartTime As Date, _
  ByVal StopTime As Date _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*StartTime* \[ in\]
</dt> <dd>

Data di inizio utilizzata per recuperare i valori dei contatori dai file di log.

</dd> <dt>

*StopTime* \[ in\]
</dt> <dd>

Data di fine utilizzata per recuperare i valori dei contatori dai file di log.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

SYSMON recupera i valori dei contatori dai file di log che rientrano nelle date di inizio e di fine, inclusi.

Se non si specifica una data di inizio o si imposta la data di inizio su un valore di data non compreso nell'intervallo dei valori di data presenti nei file di log, SYSMON modifica il valore in un valore di data meno recente trovato nei file di log. Se il valore iniziale è maggiore del valore di arresto, SYSMON modifica il valore iniziale in modo che corrisponda al valore di stop.

Se non si specifica un valore di interruzione o si imposta il valore di interruzione su un valore di data successivo all'ultima data contenuta nel file di log, SYSMON modifica il valore con il valore di data più recente trovato nei file di log. Se il valore di arresto è inferiore al valore di arresto, SYSMON modifica il valore di interruzione in modo che corrisponda al valore iniziale.

Se si specifica una data di inizio e di fine, è necessario specificare le date prima di impostare [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md). Se si impostano le date dopo l'impostazione di **SystemMonitor. DataSourceType**, solo il primo valore del contatore viene recuperato dal file di log.

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

[**SystemMonitor. GetLogViewRange**](systemmonitor-getlogviewrange.md)
</dt> </dl>

 

 





