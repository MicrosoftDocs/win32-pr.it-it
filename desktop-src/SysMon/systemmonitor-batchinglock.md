---
title: SystemMonitor.Batmetodo chingLock
description: Blocca Monitoraggio di sistema per impedire il campionamento dei dati dei contatori dal nuovo contatore o file di log aggiunto.
ms.assetid: 6b9d683a-7a97-44a4-9eb6-6caaafe2abdd
keywords:
- Metodo BatchingLock SysMon
- Metodo BatchingLock SysMon , oggetto SystemMonitor
- Oggetto SystemMonitor SysMon , metodo BatchingLock
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
ms.openlocfilehash: 8f028a3cb985a530b6e034ceabe430d2dda7b12e337af40d6510a3a8d77bd0d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118882937"
---
# <a name="systemmonitorbatchinglock-method"></a>SystemMonitor.Batmetodo chingLock

Blocca Monitoraggio di sistema per impedire il campionamento dei dati dei contatori dal nuovo contatore o file di log aggiunto.

## <a name="syntax"></a>Sintassi


```VB
SystemMonitor.BatchingLock( _
  ByVal lock As Boolean, _
  ByVal batchReason As SysmonBatchReason _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*blocco* \[ Pollici\]
</dt> <dd>

Impostare su True per bloccare Monitoraggio di sistema per impedire il campionamento dei dati dei contatori dal file di log o del contatore appena aggiunto. Impostare su False per rimuovere il blocco.

</dd> <dt>

*batchReason* \[ Pollici\]
</dt> <dd>

Identifica l'origine dei dati che si sta bloccando. Usare lo stesso valore di motivo quando si blocca e si sblocca la risorsa. Per i valori possibili, vedere [**l'enumerazione SysmonBatchReason.**](/windows/win32/api/isysmon/ne-isysmon-sysmonbatchreason)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

È necessario chiamare questo metodo due volte, una volta per bloccare l'origine (True) e una volta per sbloccare l'origine (False).

È possibile inserire un solo blocco. Ad esempio, se si imposta il blocco per SysmonBatchAddFiles e quindi si effettua una seconda chiamata usando SysmonBatchAddCounters come motivo, la seconda chiamata rimuove il blocco inserito dalla prima chiamata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> </dl>

 

 





