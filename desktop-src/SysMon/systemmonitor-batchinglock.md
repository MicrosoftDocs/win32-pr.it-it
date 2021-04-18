---
title: Metodo chingLock SystemMonitor.Bat
description: Blocca il monitor di sistema per impedirne il campionamento dei dati del contatore o del file di log appena aggiunto.
ms.assetid: 6b9d683a-7a97-44a4-9eb6-6caaafe2abdd
keywords:
- Metodo BatchingLock SysMon
- Metodo BatchingLock SysMon, oggetto SystemMonitor
- Oggetto SystemMonitor SysMon, metodo BatchingLock
topic_type:
- apiref
api_name:
- SystemMonitor.BatchingLock
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b858a6920b039d911ae571d81744eb99dea4ef4f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301791"
---
# <a name="systemmonitorbatchinglock-method"></a>Metodo chingLock SystemMonitor.Bat

Blocca il monitor di sistema per impedirne il campionamento dei dati del contatore o del file di log appena aggiunto.

## <a name="syntax"></a>Sintassi


```VB
SystemMonitor.BatchingLock( _
  ByVal lock As Boolean, _
  ByVal batchReason As SysmonBatchReason _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*blocca* \[ in\]
</dt> <dd>

Impostare su true per bloccare il monitor di sistema in modo da impedire il campionamento dei dati del contatore dal nuovo contatore o dal file di log appena aggiunto. Impostare su false per rimuovere il blocco.

</dd> <dt>

*batchReason* \[ in\]
</dt> <dd>

Identifica l'origine dei dati che si stanno bloccando. Utilizzare lo stesso valore motivo per bloccare e sbloccare la risorsa. Per i valori possibili, vedere l'enumerazione [**SysmonBatchReason**](/windows/win32/api/isysmon/ne-isysmon-sysmonbatchreason) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

È necessario chiamare questo metodo due volte, una volta per bloccare l'origine (true) e una volta per sbloccare l'origine (false).

È possibile inserire un solo blocco. Se ad esempio si imposta il blocco per SysmonBatchAddFiles e quindi si effettua una seconda chiamata usando SysmonBatchAddCounters come motivo, la seconda chiamata rimuove il blocco inserito dalla prima chiamata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> </dl>

 

 





