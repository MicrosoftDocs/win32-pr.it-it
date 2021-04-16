---
title: Metodo SystemMonitor CollectSample
description: Campiona un valore per ogni contatore nell'oggetto contatori.
ms.assetid: 4c91c759-597f-4aa8-aa77-eb181616e8b0
keywords:
- Metodo CollectSample SysMon
- Metodo CollectSample SysMon, interfaccia SystemMonitor
- Interfaccia SystemMonitor SysMon, metodo CollectSample
topic_type:
- apiref
api_name:
- SystemMonitor.CollectSample
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e1c269d044c17a2ec1322fa969e0c86f468a901
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477098"
---
# <a name="systemmonitorcollectsample-method"></a>Metodo SystemMonitor:: CollectSample

Campiona un valore per ogni contatore nell'oggetto [**contatori**](counters.md) .

## <a name="syntax"></a>Sintassi


```VB
Sub CollectSample()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Chiamare **CollectSample** solo se [**ManualUpdate**](systemmonitor-manualupdate.md) è true e i valori del contatore di campionamento dall'attività corrente del computer non utilizzano questo metodo durante il campionamento da un file di log. Il grafico o il report viene aggiornato con il nuovo valore. Si noti che alcuni tipi di grafici richiedono due esempi per rappresentare i dati, ad esempio il grafico a linee.

Per ricevere una notifica quando l'esempio è stato raccolto, implementare l'evento [**OnSampleCollected**](-systemmonitor-onsamplecollected.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Contatori**](counters.md)
</dt> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> </dl>

 

 





